# Presentasjon-Tidslinje-KI-Innovasjonsprosjekt-Periode-2022-2026-
Tidslinje for KI Innovasjonsprosjekt
<!DOCTYPE html>
<html lang="no">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tidslinje – KI Innovasjonsprosjekt UNN</title>
<link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,500;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg:#faf9f7; --surface:#fff; --surface2:#f4f2ee; --border:#e8e4dc; --border2:#ccc8c0;
    --text:#2c2a26; --text2:#6b665c; --text3:#9c9487;
    --done:#2d7a4f; --done-bg:#edf7f1; --done-border:#a8d9bc;
    --ongoing:#8a5e1a; --ongoing-bg:#fdf4e7; --ongoing-border:#e8c88a;
    --dropped:#8a3030; --dropped-bg:#fdf0f0; --dropped-border:#e0b0b0;
    --accent:#3d6b9e; --accent-bg:#eef3f9; --accent-border:#b8cfe4;
    --key:#1e4d80;
    --y2023:#4a7c59; --y2024:#3d6b9e; --y2025:#7a4e9e; --y2026:#c47a20;
  }
  *{margin:0;padding:0;box-sizing:border-box}
  body{background:var(--bg);color:var(--text);font-family:'DM Sans',sans-serif;font-size:14px;line-height:1.6}

  /* NAV TABS */
  .nav-tabs{display:flex;background:var(--surface);border-bottom:1px solid var(--border);overflow-x:auto;position:sticky;top:0;z-index:100}
  .nav-tab{flex-shrink:0;padding:13px 22px;font-size:13px;font-weight:400;cursor:pointer;border:none;background:none;color:var(--text2);border-bottom:2px solid transparent;transition:all .15s;font-family:'DM Sans',sans-serif;white-space:nowrap}
  .nav-tab:hover{color:var(--text);background:var(--surface2)}
  .nav-tab.active{color:var(--accent);border-bottom-color:var(--accent);font-weight:500}

  /* PANELS */
  .panel{display:none;animation:fadeIn .25s ease}
  .panel.active{display:block}
  @keyframes fadeIn{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:none}}

  /* INTRO PANEL */
  .intro-wrap{max-width:860px;margin:0 auto;padding:48px 48px 72px}
  .intro-kicker{font-size:11px;font-weight:500;letter-spacing:.12em;text-transform:uppercase;color:var(--text3);margin-bottom:14px}
  .intro-h1{font-family:'Lora',serif;font-size:clamp(26px,3vw,38px);font-weight:400;line-height:1.2;margin-bottom:10px}
  .intro-h1 em{font-style:italic;color:var(--accent)}
  .intro-sub{font-size:14px;color:var(--text2);margin-bottom:36px;line-height:1.7}

  .intro-section{margin-bottom:36px}
  .intro-section-title{font-family:'Lora',serif;font-size:18px;font-weight:500;color:var(--text);margin-bottom:14px;padding-bottom:8px;border-bottom:1px solid var(--border)}
  .intro-body{font-size:14px;color:var(--text2);line-height:1.8}
  .intro-body p{margin-bottom:12px}
  .intro-body p:last-child{margin-bottom:0}

  .highlight-box{background:var(--done-bg);border:1px solid var(--done-border);border-radius:10px;padding:18px 22px;margin:20px 0;font-size:13px;color:var(--done);line-height:1.7}
  .highlight-box strong{font-weight:500}

  .stat-row{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:10px;margin:24px 0}
  .stat-box{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:14px 16px}
  .stat-num{font-family:'Lora',serif;font-size:28px;font-weight:400;line-height:1;margin-bottom:2px}
  .stat-lbl{font-size:11px;text-transform:uppercase;letter-spacing:.07em;color:var(--text3);font-weight:500}
  .stat-num.done{color:var(--done)} .stat-num.drop{color:var(--dropped)} .stat-num.ong{color:var(--ongoing)}

  /* INTERESTS PANEL */
  .section-wrap{max-width:900px;margin:0 auto;padding:40px 48px 72px}
  .section-title{font-family:'Lora',serif;font-size:22px;font-weight:400;color:var(--text);margin-bottom:6px}
  .section-desc{font-size:13px;color:var(--text2);margin-bottom:28px}

  .int-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:12px;margin-bottom:40px}
  .int-card{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:16px 18px;transition:border-color .15s}
  .int-card:hover{border-color:var(--border2)}
  .int-name{font-size:14px;font-weight:500;color:var(--text);margin-bottom:4px}
  .int-role{font-size:12px;color:var(--text2);margin-bottom:8px;line-height:1.5}
  .int-tags{display:flex;flex-wrap:wrap;gap:5px}
  .int-tag{display:inline-block;font-size:10px;padding:2px 8px;border-radius:100px;font-weight:500}
  .int-tag.core{background:var(--accent-bg);color:var(--key);border:1px solid var(--accent-border)}
  .int-tag.support{background:var(--done-bg);color:var(--done);border:1px solid var(--done-border)}
  .int-tag.info{background:var(--surface2);color:var(--text2);border:1px solid var(--border)}
  .int-tag.forkastet{background:var(--dropped-bg);color:var(--dropped);border:1px solid var(--dropped-border)}

  /* GAINS */
  .gains-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:12px}
  .gain-card{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:16px 18px}
  .gain-icon{font-size:22px;margin-bottom:8px;display:block}
  .gain-title{font-size:14px;font-weight:500;color:var(--text);margin-bottom:5px}
  .gain-body{font-size:12px;color:var(--text2);line-height:1.6}

  /* TIMELINE PANEL */
  .tl-wrap{display:flex;min-height:calc(100vh - 50px)}

  .sidebar{width:110px;flex-shrink:0;background:var(--surface);border-right:1px solid var(--border);position:sticky;top:50px;align-self:flex-start;height:calc(100vh - 50px);overflow-y:auto;padding:20px 0}
  .sid-lbl{font-size:10px;font-weight:500;letter-spacing:.1em;text-transform:uppercase;color:var(--text3);padding:0 18px 10px;border-bottom:1px solid var(--border);margin-bottom:6px}
  .yr-btn{display:block;padding:9px 16px;font-size:17px;font-family:'Lora',serif;color:var(--text3);cursor:pointer;border:none;background:none;width:100%;text-align:left;border-left:3px solid transparent;transition:all .15s}
  .yr-btn:hover{color:var(--text);background:var(--surface2)}
  .yr-btn.y2023{border-left-color:var(--y2023);color:var(--y2023)}
  .yr-btn.y2024{border-left-color:var(--y2024);color:var(--y2024)}
  .yr-btn.y2025{border-left-color:var(--y2025);color:var(--y2025)}
  .yr-btn.y2026{border-left-color:var(--y2026);color:var(--y2026)}
  .yr-btn .cnt{display:block;font-size:10px;font-family:'DM Sans',sans-serif;color:var(--text3);font-weight:400;letter-spacing:0}

  .tl-content{flex:1;padding:32px 44px 80px;max-width:800px}

  .progress-wrap{margin-bottom:28px}
  .pb-bg{height:4px;background:var(--border);border-radius:2px;overflow:hidden;margin-bottom:5px}
  .pb-fill{height:100%;border-radius:2px;background:linear-gradient(90deg,var(--done) 0%,var(--done) 76%,var(--ongoing) 76%)}
  .pb-lbl{font-size:11px;color:var(--text3)}

  .yr-section{margin-bottom:52px;scroll-margin-top:70px}
  .yr-hdr{display:flex;align-items:baseline;gap:14px;margin-bottom:18px;padding-bottom:10px;border-bottom:2px solid var(--border)}
  .yr-num{font-family:'Lora',serif;font-size:26px;font-weight:400;line-height:1}
  .yr-num.y2023{color:var(--y2023)} .yr-num.y2024{color:var(--y2024)} .yr-num.y2025{color:var(--y2025)} .yr-num.y2026{color:var(--y2026)}
  .yr-tag{font-family:'Lora',serif;font-style:italic;font-size:14px;color:var(--text3);flex:1}
  .yr-cnt{font-size:11px;color:var(--text3);background:var(--surface2);border:1px solid var(--border);padding:2px 10px;border-radius:100px}

  /* mini-tl */
  .mini-tl{position:relative;display:flex;gap:0;margin-bottom:20px;overflow-x:auto;padding-bottom:4px}
  .mini-tl::before{content:'';position:absolute;top:13px;left:0;right:0;height:2px;background:var(--border2);z-index:0}
  .mini-evt{flex-shrink:0;width:130px;padding-top:30px;padding-right:6px;position:relative;z-index:1}
  .mini-dot{position:absolute;top:6px;left:5px;width:14px;height:14px;border-radius:50%;border:2px solid var(--bg);z-index:2}
  .mini-dot.done{background:var(--done)} .mini-dot.dropped{background:var(--dropped)} .mini-dot.ongoing{background:var(--ongoing)}
  .mini-dot.key{box-shadow:0 0 0 3px rgba(61,107,158,.22)}
  .mini-date{font-size:10px;color:var(--text3);display:block;margin-bottom:1px;font-weight:500}
  .mini-name{font-size:11px;color:var(--text);line-height:1.3}

  /* event cards */
  .events{display:flex;flex-direction:column;gap:7px}
  .ev{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:13px 17px;display:grid;grid-template-columns:48px 1fr;gap:0 12px;transition:border-color .15s,transform .15s;opacity:0;transform:translateX(-10px)}
  .ev.visible{opacity:1!important;transform:translateX(0)!important}
  .ev:hover{border-color:var(--border2);transform:translateX(2px)}
  .ev.dropped{opacity:0;} .ev.dropped.visible{opacity:.55!important}
  .ev.key{border-left:3px solid var(--accent)}
  .ev.finish{background:var(--done-bg);border-color:var(--done-border);border-left:3px solid var(--done)}

  .ev-left{display:flex;flex-direction:column;align-items:center;padding-top:2px;gap:5px}
  .ev-dot{width:11px;height:11px;border-radius:50%;flex-shrink:0}
  .ev-dot.done{background:var(--done)} .ev-dot.dropped{background:var(--dropped)} .ev-dot.ongoing{background:var(--ongoing)}

  .badge{display:inline-flex;align-items:center;gap:3px;padding:2px 7px;border-radius:100px;font-size:10px;font-weight:500;white-space:nowrap;text-align:center}
  .badge.done{background:var(--done-bg);color:var(--done);border:1px solid var(--done-border)}
  .badge.ongoing{background:var(--ongoing-bg);color:var(--ongoing);border:1px solid var(--ongoing-border)}
  .badge.dropped{background:var(--dropped-bg);color:var(--dropped);border:1px solid var(--dropped-border)}

  .ev-phase{font-size:10px;text-transform:uppercase;letter-spacing:.07em;color:var(--text3);font-weight:500;margin-bottom:2px}
  .ev-top{display:flex;align-items:flex-start;gap:8px;margin-bottom:3px}
  .ev-title{font-size:14px;font-weight:500;color:var(--text);flex:1;line-height:1.35}
  .ev-meta{display:flex;align-items:center;gap:6px;flex-wrap:wrap;margin-bottom:4px}
  .ev-date{font-size:11px;color:var(--text3)}
  .ev-tag{display:inline-block;font-size:9px;font-weight:500;letter-spacing:.05em;text-transform:uppercase;color:var(--key);background:var(--accent-bg);border:1px solid var(--accent-border);padding:1px 7px;border-radius:4px}
  .ev-tag.finish{color:var(--done);background:var(--done-bg);border-color:var(--done-border)}
  .ev-desc{font-size:12px;color:var(--text2);line-height:1.55}
  .ev-comment{font-size:11px;color:var(--text3);font-style:italic;font-family:'Lora',serif;margin-top:5px;padding-top:5px;border-top:1px solid var(--border);line-height:1.5}

  /* legend strip */
  .legend{display:flex;flex-wrap:wrap;align-items:center;gap:6px 16px;padding:10px 44px;background:var(--surface);border-bottom:1px solid var(--border);font-size:12px;color:var(--text2)}
  .l-item{display:flex;align-items:center;gap:4px}
  .l-pip{width:9px;height:9px;border-radius:50%;flex-shrink:0}

  @media(max-width:680px){
    .sidebar{display:none}
    .tl-content,.intro-wrap,.section-wrap{padding-left:20px;padding-right:20px}
    .intro-wrap{padding-top:28px}
  }
</style>
</head>
<body>

<!-- TAB NAV -->
<div class="nav-tabs" role="tablist">
  <button class="nav-tab active" onclick="showTab('intro',this)" role="tab">Om prosjektet</button>
  <button class="nav-tab" onclick="showTab('timeline',this)" role="tab">Tidslinje</button>
  <button class="nav-tab" onclick="showTab('stakeholders',this)" role="tab">Interessenter</button>
  <button class="nav-tab" onclick="showTab('gains',this)" role="tab">Gevinster</button>
</div>

<!-- ══════════════════════════════════
     PANEL 1: OM PROSJEKTET
══════════════════════════════════ -->
<div class="panel active" id="panel-intro">
<div class="intro-wrap">
  <div class="intro-kicker">Fyrtårnprosjektet · UNN Tromsø · Skadekoordinator</div>
  <h1 class="intro-h1">KI-assistert utfylling av<br><em>personskadeskjema i DIPS</em></h1>
  <p class="intro-sub">Et innovasjonsprosjekt ved Universitetssykehuset Nord-Norge (UNN) Tromsø<br>
  Prosjektleder: Ida Wood Aasland · Oktober 2023 – Mai 2026</p>

  <div class="stat-row">
    <div class="stat-box"><div class="stat-num done">15</div><div class="stat-lbl">Fullførte milepæler</div></div>
    <div class="stat-box"><div class="stat-num ong">0</div><div class="stat-lbl">Pågående</div></div>
    <div class="stat-box"><div class="stat-num drop">7</div><div class="stat-lbl">Forkastet</div></div>
    <div class="stat-box"><div class="stat-num" style="color:var(--y2026)">6</div><div class="stat-lbl">Nøkkelpartnere</div></div>
  </div>

  <div class="highlight-box">
    🎯 <strong>Prosjektresultat:</strong> Masteroppgave om KI og automatisk utfylling av personskadeskjema er levert ved UiT i mai 2026. Prosjektet ansees som vellykket og er et resultat av samarbeid mellom UNN, DIPS, SPKI, HN-IKT, UiT og Akuttmottaket Tromsø. Videre realisering er forankret i DIPS' nasjonale prosjekt <strong>«Smart journal»</strong>.
  </div>

  <div class="intro-section">
    <div class="intro-section-title">Bakgrunn for ideen</div>
    <div class="intro-body">
      <p>Personskaderegistrering er lovpålagt i Norge og nedfelt i Norsk pasientregisterforskrift. Alle sykehus plikter å fylle ut et Felles minimum datasett (FMDS) – det såkalte personskadeskjemaet – ved skader og ulykker, og rapportere disse til Norsk pasientregister (NPR). Dataene er et kritisk grunnlag for nasjonal skadestatistikk, folkehelsepolitikk og forebygging.</p>
      <p>Virkeligheten ved norske sykehus er at oppslutningen om registreringen er lav – og har vært det lenge. Skjemaet fylles ut manuelt av klinisk personell, gjerne i etterkant av behandling, og oppleves som tidkrevende dobbeltarbeid. All nødvendig informasjon finnes allerede i den strukturerte elektroniske pasientjournalen i DIPS, men ingen prosess henter den ut automatisk.</p>
      <p>Ida Wood Aasland, Skadekoordinator ved UNN Tromsø, stilte seg spørsmålet: <em>Kan kunstig intelligens brukes til å hente ut denne informasjonen fra journalen og fylle ut personskadeskjemaet automatisk?</em></p>
      <p>Ideen treffer et reelt og udekket behov som også vil spare helsepersonell for administrative oppgaver: å automatisere en lovpålagt, men svært ressurskrevende prosess pga mengde registreinger – og dermed sikre bedre og mer fullstendig skadestatistikk. Prosjektets resultat har potensiale for alle som bruker DIPS i dag.</p>
    </div>
  </div>

  <div class="intro-section">
    <div class="intro-section-title">Hva er Fyrtårnprosjektet?</div>
    <div class="intro-body">
      <p>Fyrtårnprosjektet er et nasjonalt prosjekt finansiert av Helse- og omsorgsdepartementet (HOD) og Samferdselsdepartementet (SD). Det har som mål å bedre registrering og kvalitet på skadedata i Norge, med UNN Tromsø som ett av de sentrale sykehusene som er med i prosjektet.</p>
      <p>Som skadekoordinator i Fyrtårnprosjektet ved UNN skal Ida Wood Aasland bidra til komplett personskaderegistrering ved UNN Tromsø. Prosjektet gir mandat og faglig forankring for arbeidet med å forbedre registreringsprosessen – og KI-prosjektet springer direkte ut av erfaringene med hvor vanskelig og personavhengig registreringen er i dag.</p>
      <p>Fyrtårnprosjektet er ikke et e-helseprosjekt i Helsedirektoratets forstand, og personskaderegisteret er heller ikke et helseregister – noe som fikk betydning for hvilke søknadsveier som var aktuelle. Registreringen er forankret i lov gjennom Norsk pasientregisterforskrift §1-7 og Helsepersonelloven §26, noe som også åpner for muligheten til å unngå søknad om fritakelse fra taushetsplikten og få tilgang til pasientdata for testing.</p>
      <p>KI-innovasjonsprosjektet er Idas initiativ for å modernisere selve prosessen bak registreringen, og er ment å løfte arbeidet fra enkeltpersonavhengig manuell inntasting til en skalerbar, automatisert løsning integrert i DIPS Arena.</p>
    </div>
  </div>

  <div class="intro-section">
    <div class="intro-section-title">Prosjektets hovedutfordringer underveis</div>
    <div class="intro-body">
      <p><strong>Tilgang til pasientdata</strong> viste seg å være den viktigste hindringen. Uten journaldata kan ingen KI-modell trenes eller testes på en valid måte. PVO ved UNN manglet kunnskap om bruk av språkmodeller med sensitive journaldata og kunne ikke godkjenne et nytt prosjekt. Dispensasjonssøknad til Helsedirektoratet stagnerte pga manglende kunnskap hos Skadekoordinatoren på teknisk løsninger som blant annet lagring av data som hentes ut av journaler. Norsk Helsenett og FHI hadde ingen tilgjengelige anonymiserte data som kunne brukes. Løsningen kom gjennom SPKI og prosjektet QUAKE II, som ble godkjent i fagrådsmøte februar 2026 – og ga masterstudentene tilgang de trengte.</p>
      <p><strong>Juridisk kompleksitet</strong> preget hele prosjektperioden. Lovforankringen i Helsepersonelloven §29 og pasientregisterforskriften ble avgjørende.</p>
      <p><strong>Teknisk usikkerhet</strong> rundt DIPS-språkmodellen og RPA-løsninger ble avklart tidlig – RPA var uegnet fordi data ikke var nok strukturert, og DIPS med KI satsning ble den rette teknologipartneren som resulterte i engasjement av studenter ved UiT og en masteroppgave. Masteroppgaven viser at informasjon i behandlerdokumentasjonen i dag er for ufullstendig til komplett automatisering – men at løsningen ligger i kombinasjonen av tale-til-notat og AIS-gradering av ICD-10-koder i «Smart journal».</p>
    </div>
  </div>
</div>
</div>

<!-- ══════════════════════════════════
     PANEL 2: TIDSLINJE
══════════════════════════════════ -->
<div class="panel" id="panel-timeline">

<div class="legend">
  <span style="font-weight:500;color:var(--text);margin-right:4px">Status:</span>
  <div class="l-item"><span class="l-pip" style="background:var(--done)"></span>Fullført</div>
  <div class="l-item"><span class="l-pip" style="background:var(--ongoing)"></span>Pågående</div>
  <div class="l-item"><span class="l-pip" style="background:var(--dropped)"></span>Forkastet</div>
  <div class="l-item" style="margin-left:8px;padding-left:12px;border-left:1px solid var(--border)">
    <span style="width:10px;height:10px;border-left:3px solid var(--accent);display:inline-block"></span>&nbsp;Vendepunkt
  </div>
  <div class="l-item">
    <span style="width:10px;height:10px;border-left:3px solid var(--done);display:inline-block"></span>&nbsp;Prosjektresultat
  </div>
</div>

<div class="tl-wrap">
  <nav class="sidebar">
    <div class="sid-lbl">År</div>
    <button class="yr-btn y2023" onclick="scrollToYr('yr2023')">2023<span class="cnt">4 hendelser</span></button>
    <button class="yr-btn y2024" onclick="scrollToYr('yr2024')">2024<span class="cnt">10 hendelser</span></button>
    <button class="yr-btn y2025" onclick="scrollToYr('yr2025')">2025<span class="cnt">9 hendelser</span></button>
    <button class="yr-btn y2026" onclick="scrollToYr('yr2026')">2026<span class="cnt">5 hendelser</span></button>
  </nav>

  <main class="tl-content">
    <div class="progress-wrap">
      <div class="pb-bg"><div class="pb-fill" style="width:100%"></div></div>
      <div class="pb-lbl">Prosjekt fullført · 13 fullførte, 2 pågående, 7 forkastet · 2 år 7 måneder</div>
    </div>

    <!-- ══ 2023 ══ -->
    <section class="yr-section" id="yr2023">
      <div class="yr-hdr">
        <span class="yr-num y2023">2023</span>
        <span class="yr-tag">Idéen tar form</span>
        <span class="yr-cnt">4 hendelser</span>
      </div>
      <div class="mini-tl">
        <div class="mini-evt"><div class="mini-dot done key"></div><span class="mini-date">Okt 2023</span><span class="mini-name">Kontakt SPKI ⚡</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Nov 2023</span><span class="mini-name">Innmeldt Induct</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Des 2023</span><span class="mini-name">Innovasjonsteamet</span></div>
        <div class="mini-evt"><div class="mini-dot done key"></div><span class="mini-date">Mar 2024</span><span class="mini-name">DIPS – Bjørn ⚡</span></div>
      </div>
      <div class="events">

        <div class="ev key">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 1 · Idéutvikling og forankring</div>
            <div class="ev-top"><div class="ev-title">Kontakt med SPKI – Karl Øyvind Mikalsen</div></div>
            <div class="ev-meta"><span class="ev-date">09.10.23 → Okt–Des 2023</span><span class="ev-tag">⚡ Vendepunkt</span></div>
            <div class="ev-desc">Sendte kontaktskjema til SPKI 09.10.23. Innlegg om Fyrtårnprosjektet på fellesmøte for SPKI 17.10.23 – ca. 17 deltakere. Spørsmål til SPKI: Kan KI hente informasjon fra strukturert journal og fylle inn personskadeskjema i DIPS Arena automatisk?</div>
            <div class="ev-comment">«Døråpner for videre samarbeid». 3 møter: 17.10, 20.11, 11.12.23. SPKI positiv og ønsket klinisk prosjektleder. Pågående prosjekter med lignende formål omtalt.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 1 · Idéutvikling og forankring</div>
            <div class="ev-top"><div class="ev-title">Innmelding innovasjonsidé – Induct / Helse Nord</div></div>
            <div class="ev-meta"><span class="ev-date">23.11.23</span></div>
            <div class="ev-desc">Meldt inn som innovasjonsidé på unn.induct.no: «Registrering av personskadeskjema ved hjelp av KI». Ideen tilgjengelig nasjonalt i Induct-systemet.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 1 · Idéutvikling og forankring</div>
            <div class="ev-top"><div class="ev-title">Presentasjon for Innovasjonsteamet UNN</div></div>
            <div class="ev-meta"><span class="ev-date">08.12.23</span></div>
            <div class="ev-desc">Ida presenterer Fyrtårnprosjektet for Innovasjonsteamet. 4 medlemmer deltok. Stort engasjement. Innovasjonsteamet kjenner til Børge Ytterstads arbeid i Harstad. De kan bistå med møter med eksterne parter og søknad om midler.</div>
          </div>
        </div>

      </div>
    </section>

    <!-- ══ 2024 ══ -->
    <section class="yr-section" id="yr2024">
      <div class="yr-hdr">
        <span class="yr-num y2024">2024</span>
        <span class="yr-tag">Forankring og tidlige veivalg</span>
        <span class="yr-cnt">10 hendelser</span>
      </div>
      <div class="mini-tl">
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Jan 2024</span><span class="mini-name">Norinnova</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Feb 2024</span><span class="mini-name">KI-gruppe UNN</span></div>
        <div class="mini-evt"><div class="mini-dot done key"></div><span class="mini-date">Mar 2024</span><span class="mini-name">DIPS – Bjørn ⚡</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Apr 2024</span><span class="mini-name">FHI-kontakt</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Mai 2024</span><span class="mini-name">PVO-møte</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Mai 2024</span><span class="mini-name">BUK-midler</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Mai 2024</span><span class="mini-name">Hdir webinar</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Jun 2024</span><span class="mini-name">HN-IKT</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Okt 2024</span><span class="mini-name">Helse Vest IKT</span></div>
        <div class="mini-evt"><div class="mini-dot dropped"></div><span class="mini-date">2024</span><span class="mini-name">Hdir-søknad ✖</span></div>
      </div>
      <div class="events">

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 1 · Idéutvikling og forankring</div>
            <div class="ev-top"><div class="ev-title">Møte Norinnova – NER-modell og automatisk høsting</div></div>
            <div class="ev-meta"><span class="ev-date">04.01.24</span></div>
            <div class="ev-desc">Møte med Norinnova (Ingrid Skjæveland), Siv-Hege Blikfeldt, Lars Ailo Bongo og Mohsen Gamal Saad Askar (produktutvikler). Gjennomgang av Induct og NER-modell for journaluttrekk. Estimat: kr 200 000,- / 2 mnd for første resultater.</div>
            <div class="ev-comment">Krevende pga. personvern ved ekstern part. PVO tipset om pilot med ~30 pasienter og dispensasjonssøknad til Hdir.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 1 · Idéutvikling og forankring</div>
            <div class="ev-top"><div class="ev-title">Møte arbeidsgruppe for administrativ KI i UNN + Kent-Ole Larsen</div></div>
            <div class="ev-meta"><span class="ev-date">31.01.24 og 02.02.24</span></div>
            <div class="ev-desc">Ida presenterer prosjektet for arbeidsgruppen (31.01.24). Oppfølgingsmøte med produktutvikler Kent-Ole Larsen 02.02.24 – Ida viser DIPS-skjema opprettet fra bunnen av. RPA er dårlig rigget for formålet. Språkmodeller anbefalt.</div>
          </div>
        </div>

        <div class="ev key">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 1 · Idéutvikling og forankring</div>
            <div class="ev-top"><div class="ev-title">Kontakt og møte DIPS – Bjørn Fjukstad</div></div>
            <div class="ev-meta"><span class="ev-date">19.03.24 → Møte 21.03.24</span><span class="ev-tag">⚡ Vendepunkt</span></div>
            <div class="ev-desc">Via DIPS-podkast: Ida tar kontakt med Bjørn Fjukstad (produkteier for språkmodeller). Møte 21.03.24 med Bjørn og Eivind Holt. DIPS i startfasen for språkmodeller – personskadeskjema kan være starten på mange uttrekk DIPS ønsker å teste. Bjørn svært interessert.</div>
            <div class="ev-comment">Bjørn nå i pappaperm. Vidar Åsbakk er kontaktperson. Bjørn deltok på Workshop 01.07.25.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 2 · Juridisk avklaring</div>
            <div class="ev-top"><div class="ev-title">Kontakt med FHI-prosjektleder – Eva Håndlykken, Fyrtårnprosjektet</div></div>
            <div class="ev-meta"><span class="ev-date">Epost 27.04.24</span></div>
            <div class="ev-desc">Kontakt med Eva Håndlykken for å avklare hvorfor personskaderegisteret ikke er en del av e-helseregistrene hos Helsedirektoratet – og dermed ikke er tilgjengelig via enklere søknadsveier.</div>
            <div class="ev-comment">Konklusjon: Personskaderegistrering er lovpålagt via Norsk pasientregisterforskrift – ikke et helseregister. Dette fikk juridisk betydning for søknadsstrategien.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 2 · Juridisk avklaring</div>
            <div class="ev-top"><div class="ev-title">Møte PVO UNN – avklaring prosjektregistrering</div></div>
            <div class="ev-meta"><span class="ev-date">15.05.24</span></div>
            <div class="ev-desc">Tilstede: Ida, Karl-Petter Simonsen (PVO), John Christian Vedal (PVO), Siv-Hege Blikfeldt(innovasjonsteamet). Spørsmål: Kan prosjekt 3125 utvides, eller må nytt prosjekt meldes inn?</div>
            <div class="ev-comment">Konklusjon: Nytt prosjekt nødvendig. PVO anbefalte å vente – manglet kunnskap om bruk av språkmodeller med sensitive journaldata. Prosessen stoppet opp, og nytt prosjekt ikke meldt inn da QUAKE II løste datatilgangen i 2026.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 1 · Idéutvikling og forankring</div>
            <div class="ev-top"><div class="ev-title">BUK forskningsmidler tildelt + Forskningsdag BUK</div></div>
            <div class="ev-meta"><span class="ev-date">08.05.24 + 31.05.24</span></div>
            <div class="ev-desc">Kr 82 000,- tildelt fra BUK forskningsfond 08.05.24. 10-minutters presentasjon på Forskningsdag BUK 31.05.24. Grunnlag: Fyrtårnprosjektet og Årsrapport personskadedata 2023 (FHI).</div>
            <div class="ev-comment">Midler ble ikke benyttet – prosjektet ikke i gang og uklart hva prosjektmidlene kunne brukes til - Lønn?, fribruk?... En helhetsvurdering ble tatt av Skadekoordinator - prosjekt først utsatt til 2025 - prosessen ble så avsluttet - kan evt. søke på nytt i 2026.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 1 · Idéutvikling og forankring</div>
            <div class="ev-top"><div class="ev-title">Helsedirektoratet – webinar og kunnskapsgrunnlag KI</div></div>
            <div class="ev-meta"><span class="ev-date">23.05.24</span></div>
            <div class="ev-desc">Deltok på Hdir webinar: «Plan for trygg innføring av KI i helse». Satte seg inn i kunnskapsgrunnlaget «Store språkmodeller i helse- og omsorgstjenesten» publisert 06.05.24. Fulgte nettverket KIN (Kunstig intelligens i norsk helsetjeneste).</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 1 · Idéutvikling og forankring</div>
            <div class="ev-top"><div class="ev-title">Møte HN-IKT</div></div>
            <div class="ev-meta"><span class="ev-date">20.06.24</span></div>
            <div class="ev-desc">Møte med Michelle Hokland, Are Edvardsen, Eivind Larsen og Magnus Engeset. Ida presenterer Fyrtårnprosjektet og ønske om automatisering. Tips om June Nepstad Knappskog (strukturerte skjemaer i DIPS) og om personskadeskjema som pasientoppgave i Helse Vest.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 1 · Idéutvikling og forankring</div>
            <div class="ev-top"><div class="ev-title">Kontakt Helse Vest IKT – Marte Reinkind</div></div>
            <div class="ev-meta"><span class="ev-date">Epost 01.10.24</span></div>
            <div class="ev-desc">Tips fra HN-IKT om at Helse Vest har innført personskadeskjema som pasientoppgave. Epost til Marte Reinkind for å høre om det er enkelt å generere skjemaet som pasientoppgave og om de kan dele sitt skjema.</div>
            <div class="ev-comment">Ikke fått svar. HN-IKT tar kommunikasjon videre.</div>
          </div>
        </div>

        <div class="ev dropped">
          <div class="ev-left"><div class="ev-dot dropped"></div><span class="badge dropped">✖</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 2 · Juridisk avklaring</div>
            <div class="ev-top"><div class="ev-title">Søknad Helsedirektoratet – dispensasjon fra taushetsplikt</div></div>
            <div class="ev-meta"><span class="ev-date">Uke 20, 2024</span></div>
            <div class="ev-desc">Utkast laget for søknad om dispensasjon for å hente ut journalinformasjon fra EPJ til KI-modellen. Søknaden stopper opp fordi det er uklart hvordan data lagres og hvordan DIPS-modellen brukes til formålet - DIPS har ikke egen risikoanalyse – mer informasjon var nødvendig for å besvare søknadskravene.</div>
            <div class="ev-comment">Forkastet – ikke nødvendig da løsning via SPKI og QUAKE II kom opp i 2025/2026.</div>
          </div>
        </div>

      </div>
    </section>

    <!-- ══ 2025 ══ -->
    <section class="yr-section" id="yr2025">
      <div class="yr-hdr">
        <span class="yr-num y2025">2025</span>
        <span class="yr-tag">Gjennombrudd og avgjørende samarbeid</span>
        <span class="yr-cnt">9 hendelser</span>
      </div>
      <div class="mini-tl">
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Apr 2025</span><span class="mini-name">FORSK HN-IKT</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Mai 2025</span><span class="mini-name">SKDE – Heidi</span></div>
        <div class="mini-evt"><div class="mini-dot dropped"></div><span class="mini-date">Mai 2025</span><span class="mini-name">RPA ✖</span></div>
        <div class="mini-evt"><div class="mini-dot done key"></div><span class="mini-date">01.07.25</span><span class="mini-name">Workshop ⚡</span></div>
        <div class="mini-evt"><div class="mini-dot done key"></div><span class="mini-date">Aug 2025</span><span class="mini-name">UiT-studenter ⚡</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Sep 2025</span><span class="mini-name">E-helse webinar</span></div>
        <div class="mini-evt"><div class="mini-dot done key"></div><span class="mini-date">27.10.25</span><span class="mini-name">Trepartsmøte ⚡</span></div>
        <div class="mini-evt"><div class="mini-dot dropped"></div><span class="mini-date">2025</span><span class="mini-name">NHN ✖</span></div>
        <div class="mini-evt"><div class="mini-dot dropped"></div><span class="mini-date">—</span><span class="mini-name">HN-IKT jurist ✖</span></div>
      </div>
      <div class="events">

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 2 · Juridisk avklaring</div>
            <div class="ev-top"><div class="ev-title">Kontakt FORSK – Jonas Nordhaug Myhre, HN-IKT</div></div>
            <div class="ev-meta"><span class="ev-date">30.04.25 → 02.05.25</span></div>
            <div class="ev-desc">Meldt inn forespørsel til FORSK om prosjektet kan unntas taushetsplikt via Helsepersonelloven §26 og Norsk pasientregisterforskrift §1-7. Møte på Teams 02.05.25 med Jonas Nordhaug Myhre.</div>
            <div class="ev-comment">FORSK manglet verktøy for å hjelpe direkte. Representant Vebjørn deltok på Workshop 01.07.25 og bidro med erfaringsutveksling fra QUAKE II-datauttrekk.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 2 · Juridisk avklaring</div>
            <div class="ev-top"><div class="ev-title">Jurist SKDE – Heidi Talsethagen</div></div>
            <div class="ev-meta"><span class="ev-date">05.05.25</span></div>
            <div class="ev-desc">Kontakt via Philip André Skau. Telefonsamtale med Heidi Talsethagen (jurist, SKDE) 05.05.25. Positiv til prosjektet. Avklarte at dispensasjon kan unngås om formålet er forankret i forskriften alene – men ved UiT-studenter inne må dispensasjon søkes.</div>
            <div class="ev-comment">Heidi deltok på Workshop 01.07.25 og er tilgjengelig for videre kontakt.</div>
          </div>
        </div>

        <div class="ev dropped">
          <div class="ev-left"><div class="ev-dot dropped"></div><span class="badge dropped">✖</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 3 · Datainnhenting og teknisk løsning</div>
            <div class="ev-top"><div class="ev-title">RPA-løsning – Digitale tjenester, Kent Ole Larsen</div></div>
            <div class="ev-meta"><span class="ev-date">23.05.25</span></div>
            <div class="ev-desc">Møte med Kent-Ole Larsen for å undersøke om RPA fra fritekst kan automatisere utfylling av personskadeskjema.</div>
            <div class="ev-comment">Forkastet – ikke mulig å automatisere via RPA. RPA er dårlig rigget for dette formålet.</div>
          </div>
        </div>

        <div class="ev key">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 3 · Datainnhenting og teknisk løsning</div>
            <div class="ev-top"><div class="ev-title">Workshop – alle interessenter samlet</div></div>
            <div class="ev-meta"><span class="ev-date">01.07.25</span><span class="ev-tag">⚡ Vendepunkt</span></div>
            <div class="ev-desc">Workshop med PVO, SPKI, HN-IKT, DIPS, SKDE og FORSK. Tema: personvern, etikk, språkmodell, risikovurdering, datalagring, juridisk forankring. Miro-tavle brukt. Innkjøp: kanelboller.</div>
            <div class="ev-comment">Deltakere: Bjørn (DIPS), Karl Øyvind + Vebjørn (SPKI), Heidi (SKDE), Jonas/Vebjørn (FORSK/HN-IKT), Joel. Avgjørende samling for prosjektets fremdrift.</div>
          </div>
        </div>

        <div class="ev key">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 4 · Masterprosjekt og pilotering</div>
            <div class="ev-top"><div class="ev-title">UiT-masterstudenter engasjert – Håvard og Ludvig</div></div>
            <div class="ev-meta"><span class="ev-date">Aug–Sep 2025, presentasjon 25.09.25</span><span class="ev-tag">⚡ Avgjørende</span></div>
            <div class="ev-desc">DIPS engasjerer 2 UiT-studenter for masteroppgave om KI og personskadeskjema. Ida presenterer Fyrtårnprosjektet for studenter og veileder Einar Holsbøe 25.09.25. Masterprosjektbeskrivelse fra DIPS datert 30.04.25.</div>
            <div class="ev-comment">Samarbeid: UNN–DIPS–UiT–SPKI–HN-IKT.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 3 · Datainnhenting og teknisk løsning</div>
            <div class="ev-top"><div class="ev-title">E-helse webinarer om syntetiske pasientdata og KI</div></div>
            <div class="ev-meta"><span class="ev-date">04.09.25 og 14.01.26</span></div>
            <div class="ev-desc">04.09.25: «Hvordan bruke syntetiske pasientdata for å utvikle trygge KI-løsninger». 14.01.26: «KI i praksis – erfaringer med automatisk journalsammendrag». Begge webinarer fra ehealthresearch.no.</div>
            <div class="ev-comment">Inspirerte til kontakt med Norsk Helsenett – som dessverre ikke hadde data å gi ut.</div>
          </div>
        </div>

        <div class="ev key">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 3 · Datainnhenting og teknisk løsning</div>
            <div class="ev-top"><div class="ev-title">Møte SPKI + DIPS + UNN – QUAKE II-løsningen</div></div>
            <div class="ev-meta"><span class="ev-date">27.10.25</span><span class="ev-tag">⚡ Avgjørende</span></div>
            <div class="ev-desc">Epost fra Bjørn 30.09.25 innkaller til møte. Deltakere: Ida, Bjørn Fjukstad (DIPS) og Karl Øyvind (SPKI). Lovforankring: Helsepersonelloven §29 (klinisk beslutningsverktøy). Ny vending: Karl Øyvind foreslår QUAKE II som paraply.</div>
            <div class="ev-comment">Karl Øyvind oppretter innovasjonsprosjektet som underprosjekt til QUAKE II. Miniprotokoll skrives – Ida bidrar. Avgjørende gjennombrudd for tilgang til pasientdata.</div>
          </div>
        </div>

        <div class="ev dropped">
          <div class="ev-left"><div class="ev-dot dropped"></div><span class="badge dropped">✖</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 3 · Datainnhenting og teknisk løsning</div>
            <div class="ev-top"><div class="ev-title">Norsk Helsenett – anonymisert pasientdata</div></div>
            <div class="ev-meta"><span class="ev-date">2025</span></div>
            <div class="ev-desc">Undersøkte datasjø med anonymiserte pasientdata fra Norsk Helsenett. Kontaktet også FHI avd. Pasientregister i etterkant.</div>
            <div class="ev-comment">Forkastet – NHN har ikke data å gi ut enda, tross markedsføring av datasjø. FHI hadde heller ikke kapasitet. Samarbeid avsluttet.</div>
          </div>
        </div>

        <div class="ev dropped">
          <div class="ev-left"><div class="ev-dot dropped"></div><span class="badge dropped">✖</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 2 · Juridisk avklaring</div>
            <div class="ev-top"><div class="ev-title">Kontakt Helse Nord IKT – jurist</div></div>
            <div class="ev-meta"><span class="ev-date">—</span></div>
            <div class="ev-comment">Forkastet – ikke nødvendig da prosjektet fikk tilgang til pasientdata via QUAKE II-prosjektet.</div>
          </div>
        </div>

      </div>
    </section>

    <!-- ══ 2026 ══ -->
    <section class="yr-section" id="yr2026">
      <div class="yr-hdr">
        <span class="yr-num y2026">2026</span>
        <span class="yr-tag">Mål nådd – og videre</span>
        <span class="yr-cnt">5 hendelser</span>
      </div>
      <div class="mini-tl">
        <div class="mini-evt"><div class="mini-dot done key"></div><span class="mini-date">24.02.26</span><span class="mini-name">QUAKE II ⚡</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">Jan–Mar 2026</span><span class="mini-name">Akuttmottaket</span></div>
        <div class="mini-evt"><div class="mini-dot done"></div><span class="mini-date">15.05.26</span><span class="mini-name">Masteroppgave 🏁</span></div>
        <div class="mini-evt"><div class="mini-dot ongoing"></div><span class="mini-date">Sommer 2026</span><span class="mini-name">Publisering</span></div>
        <div class="mini-evt"><div class="mini-dot ongoing"></div><span class="mini-date">Videre</span><span class="mini-name">Smart journal</span></div>
      </div>
      <div class="events">

        <div class="ev key">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 3 · Datainnhenting og teknisk løsning</div>
            <div class="ev-top"><div class="ev-title">QUAKE II godkjent – tilgang til pasientdata</div></div>
            <div class="ev-meta"><span class="ev-date">24.02.26</span><span class="ev-tag">⚡ Avgjørende</span></div>
            <div class="ev-desc">Karl Øyvind melder inn innovasjonsprosjektet som underprosjekt til QUAKE II hos SPKI. Godkjent i fagrådsmøte for bruk av pasientdata til undersøkelser om automatisering av skadedata. Håvard ansettes 0% i SPKI for tilgang via HN-IKT server.</div>
            <div class="ev-comment">Avgjørende for at studentene fikk tilgang til pasientdata å teste forskjellige LLM modeller på.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 4 · Masterprosjekt og pilotering</div>
            <div class="ev-top"><div class="ev-title">Akuttmottaket Tromsø involvert – caseutfylling</div></div>
            <div class="ev-meta"><span class="ev-date">Involvert 12.01.26 · Levert 12.03.26</span></div>
            <div class="ev-desc">Akuttmottaket fyller ut personskadeskjema for 50 KI-genererte caser (2 sekretærer, 25 caser hver). Ida fyller ut 50 caser som skadekoordinator. Disse sees opp mot KI-modellens resultater i masteroppgaven.</div>
            <div class="ev-comment">Akuttmottaket fikk gavekort finansiert av Fyrtårnprosjektet.</div>
          </div>
        </div>

        <div class="ev finish">
          <div class="ev-left"><div class="ev-dot done"></div><span class="badge done">✔</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 4 · Masterprosjekt og pilotering</div>
            <div class="ev-top"><div class="ev-title">Masteroppgave levert – UiT</div></div>
            <div class="ev-meta"><span class="ev-date">15.05.26</span><span class="ev-tag finish">🏁 Prosjektresultat</span></div>
            <div class="ev-desc">Ludvig og Håvard leverer masteroppgave om KI og automatisk utfylling av personskadeskjema. Samarbeid: UNN Tromsø, Akuttmottaket Tromsø, SPKI, DIPS, HN-IKT og UiT. Prosjektet ansees som vellykket.</div>
            <div class="ev-comment">Sentralt funn: Informasjon mangler i behandlerdokumentasjonen for å fylle ut skjema komplett. Skadekoordinators syn: Videre løsningen ligger i tale-til-notat og AIS-gradering av ICD-10-koder for «Smart journal» som er et nasjonalt prosjekt. DIPS tar dette videre inn i prosjektet.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot ongoing"></div><span class="badge ongoing">◉</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 5 · Realisering og videre arbeid</div>
            <div class="ev-top"><div class="ev-title">Publisering av masteroppgavefunn</div></div>
            <div class="ev-meta"><span class="ev-date">Sommer 2026</span></div>
            <div class="ev-desc">Bjørn Fjukstad (DIPS) ønsker publisering av funn fra masteroppgaven – Northern Lights Deep Learning Conference vurderes.</div>
          </div>
        </div>

        <div class="ev">
          <div class="ev-left"><div class="ev-dot ongoing"></div><span class="badge ongoing">◉</span></div>
          <div class="ev-right">
            <div class="ev-phase">Fase 5 · Realisering og videre arbeid</div>
            <div class="ev-top"><div class="ev-title">Forankring i DIPS «Smart journal»</div></div>
            <div class="ev-meta"><span class="ev-date">Usikker tidshorisont</span></div>
            <div class="ev-desc">DIPS tar med seg personskaderegistrering inn i det nasjonale prosjektet «Smart journal».</div>
          </div>
        </div>

      </div>
    </section>
  </main>
</div><!-- tl-wrap -->
</div><!-- panel-timeline -->

<!-- ══════════════════════════════════
     PANEL 3: INTERESSENTER
══════════════════════════════════ -->
<div class="panel" id="panel-stakeholders">
<div class="section-wrap">
  <h2 class="section-title">Interessenter</h2>
  <p class="section-desc">Aktører som har hatt rolle, interesse eller innflytelse i prosjektet · Basert på interessentanalyse i arbeidsdokumentet</p>

  <div class="int-grid">
    <div class="int-card">
      <div class="int-name">DIPS</div>
      <div class="int-role">Teknologipartner og initiativtaker til masteroppgave. Bjørn Fjukstad og Vidar Åsbakk + Eivind Holt. Ansvarlig for språkmodell og DIPS Arena-integrasjon.</div>
      <div class="int-tags"><span class="int-tag core">Kjernepartner</span><span class="int-tag core">Teknologi</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">SPKI – Senter for pasientnær Kunstigintelligens</div>
      <div class="int-role">Karl Øyvind Mikalsen (avdelingsleder) og Vebjørn. Faglig partner, QUAKE II-paraplyen og tilgang til pasientdata. Avgjørende for prosjektets gjennomføring.</div>
      <div class="int-tags"><span class="int-tag core">Kjernepartner</span><span class="int-tag core">Datainnhenting</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">UiT – Masterstudenter</div>
      <div class="int-role">Håvard og Ludvig. Engasjert av DIPS. Veileder: Einar Holsbøe, UiT. Gjennomførte masteroppgaven som er prosjektets leveranse.</div>
      <div class="int-tags"><span class="int-tag core">Kjernepartner</span><span class="int-tag core">Forskning</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">HN-IKT / FORSK</div>
      <div class="int-role">Michelle Hokland, Are Edvardsen, Eivind Larsen, Magnus Engeset. Jonas Nordhaug Myhre (FORSK). Datainfrastruktur, tilgang via server for Håvard.</div>
      <div class="int-tags"><span class="int-tag support">Støttepartner</span><span class="int-tag support">Infrastruktur</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">Akuttmottaket Tromsø</div>
      <div class="int-role">Bidro med caseutfylling – 2 sekretærer fylte ut 50 caser til sammenligning mot KI-modellen. Klinisk pilotering.</div>
      <div class="int-tags"><span class="int-tag core">Klinisk pilot</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">UNN – PVO</div>
      <div class="int-role">John Christian Vedal, Karl-Petter Simonsen. Personvernombud. Viktig for prosjektregistrering og godkjenning. Begrenset av manglende kunnskap om språkmodeller.</div>
      <div class="int-tags"><span class="int-tag support">Godkjenning</span><span class="int-tag support">Personvern</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">SKDE – Jurist</div>
      <div class="int-role">Heidi Talsethagen. Juridisk støtte – avklarte at dispensasjonssøknad kan unngås under gitte forutsetninger. Deltok på workshop.</div>
      <div class="int-tags"><span class="int-tag support">Juridisk</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">Innovasjonsteamet UNN</div>
      <div class="int-role">Siv-Hege Blikfeldt, Magnus Engeset - Heier på Innovasjonsprosjektet - en uvurderlig støtte. Hjelp med møter og søknader. Koblet Ida til Norinnova og andre ressurser i og utenfor UNN.</div>
      <div class="int-tags"><span class="int-tag support">Innovasjon</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">Fyrtårnprosjektet / FHI</div>
      <div class="int-role">Eva Håndlykken (FHI). Avklarte at personskaderegisteret ikke er et helseregister – viktig for søknadsstrategi og juridisk forankring.</div>
      <div class="int-tags"><span class="int-tag info">Kontekst</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">Helsedirektoratet</div>
      <div class="int-role">Webinar og kunnskapsgrunnlag om KI i helse. Søknad om dispensasjon fra taushetsplikt vurdert, men forkastet. Plan for trygg innføring av KI.</div>
      <div class="int-tags"><span class="int-tag info">Myndighetsorgan</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">Norinnova</div>
      <div class="int-role">Ingrid Skjæveland, Mohsen Gamal Saad Askar. Mulig teknologileverandør for NER-modell. Estimat gitt, men ikke videreført pga. personvernutfordringer og manglende pasientdata.</div>
      <div class="int-tags"><span class="int-tag forkastet">Forkastet</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">Norsk Helsenett / FHI Pasientregister</div>
      <div class="int-role">Undersøkt som kilde for anonymiserte pasientdata. Verken NHN eller FHI avd. Pasientregister hadde tilgjengelige data eller kapasitet for å jobbe med dette.</div>
      <div class="int-tags"><span class="int-tag forkastet">Forkastet</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">Helse Vest IKT – Marte Reinkind</div>
      <div class="int-role">Helse Vest har innført personskadeskjema som pasientoppgave. Kontaktet for erfaringsutveksling. Ikke fått svar – HN-IKT tar kommunikasjon videre.</div>
      <div class="int-tags"><span class="int-tag info">Erfaringsutveksling</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">Traumeregisteret</div>
      <div class="int-role"> Veslemøy (registeret) - Internt i UNN Helle Traumeavdelingen - Interessent i personskadedata og registreringsprosessen. Tilstøtende fagmiljø som berøres av bedre skaderegistrering.</div>
      <div class="int-tags"><span class="int-tag info">Fagmiljø</span></div>
    </div>
    <div class="int-card">
      <div class="int-name">Skadeforebyggende forum</div>
      <div class="int-role">Eva i Skafor - Nasjonal aktør innen skadeforebygging. Nyttiggjør seg av personskadedata for statistikk og forebygging.</div>
      <div class="int-tags"><span class="int-tag info">Fagmiljø</span></div>
    </div>
  </div>
</div>
</div>

<!-- ══════════════════════════════════
     PANEL 4: GEVINSTER
══════════════════════════════════ -->
<div class="panel" id="panel-gains">
<div class="section-wrap">
  <h2 class="section-title">Gevinster</h2>
  <p class="section-desc">Forventede og realiserte gevinster ved KI-assistert personskaderegistrering</p>

  <div class="gains-grid">
    <div class="gain-card" style="border-left:3px solid var(--done)">
      <span class="gain-icon">📊</span>
      <div class="gain-title">Bedre kvalitet og fullstendighet på skadedata</div>
      <div class="gain-body">KI henter informasjon direkte fra strukturert journal, noe som reduserer menneskelige feil og mangler. Bedre grunnlag for nasjonal skadestatistikk og Norsk pasientregister.</div>
    </div>
    <div class="gain-card" style="border-left:3px solid var(--done)">
      <span class="gain-icon">⏱️</span>
      <div class="gain-title">Tidsbesparelse for klinisk personell</div>
      <div class="gain-body">Eliminerer manuell dobbeltregistrering. Behandlere slipper å fylle ut skjema separat i tillegg til dokumentasjon i journal – informasjonen hentes automatisk fra journalnotatene de allerede skriver.</div>
    </div>
    <div class="gain-card" style="border-left:3px solid var(--done)">
      <span class="gain-icon">📈</span>
      <div class="gain-title">Økt registreringsoppslutning nasjonalt</div>
      <div class="gain-body">Lav oppslutning har vært et vedvarende problem. Automatisering for utfylling av skadeskjema vil gi vesentlig høyere dekningsgrad - og har potensiale for økt registrering på alle norske sykehus som benytter DIPS i dag.</div>
    </div>
    <div class="gain-card" style="border-left:3px solid var(--accent)">
      <span class="gain-icon">🏥</span>
      <div class="gain-title">Bedre grunnlag for skadeforebygging</div>
      <div class="gain-body">Fullstendig og korrekt skaderegistrering gir kommuner, FHI og myndigheter bedre datagrunnlag for å identifisere risikofaktorer og iverksette målrettede forebyggingstiltak.</div>
    </div>
    <div class="gain-card" style="border-left:3px solid var(--accent)">
      <span class="gain-icon">🔗</span>
      <div class="gain-title">Nasjonal skalerbarhet via DIPS «Smart journal»</div>
      <div class="gain-body">Løsningen er ikke begrenset til UNN. Nasjonale prosjekt «Smart journal» har potensiale til å videreføre automatisert personskaderegistrering til alle sykehus som bruker DIPS Arena.</div>
    </div>
    <div class="gain-card" style="border-left:3px solid var(--accent)">
      <span class="gain-icon">🧬</span>
      <div class="gain-title">Forskningsverdi og kompetansebygging</div>
      <div class="gain-body">Masteroppgaven ved UiT genererer ny kunnskap om KI i klinisk registreringspraksis. Publisering planlegges til Northern Lights Deep Learning Conference. Bygger nasjonalt kompetansemiljø.</div>
    </div>
    <div class="gain-card" style="border-left:3px solid var(--y2025)">
      <span class="gain-icon">⚖️</span>
      <div class="gain-title">Juridisk rammeverk avklart</div>
      <div class="gain-body">Prosjektet har kartlagt og belyst utfordringer i juridiske spørsmål knyttet til bruk av pasientdata i LLM – nyttig kunnskap for fremtidige tilsvarende prosjekter i norsk helsesektor.</div>
    </div>
    <div class="gain-card" style="border-left:3px solid var(--y2025)">
      <span class="gain-icon">🤝</span>
      <div class="gain-title">Etablert tverrfaglig kontakt i forskjellige nettverk</div>
      <div class="gain-body">Samarbeidet mellom blant annet UNN Tromsø, DIPS, SPKI, UiT, HN-IKT, Akuttmottaket, SKDE, Ortopedik avdeling, FORSK-HN IKT. Etablerte nettverk og tverrfaglig samarbeid. Dette nettverket har verdi langt utover dette prosjektet.</div>
    </div>
    <div class="gain-card" style="border-left:3px solid var(--y2026)">
      <span class="gain-icon">🗂️</span>
      <div class="gain-title">Tale-til-notat + AIS-gradering</div>
      <div class="gain-body">Funnene peker mot at kombinasjonen av tale-til-notat (bedre dokumentasjon fra behandler) og automatisk AIS-gradering av ICD-10-koder vil gi tilnærmet komplett skjemautfylling.</div>
    </div>
  </div>
</div>
</div>

<script>
  function showTab(id, btn) {
    document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
    document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
    document.getElementById('panel-'+id).classList.add('active');
    btn.classList.add('active');
    animateCards();
  }

  function scrollToYr(id) {
    const el = document.getElementById(id);
    if (el) el.scrollIntoView({behavior:'smooth', block:'start'});
  }

  function animateCards() {
    document.querySelectorAll('.ev').forEach((card, i) => {
      card.style.transition = 'none';
      card.classList.remove('visible');
      setTimeout(() => {
        card.style.transition = 'opacity .32s ease, transform .32s ease';
        setTimeout(() => card.classList.add('visible'), 40 + i * 30);
      }, 10);
    });
  }

  // IntersectionObserver for scroll-triggered animation
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        observer.unobserve(e.target);
      }
    });
  }, {threshold: 0.08});
  document.querySelectorAll('.ev').forEach(c => observer.observe(c));

  // Sidebar year highlight on scroll
  const yrs = ['yr2023','yr2024','yr2025','yr2026'];
  const yrBtns = document.querySelectorAll('.yr-btn');
  const so = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        yrBtns.forEach(b => b.style.fontWeight='400');
        const idx = yrs.indexOf(e.target.id);
        if (idx>=0) yrBtns[idx].style.fontWeight='500';
      }
    });
  }, {threshold: 0.25});
  yrs.forEach(id => { const el=document.getElementById(id); if(el) so.observe(el); });
</script>
</body>
</html>
