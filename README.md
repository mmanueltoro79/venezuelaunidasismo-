[index.html](https://github.com/user-attachments/files/29355055/index.html)
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Venezuela Unida · Boletín de Emergencia · Terremoto 24 jun 2026</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@500;600;700;800&family=Inter:wght@400;500;600;700&family=IBM+Plex+Mono:wght@500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#14181b;
    --ink-soft:#2a3138;
    --paper:#fbfaf7;
    --line:#ddd7ca;
    --line-strong:#bcb4a2;
    --red:#c2271f;
    --red-deep:#8f1812;
    --amber:#b57100;
    --amber-bg:#fbf2dd;
    --green:#15704a;
    --green-bg:#e6f1ea;
    --muted:#6a6b63;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{-webkit-text-size-adjust:100%}
  body{
    background:#e9e6df;
    color:var(--ink);
    font-family:'Inter',system-ui,sans-serif;
    line-height:1.45;
    padding:24px 14px 60px;
  }
  .sheet{
    max-width:860px;margin:0 auto;
    background:var(--paper);
    border:1px solid var(--line-strong);
    box-shadow:0 18px 50px rgba(20,24,27,.16);
  }

  /* ---------- TOP CREATOR BAR (punta de arriba) ---------- */
  .topbar{
    background:var(--red);color:#fff;
    display:flex;align-items:center;justify-content:center;gap:10px;flex-wrap:wrap;
    padding:9px 18px;text-align:center;
  }
  .topbar .by{
    font-family:'IBM Plex Mono',monospace;font-size:10.5px;letter-spacing:.2em;
    text-transform:uppercase;color:#f6cfcb;
  }
  .topbar .who{
    font-family:'Barlow Condensed',sans-serif;font-weight:800;text-transform:uppercase;
    font-size:clamp(17px,4vw,23px);line-height:1;letter-spacing:.03em;color:#fff;
  }
  .topbar .who .sep{color:#f3b3ad;margin:0 7px;font-weight:600}

  /* ---------- MASTHEAD ---------- */
  .masthead{
    background:var(--ink);color:#f3f0e9;
    padding:20px 26px 18px;
    display:grid;grid-template-columns:1fr auto;gap:18px;align-items:start;
    border-bottom:4px solid var(--red);
  }
  .brand-eyebrow{
    font-family:'IBM Plex Mono',monospace;font-size:11px;letter-spacing:.22em;
    text-transform:uppercase;color:#b9b3a4;margin-bottom:7px;
  }
  .brand-title{
    font-family:'Barlow Condensed',sans-serif;font-weight:800;
    font-size:clamp(30px,7vw,50px);line-height:.92;letter-spacing:.01em;text-transform:uppercase;
  }
  .brand-sub{
    font-family:'Barlow Condensed',sans-serif;font-weight:600;
    font-size:clamp(15px,3.4vw,20px);color:#e7c9c6;margin-top:6px;letter-spacing:.02em;
  }
  .brand-credit{
    margin-top:13px;padding-top:11px;border-top:1px solid #2f363c;
    display:flex;align-items:baseline;gap:9px;flex-wrap:wrap;
  }
  .brand-credit .by{
    font-family:'IBM Plex Mono',monospace;font-size:11px;letter-spacing:.14em;
    text-transform:uppercase;color:#9aa0a6;
  }
  .brand-credit .who{
    font-family:'Barlow Condensed',sans-serif;font-weight:800;text-transform:uppercase;
    font-size:clamp(20px,4.6vw,28px);line-height:1;letter-spacing:.02em;color:#fff;
  }
  .brand-credit .who b{color:var(--red)}
  .brand-credit .who .sep{color:#57606a;font-weight:600;margin:0 4px}
  /* update stamp = signature element */
  .stamp{
    border:1.5px solid #57606a;border-radius:3px;
    padding:9px 12px;min-width:172px;text-align:left;
    background:#1c2227;
  }
  .stamp .live{
    display:flex;align-items:center;gap:7px;
    font-family:'IBM Plex Mono',monospace;font-size:10px;letter-spacing:.14em;
    text-transform:uppercase;color:#9fb8aa;margin-bottom:7px;
  }
  .dot{width:8px;height:8px;border-radius:50%;background:#3fd07f;box-shadow:0 0 0 0 rgba(63,208,127,.6);animation:pulse 1.8s infinite}
  @keyframes pulse{0%{box-shadow:0 0 0 0 rgba(63,208,127,.55)}70%{box-shadow:0 0 0 9px rgba(63,208,127,0)}100%{box-shadow:0 0 0 0 rgba(63,208,127,0)}}
  .stamp .when{font-family:'IBM Plex Mono',monospace;font-weight:700;font-size:17px;color:#fff;line-height:1.2}
  .stamp .meta{font-family:'IBM Plex Mono',monospace;font-size:11px;color:#9aa0a6;margin-top:4px}

  /* ---------- STAT STRIP ---------- */
  .stats{
    display:grid;grid-template-columns:repeat(4,1fr) 1.3fr;
    border-bottom:1px solid var(--line);
  }
  .stat{padding:14px 12px 12px;border-right:1px solid var(--line);text-align:center}
  .stat:last-child{border-right:0}
  .stat .num{font-family:'IBM Plex Mono',monospace;font-weight:700;font-size:clamp(24px,5.5vw,34px);line-height:1;color:var(--red-deep)}
  .stat .lbl{font-size:10.5px;text-transform:uppercase;letter-spacing:.09em;color:var(--muted);margin-top:6px;font-weight:600}
  .stat.zone{background:var(--red);color:#fff;display:flex;flex-direction:column;justify-content:center}
  .stat.zone .num{font-family:'Barlow Condensed',sans-serif;font-size:clamp(20px,4.6vw,27px);color:#fff;letter-spacing:.02em}
  .stat.zone .lbl{color:#f4d4d1}

  /* ---------- BODY GRID ---------- */
  .body{display:grid;grid-template-columns:1.05fr .95fr}
  .col{padding:20px 24px}
  .col.left{border-right:1px solid var(--line)}

  .sec{margin-bottom:22px}
  .sec:last-child{margin-bottom:0}
  .sec-head{
    display:flex;align-items:baseline;gap:9px;margin-bottom:10px;
    border-bottom:2px solid var(--ink);padding-bottom:5px;
  }
  .sec-head h2{
    font-family:'Barlow Condensed',sans-serif;font-weight:700;text-transform:uppercase;
    font-size:21px;letter-spacing:.03em;line-height:1;
  }
  .sec-head .tag{
    margin-left:auto;font-family:'IBM Plex Mono',monospace;font-size:9.5px;font-weight:600;
    letter-spacing:.08em;text-transform:uppercase;padding:3px 7px;border-radius:3px;white-space:nowrap;
  }
  .tag.ok{background:var(--ink);color:#fff}
  .tag.warn{background:var(--amber-bg);color:var(--amber);border:1px solid #e6c987}

  p.lead{font-size:13px;color:var(--ink-soft);margin-bottom:10px}
  .zonas{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:12px}
  .chip{font-family:'IBM Plex Mono',monospace;font-size:11px;font-weight:600;background:#efe9db;border:1px solid var(--line-strong);border-radius:30px;padding:3px 10px;color:var(--ink-soft)}

  .blockquote{
    border-left:3px solid var(--red);background:#f6ece9;
    padding:9px 12px;font-size:12.5px;color:var(--ink-soft);margin-bottom:12px;
  }
  .blockquote b{color:var(--red-deep)}

  .edif-label{font-size:11px;text-transform:uppercase;letter-spacing:.07em;color:var(--muted);font-weight:700;margin-bottom:7px}
  .edif-list{
    font-family:'IBM Plex Mono',monospace;font-size:11.5px;line-height:1.7;color:var(--ink);
    column-count:2;column-gap:18px;
  }
  .edif-list span{display:block;break-inside:avoid;padding-left:13px;position:relative}
  .edif-list span::before{content:"▪";position:absolute;left:0;color:var(--red);font-size:9px;top:2px}

  ul.facts{list-style:none}
  ul.facts li{font-size:12.5px;padding:7px 0 7px 18px;position:relative;border-bottom:1px dashed var(--line);color:var(--ink-soft)}
  ul.facts li:last-child{border-bottom:0}
  ul.facts li::before{content:"";position:absolute;left:0;top:13px;width:7px;height:7px;background:var(--ink);transform:rotate(45deg)}
  ul.facts li b{color:var(--ink)}

  .aid{display:flex;flex-wrap:wrap;gap:6px;margin-top:8px}
  .aid .flag{font-family:'IBM Plex Mono',monospace;font-size:10.5px;font-weight:600;background:#fff;border:1px solid var(--line-strong);padding:3px 8px;border-radius:3px}

  /* ---------- RESOURCES (green, loudest help block) ---------- */
  .resources{background:var(--green-bg);border:1.5px solid var(--green);border-radius:5px;padding:15px 16px;margin-top:4px}
  .resources .rh{display:flex;align-items:center;gap:8px;margin-bottom:11px}
  .resources .rh h3{font-family:'Barlow Condensed',sans-serif;font-weight:700;text-transform:uppercase;font-size:19px;color:var(--green);letter-spacing:.03em}
  .emerg{display:flex;gap:10px;margin-bottom:13px}
  .emerg .e{flex:1;background:var(--green);color:#fff;border-radius:4px;text-align:center;padding:9px 4px}
  .emerg .e .n{font-family:'IBM Plex Mono',monospace;font-weight:700;font-size:26px;line-height:1}
  .emerg .e .t{font-size:9.5px;text-transform:uppercase;letter-spacing:.1em;margin-top:3px;color:#cfe6da}
  .plats{list-style:none}
  .plats li{padding:7px 0;border-bottom:1px solid #cfe2d6;font-size:12.5px}
  .plats li:last-child{border-bottom:0}
  .plats .u{font-family:'IBM Plex Mono',monospace;font-weight:700;color:var(--green);font-size:12.5px}
  .plats .d{display:block;color:var(--ink-soft);font-size:11.5px;margin-top:1px}

  /* ---------- WARNING + SOURCES FOOTER ---------- */
  .note{background:var(--amber-bg);border-top:3px solid var(--amber);padding:14px 24px;font-size:12px;color:#5e4307}
  .note b{color:var(--amber)}
  .note .nt{font-family:'Barlow Condensed',sans-serif;font-weight:700;text-transform:uppercase;font-size:15px;letter-spacing:.04em;color:var(--amber);margin-bottom:4px}

  .sources{background:var(--ink);color:#cfcbc1;padding:16px 24px 20px}
  .sources .sh{font-family:'Barlow Condensed',sans-serif;font-weight:700;text-transform:uppercase;letter-spacing:.06em;font-size:15px;color:#fff;margin-bottom:9px;border-bottom:1px solid #3a4147;padding-bottom:5px}
  .src-grid{display:grid;grid-template-columns:1fr 1fr;gap:5px 22px}
  .src-grid div{font-size:11px;padding:3px 0;border-bottom:1px solid #262c31}
  .src-grid b{color:#fff;font-weight:600}
  .src-grid .o{font-family:'IBM Plex Mono',monospace;color:#7fd3a6;font-size:9.5px;letter-spacing:.06em}
  .colophon{font-family:'IBM Plex Mono',monospace;font-size:10px;color:#7c8087;margin-top:12px;line-height:1.6}

  /* ---------- RESPONSIVE ---------- */
  @media(max-width:680px){
    body{padding:12px 8px 40px}
    .masthead{grid-template-columns:1fr;gap:14px}
    .stamp{justify-self:start}
    .stats{grid-template-columns:repeat(2,1fr)}
    .stat{border-bottom:1px solid var(--line)}
    .stat.zone{grid-column:1 / -1}
    .body{grid-template-columns:1fr}
    .col.left{border-right:0;border-bottom:1px solid var(--line)}
    .edif-list{column-count:1}
    .src-grid{grid-template-columns:1fr}
  }

  /* ---------- PRINT (2 hojas limpias) ---------- */
  @media print{
    @page{size:A4;margin:9mm}
    body{background:#fff;padding:0;-webkit-print-color-adjust:exact;print-color-adjust:exact}
    .sheet{box-shadow:none;border:none;max-width:none}
    .dot{animation:none}
    .edif-list{column-count:2}
    .stats{grid-template-columns:repeat(4,1fr) 1.3fr}
    .body{grid-template-columns:1.05fr .95fr}
  }
</style>
</head>
<body>
<div class="sheet">

  <!-- ============ TOP CREATOR BAR ============ -->
  <div class="topbar">
    <span class="by">Creado por</span>
    <span class="who">Mundoxpress VNZ<span class="sep">·</span>Manuel Toro</span>
  </div>

  <!-- ============ MASTHEAD ============ -->
  <header class="masthead">
    <div>
      <div class="brand-eyebrow">Centro de difusión ciudadana · Información verificada</div>
      <div class="brand-title">Venezuela Unida</div>
      <div class="brand-sub">Boletín de emergencia · Terremoto 24 jun 2026 · M7,2 + M7,5</div>
    </div>
    <!-- ▼▼ EDITAR AL ACTUALIZAR: fecha/hora y versión ▼▼ -->
    <div class="stamp">
      <div class="live"><span class="dot"></span> Última actualización</div>
      <div class="when">25 JUN · 2:15 PM</div>
      <div class="meta">Hora Caracas · v1.2</div>
    </div>
    <!-- ▲▲ -->
  </header>

  <!-- ============ STAT STRIP (cifras oficiales) ============ -->
  <section class="stats">
    <div class="stat"><div class="num">188</div><div class="lbl">Fallecidos</div></div>
    <div class="stat"><div class="num">1.520</div><div class="lbl">Heridos</div></div>
    <div class="stat"><div class="num">250</div><div class="lbl">Edif. dañados</div></div>
    <div class="stat"><div class="num">25</div><div class="lbl">Muertos Caracas</div></div>
    <div class="stat zone"><div class="num">La Guaira</div><div class="lbl">Zona de desastre</div></div>
  </section>

  <!-- ============ BODY ============ -->
  <div class="body">

    <!-- ---- COLUMNA IZQUIERDA: territorio ---- -->
    <div class="col left">

      <div class="sec">
        <div class="sec-head"><h2>El evento</h2><span class="tag ok">USGS · Funvisis</span></div>
        <p class="lead">Dos sismos sucesivos el <b>24 jun 2026, ~6:04 p.m.</b>, con <b>39 segundos</b> de diferencia: precursor <b>M7,2</b> (San Felipe) y principal <b>M7,5</b> (Yumare), epicentros en la zona Morón–San Felipe (Carabobo / Yaracuy). El más fuerte en Venezuela desde 1900. Más de <b>138 réplicas</b> registradas.</p>
      </div>

      <div class="sec">
        <div class="sec-head"><h2>La Guaira</h2><span class="tag ok">Oficial</span></div>
        <p class="lead">Estado más golpeado, declarado <b>zona de desastre</b>. Sectores más afectados:</p>
        <div class="zonas">
          <span class="chip">Playa Grande</span><span class="chip">Catia La Mar</span>
          <span class="chip">Caribe</span><span class="chip">Macuto</span>
          <span class="chip">Los Corales</span><span class="chip">Tanaguarena</span>
          <span class="chip">Caraballeda</span>
        </div>
        <div class="blockquote">El <b>Hotel Eduard's</b> (Macuto, frente al estadio Jorge Luis García Carneiro) se desplomó por completo.</div>

        <div class="edif-label">Edificios colapsados — lista no oficial, confirmada por El Estímulo</div>
        <div class="edif-list">
          <span>Hotel Eduard's</span><span>Portofino</span><span>Rocapark</span><span>Bahía Mar</span>
          <span>Rita</span><span>Sol Palace</span><span>Mariola y Maribel</span><span>Gran Terraza</span>
          <span>Breogan</span><span>Caribe</span><span>La Trinidad</span><span>Rosanday</span>
          <span>Costa Brava</span><span>Llona</span><span>Miramar</span><span>La Mar Suites</span>
          <span>Oasis Beach</span><span>Parque Caraballeda</span><span>Coral Beach</span><span>Albatros Los Corales</span>
          <span>Golf Mar</span><span>Punta Brisas</span><span>Punta Brava</span><span>La Gabarra</span>
          <span>Pez Vela</span><span>Vistamar</span><span>Mariana Grande / Mar</span><span>M. Vivienda Los Cocos</span>
          <span>Tahiti</span><span>Los Delfines</span><span>Bello Horizonte</span><span>La Llovizna</span>
          <span>Coral Bella</span><span>Club de Playa</span><span>Las Palmas</span><span>Bucanero</span>
          <span>La Estrella</span><span>Albatroz</span><span>Canes</span>
        </div>
      </div>

      <div class="sec">
        <div class="sec-head"><h2>Caracas</h2><span class="tag ok">Oficial</span></div>
        <ul class="facts">
          <li><b>Chacao — punto crítico:</b> colapso total del <b>Edificio Petunia</b>. Alcaldía (G. Duque): ≥4 edificios colapsados, 6 con daños graves.</li>
          <li><b>Rescate concentrado</b> en Los Palos Grandes, Altamira y Bello Campo. +500 efectivos; al menos 18 personas rescatadas con vida.</li>
          <li>Colapsó un <b>edificio de Bancaribe</b> en la capital; otro de vieja data cedió en <b>San Bernardino</b> (centro), con rescatados.</li>
          <li>Afectación también en <b>Miranda, Aragua, Yaracuy, Trujillo y Carabobo.</b></li>
        </ul>
      </div>

    </div>

    <!-- ---- COLUMNA DERECHA: estado + recursos ---- -->
    <div class="col right">

      <div class="sec">
        <div class="sec-head"><h2>Servicios y estado</h2><span class="tag ok">Oficial</span></div>
        <ul class="facts">
          <li><b>Aeropuerto de Maiquetía cerrado</b> por daños graves; <b>Copa, Avianca y Latam</b> cancelaron vuelos a Caracas.</li>
          <li><b>Clases suspendidas</b> ~1 semana; actividades no esenciales detenidas.</li>
          <li><b>Gas cortado</b> de forma preventiva en ciertos edificios mientras se evalúan estructuras.</li>
          <li><b>Internet caído</b> en buena parte del país (NetBlocks): muchas personas están <b>incomunicadas, no desaparecidas.</b></li>
          <li><b>Fondo de reconstrucción</b> anunciado: US$ 200 millones.</li>
          <li><b>⚠ Reportes de saqueos en Catia La Mar</b> (La Guaira); el DGCIM acudió a la zona.</li>
        </ul>
        <div class="edif-label" style="margin-top:12px">Rescatistas en camino</div>
        <div class="aid">
          <span class="flag">EE.UU.</span><span class="flag">Catar</span>
          <span class="flag">Rep. Dominicana</span><span class="flag">México</span><span class="flag">El Salvador</span>
          <span class="flag">Suiza</span><span class="flag">Chile</span><span class="flag">España</span>
          <span class="flag">Italia</span><span class="flag">Rep. Checa</span><span class="flag">Países Bajos</span><span class="flag">UE</span>
        </div>
      </div>

      <!-- RECURSOS = bloque de ayuda más visible -->
      <div class="resources">
        <div class="rh"><h3>Si necesitas ayuda</h3></div>
        <div class="emerg">
          <div class="e"><div class="n">171</div><div class="t">Emergencias</div></div>
          <div class="e"><div class="n">911</div><div class="t">Emergencias</div></div>
        </div>
        <ul class="plats">
          <li><span class="u">terremotovenezuela.app</span><span class="d">Mapa: desaparecidos, localizados a salvo, suministros, refugios, daños.</span></li>
          <li><span class="u">desaparecidosterremotovenezuela.com</span><span class="d">Reconexión de familias: reporta o avisa cuando lo encuentres.</span></li>
          <li><span class="u">sosvzla.lat</span><span class="d">Reportes en tiempo real, sin registro.</span></li>
          <li><span class="u">sosvenezuela2026.com</span><span class="d">Mapa colaborativo en vivo del sismo.</span></li>
        </ul>
        <div style="margin-top:10px;font-size:11px;color:#33503f;border-top:1px solid #cfe2d6;padding-top:8px;line-height:1.5">
          Las plataformas ya acumulan <b>32.351 reportes</b> · 30.600 sin contacto · 1.751 localizados a salvo.
        </div>
      </div>

    </div>
  </div>

  <!-- ============ NOTA: lo no confirmado ============ -->
  <section class="note">
    <div class="nt">⚠ Antes de difundir — lo que NO está confirmado</div>
    <p><b>Proyección de víctimas:</b> el USGS estima ~40% de probabilidad de entre 10.000 y 100.000 fallecidos. Es un <b>modelo estadístico, no un conteo real</b> — nunca lo difundas como cifra de muertos. &nbsp;·&nbsp; <b>Identidad de víctimas</b> (ej. familiares de peloteros en el Hotel Eduard's): reportes de redes, sin confirmación oficial. &nbsp;·&nbsp; Usa "<b>sin contacto</b>" en vez de "desaparecido": un dato errado multiplica el dolor.</p>
  </section>

  <!-- ============ FUENTES OFICIALES ============ -->
  <footer class="sources">
    <div class="sh">Fuentes</div>
    <div class="src-grid">
      <div><span class="o">SISMO</span> &nbsp;<b>USGS · Funvisis</b> (oficial Venezuela)</div>
      <div><span class="o">CIFRAS NACIONALES</span> &nbsp;<b>Jorge Rodríguez</b> (Asamblea Nac.) · <b>Delcy Rodríguez</b> vía VTV</div>
      <div><span class="o">CARACAS</span> &nbsp;<b>Carmen Meléndez</b> — Alcaldía de Caracas</div>
      <div><span class="o">CHACAO</span> &nbsp;<b>Gustavo Duque</b> — Alcaldía de Chacao</div>
      <div><span class="o">EDIFICIOS LA GUAIRA</span> &nbsp;<b>El Estímulo</b> — elestimulo.com</div>
      <div><span class="o">PRENSA</span> &nbsp;<b>CNN en Español · NBC News · Infobae · Ámbito</b></div>
    </div>
    <div class="colophon">
      Boletín ciudadano · Venezuela Unida · v1.2 — 25 jun 2026, 2:15 PM (Caracas).<br>
      Creado por Mundoxpress VNZ · Manuel Toro.<br>
      Documento vivo: las cifras son las últimas oficiales disponibles y aumentarán. Verifica antes de reenviar.
    </div>
  </footer>

</div>
</body>
</html>
