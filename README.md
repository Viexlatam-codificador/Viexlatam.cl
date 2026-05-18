<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Viex Salud — Asesoría en Isapre</title>
<meta name="description" content="Asesoría gratuita en Isapre. Encuentra el mejor plan de salud para ti y tu familia. Cotiza sin compromiso.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600;700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  /* ESTILOS MÍNIMOS - FUNCIONA TODO */
  :root{--navy:#0a1628;--teal:#00b4a0;--teal-light:#00d4bc;--gold:#c9a84c;--white:#f7f5f0;--muted:#8a9bb5;--glass:rgba(255,255,255,0.04);--glass-border:rgba(255,255,255,0.08)}
 *{box-sizing:border-box;margin:0;padding:0}
  body{background:var(--navy);color:var(--white);font-family:'DM Sans',sans-serif;min-height:100vh;position:relative}
  body::before{content:'';position:fixed;inset:0;background:radial-gradient(ellipse 80% 60% at 20% 10%, rgba(0,180,160,0.12) 0%, transparent 60%),radial-gradient(ellipse 60% 80% at 85% 90%, rgba(201,168,76,0.08) 0%, transparent 60%);pointer-events:none;z-index:0}
  .container{position:relative;z-index:1;max-width:520px;margin:0 auto;padding:40px 20px 60px}
  .header{text-align:center;margin-bottom:30px}
  .logo-ring{width:80px;height:80px;border-radius:50%;background:linear-gradient(135deg,var(--teal),var(--gold));display:flex;align-items:center;justify-content:center;margin:0 auto 16px;box-shadow:0 0 40px rgba(0,180,160,0.3)}
  .logo-ring::before{content:'';position:absolute;inset:3px;border-radius:50%;background:var(--navy)}
  .logo-inner{position:relative;z-index:1;font-family:'Cormorant Garamond',serif;font-size:26px;font-weight:700;background:linear-gradient(135deg,var(--teal-light),#e8c97a);-webkit-background-clip:text;-webkit-text-fill-color:transparent}
  .brand-name{font-family:'Cormorant Garamond',serif;font-size:28px;font-weight:600;background:linear-gradient(135deg,#fff 40%,var(--teal-light));-webkit-background-clip:text;-webkit-text-fill-color:transparent;margin-bottom:6px}
  .brand-tagline{font-size:12px;color:var(--teal);letter-spacing:2px;text-transform:uppercase;margin-bottom:10px}
  .header-desc{font-size:13px;color:var(--muted);line-height:1.5}
  .free-badge{display:inline-flex;align-items:center;gap:6px;background:rgba(0,180,160,0.1);border:1px solid rgba(0,180,160,0.25);border-radius:100px;padding:5px 14px;font-size:11px;color:var(--teal-light);margin-bottom:24px}
  .links-section{display:flex;flex-direction:column;gap:10px}
  .link-card{display:flex;align-items:center;gap:14px;padding:14px 16px;background:var(--glass);border:1px solid var(--glass-border);border-radius:14px;text-decoration:none;color:var(--white);transition:all 0.3s}
  .link-card:hover{transform:translateY(-2px);border-color:rgba(255,255,255,0.2)}
  .icon-box{width:40px;height:40px;border-radius:10px;display:flex;align-items:center;justify-content:center;flex-shrink:0}
  .icon-box.green{background:rgba(37,211,102,0.15)}
  .icon-box.pink{background:rgba(225,48,108,0.15)}
  .icon-box.blue{background:rgba(24,119,242,0.15)}
  .icon-box.teal{background:rgba(0,180,160,0.15)}
  .link-text{flex:1}
  .link-title{font-size:14px;font-weight:500}
  .link-sub{font-size:11px;color:var(--muted);margin-top:2px}
  .link-arrow{color:var(--muted);font-size:18px}
  .trust-row{display:flex;flex-wrap:wrap;justify-content:center;gap:8px;margin-top:24px}
  .trust-pill{background:var(--glass);border:1px solid var(--glass-border);border-radius:100px;padding:5px 12px;font-size:10.5px;color:var(--muted)}
  .testi-viewport{width:100%;overflow:hidden;border-radius:16px;margin-top:24px}
  .testi-track{display:flex;gap:12px;width:max-content;animation:scroll 30s linear infinite}
  .testi-track:hover{animation-play-state:paused}
  @keyframes scroll{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}
  .testi-card{flex-shrink:0;width:240px;background:var(--glass);border:1px solid var(--glass-border);border-radius:14px;padding:16px}
  .testi-source{display:inline-flex;border-radius:100px;padding:3px 10px;font-size:10px;margin-bottom:10px}
  .testi-source.fb{background:rgba(24,119,242,0.15);color:#6baaf7}
  .testi-source.ig{background:rgba(225,48,108,0.15);color:#f087b0}
  .testi-source.wa{background:rgba(37,211,102,0.15);color:#5ee09a}
  .testi-stars{color:var(--gold);font-size:11px;margin-bottom:8px}
  .testi-text{font-size:12px;color:rgba(247,245,240,0.8);line-height:1.5;font-style:italic}
  .testi-author{display:flex;align-items:center;gap:10px;margin-top:12px}
  .testi-avatar{width:30px;height:30px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:600;background:linear-gradient(135deg,var(--teal),var(--gold));color:var(--navy)}
  .testi-name{font-size:12px;font-weight:500}
  .testi-meta{font-size:10px;color:var(--muted)}
  .form-card{width:100%;background:var(--glass);border:1px solid var(--glass-border);border-radius:18px;padding:24px;margin-top:28px}
  .form-title{font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:600;margin-bottom:4px}
  .form-sub{font-size:12px;color:var(--muted);margin-bottom:18px}
  .form-sub span{color:var(--teal)}
  .form-group{margin-bottom:12px}
  .form-label{font-size:10px;font-weight:500;letter-spacing:1px;text-transform:uppercase;color:var(--muted);margin-bottom:5px}
  .form-input,.form-select{width:100%;background:rgba(255,255,255,0.04);border:1px solid var(--glass-border);border-radius:10px;padding:10px 14px;color:var(--white);font-family:'DM Sans',sans-serif;font-size:13px;outline:none}
  .form-input::placeholder{color:rgba(138,155,181,0.5)}
  .form-input:focus,.form-select:focus{border-color:rgba(0,180,160,0.5)}
  .form-select option{background:var(--navy)}
  .form-row{display:grid;grid-template-columns:1fr 1fr;gap:10px}
  .form-checkbox{display:flex;align-items:flex-start;gap:8px;margin:14px 0 18px}
  .form-checkbox input{width:14px;accent-color:var(--teal)}
  .form-checkbox label{font-size:11px;color:var(--muted);line-height:1.4}
  .btn-submit{width:100%;background:linear-gradient(135deg,var(--teal),#008f80);border:none;border-radius:12px;padding:14px;color:#fff;font-family:'DM Sans',sans-serif;font-size:14px;font-weight:500;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:8px}
  .btn-submit:hover{box-shadow:0 8px 24px rgba(0,180,160,0.35)}
  .success-msg{display:none;text-align:center;padding:20px}
  .success-msg h3{font-family:'Cormorant Garamond',serif;font-size:20px;color:var(--teal-light);margin-bottom:8px}
  .success-msg p{font-size:13px;color:var(--muted);line-height:1.6}
  .success-msg .btn-submit{margin-top:16px;text-decoration:none}
  .footer{text-align:center;font-size:10px;color:rgba(138,155,181,0.5);margin-top:32px;line-height:1.6}
  .footer a{color:var(--teal);text-decoration:none}
  .float-wa{position:fixed;bottom:20px;right:20px;width:54px;height:54px;background:#25D366;border-radius:50%;display:flex;align-items:center;justify-content:center;box-shadow:0 4px 20px rgba(37,211,102,0.4);z-index:999;transition:transform 0.3s}
  .float-wa:hover{transform:scale(1.1)}
  .float-wa svg{width:26px;height:26px;fill:white}
  .admin-panel{display:none;background:rgba(10,22,40,0.95);border:1px solid rgba(0,180,160,0.3);border-radius:14px;padding:16px;margin-top:12px}
  .admin-panel.open{display:block}
  .admin-toggle{width:100%;background:none;border:1px dashed rgba(255,255,255,0.15);border-radius:10px;padding:10px;color:var(--muted);font-size:11px;cursor:pointer;margin-top:12px;display:flex;align-items:center;justify-content:center;gap:6px}
  .admin-toggle:hover{border-color:var(--teal);color:var(--teal-light)}
  @media(max-width:480px){.container{padding:30px 16px 50px}.form-row{grid-template-columns:1fr}}
</style>
</head>
<body>

<!-- WhatsApp Flotante -->
<a href="https://wa.me/56948627767?text=Hola%2C%20me%20interesa%20obtener%20asesor%C3%ADa%20gratuita%20para%20contratar%20una%20Isapre" target="_blank" class="float-wa" title="Escríbenos por WhatsApp">
<svg viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
</a>

<div class="container">

  <!-- HEADER -->
  <div class="header">
    <div class="logo-ring"><span class="logo-inner">VS</span></div>
    <h1 class="brand-name">Viex Salud</h1>
    <p class="brand-tagline">Asesoría en Isapre · Chile</p>
    <p class="header-desc">Te ayudamos a encontrar el mejor plan de salud para ti y tu familia, sin costo y sin compromiso.</p>
  </div>

  <div class="free-badge">✦ Asesoría 100% gratuita y sin compromiso</div>

  <!-- ENLACES DIRECTOS -->
