<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SecureOS — Sistema de Segurança Avançado</title>
<style>
  :root {
    --bg: #0a0e1a;
    --bg2: #0f1420;
    --bg3: #141824;
    --sidebar: #0c1019;
    --card: #141824;
    --card2: #1a2030;
    --border: #1e2840;
    --accent: #00d4ff;
    --accent2: #7c3aed;
    --accent3: #10b981;
    --danger: #ef4444;
    --warning: #f59e0b;
    --text: #e2e8f0;
    --text2: #94a3b8;
    --text3: #64748b;
    --glow: 0 0 20px rgba(0,212,255,0.15);
    --glow2: 0 0 20px rgba(124,58,237,0.15);
  }
  * { margin:0; padding:0; box-sizing:border-box; }
  body { font-family: 'Segoe UI', system-ui, sans-serif; background:var(--bg); color:var(--text); overflow-x:hidden; }

  /* ── AUTH SCREEN ── */
  #auth-screen {
    position:fixed; inset:0; background:var(--bg);
    display:flex; align-items:center; justify-content:center;
    z-index:9999; overflow:hidden;
  }
  .auth-bg {
    position:absolute; inset:0;
    background: radial-gradient(ellipse at 20% 50%, rgba(0,212,255,0.06) 0%, transparent 60%),
                radial-gradient(ellipse at 80% 20%, rgba(124,58,237,0.06) 0%, transparent 60%);
  }
  .auth-grid {
    position:absolute; inset:0; opacity:0.03;
    background-image: linear-gradient(#00d4ff 1px, transparent 1px), linear-gradient(90deg,#00d4ff 1px,transparent 1px);
    background-size: 40px 40px;
  }
  .auth-box {
    position:relative; width:420px; max-width:95vw;
    background:var(--card); border:1px solid var(--border);
    border-radius:16px; padding:40px;
    box-shadow: 0 0 60px rgba(0,212,255,0.08), 0 20px 60px rgba(0,0,0,0.5);
  }
  .auth-logo {
    text-align:center; margin-bottom:28px;
  }
  .auth-logo .icon {
    width:60px; height:60px; margin:0 auto 12px;
    background:linear-gradient(135deg,var(--accent),var(--accent2));
    border-radius:16px; display:flex; align-items:center; justify-content:center;
    font-size:28px; box-shadow:0 0 30px rgba(0,212,255,0.3);
  }
  .auth-logo h1 { font-size:22px; font-weight:700; color:var(--text); letter-spacing:1px; }
  .auth-logo p { font-size:12px; color:var(--text3); margin-top:4px; letter-spacing:2px; text-transform:uppercase; }
  .auth-tabs { display:flex; gap:4px; background:var(--bg); border-radius:8px; padding:4px; margin-bottom:24px; }
  .auth-tab {
    flex:1; padding:8px; text-align:center; cursor:pointer;
    border-radius:6px; font-size:13px; font-weight:500; color:var(--text2);
    transition:all .2s;
  }
  .auth-tab.active { background:var(--accent); color:#000; font-weight:600; }
  .form-group { margin-bottom:16px; }
  .form-group label { display:block; font-size:12px; font-weight:500; color:var(--text2); margin-bottom:6px; letter-spacing:.5px; }
  .form-group input {
    width:100%; padding:11px 14px; background:var(--bg);
    border:1px solid var(--border); border-radius:8px; color:var(--text);
    font-size:14px; outline:none; transition:all .2s;
  }
  .form-group input:focus { border-color:var(--accent); box-shadow:0 0 0 3px rgba(0,212,255,0.1); }
  .form-group .input-wrap { position:relative; }
  .form-group .input-icon { position:absolute; right:12px; top:50%; transform:translateY(-50%); color:var(--text3); cursor:pointer; font-size:16px; }
  .strength-bar { margin-top:6px; }
  .strength-bar .bar { height:3px; background:var(--border); border-radius:2px; margin-bottom:4px; overflow:hidden; }
  .strength-bar .fill { height:100%; border-radius:2px; transition:all .3s; width:0; }
  .strength-bar .label { font-size:11px; color:var(--text3); }
  .mfa-section { background:var(--bg); border:1px solid var(--border); border-radius:8px; padding:14px; margin-bottom:16px; }
  .mfa-section label { display:flex; align-items:center; gap:8px; cursor:pointer; font-size:13px; }
  .mfa-section input[type=checkbox] { accent-color:var(--accent); width:15px; height:15px; }
  .btn-primary {
    width:100%; padding:12px; background:linear-gradient(135deg,var(--accent),#0099cc);
    border:none; border-radius:8px; color:#000; font-size:14px; font-weight:700;
    cursor:pointer; letter-spacing:.5px; transition:all .2s;
  }
  .btn-primary:hover { opacity:.9; transform:translateY(-1px); box-shadow:0 4px 20px rgba(0,212,255,0.3); }
  .auth-footer { margin-top:20px; text-align:center; font-size:12px; color:var(--text3); }
  .auth-error { background:rgba(239,68,68,.1); border:1px solid rgba(239,68,68,.3); color:#fca5a5; font-size:13px; padding:10px 14px; border-radius:8px; margin-bottom:14px; display:none; }

  /* ── MAIN APP ── */
  #app { display:none; height:100vh; overflow:hidden; }
  #app.active { display:flex; }

  /* SIDEBAR */
  .sidebar {
    width:260px; min-width:260px; background:var(--sidebar);
    border-right:1px solid var(--border); display:flex; flex-direction:column;
    overflow-y:auto; overflow-x:hidden; transition:width .3s;
  }
  .sidebar.collapsed { width:60px; min-width:60px; }
  .sidebar-header {
    padding:20px 16px; border-bottom:1px solid var(--border);
    display:flex; align-items:center; gap:12px; cursor:pointer;
  }
  .sidebar-logo {
    width:36px; height:36px; min-width:36px;
    background:linear-gradient(135deg,var(--accent),var(--accent2));
    border-radius:10px; display:flex; align-items:center; justify-content:center;
    font-size:18px; box-shadow:0 0 20px rgba(0,212,255,0.2);
  }
  .sidebar-title { font-size:16px; font-weight:700; color:var(--text); letter-spacing:.5px; white-space:nowrap; overflow:hidden; }
  .sidebar-title span { display:block; font-size:10px; color:var(--text3); font-weight:400; letter-spacing:1px; text-transform:uppercase; }
  .nav-section { padding:8px 10px; }
  .nav-label { font-size:10px; color:var(--text3); letter-spacing:1.5px; text-transform:uppercase; padding:8px 6px 4px; white-space:nowrap; overflow:hidden; }
  .nav-item {
    display:flex; align-items:center; gap:10px; padding:9px 10px;
    border-radius:8px; cursor:pointer; color:var(--text2); font-size:13px;
    transition:all .15s; position:relative; margin-bottom:1px; white-space:nowrap;
  }
  .nav-item:hover { background:var(--card); color:var(--text); }
  .nav-item.active { background:rgba(0,212,255,0.1); color:var(--accent); }
  .nav-item.active::before { content:''; position:absolute; left:0; top:50%; transform:translateY(-50%); width:3px; height:60%; background:var(--accent); border-radius:2px; }
  .nav-icon { font-size:16px; min-width:20px; text-align:center; }
  .nav-badge {
    margin-left:auto; background:var(--danger); color:#fff;
    font-size:10px; font-weight:700; padding:1px 6px; border-radius:10px; min-width:18px; text-align:center;
  }
  .nav-badge.green { background:var(--accent3); }
  .nav-badge.yellow { background:var(--warning); color:#000; }
  .nav-arrow { margin-left:auto; font-size:10px; color:var(--text3); transition:transform .2s; }
  .nav-item.open .nav-arrow { transform:rotate(90deg); }
  .nav-sub { display:none; padding-left:20px; }
  .nav-sub.open { display:block; }
  .nav-sub .nav-item { font-size:12px; padding:7px 10px; }
  .sidebar-footer { margin-top:auto; padding:12px; border-top:1px solid var(--border); }
  .user-card { display:flex; align-items:center; gap:10px; padding:10px; border-radius:8px; background:var(--card); cursor:pointer; }
  .user-avatar { width:34px; height:34px; min-width:34px; border-radius:50%; background:linear-gradient(135deg,var(--accent),var(--accent2)); display:flex; align-items:center; justify-content:center; font-weight:700; font-size:14px; color:#000; }
  .user-info { overflow:hidden; }
  .user-name { font-size:13px; font-weight:600; color:var(--text); white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
  .user-role { font-size:11px; color:var(--text3); }
  .status-dot { width:8px; height:8px; min-width:8px; border-radius:50%; background:var(--accent3); margin-left:auto; box-shadow:0 0 6px var(--accent3); }

  /* MAIN */
  .main { flex:1; display:flex; flex-direction:column; overflow:hidden; }
  .topbar {
    height:56px; background:var(--bg2); border-bottom:1px solid var(--border);
    display:flex; align-items:center; padding:0 20px; gap:12px; flex-shrink:0;
  }
  .topbar-title { font-size:16px; font-weight:600; color:var(--text); flex:1; }
  .topbar-search { position:relative; }
  .topbar-search input { background:var(--bg3); border:1px solid var(--border); border-radius:8px; padding:7px 12px 7px 34px; font-size:13px; color:var(--text); outline:none; width:220px; }
  .topbar-search input:focus { border-color:var(--accent); }
  .topbar-search .si { position:absolute; left:10px; top:50%; transform:translateY(-50%); color:var(--text3); }
  .topbar-btns { display:flex; align-items:center; gap:8px; }
  .icon-btn {
    width:36px; height:36px; background:var(--bg3); border:1px solid var(--border);
    border-radius:8px; display:flex; align-items:center; justify-content:center;
    cursor:pointer; color:var(--text2); font-size:16px; transition:all .2s; position:relative;
  }
  .icon-btn:hover { border-color:var(--accent); color:var(--accent); }
  .icon-btn .notif-badge { position:absolute; top:-4px; right:-4px; background:var(--danger); color:#fff; font-size:9px; font-weight:700; width:16px; height:16px; border-radius:50%; display:flex; align-items:center; justify-content:center; }
  .threat-level {
    display:flex; align-items:center; gap:6px; padding:6px 12px;
    background:rgba(239,68,68,.1); border:1px solid rgba(239,68,68,.2); border-radius:8px;
    font-size:12px; font-weight:600; color:#fca5a5; cursor:pointer;
  }
  .threat-dot { width:8px; height:8px; border-radius:50%; background:var(--danger); box-shadow:0 0 8px var(--danger); animation:pulse 1.5s infinite; }
  @keyframes pulse { 0%,100%{opacity:1}50%{opacity:.4} }
  .content { flex:1; overflow-y:auto; padding:20px; }

  /* CARDS */
  .page { display:none; }
  .page.active { display:block; }
  .metrics-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:14px; margin-bottom:20px; }
  .metric-card {
    background:var(--card); border:1px solid var(--border); border-radius:12px; padding:18px;
    position:relative; overflow:hidden; transition:all .2s;
  }
  .metric-card:hover { border-color:var(--accent); transform:translateY(-2px); box-shadow:var(--glow); }
  .metric-card::before { content:''; position:absolute; top:0; right:0; width:80px; height:80px; border-radius:50%; filter:blur(30px); opacity:.15; }
  .metric-card.blue::before { background:var(--accent); }
  .metric-card.purple::before { background:var(--accent2); }
  .metric-card.green::before { background:var(--accent3); }
  .metric-card.red::before { background:var(--danger); }
  .metric-card.yellow::before { background:var(--warning); }
  .metric-icon { font-size:22px; margin-bottom:10px; }
  .metric-value { font-size:28px; font-weight:800; color:var(--text); }
  .metric-label { font-size:12px; color:var(--text3); margin-top:2px; }
  .metric-change { font-size:11px; margin-top:6px; display:flex; align-items:center; gap:4px; }
  .metric-change.up { color:var(--accent3); }
  .metric-change.down { color:var(--danger); }
  .grid-2 { display:grid; grid-template-columns:1fr 1fr; gap:14px; margin-bottom:20px; }
  .grid-3 { display:grid; grid-template-columns:1fr 1fr 1fr; gap:14px; margin-bottom:20px; }
  .panel {
    background:var(--card); border:1px solid var(--border); border-radius:12px; padding:20px;
  }
  .panel-header { display:flex; align-items:center; justify-content:space-between; margin-bottom:16px; }
  .panel-title { font-size:14px; font-weight:600; color:var(--text); display:flex; align-items:center; gap:8px; }
  .panel-action { font-size:12px; color:var(--accent); cursor:pointer; }

  /* CHART FAKE */
  .chart-wrap { position:relative; height:140px; overflow:hidden; }
  .chart-svg { width:100%; height:100%; }

  /* TABLE */
  .data-table { width:100%; border-collapse:collapse; font-size:13px; }
  .data-table th { padding:10px 12px; background:var(--bg); color:var(--text3); font-weight:500; font-size:11px; text-transform:uppercase; letter-spacing:.5px; text-align:left; border-bottom:1px solid var(--border); }
  .data-table td { padding:10px 12px; border-bottom:1px solid rgba(30,40,64,.5); color:var(--text2); }
  .data-table tr:last-child td { border:none; }
  .data-table tr:hover td { background:rgba(255,255,255,.02); }
  .badge { display:inline-flex; align-items:center; gap:4px; padding:3px 8px; border-radius:6px; font-size:11px; font-weight:600; }
  .badge.green { background:rgba(16,185,129,.15); color:#34d399; }
  .badge.red { background:rgba(239,68,68,.15); color:#f87171; }
  .badge.yellow { background:rgba(245,158,11,.15); color:#fbbf24; }
  .badge.blue { background:rgba(0,212,255,.15); color:var(--accent); }
  .badge.purple { background:rgba(124,58,237,.15); color:#a78bfa; }
  .badge.gray { background:rgba(100,116,139,.15); color:#94a3b8; }

  /* ACTIVITY FEED */
  .activity-item { display:flex; gap:12px; padding:10px 0; border-bottom:1px solid rgba(30,40,64,.5); }
  .activity-item:last-child { border:none; }
  .activity-icon { width:32px; height:32px; min-width:32px; border-radius:8px; display:flex; align-items:center; justify-content:center; font-size:14px; }
  .activity-icon.success { background:rgba(16,185,129,.15); }
  .activity-icon.danger { background:rgba(239,68,68,.15); }
  .activity-icon.warning { background:rgba(245,158,11,.15); }
  .activity-icon.info { background:rgba(0,212,255,.15); }
  .activity-body { flex:1; }
  .activity-text { font-size:13px; color:var(--text); }
  .activity-meta { font-size:11px; color:var(--text3); margin-top:2px; }
  .activity-time { font-size:11px; color:var(--text3); white-space:nowrap; }

  /* REALTIME */
  .realtime-bar {
    background:var(--bg); border:1px solid var(--border); border-radius:8px; padding:10px 14px;
    display:flex; align-items:center; gap:10px; margin-bottom:14px;
  }
  .rt-dot { width:8px; height:8px; border-radius:50%; background:var(--accent3); animation:pulse 1s infinite; box-shadow:0 0 8px var(--accent3); }
  .rt-label { font-size:12px; color:var(--text3); }
  .rt-value { font-size:12px; color:var(--accent); font-weight:600; margin-left:auto; }

  /* PROGRESS */
  .prog-item { margin-bottom:12px; }
  .prog-label { display:flex; justify-content:space-between; font-size:12px; color:var(--text2); margin-bottom:5px; }
  .prog-bar { height:6px; background:var(--bg); border-radius:3px; overflow:hidden; }
  .prog-fill { height:100%; border-radius:3px; transition:width 1s ease; }

  /* MAP */
  .world-map { background:var(--bg); border-radius:8px; height:200px; position:relative; overflow:hidden; display:flex; align-items:center; justify-content:center; }
  .map-grid { position:absolute; inset:0; opacity:.05; background-image:linear-gradient(var(--border) 1px,transparent 1px),linear-gradient(90deg,var(--border) 1px,transparent 1px); background-size:20px 20px; }
  .map-dot { position:absolute; width:6px; height:6px; border-radius:50%; animation:pulse 2s infinite; }
  .map-dot.green { background:var(--accent3); box-shadow:0 0 10px var(--accent3); }
  .map-dot.red { background:var(--danger); box-shadow:0 0 10px var(--danger); }
  .map-dot.blue { background:var(--accent); box-shadow:0 0 10px var(--accent); }

  /* TOGGLE */
  .toggle { position:relative; width:40px; height:22px; }
  .toggle input { opacity:0; width:0; height:0; }
  .toggle-slider { position:absolute; inset:0; background:var(--border); border-radius:11px; cursor:pointer; transition:.3s; }
  .toggle-slider::before { content:''; position:absolute; width:16px; height:16px; left:3px; top:3px; background:var(--text3); border-radius:50%; transition:.3s; }
  .toggle input:checked + .toggle-slider { background:var(--accent); }
  .toggle input:checked + .toggle-slider::before { transform:translateX(18px); background:#000; }

  /* VPN */
  .vpn-status {
    background:var(--card); border:1px solid var(--border); border-radius:12px; padding:24px;
    text-align:center; margin-bottom:20px;
  }
  .vpn-globe { width:80px; height:80px; margin:0 auto 16px; border-radius:50%; background:linear-gradient(135deg,var(--accent),var(--accent2)); display:flex; align-items:center; justify-content:center; font-size:36px; box-shadow:0 0 40px rgba(0,212,255,0.3); animation:vpn-pulse 3s infinite; }
  @keyframes vpn-pulse { 0%,100%{box-shadow:0 0 40px rgba(0,212,255,.3)} 50%{box-shadow:0 0 60px rgba(0,212,255,.5)} }
  .vpn-globe.off { background:linear-gradient(135deg,#374151,#1f2937); box-shadow:none; animation:none; }
  .vpn-name { font-size:20px; font-weight:700; }
  .vpn-ip { font-size:13px; color:var(--text3); margin:4px 0 16px; }
  .btn-vpn { padding:12px 32px; border-radius:10px; border:none; font-size:14px; font-weight:700; cursor:pointer; transition:all .2s; }
  .btn-vpn.connect { background:linear-gradient(135deg,var(--accent3),#059669); color:#fff; }
  .btn-vpn.disconnect { background:linear-gradient(135deg,var(--danger),#dc2626); color:#fff; }

  /* LOGS */
  .log-line { font-family:monospace; font-size:12px; padding:4px 0; border-bottom:1px solid rgba(30,40,64,.3); display:flex; gap:10px; }
  .log-time { color:var(--text3); min-width:90px; }
  .log-level { min-width:60px; font-weight:700; }
  .log-level.info { color:var(--accent); }
  .log-level.warn { color:var(--warning); }
  .log-level.error { color:var(--danger); }
  .log-level.success { color:var(--accent3); }
  .log-msg { color:var(--text2); }
  .log-scroll { max-height:320px; overflow-y:auto; }

  /* SETTINGS */
  .setting-row { display:flex; align-items:center; justify-content:space-between; padding:14px 0; border-bottom:1px solid rgba(30,40,64,.5); }
  .setting-row:last-child { border:none; }
  .setting-info h4 { font-size:14px; color:var(--text); }
  .setting-info p { font-size:12px; color:var(--text3); margin-top:2px; }

  /* TAG INPUT */
  .tag-list { display:flex; flex-wrap:wrap; gap:6px; }
  .tag { display:inline-flex; align-items:center; gap:6px; padding:4px 10px; background:rgba(0,212,255,.1); border:1px solid rgba(0,212,255,.2); border-radius:20px; font-size:12px; color:var(--accent); }
  .tag.red { background:rgba(239,68,68,.1); border-color:rgba(239,68,68,.2); color:#f87171; }
  .tag-remove { cursor:pointer; color:inherit; opacity:.6; }

  /* NOTIFICATIONS PANEL */
  .notif-panel {
    position:fixed; right:0; top:56px; bottom:0; width:340px;
    background:var(--bg2); border-left:1px solid var(--border);
    z-index:100; transform:translateX(100%); transition:transform .3s;
    display:flex; flex-direction:column;
  }
  .notif-panel.open { transform:none; }
  .notif-header { padding:16px; border-bottom:1px solid var(--border); display:flex; align-items:center; justify-content:space-between; }
  .notif-header h3 { font-size:14px; font-weight:600; }
  .notif-close { cursor:pointer; color:var(--text3); font-size:18px; }
  .notif-list { flex:1; overflow-y:auto; padding:8px; }
  .notif-item { padding:12px; border-radius:8px; margin-bottom:4px; cursor:pointer; transition:background .15s; }
  .notif-item:hover { background:var(--card); }
  .notif-item h4 { font-size:13px; color:var(--text); }
  .notif-item p { font-size:12px; color:var(--text3); margin-top:2px; }
  .notif-item .nt { font-size:11px; color:var(--text3); margin-top:4px; }

  /* MFA MODAL */
  .modal-overlay { position:fixed; inset:0; background:rgba(0,0,0,.7); z-index:1000; display:none; align-items:center; justify-content:center; }
  .modal-overlay.open { display:flex; }
  .modal { background:var(--card); border:1px solid var(--border); border-radius:16px; padding:32px; width:380px; max-width:95vw; text-align:center; }
  .modal h3 { font-size:18px; font-weight:700; margin-bottom:8px; }
  .modal p { font-size:13px; color:var(--text3); margin-bottom:24px; }
  .otp-inputs { display:flex; gap:8px; justify-content:center; margin-bottom:24px; }
  .otp-inputs input { width:46px; height:54px; text-align:center; font-size:22px; font-weight:700; background:var(--bg); border:2px solid var(--border); border-radius:10px; color:var(--text); outline:none; }
  .otp-inputs input:focus { border-color:var(--accent); }

  /* IP LIST */
  .ip-item { display:flex; align-items:center; gap:10px; padding:10px 0; border-bottom:1px solid rgba(30,40,64,.4); }
  .ip-item:last-child { border:none; }
  .ip-addr { font-family:monospace; font-size:13px; flex:1; }
  .ip-flag { font-size:18px; }

  /* PAGE-SPECIFIC */
  .section-title { font-size:18px; font-weight:700; color:var(--text); margin-bottom:4px; }
  .section-sub { font-size:13px; color:var(--text3); margin-bottom:20px; }


  /* ── HACKER MODULE ── */
  :root { --hack: #ff0040; --hack2: #ff6b00; --matrix: #00ff41; }

  /* Matrix rain */
  #matrix-canvas { position:absolute; inset:0; opacity:.18; pointer-events:none; }

  .hack-panel {
    background:linear-gradient(135deg,#0a0a0a,#0d0010);
    border:1px solid rgba(255,0,64,.3); border-radius:12px; padding:20px;
    position:relative; overflow:hidden;
  }
  .hack-panel::before { content:''; position:absolute; inset:0; background:radial-gradient(ellipse at 50% 0%,rgba(255,0,64,.08),transparent 70%); pointer-events:none; }
  .hack-glow { box-shadow:0 0 30px rgba(255,0,64,.2); }

  /* Target card */
  .target-card {
    background:#0a0508; border:1px solid rgba(255,0,64,.25); border-radius:10px;
    padding:14px; display:flex; align-items:center; gap:12px; margin-bottom:8px;
    transition:all .2s; cursor:pointer; position:relative; overflow:hidden;
  }
  .target-card:hover { border-color:var(--hack); background:#0f060a; box-shadow:0 0 20px rgba(255,0,64,.15); }
  .target-card.selected { border-color:var(--hack); background:#12060a; }
  .target-avatar {
    width:40px; height:40px; min-width:40px; border-radius:8px;
    background:linear-gradient(135deg,#1a0010,#2a0020);
    border:1px solid rgba(255,0,64,.3); display:flex; align-items:center; justify-content:center; font-size:18px;
  }
  .target-info { flex:1; }
  .target-name { font-size:13px; font-weight:600; color:#ff6b6b; }
  .target-ip { font-size:11px; color:#666; font-family:monospace; }
  .target-os { font-size:11px; color:#555; margin-top:1px; }
  .target-status { display:flex; flex-direction:column; align-items:flex-end; gap:4px; }
  .hack-dot { width:8px; height:8px; border-radius:50%; }
  .hack-dot.online { background:#ff0040; box-shadow:0 0 8px #ff0040; animation:pulse 1s infinite; }
  .hack-dot.idle { background:#ff6b00; box-shadow:0 0 8px #ff6b00; animation:pulse 2s infinite; }
  .hack-dot.offline { background:#333; }

  /* Screen viewer */
  .screen-viewer {
    background:#000; border:2px solid rgba(255,0,64,.4); border-radius:10px;
    aspect-ratio:16/9; position:relative; overflow:hidden; cursor:pointer;
  }
  .screen-viewer .sv-top {
    position:absolute; top:0; left:0; right:0; height:24px;
    background:rgba(255,0,64,.15); display:flex; align-items:center; padding:0 10px; gap:6px; z-index:2;
  }
  .sv-dot2 { width:8px; height:8px; border-radius:50%; }
  .screen-content { position:absolute; inset:0; padding:30px 12px 12px; font-family:monospace; font-size:11px; color:#0f0; overflow:hidden; }
  .screen-overlay { position:absolute; inset:0; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:8px; background:rgba(0,0,0,.6); z-index:3; }
  .screen-overlay .connect-btn { background:var(--hack); color:#fff; border:none; padding:8px 20px; border-radius:6px; cursor:pointer; font-size:12px; font-weight:700; }

  /* Bot grid */
  .bot-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(120px,1fr)); gap:8px; }
  .bot-card {
    background:#0a0305; border:1px solid rgba(255,0,64,.2); border-radius:8px;
    padding:10px; text-align:center; cursor:pointer; transition:all .2s;
  }
  .bot-card:hover { border-color:var(--hack); box-shadow:0 0 12px rgba(255,0,64,.2); }
  .bot-card.active { border-color:#ff6b00; background:#0f0600; }
  .bot-flag { font-size:20px; margin-bottom:4px; }
  .bot-ip { font-size:10px; color:#666; font-family:monospace; }
  .bot-label { font-size:11px; color:#ff6b6b; font-weight:600; margin-top:2px; }

  /* Hack actions */
  .hack-action {
    background:#0a0508; border:1px solid rgba(255,0,64,.2); border-radius:8px;
    padding:12px 14px; display:flex; align-items:center; gap:10px;
    cursor:pointer; transition:all .2s; margin-bottom:8px;
  }
  .hack-action:hover { border-color:var(--hack); background:#0f060a; transform:translateX(4px); }
  .hack-action .ha-icon { font-size:18px; min-width:24px; }
  .hack-action .ha-info h4 { font-size:13px; color:#ff6b6b; }
  .hack-action .ha-info p { font-size:11px; color:#555; margin-top:2px; }
  .hack-action .ha-badge { margin-left:auto; padding:2px 8px; border-radius:4px; font-size:10px; font-weight:700; }
  .ha-badge.live { background:rgba(255,0,64,.2); color:#ff0040; border:1px solid rgba(255,0,64,.3); animation:pulse 1s infinite; }
  .ha-badge.ready { background:rgba(255,107,0,.2); color:#ff6b00; border:1px solid rgba(255,107,0,.3); }
  .ha-badge.idle2 { background:rgba(100,100,100,.2); color:#666; border:1px solid rgba(100,100,100,.2); }

  /* Terminal hacker */
  .hack-terminal {
    background:#050505; border:1px solid rgba(0,255,65,.2); border-radius:8px;
    padding:14px; font-family:monospace; font-size:12px;
  }
  .ht-line { color:#00ff41; line-height:1.9; }
  .ht-line.red { color:#ff0040; }
  .ht-line.yellow { color:#ffb700; }
  .ht-line.gray { color:#444; }
  .ht-cursor { display:inline-block; width:8px; height:14px; background:#00ff41; vertical-align:middle; animation:blink .8s infinite; }
  @keyframes blink { 0%,100%{opacity:1}50%{opacity:0} }

  /* Live logins ticker */
  .login-ticker {
    background:#0a0e1a; border:1px solid var(--border); border-radius:8px;
    padding:10px 14px; font-size:12px; overflow:hidden; height:38px; position:relative;
  }
  .ticker-inner { position:absolute; white-space:nowrap; animation:ticker 0s linear; }

  /* Fake progress bar */
  .fake-prog { height:4px; background:rgba(255,0,64,.1); border-radius:2px; overflow:hidden; margin-top:6px; }
  .fake-prog-fill { height:100%; background:var(--hack); border-radius:2px; transition:width .5s; }

  /* Infected screen fake OS */
  .fake-screen {
    background:#1a1a2e; width:100%; height:100%; padding:24px 10px 10px;
    display:flex; flex-direction:column; gap:6px; font-family:monospace; font-size:10px; color:#ccc;
  }
  .fake-taskbar {
    position:absolute; bottom:0; left:0; right:0; height:22px;
    background:#0d0d1a; border-top:1px solid #333;
    display:flex; align-items:center; padding:0 8px; gap:6px;
  }
  .ftb-btn { background:#1e3a5f; border-radius:3px; padding:2px 8px; font-size:9px; color:#7fc; cursor:pointer; }

  /* Notification badge big */
  .notif-badge-big { background:var(--danger); color:#fff; font-size:9px; font-weight:700; padding:1px 5px; border-radius:10px; }

  /* Stats hacker */
  .hstat { text-align:center; }
  .hstat .hval { font-size:26px; font-weight:800; color:var(--hack); font-family:monospace; }
  .hstat .hlabel { font-size:10px; color:#555; text-transform:uppercase; letter-spacing:1px; }

  /* Scan progress */
  .scan-item { display:flex; align-items:center; gap:10px; padding:7px 0; border-bottom:1px solid rgba(255,0,64,.08); font-size:12px; }
  .scan-item:last-child { border:none; }
  .scan-ip { font-family:monospace; color:#ff6b6b; flex:1; }
  .scan-port { color:#666; min-width:60px; }
  .scan-result { min-width:70px; text-align:right; }

  /* Admin list */
  .admin-row { display:flex; align-items:center; gap:10px; padding:8px 0; border-bottom:1px solid rgba(30,40,64,.4); font-size:12px; }
  .admin-row:last-child { border:none; }
  .admin-ava { width:28px; height:28px; border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:12px; font-weight:700; color:#000; flex-shrink:0; }

  /* SCROLLBAR */
  ::-webkit-scrollbar { width:6px; height:6px; }
  ::-webkit-scrollbar-track { background:var(--bg); }
  ::-webkit-scrollbar-thumb { background:var(--border); border-radius:3px; }
  ::-webkit-scrollbar-thumb:hover { background:var(--text3); }

  /* RESPONSIVE */
  @media(max-width:768px) {
    .sidebar { position:fixed; z-index:200; height:100vh; transform:translateX(-100%); transition:transform .3s; }
    .sidebar.mobile-open { transform:none; }
    .grid-2,.grid-3 { grid-template-columns:1fr; }
    .metrics-grid { grid-template-columns:1fr 1fr; }
  }

  /* FIREWALL */
  .rule-item { display:flex; align-items:center; gap:10px; padding:10px 12px; background:var(--bg); border-radius:8px; margin-bottom:8px; font-size:13px; }
  .rule-action { padding:2px 8px; border-radius:4px; font-size:11px; font-weight:700; }
  .rule-action.allow { background:rgba(16,185,129,.2); color:#34d399; }
  .rule-action.deny { background:rgba(239,68,68,.2); color:#f87171; }

  /* GAUGE */
  .gauge-wrap { display:flex; flex-direction:column; align-items:center; }
  .gauge-arc { position:relative; width:90px; height:50px; overflow:hidden; margin-bottom:4px; }
  .gauge-arc svg { position:absolute; top:0; left:0; }

  /* FORM INLINE */
  .inline-form { display:flex; gap:8px; margin-bottom:14px; }
  .inline-form input { flex:1; padding:9px 12px; background:var(--bg); border:1px solid var(--border); border-radius:8px; color:var(--text); font-size:13px; outline:none; }
  .inline-form input:focus { border-color:var(--accent); }
  .btn-sm { padding:9px 14px; background:var(--accent); border:none; border-radius:8px; color:#000; font-size:12px; font-weight:700; cursor:pointer; white-space:nowrap; }
  .btn-sm.red { background:var(--danger); color:#fff; }
  .btn-sm.outline { background:transparent; border:1px solid var(--border); color:var(--text2); }

  /* CPU/RAM BARS */
  .resource-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(160px,1fr)); gap:12px; }
  .resource-card { background:var(--bg); border-radius:10px; padding:14px; text-align:center; }
  .resource-val { font-size:26px; font-weight:800; }
  .resource-label { font-size:11px; color:var(--text3); margin-top:2px; margin-bottom:10px; }

  .loading-overlay { position:fixed; inset:0; background:var(--bg); z-index:9998; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:16px; }
  .loading-spinner { width:48px; height:48px; border:3px solid var(--border); border-top-color:var(--accent); border-radius:50%; animation:spin .8s linear infinite; }
  @keyframes spin { to { transform:rotate(360deg); } }
  .loading-text { font-size:13px; color:var(--text3); letter-spacing:1px; }
</style>
</head>
<body>

<!-- LOADING -->
<div class="loading-overlay" id="loading">
  <div class="loading-spinner"></div>
  <div class="loading-text">INICIANDO SECUREOS...</div>
</div>

<!-- AUTH SCREEN -->
<div id="auth-screen">
  <div class="auth-bg"></div>
  <div class="auth-grid"></div>
  <div class="auth-box">
    <div class="auth-logo">
      <div class="icon">🛡️</div>
      <h1>SecureOS</h1>
      <p>Sistema de Segurança Avançado</p>
    </div>
    <div class="auth-tabs">
      <div class="auth-tab active" onclick="switchAuthTab('login')">Entrar</div>
      <div class="auth-tab" onclick="switchAuthTab('register')">Registrar</div>
    </div>
    <div id="auth-error" class="auth-error"></div>

    <!-- LOGIN -->
    <div id="login-form">
      <div class="form-group">
        <label>USUÁRIO / EMAIL</label>
        <div class="input-wrap">
          <input type="text" id="login-user" placeholder="admin@secureos.com" value="admin@secureos.com">
        </div>
      </div>
      <div class="form-group">
        <label>SENHA</label>
        <div class="input-wrap">
          <input type="password" id="login-pass" placeholder="••••••••" value="Admin@123">
          <span class="input-icon" onclick="togglePass('login-pass',this)">👁️</span>
        </div>
      </div>
      <button class="btn-primary" onclick="doLogin()">🔐 ENTRAR COM SEGURANÇA</button>
      <div class="auth-footer">Esqueceu a senha? <span style="color:var(--accent);cursor:pointer">Redefinir</span></div>
    </div>

    <!-- REGISTER -->
    <div id="register-form" style="display:none">
      <div class="form-group">
        <label>NOME COMPLETO</label>
        <input type="text" id="reg-name" placeholder="João Silva">
      </div>
      <div class="form-group">
        <label>EMAIL</label>
        <input type="email" id="reg-email" placeholder="joao@empresa.com">
      </div>
      <div class="form-group">
        <label>SENHA</label>
        <div class="input-wrap">
          <input type="password" id="reg-pass" placeholder="Mínimo 8 caracteres" oninput="checkStrength(this)">
          <span class="input-icon" onclick="togglePass('reg-pass',this)">👁️</span>
        </div>
        <div class="strength-bar">
          <div class="bar"><div class="fill" id="strength-fill"></div></div>
          <div class="label" id="strength-label">Digite uma senha</div>
        </div>
      </div>
      <div class="form-group">
        <label>CONFIRMAR SENHA</label>
        <input type="password" id="reg-pass2" placeholder="Repita a senha">
      </div>
      <div class="mfa-section">
        <label><input type="checkbox" id="reg-mfa" checked> Ativar autenticação multifator (MFA) 🔐</label>
      </div>
      <button class="btn-primary" onclick="doRegister()">✅ CRIAR CONTA</button>
    </div>
  </div>
</div>

<!-- MFA MODAL -->
<div class="modal-overlay" id="mfa-modal">
  <div class="modal">
    <div style="font-size:48px;margin-bottom:12px">📱</div>
    <h3>Autenticação de 2 Fatores</h3>
    <p>Insira o código de 6 dígitos enviado para seu dispositivo</p>
    <div class="otp-inputs" id="otp-inputs">
      <input maxlength="1" oninput="otpNext(this,0)">
      <input maxlength="1" oninput="otpNext(this,1)">
      <input maxlength="1" oninput="otpNext(this,2)">
      <input maxlength="1" oninput="otpNext(this,3)">
      <input maxlength="1" oninput="otpNext(this,4)">
      <input maxlength="1" oninput="otpNext(this,5)">
    </div>
    <button class="btn-primary" onclick="verifyMFA()">✅ VERIFICAR</button>
    <p style="margin-top:14px;font-size:12px">Código demo: <strong style="color:var(--accent)">123456</strong></p>
  </div>
</div>

<!-- NOTIFICATIONS PANEL -->
<div class="notif-panel" id="notif-panel">
  <div class="notif-header">
    <h3>🔔 Notificações</h3>
    <span class="notif-close" onclick="toggleNotif()">✕</span>
  </div>
  <div class="notif-list">
    <div class="notif-item" style="border-left:3px solid var(--danger);background:rgba(239,68,68,.05)">
      <h4>🚨 Ataque de força bruta detectado</h4>
      <p>IP 203.45.12.8 tentou 47 logins em 2 min</p>
      <div class="nt">Há 2 minutos</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--danger);background:rgba(239,68,68,.07)">
      <h4>🆘 Admin carlos.mendes pede ajuda urgente</h4>
      <p>Acesso bloqueado — perdeu autenticador MFA</p>
      <div class="nt">Há 3 minutos</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--danger);background:rgba(239,68,68,.05)">
      <h4>🆘 fernanda.ops não consegue logar</h4>
      <p>Diz que senha foi alterada sem aviso</p>
      <div class="nt">Há 7 minutos</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--warning);background:rgba(245,158,11,.05)">
      <h4>⚠️ CPU em 87%</h4>
      <p>Servidor principal com carga elevada</p>
      <div class="nt">Há 5 minutos</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--warning);background:rgba(245,158,11,.05)">
      <h4>⚠️ lucas.ti@empresa.com reporta comportamento estranho</h4>
      <p>Mouse se movendo sozinho no computador</p>
      <div class="nt">Há 9 minutos</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--danger);background:rgba(239,68,68,.05)">
      <h4>🆘 juliana.adm pede suporte imediato</h4>
      <p>Arquivos sendo deletados automaticamente</p>
      <div class="nt">Há 12 minutos</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--warning)">
      <h4>⚠️ 14 novos logins simultâneos</h4>
      <p>Pico incomum de autenticações detectado</p>
      <div class="nt">Há 15 minutos</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--danger);background:rgba(239,68,68,.05)">
      <h4>🆘 roberto.sec: meu PC está travado</h4>
      <p>Não consegue fechar programas nem desligar</p>
      <div class="nt">Há 18 minutos</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--accent3)">
      <h4>✅ Backup concluído</h4>
      <p>Backup automático realizado com sucesso</p>
      <div class="nt">Há 1 hora</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--accent)">
      <h4>🔐 Certificado SSL renovado</h4>
      <p>secureos.com válido por mais 365 dias</p>
      <div class="nt">Há 2 horas</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--danger)">
      <h4>🆘 ana.paula.rh: não reconheço minha senha</h4>
      <p>Afirma que nunca a alterou</p>
      <div class="nt">Há 2 horas</div>
    </div>
    <div class="notif-item" style="border-left:3px solid var(--accent2)">
      <h4>👤 23 novos usuários cadastrados hoje</h4>
      <p>Volume acima do normal para esta hora</p>
      <div class="nt">Há 3 horas</div>
    </div>
  </div>
</div>

<!-- MAIN APP -->
<div id="app">
  <div class="sidebar" id="sidebar">
    <div class="sidebar-header" onclick="toggleSidebar()">
      <div class="sidebar-logo">🛡️</div>
      <div class="sidebar-title">SecureOS <span>v3.0 Enterprise</span></div>
    </div>

    <div class="nav-section">
      <div class="nav-label">Principal</div>
      <div class="nav-item active" onclick="showPage('dashboard',this)">
        <span class="nav-icon">🏠</span><span class="nav-text">Dashboard</span>
        <span class="nav-badge red">3</span>
      </div>
    </div>

    <div class="nav-section">
      <div class="nav-label">Identidade</div>
      <div class="nav-item" onclick="toggleSub('sub-users',this)">
        <span class="nav-icon">👤</span><span class="nav-text">Usuários & Acesso</span>
        <span class="nav-arrow">›</span>
      </div>
      <div class="nav-sub" id="sub-users">
        <div class="nav-item" onclick="showPage('users',this)"><span class="nav-icon">👥</span><span class="nav-text">Cadastro</span></div>
        <div class="nav-item" onclick="showPage('roles',this)"><span class="nav-icon">🎭</span><span class="nav-text">Perfis & RBAC</span></div>
        <div class="nav-item" onclick="showPage('sessions',this)"><span class="nav-icon">🔗</span><span class="nav-text">Sessões Ativas</span></div>
        <div class="nav-item" onclick="showPage('access-log',this)"><span class="nav-icon">📋</span><span class="nav-text">Histórico de Acesso</span></div>
      </div>
    </div>

    <div class="nav-section">
      <div class="nav-label">Proteção</div>
      <div class="nav-item" onclick="toggleSub('sub-sec',this)">
        <span class="nav-icon">🔐</span><span class="nav-text">Segurança</span>
        <span class="nav-badge yellow">2</span>
        <span class="nav-arrow">›</span>
      </div>
      <div class="nav-sub" id="sub-sec">
        <div class="nav-item" onclick="showPage('mfa-config',this)"><span class="nav-icon">📱</span><span class="nav-text">MFA</span></div>
        <div class="nav-item" onclick="showPage('encryption',this)"><span class="nav-icon">🔑</span><span class="nav-text">Criptografia</span></div>
        <div class="nav-item" onclick="showPage('passwords',this)"><span class="nav-icon">🗝️</span><span class="nav-text">Senhas</span></div>
        <div class="nav-item" onclick="showPage('threats',this)"><span class="nav-icon">🎯</span><span class="nav-text">Detecção de Ameaças</span><span class="nav-badge red">1</span></div>
        <div class="nav-item" onclick="showPage('iplist',this)"><span class="nav-icon">🚫</span><span class="nav-text">IPs Bloqueados</span></div>
        <div class="nav-item" onclick="showPage('firewall',this)"><span class="nav-icon">🔥</span><span class="nav-text">Firewall</span></div>
      </div>
    </div>

    <div class="nav-section">
      <div class="nav-label">Rede</div>
      <div class="nav-item" onclick="showPage('vpn',this)">
        <span class="nav-icon">🌐</span><span class="nav-text">VPN</span>
        <span class="nav-badge green">ON</span>
      </div>
      <div class="nav-item" onclick="showPage('network',this)">
        <span class="nav-icon">📡</span><span class="nav-text">Rede & Conectividade</span>
      </div>
    </div>

    <div class="nav-section">
      <div class="nav-label">Monitoramento</div>
      <div class="nav-item" onclick="showPage('monitoring',this)">
        <span class="nav-icon">📊</span><span class="nav-text">Monitoramento</span>
      </div>
      <div class="nav-item" onclick="showPage('logs',this)">
        <span class="nav-icon">📜</span><span class="nav-text">Logs em Tempo Real</span>
      </div>
      <div class="nav-item" onclick="showPage('audit',this)">
        <span class="nav-icon">🔍</span><span class="nav-text">Auditoria</span>
      </div>
    </div>

    <div class="nav-section">
      <div class="nav-label">Sistema</div>
      <div class="nav-item" onclick="showPage('data',this)">
        <span class="nav-icon">🗄️</span><span class="nav-text">Dados & Backup</span>
      </div>
      <div class="nav-item" onclick="showPage('automation',this)">
        <span class="nav-icon">🤖</span><span class="nav-text">Automação</span>
      </div>
      <div class="nav-item" onclick="showPage('notifications-cfg',this)">
        <span class="nav-icon">📢</span><span class="nav-text">Notificações</span>
      </div>
      <div class="nav-item" onclick="showPage('reports',this)">
        <span class="nav-icon">📈</span><span class="nav-text">Relatórios</span>
      </div>
      <div class="nav-item" onclick="showPage('tools',this)">
        <span class="nav-icon">🛠️</span><span class="nav-text">Ferramentas Avançadas</span>
      </div>
      <div class="nav-item" onclick="showPage('compliance',this)">
        <span class="nav-icon">📜</span><span class="nav-text">Conformidade</span>
      </div>
      <div class="nav-item" onclick="showPage('settings',this)">
        <span class="nav-icon">⚙️</span><span class="nav-text">Configurações</span>
      </div>
      <div class="nav-item" onclick="showPage('support',this)">
        <span class="nav-icon">🧑‍💻</span><span class="nav-text">Suporte</span>
      </div>
    </div>


    <div class="nav-section">
      <div class="nav-label" style="color:#ff0040;letter-spacing:2px">⚠ HACKER TOOLS</div>
      <div class="nav-item" onclick="toggleSub('sub-hack',this)" style="color:#ff6b6b">
        <span class="nav-icon">💀</span><span class="nav-text">Painel do Hacker</span>
        <span class="nav-badge red" id="hack-badge" style="background:#ff0040;animation:pulse 1s infinite">47</span>
        <span class="nav-arrow">›</span>
      </div>
      <div class="nav-sub open" id="sub-hack">
        <div class="nav-item" onclick="showPage('hack-targets',this)"><span class="nav-icon">🎯</span><span class="nav-text">Alvos Infectados</span><span class="nav-badge red">23</span></div>
        <div class="nav-item" onclick="showPage('hack-screen',this)"><span class="nav-icon">🖥️</span><span class="nav-text">Visualizar Tela</span></div>
        <div class="nav-item" onclick="showPage('hack-botnet',this)"><span class="nav-icon">🤖</span><span class="nav-text">Rede de Bots</span><span class="nav-badge red">312</span></div>
        <div class="nav-item" onclick="showPage('hack-tools',this)"><span class="nav-icon">🔧</span><span class="nav-text">Ferramentas</span></div>
        <div class="nav-item" onclick="showPage('hack-terminal',this)"><span class="nav-icon">💻</span><span class="nav-text">Terminal Remoto</span></div>
        <div class="nav-item" onclick="showPage('hack-scan',this)"><span class="nav-icon">📡</span><span class="nav-text">Scanner de Rede</span></div>
      </div>
    </div>
    <div class="sidebar-footer">
      <div class="user-card">
        <div class="user-avatar" id="user-avatar">A</div>
        <div class="user-info">
          <div class="user-name" id="user-name-display">Admin</div>
          <div class="user-role">Super Administrador</div>
        </div>
        <div class="status-dot"></div>
      </div>
    </div>
  </div>

  <div class="main">
    <!-- TOPBAR -->
    <div class="topbar">
      <span style="font-size:20px;cursor:pointer;color:var(--text3)" onclick="toggleSidebar()">☰</span>
      <div class="topbar-title" id="page-title">Dashboard</div>
      <div class="topbar-search">
        <span class="si">🔍</span>
        <input placeholder="Pesquisar...">
      </div>
      <div class="topbar-btns">
        <div class="threat-level" title="Nível de Ameaça: ALTO">
          <div class="threat-dot"></div>
          <span>ALTO</span>
        </div>
        <div class="icon-btn" onclick="toggleNotif()">🔔<span class="notif-badge">12</span></div>
        <div class="icon-btn" title="Tema">🌙</div>
        <div class="icon-btn" onclick="doLogout()" title="Sair">🚪</div>
      </div>
    </div>

    <div class="content">

      <!-- ── DASHBOARD ── -->
      <div class="page active" id="page-dashboard">
        <div class="realtime-bar">
          <div class="rt-dot"></div>
          <span class="rt-label">Monitoramento em tempo real ativo</span>
          <span style="color:var(--text3);font-size:12px" id="rt-time"></span>
          <span class="rt-value" id="rt-events">0 eventos/min</span>
        </div>

        <div class="metrics-grid">
          <div class="metric-card blue">
            <div class="metric-icon">🛡️</div>
            <div class="metric-value" id="m-threats">1.847</div>
            <div class="metric-label">Ameaças Bloqueadas Hoje</div>
            <div class="metric-change up">↑ 12% em relação a ontem</div>
          </div>
          <div class="metric-card green">
            <div class="metric-icon">👤</div>
            <div class="metric-value" id="m-users">4,712</div>
            <div class="metric-label">Usuários Ativos</div>
            <div class="metric-change up">↑ 143 novos hoje</div>
          </div>
          <div class="metric-card purple">
            <div class="metric-icon">🔐</div>
            <div class="metric-value">99.98%</div>
            <div class="metric-label">Uptime do Sistema</div>
            <div class="metric-change up">↑ Estável</div>
          </div>
          <div class="metric-card red">
            <div class="metric-icon">🚨</div>
            <div class="metric-value" id="m-alerts">14</div>
            <div class="metric-label">Alertas Críticos</div>
            <div class="metric-change down">↑ Requer atenção</div>
          </div>
          <div class="metric-card yellow">
            <div class="metric-icon">🌐</div>
            <div class="metric-value">VPN ON</div>
            <div class="metric-label">Status da VPN</div>
            <div class="metric-change up">↑ 3 servidores ativos</div>
          </div>
          <div class="metric-card blue">
            <div class="metric-icon">📡</div>
            <div class="metric-value" id="m-bandwidth">1.2 GB</div>
            <div class="metric-label">Tráfego Hoje</div>
            <div class="metric-change up">↑ Normal</div>
          </div>
        </div>


          <div class="panel" style="margin-bottom:14px">
            <div class="panel-header">
              <div class="panel-title">🔴 Logins ao Vivo <span class="badge red" style="font-size:9px;margin-left:6px;animation:pulse 1s infinite">● LIVE</span></div>
              <span class="panel-action">Ver histórico</span>
            </div>
            <div id="login-live-feed">
              <div class="activity-item"><div class="activity-icon success">🟢</div><div class="activity-body"><div class="activity-text">carlos.mendes@empresa.com fez login</div><div class="activity-meta">192.168.4.12</div></div><div class="activity-time">Agora</div></div>
              <div class="activity-item"><div class="activity-icon success">🟢</div><div class="activity-body"><div class="activity-text">fernanda.ops@empresa.com fez login</div><div class="activity-meta">10.0.1.44</div></div><div class="activity-time">30s</div></div>
              <div class="activity-item"><div class="activity-icon success">🟢</div><div class="activity-body"><div class="activity-text">juliana.adm@empresa.com fez login</div><div class="activity-meta">192.168.1.201</div></div><div class="activity-time">1min</div></div>
              <div class="activity-item"><div class="activity-icon danger">🔴</div><div class="activity-body"><div class="activity-text">unknown@evil.com — BLOQUEADO</div><div class="activity-meta">203.45.12.8</div></div><div class="activity-time">1min</div></div>
              <div class="activity-item"><div class="activity-icon success">🟢</div><div class="activity-body"><div class="activity-text">maria.silva@empresa.com fez login</div><div class="activity-meta">177.23.45.90</div></div><div class="activity-time">2min</div></div>
            </div>
          </div>
        <div class="grid-2">
          <div class="panel">
            <div class="panel-header">
              <div class="panel-title">📈 Atividade do Sistema (24h)</div>
              <span class="panel-action">Ver mais</span>
            </div>
            <div class="chart-wrap">
              <svg class="chart-svg" id="activity-chart" viewBox="0 0 400 120" preserveAspectRatio="none">
                <defs>
                  <linearGradient id="g1" x1="0" y1="0" x2="0" y2="1">
                    <stop offset="0%" stop-color="#00d4ff" stop-opacity=".3"/>
                    <stop offset="100%" stop-color="#00d4ff" stop-opacity="0"/>
                  </linearGradient>
                </defs>
                <path id="chart-area" fill="url(#g1)"/>
                <path id="chart-line" fill="none" stroke="#00d4ff" stroke-width="2"/>
              </svg>
            </div>
          </div>
          <div class="panel">
            <div class="panel-header">
              <div class="panel-title">🚨 Alertas Recentes</div>
              <span class="panel-action">Ver todos</span>
            </div>
            <div class="activity-item">
              <div class="activity-icon danger">🔴</div>
              <div class="activity-body"><div class="activity-text">Força bruta detectada — IP 203.45.12.8</div><div class="activity-meta">47 tentativas em 2 min</div></div>
              <div class="activity-time">2min</div>
            </div>
            <div class="activity-item">
              <div class="activity-icon warning">⚠️</div>
              <div class="activity-body"><div class="activity-text">CPU acima de 85% por 5 min</div><div class="activity-meta">Servidor principal</div></div>
              <div class="activity-time">5min</div>
            </div>
            <div class="activity-item">
              <div class="activity-icon success">✅</div>
              <div class="activity-body"><div class="activity-text">SSL renovado com sucesso</div><div class="activity-meta">Válido 365 dias</div></div>
              <div class="activity-time">2h</div>
            </div>
            <div class="activity-item">
              <div class="activity-icon info">🔵</div>
              <div class="activity-body"><div class="activity-text">Backup automático concluído</div><div class="activity-meta">14.2 GB — 0 erros</div></div>
              <div class="activity-time">4h</div>
            </div>
          </div>
        </div>

        <div class="grid-2">
          <div class="panel">
            <div class="panel-header"><div class="panel-title">💻 Recursos do Sistema</div></div>
            <div class="resource-grid">
              <div class="resource-card">
                <div class="resource-val" id="cpu-val" style="color:var(--warning)">67%</div>
                <div class="resource-label">CPU</div>
                <div class="prog-bar"><div class="prog-fill" id="cpu-bar" style="width:67%;background:var(--warning)"></div></div>
              </div>
              <div class="resource-card">
                <div class="resource-val" id="ram-val" style="color:var(--accent)">54%</div>
                <div class="resource-label">RAM</div>
                <div class="prog-bar"><div class="prog-fill" id="ram-bar" style="width:54%;background:var(--accent)"></div></div>
              </div>
              <div class="resource-card">
                <div class="resource-val" id="disk-val" style="color:var(--accent3)">38%</div>
                <div class="resource-label">DISCO</div>
                <div class="prog-bar"><div class="prog-fill" id="disk-bar" style="width:38%;background:var(--accent3)"></div></div>
              </div>
              <div class="resource-card">
                <div class="resource-val" id="net-val" style="color:var(--accent2)">72%</div>
                <div class="resource-label">REDE</div>
                <div class="prog-bar"><div class="prog-fill" id="net-bar" style="width:72%;background:var(--accent2)"></div></div>
              </div>
            </div>
          </div>
          <div class="panel">
            <div class="panel-header"><div class="panel-title">🗺️ Mapa de Ameaças</div><span class="panel-action">Ao vivo</span></div>
            <div class="world-map">
              <div class="map-grid"></div>
              <div class="map-dot red" style="top:30%;left:25%"></div>
              <div class="map-dot red" style="top:45%;left:72%"></div>
              <div class="map-dot red" style="top:20%;left:60%"></div>
              <div class="map-dot green" style="top:55%;left:42%"></div>
              <div class="map-dot blue" style="top:38%;left:50%"></div>
              <div class="map-dot green" style="top:65%;left:30%"></div>
              <div class="map-dot red" style="top:28%;left:80%"></div>
              <span style="font-size:13px;color:var(--text3);position:absolute;bottom:10px;right:10px">🔴 Ataque &nbsp; 🟢 Seguro &nbsp; 🔵 Sua Localização</span>
            </div>
          </div>
        </div>
      </div>

      <!-- ── USUÁRIOS ── -->
      <div class="page" id="page-users">
        <div class="section-title">👥 Gerenciamento de Usuários</div>
        <div class="section-sub">Cadastre, edite e gerencie todos os usuários do sistema</div>
        <div class="inline-form">
          <input placeholder="Nome completo" id="new-user-name">
          <input placeholder="Email" id="new-user-email">
          <select style="padding:9px 12px;background:var(--bg);border:1px solid var(--border);border-radius:8px;color:var(--text);font-size:13px;outline:none">
            <option>Admin</option><option>Moderador</option><option>Usuário</option><option>Leitura</option>
          </select>
          <button class="btn-sm" onclick="addUser()">+ Adicionar</button>
        </div>
        <div class="panel">
          <table class="data-table" id="users-table">
            <thead><tr><th>#</th><th>Nome</th><th>Email</th><th>Perfil</th><th>Status</th><th>Último Acesso</th><th>MFA</th><th>Ações</th></tr></thead>
            <tbody id="users-tbody"></tbody>
          </table>
        </div>
      </div>

      <!-- ── ROLES ── -->
      <div class="page" id="page-roles">
        <div class="section-title">🎭 Perfis & Permissões (RBAC)</div>
        <div class="section-sub">Controle granular de acesso baseado em funções</div>
        <div class="grid-3">
          <div class="panel">
            <div class="panel-header"><div class="panel-title" style="color:var(--danger)">🔴 Super Admin</div></div>
            <div style="font-size:12px;color:var(--text3);margin-bottom:12px">Acesso total ao sistema</div>
            <div class="tag-list">
              <span class="tag">Ler</span><span class="tag">Escrever</span><span class="tag">Deletar</span>
              <span class="tag">Config</span><span class="tag">Usuários</span><span class="tag">Logs</span>
            </div>
          </div>
          <div class="panel">
            <div class="panel-header"><div class="panel-title" style="color:var(--warning)">🟡 Administrador</div></div>
            <div style="font-size:12px;color:var(--text3);margin-bottom:12px">Gerencia usuários e configurações</div>
            <div class="tag-list">
              <span class="tag">Ler</span><span class="tag">Escrever</span><span class="tag">Usuários</span>
              <span class="tag">Logs</span><span class="tag red">Config</span>
            </div>
          </div>
          <div class="panel">
            <div class="panel-header"><div class="panel-title" style="color:var(--accent3)">🟢 Usuário</div></div>
            <div style="font-size:12px;color:var(--text3);margin-bottom:12px">Acesso básico ao sistema</div>
            <div class="tag-list">
              <span class="tag">Ler</span><span class="tag red">Escrever</span><span class="tag red">Deletar</span>
            </div>
          </div>
        </div>
      </div>

      <!-- ── SESSIONS ── -->
      <div class="page" id="page-sessions">
        <div class="section-title">🔗 Sessões Ativas</div>
        <div class="section-sub">Dispositivos conectados em tempo real</div>
        <div class="panel">
          <table class="data-table">
            <thead><tr><th>Usuário</th><th>Dispositivo</th><th>IP</th><th>Local</th><th>Início</th><th>Status</th><th>Ação</th></tr></thead>
            <tbody>
              <tr><td>admin@secureos.com</td><td>💻 Chrome/Win11</td><td>192.168.1.10</td><td>🇧🇷 São Paulo</td><td>10:42</td><td><span class="badge green">● Ativo</span></td><td><button class="btn-sm red" style="font-size:11px;padding:4px 8px">Encerrar</button></td></tr>
              <tr><td>maria.silva@empresa.com</td><td>📱 Safari/iOS</td><td>177.23.45.90</td><td>🇧🇷 Rio de Janeiro</td><td>09:15</td><td><span class="badge green">● Ativo</span></td><td><button class="btn-sm red" style="font-size:11px;padding:4px 8px">Encerrar</button></td></tr>
              <tr><td>joao.tech@empresa.com</td><td>🖥️ Firefox/Mac</td><td>201.12.34.56</td><td>🇧🇷 Belo Horizonte</td><td>08:30</td><td><span class="badge yellow">⚡ Idle</span></td><td><button class="btn-sm red" style="font-size:11px;padding:4px 8px">Encerrar</button></td></tr>
              <tr><td>pedro.ops@empresa.com</td><td>💻 Edge/Win10</td><td>189.34.78.21</td><td>🇧🇷 Brasília</td><td>07:55</td><td><span class="badge green">● Ativo</span></td><td><button class="btn-sm red" style="font-size:11px;padding:4px 8px">Encerrar</button></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── ACCESS LOG ── -->
      <div class="page" id="page-access-log">
        <div class="section-title">📋 Histórico de Acessos</div>
        <div class="section-sub">Registro completo de todas as autenticações</div>
        <div class="panel">
          <table class="data-table">
            <thead><tr><th>Data/Hora</th><th>Usuário</th><th>IP</th><th>Dispositivo</th><th>Resultado</th></tr></thead>
            <tbody>
              <tr><td>05/04 10:42:01</td><td>admin@secureos.com</td><td>192.168.1.10</td><td>Chrome Win11</td><td><span class="badge green">✅ Sucesso</span></td></tr>
              <tr><td>05/04 10:38:44</td><td>hacker@evil.com</td><td>203.45.12.8</td><td>Unknown</td><td><span class="badge red">❌ Bloqueado</span></td></tr>
              <tr><td>05/04 09:15:30</td><td>maria.silva@empresa.com</td><td>177.23.45.90</td><td>Safari iOS</td><td><span class="badge green">✅ Sucesso</span></td></tr>
              <tr><td>05/04 08:55:12</td><td>guest@test.com</td><td>45.66.77.88</td><td>Firefox Linux</td><td><span class="badge yellow">⚠️ MFA Pendente</span></td></tr>
              <tr><td>05/04 08:30:05</td><td>joao.tech@empresa.com</td><td>201.12.34.56</td><td>Firefox Mac</td><td><span class="badge green">✅ Sucesso</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── MFA ── -->
      <div class="page" id="page-mfa-config">
        <div class="section-title">📱 Autenticação Multifator (MFA)</div>
        <div class="section-sub">Configure os métodos de segunda autenticação</div>
        <div class="grid-2">
          <div class="panel">
            <div class="panel-title" style="margin-bottom:16px">Métodos Disponíveis</div>
            <div class="setting-row"><div class="setting-info"><h4>📱 Aplicativo Autenticador (TOTP)</h4><p>Google Authenticator, Authy</p></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>📧 Email de verificação</h4><p>Código enviado por email</p></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>📲 SMS</h4><p>Código por mensagem de texto</p></div><label class="toggle"><input type="checkbox"><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>🔑 Chave física (FIDO2/WebAuthn)</h4><p>YubiKey, hardware tokens</p></div><label class="toggle"><input type="checkbox"><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>🖐️ Biometria</h4><p>Impressão digital, Face ID</p></div><label class="toggle"><input type="checkbox"><span class="toggle-slider"></span></label></div>
          </div>
          <div class="panel">
            <div class="panel-title" style="margin-bottom:16px">Políticas de MFA</div>
            <div class="setting-row"><div class="setting-info"><h4>MFA Obrigatório para Admins</h4><p>Todos os admins precisam de MFA</p></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>MFA Obrigatório para Todos</h4><p>Todos os usuários precisam de MFA</p></div><label class="toggle"><input type="checkbox"><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Lembrar dispositivo (30 dias)</h4><p>Não pedir MFA em dispositivos confiáveis</p></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Sessão expira em 1h sem atividade</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
          </div>
        </div>
      </div>

      <!-- ── ENCRYPTION ── -->
      <div class="page" id="page-encryption">
        <div class="section-title">🔑 Criptografia</div>
        <div class="section-sub">Protocolos e status de criptografia do sistema</div>
        <div class="metrics-grid">
          <div class="metric-card green"><div class="metric-icon">🔒</div><div class="metric-value">AES-256</div><div class="metric-label">Dados em Repouso</div><div class="metric-change up">↑ Ativo</div></div>
          <div class="metric-card blue"><div class="metric-icon">🌐</div><div class="metric-value">TLS 1.3</div><div class="metric-label">Dados em Trânsito</div><div class="metric-change up">↑ Ativo</div></div>
          <div class="metric-card purple"><div class="metric-icon">📂</div><div class="metric-value">RSA-4096</div><div class="metric-label">Chaves Assimétricas</div><div class="metric-change up">↑ Ativo</div></div>
          <div class="metric-card green"><div class="metric-icon">✅</div><div class="metric-value">SHA-512</div><div class="metric-label">Hash de Senhas</div><div class="metric-change up">↑ Ativo</div></div>
        </div>
        <div class="panel">
          <div class="panel-title" style="margin-bottom:14px">Certificados SSL/TLS</div>
          <table class="data-table">
            <thead><tr><th>Domínio</th><th>Emissor</th><th>Válido até</th><th>Status</th></tr></thead>
            <tbody>
              <tr><td>secureos.com</td><td>Let's Encrypt</td><td>05/04/2027</td><td><span class="badge green">✅ Válido</span></td></tr>
              <tr><td>api.secureos.com</td><td>DigiCert</td><td>01/01/2026</td><td><span class="badge green">✅ Válido</span></td></tr>
              <tr><td>cdn.secureos.com</td><td>Cloudflare</td><td>12/06/2025</td><td><span class="badge yellow">⚠️ Expira em 68d</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── THREATS ── -->
      <div class="page" id="page-threats">
        <div class="section-title">🎯 Detecção de Ameaças</div>
        <div class="section-sub">Comportamentos suspeitos detectados em tempo real</div>
        <div class="panel" style="margin-bottom:14px;border-color:var(--danger)">
          <div style="display:flex;align-items:center;gap:10px;color:var(--danger);font-weight:700;margin-bottom:12px">🚨 ALERTA ATIVO — Ataque de Força Bruta</div>
          <p style="font-size:13px;color:var(--text2)">IP <strong>203.45.12.8</strong> (CN — China) realizou 47 tentativas de login falhadas nos últimos 2 minutos. Bloqueio automático ativado.</p>
          <div style="display:flex;gap:8px;margin-top:12px">
            <button class="btn-sm red">🚫 Bloquear IP</button>
            <button class="btn-sm outline">📋 Ver Detalhes</button>
            <button class="btn-sm outline">✅ Ignorar</button>
          </div>
        </div>
        <div class="panel">
          <table class="data-table">
            <thead><tr><th>Tipo</th><th>IP Origem</th><th>País</th><th>Tentativas</th><th>Risco</th><th>Status</th></tr></thead>
            <tbody>
              <tr><td>Força Bruta</td><td>203.45.12.8</td><td>🇨🇳 CN</td><td>47</td><td><span class="badge red">CRÍTICO</span></td><td><span class="badge red">Bloqueado</span></td></tr>
              <tr><td>Port Scan</td><td>91.232.105.66</td><td>🇷🇺 RU</td><td>1</td><td><span class="badge yellow">MÉDIO</span></td><td><span class="badge yellow">Monitorando</span></td></tr>
              <tr><td>Injeção SQL</td><td>185.220.101.9</td><td>🇩🇪 DE</td><td>3</td><td><span class="badge red">ALTO</span></td><td><span class="badge red">Bloqueado</span></td></tr>
              <tr><td>DDoS (UDP)</td><td>Multiple</td><td>🌍 Vários</td><td>5.200</td><td><span class="badge red">CRÍTICO</span></td><td><span class="badge green">Mitigado</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── IP LIST ── -->
      <div class="page" id="page-iplist">
        <div class="section-title">🚫 IPs Permitidos / Bloqueados</div>
        <div class="section-sub">Lista de controle de acesso por endereço IP</div>
        <div class="grid-2">
          <div class="panel">
            <div class="panel-header"><div class="panel-title" style="color:var(--accent3)">✅ IPs Permitidos</div></div>
            <div class="inline-form" style="margin-bottom:12px">
              <input placeholder="Ex: 192.168.1.0/24" id="allow-ip">
              <button class="btn-sm" onclick="addIP('allow')">+ Adicionar</button>
            </div>
            <div id="allowed-ips">
              <div class="ip-item"><span class="ip-flag">🏢</span><span class="ip-addr">192.168.0.0/24</span><span class="badge green">Escritório</span><button class="btn-sm red" style="padding:3px 8px;font-size:11px;margin-left:auto">✕</button></div>
              <div class="ip-item"><span class="ip-flag">🏠</span><span class="ip-addr">10.0.0.1</span><span class="badge green">VPN Admin</span><button class="btn-sm red" style="padding:3px 8px;font-size:11px;margin-left:auto">✕</button></div>
            </div>
          </div>
          <div class="panel">
            <div class="panel-header"><div class="panel-title" style="color:var(--danger)">🚫 IPs Bloqueados</div></div>
            <div class="inline-form" style="margin-bottom:12px">
              <input placeholder="Ex: 203.45.12.8" id="block-ip">
              <button class="btn-sm red" onclick="addIP('block')">+ Bloquear</button>
            </div>
            <div id="blocked-ips">
              <div class="ip-item"><span class="ip-flag">🇨🇳</span><span class="ip-addr">203.45.12.8</span><span class="badge red">Força Bruta</span><button class="btn-sm outline" style="padding:3px 8px;font-size:11px;margin-left:auto">✕</button></div>
              <div class="ip-item"><span class="ip-flag">🇷🇺</span><span class="ip-addr">91.232.105.66</span><span class="badge red">Port Scan</span><button class="btn-sm outline" style="padding:3px 8px;font-size:11px;margin-left:auto">✕</button></div>
              <div class="ip-item"><span class="ip-flag">🇩🇪</span><span class="ip-addr">185.220.101.9</span><span class="badge red">SQL Inject</span><button class="btn-sm outline" style="padding:3px 8px;font-size:11px;margin-left:auto">✕</button></div>
            </div>
          </div>
        </div>
      </div>

      <!-- ── FIREWALL ── -->
      <div class="page" id="page-firewall">
        <div class="section-title">🔥 Firewall Lógico</div>
        <div class="section-sub">Regras de segurança de rede internas</div>
        <div class="panel">
          <div class="panel-header">
            <div class="panel-title">Regras Ativas</div>
            <button class="btn-sm">+ Nova Regra</button>
          </div>
          <div class="rule-item"><span class="rule-action allow">ALLOW</span><span style="font-family:monospace;font-size:12px;flex:1">TCP 443 IN → ANY</span><span class="badge green">HTTPS</span><label class="toggle" style="margin-left:auto"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
          <div class="rule-item"><span class="rule-action allow">ALLOW</span><span style="font-family:monospace;font-size:12px;flex:1">TCP 80 IN → ANY (redirect 443)</span><span class="badge blue">HTTP→HTTPS</span><label class="toggle" style="margin-left:auto"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
          <div class="rule-item"><span class="rule-action allow">ALLOW</span><span style="font-family:monospace;font-size:12px;flex:1">UDP 1194 IN → VPN</span><span class="badge purple">VPN</span><label class="toggle" style="margin-left:auto"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
          <div class="rule-item"><span class="rule-action deny">DENY</span><span style="font-family:monospace;font-size:12px;flex:1">TCP 22 IN → 0.0.0.0/0</span><span class="badge red">SSH Público</span><label class="toggle" style="margin-left:auto"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
          <div class="rule-item"><span class="rule-action deny">DENY</span><span style="font-family:monospace;font-size:12px;flex:1">ALL → Blacklist IPs</span><span class="badge red">Bloqueados</span><label class="toggle" style="margin-left:auto"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
          <div class="rule-item"><span class="rule-action deny">DENY</span><span style="font-family:monospace;font-size:12px;flex:1">ICMP IN → rate &gt; 100/s</span><span class="badge yellow">Anti-Flood</span><label class="toggle" style="margin-left:auto"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
        </div>
      </div>

      <!-- ── VPN ── -->
      <div class="page" id="page-vpn">
        <div class="section-title">🌐 VPN — Rede Privada Virtual</div>
        <div class="section-sub">Gerencie sua conexão VPN e servidores disponíveis</div>
        <div class="vpn-status">
          <div class="vpn-globe" id="vpn-globe">🌐</div>
          <div class="vpn-name" id="vpn-name">🟢 Conectado — São Paulo, BR</div>
          <div class="vpn-ip" id="vpn-ip">IP Real: 192.168.1.10 → IP VPN: 10.0.0.45 | Protocolo: WireGuard</div>
          <button class="btn-vpn disconnect" id="vpn-btn" onclick="toggleVPN()">⏹️ Desconectar VPN</button>
        </div>
        <div class="grid-3">
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">🖥️ Servidores Disponíveis</div>
            <table class="data-table">
              <thead><tr><th>Servidor</th><th>Ping</th><th>Status</th></tr></thead>
              <tbody>
                <tr><td>🇧🇷 São Paulo</td><td>12ms</td><td><span class="badge green">● Online</span></td></tr>
                <tr><td>🇺🇸 New York</td><td>89ms</td><td><span class="badge green">● Online</span></td></tr>
                <tr><td>🇩🇪 Frankfurt</td><td>132ms</td><td><span class="badge green">● Online</span></td></tr>
                <tr><td>🇯🇵 Tokyo</td><td>210ms</td><td><span class="badge yellow">⚡ Alta carga</span></td></tr>
                <tr><td>🇬🇧 London</td><td>145ms</td><td><span class="badge green">● Online</span></td></tr>
                <tr><td>🇦🇺 Sydney</td><td>287ms</td><td><span class="badge red">● Offline</span></td></tr>
              </tbody>
            </table>
          </div>
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">⚙️ Configurações VPN</div>
            <div class="setting-row"><div class="setting-info"><h4>Kill Switch</h4><p>Bloqueia internet se VPN cair</p></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Split Tunneling</h4><p>Apenas tráfego selecionado</p></div><label class="toggle"><input type="checkbox"><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Auto-reconexão</h4><p>Reconectar ao cair</p></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Protocolo: WireGuard</h4></div><span class="badge blue">Ativo</span></div>
            <div class="setting-row"><div class="setting-info"><h4>DNS Leak Protection</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
          </div>
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">📊 Estatísticas VPN</div>
            <div class="prog-item"><div class="prog-label"><span>Download</span><span style="color:var(--accent3)">↓ 4.2 MB/s</span></div><div class="prog-bar"><div class="prog-fill" style="width:42%;background:var(--accent3)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Upload</span><span style="color:var(--accent)">↑ 1.8 MB/s</span></div><div class="prog-bar"><div class="prog-fill" style="width:18%;background:var(--accent)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Uso de Banda</span><span>2.3 GB / 10 GB</span></div><div class="prog-bar"><div class="prog-fill" style="width:23%;background:var(--accent2)"></div></div></div>
            <div style="margin-top:12px;font-size:12px;color:var(--text3)">
              <div style="margin-bottom:6px">⏱️ Tempo conectado: <strong style="color:var(--text)">3h 42min</strong></div>
              <div style="margin-bottom:6px">🔐 Criptografia: <strong style="color:var(--text)">ChaCha20-Poly1305</strong></div>
              <div>🛡️ Vazamento DNS: <strong style="color:var(--accent3)">Protegido</strong></div>
            </div>
          </div>
        </div>
      </div>

      <!-- ── NETWORK ── -->
      <div class="page" id="page-network">
        <div class="section-title">📡 Rede & Conectividade</div>
        <div class="section-sub">Status e configuração da infraestrutura de rede</div>
        <div class="metrics-grid">
          <div class="metric-card green"><div class="metric-icon">📡</div><div class="metric-value">12ms</div><div class="metric-label">Latência</div><div class="metric-change up">↑ Excelente</div></div>
          <div class="metric-card blue"><div class="metric-icon">⬇️</div><div class="metric-value">940 Mb</div><div class="metric-label">Download</div><div class="metric-change up">↑ Normal</div></div>
          <div class="metric-card purple"><div class="metric-icon">⬆️</div><div class="metric-value">420 Mb</div><div class="metric-label">Upload</div><div class="metric-change up">↑ Normal</div></div>
          <div class="metric-card green"><div class="metric-icon">🖥️</div><div class="metric-value">3/3</div><div class="metric-label">Servidores Online</div><div class="metric-change up">↑ Todos OK</div></div>
        </div>
        <div class="panel">
          <div class="panel-title" style="margin-bottom:14px">Conexões Ativas</div>
          <table class="data-table">
            <thead><tr><th>Protocolo</th><th>IP Local</th><th>IP Remoto</th><th>Porta</th><th>Status</th></tr></thead>
            <tbody>
              <tr><td>TCP</td><td>10.0.0.1</td><td>8.8.8.8</td><td>443</td><td><span class="badge green">ESTABLISHED</span></td></tr>
              <tr><td>UDP</td><td>10.0.0.1</td><td>1.1.1.1</td><td>53</td><td><span class="badge green">ESTABLISHED</span></td></tr>
              <tr><td>TCP</td><td>10.0.0.45</td><td>172.217.3.46</td><td>443</td><td><span class="badge blue">TIME_WAIT</span></td></tr>
              <tr><td>TCP</td><td>10.0.0.1</td><td>203.45.12.8</td><td>80</td><td><span class="badge red">BLOCKED</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── MONITORING ── -->
      <div class="page" id="page-monitoring">
        <div class="section-title">📊 Monitoramento em Tempo Real</div>
        <div class="section-sub">Métricas do sistema atualizadas automaticamente</div>
        <div class="realtime-bar">
          <div class="rt-dot"></div>
          <span class="rt-label">Atualização automática a cada 2 segundos</span>
          <span class="rt-value" id="monitor-timestamp">--</span>
        </div>
        <div class="metrics-grid">
          <div class="metric-card yellow"><div class="metric-icon">🖥️</div><div class="metric-value" id="mon-cpu">67%</div><div class="metric-label">CPU</div></div>
          <div class="metric-card blue"><div class="metric-icon">💾</div><div class="metric-value" id="mon-ram">54%</div><div class="metric-label">RAM (8.6/16 GB)</div></div>
          <div class="metric-card green"><div class="metric-icon">💿</div><div class="metric-value">38%</div><div class="metric-label">Disco (380/1000 GB)</div></div>
          <div class="metric-card purple"><div class="metric-icon">🌡️</div><div class="metric-value" id="mon-temp">52°C</div><div class="metric-label">Temperatura</div></div>
          <div class="metric-card blue"><div class="metric-icon">⚡</div><div class="metric-value" id="mon-proc">142</div><div class="metric-label">Processos</div></div>
          <div class="metric-card green"><div class="metric-icon">🔗</div><div class="metric-value" id="mon-conn">38</div><div class="metric-label">Conexões TCP</div></div>
        </div>
        <div class="panel">
          <div class="panel-title" style="margin-bottom:14px">📈 Histórico CPU (última hora)</div>
          <div class="chart-wrap" style="height:160px">
            <svg class="chart-svg" id="mon-chart" viewBox="0 0 400 140" preserveAspectRatio="none">
              <defs>
                <linearGradient id="g2" x1="0" y1="0" x2="0" y2="1">
                  <stop offset="0%" stop-color="#f59e0b" stop-opacity=".4"/>
                  <stop offset="100%" stop-color="#f59e0b" stop-opacity="0"/>
                </linearGradient>
              </defs>
              <path id="mon-area" fill="url(#g2)"/>
              <path id="mon-line" fill="none" stroke="#f59e0b" stroke-width="2"/>
            </svg>
          </div>
        </div>
      </div>

      <!-- ── LOGS ── -->
      <div class="page" id="page-logs">
        <div class="section-title">📜 Logs em Tempo Real</div>
        <div class="section-sub">Console de logs do sistema</div>
        <div style="display:flex;gap:8px;margin-bottom:14px;flex-wrap:wrap">
          <button class="btn-sm" onclick="filterLog('all')">Todos</button>
          <button class="btn-sm outline" onclick="filterLog('error')">Erros</button>
          <button class="btn-sm outline" onclick="filterLog('warn')">Avisos</button>
          <button class="btn-sm outline" onclick="filterLog('info')">Info</button>
          <button class="btn-sm outline" onclick="filterLog('success')">Sucesso</button>
          <button class="btn-sm red" style="margin-left:auto" onclick="clearLogs()">🗑️ Limpar</button>
        </div>
        <div class="panel" style="background:var(--bg)">
          <div class="log-scroll" id="log-container"></div>
        </div>
      </div>

      <!-- ── AUDIT ── -->
      <div class="page" id="page-audit">
        <div class="section-title">🔍 Auditoria Completa</div>
        <div class="section-sub">Trilha completa de todas as ações realizadas no sistema</div>
        <div class="panel">
          <table class="data-table">
            <thead><tr><th>Timestamp</th><th>Usuário</th><th>Ação</th><th>Recurso</th><th>IP</th><th>Resultado</th></tr></thead>
            <tbody>
              <tr><td>05/04 10:45:32</td><td>admin</td><td>UPDATE</td><td>Firewall Rule #4</td><td>192.168.1.10</td><td><span class="badge green">✅ OK</span></td></tr>
              <tr><td>05/04 10:38:44</td><td>[anon]</td><td>LOGIN_FAIL</td><td>auth/login</td><td>203.45.12.8</td><td><span class="badge red">❌ Bloqueado</span></td></tr>
              <tr><td>05/04 10:30:11</td><td>admin</td><td>DELETE</td><td>User #id:992</td><td>192.168.1.10</td><td><span class="badge green">✅ OK</span></td></tr>
              <tr><td>05/04 10:15:00</td><td>maria.silva</td><td>EXPORT</td><td>Relatório Mensal</td><td>177.23.45.90</td><td><span class="badge green">✅ OK</span></td></tr>
              <tr><td>05/04 09:50:22</td><td>admin</td><td>CONFIG_CHANGE</td><td>MFA Settings</td><td>192.168.1.10</td><td><span class="badge green">✅ OK</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── DATA ── -->
      <div class="page" id="page-data">
        <div class="section-title">🗄️ Dados & Armazenamento</div>
        <div class="section-sub">Gerenciamento de banco de dados e backups</div>
        <div class="grid-2">
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">💾 Backup Automático</div>
            <div class="setting-row"><div class="setting-info"><h4>Backup Diário (02:00)</h4><p>Último: 05/04 02:00 — 14.2 GB</p></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Backup Semanal</h4><p>Todo domingo às 01:00</p></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Retenção</h4><p>Manter últimos 30 backups</p></div><span class="badge blue">30 dias</span></div>
            <div style="margin-top:16px;display:flex;gap:8px">
              <button class="btn-sm">🔄 Backup Agora</button>
              <button class="btn-sm outline">📥 Restaurar</button>
            </div>
          </div>
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">📊 Uso de Armazenamento</div>
            <div class="prog-item"><div class="prog-label"><span>Banco de Dados</span><span>4.2 GB</span></div><div class="prog-bar"><div class="prog-fill" style="width:42%;background:var(--accent)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Backups</span><span>86 GB</span></div><div class="prog-bar"><div class="prog-fill" style="width:86%;background:var(--warning)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Logs</span><span>1.8 GB</span></div><div class="prog-bar"><div class="prog-fill" style="width:18%;background:var(--accent3)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Mídia / Arquivos</span><span>23 GB</span></div><div class="prog-bar"><div class="prog-fill" style="width:23%;background:var(--accent2)"></div></div></div>
          </div>
        </div>
      </div>

      <!-- ── AUTOMATION ── -->
      <div class="page" id="page-automation">
        <div class="section-title">🤖 Automação</div>
        <div class="section-sub">Scripts, workflows e tarefas agendadas</div>
        <div class="panel">
          <div class="panel-title" style="margin-bottom:14px">⚡ Regras Automáticas</div>
          <table class="data-table">
            <thead><tr><th>Nome</th><th>Gatilho</th><th>Ação</th><th>Última Execução</th><th>Status</th></tr></thead>
            <tbody>
              <tr><td>🚫 Auto-ban IP</td><td>5+ logins falhos</td><td>Bloquear IP por 24h</td><td>Há 2min</td><td><span class="badge green">Ativo</span></td></tr>
              <tr><td>📧 Alerta Admin</td><td>CPU > 90%</td><td>Enviar email</td><td>Há 1h</td><td><span class="badge green">Ativo</span></td></tr>
              <tr><td>🔄 Backup Auto</td><td>Diário 02:00</td><td>Backup completo</td><td>Hoje 02:00</td><td><span class="badge green">Ativo</span></td></tr>
              <tr><td>🔐 Expirar Sessão</td><td>1h sem atividade</td><td>Logout forçado</td><td>Há 15min</td><td><span class="badge green">Ativo</span></td></tr>
              <tr><td>📊 Relatório</td><td>Semanal Dom</td><td>Gerar + enviar PDF</td><td>Dom 08:00</td><td><span class="badge yellow">Agendado</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── NOTIFICATIONS CFG ── -->
      <div class="page" id="page-notifications-cfg">
        <div class="section-title">📢 Configuração de Notificações</div>
        <div class="section-sub">Configure canais e prioridades de alertas</div>
        <div class="grid-2">
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">Canais de Notificação</div>
            <div class="setting-row"><div class="setting-info"><h4>📧 Email</h4><p>admin@secureos.com</p></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>📲 SMS</h4><p>+55 11 99999-9999</p></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>🔔 Push (Browser)</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>💬 Slack</h4><p>#security-alerts</p></div><label class="toggle"><input type="checkbox"><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>📡 Webhook</h4><p>https://hooks.empresa.com</p></div><label class="toggle"><input type="checkbox"><span class="toggle-slider"></span></label></div>
          </div>
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">Prioridades</div>
            <div class="setting-row"><div class="setting-info"><h4>🔴 Crítico</h4><p>Email + SMS + Push imediato</p></div><span class="badge red">Todos canais</span></div>
            <div class="setting-row"><div class="setting-info"><h4>🟡 Alto</h4><p>Email + Push</p></div><span class="badge yellow">2 canais</span></div>
            <div class="setting-row"><div class="setting-info"><h4>🟢 Médio</h4><p>Push apenas</p></div><span class="badge green">1 canal</span></div>
            <div class="setting-row"><div class="setting-info"><h4>⚪ Baixo</h4><p>Log apenas, sem notificação</p></div><span class="badge gray">Silent</span></div>
          </div>
        </div>
      </div>

      <!-- ── REPORTS ── -->
      <div class="page" id="page-reports">
        <div class="section-title">📈 Relatórios & Análises</div>
        <div class="section-sub">Gere e exporte relatórios do sistema</div>
        <div class="grid-3">
          <div class="metric-card blue"><div class="metric-icon">🛡️</div><div class="metric-value">1.247</div><div class="metric-label">Ameaças este mês</div></div>
          <div class="metric-card green"><div class="metric-icon">👤</div><div class="metric-value">284</div><div class="metric-label">Logins bem-sucedidos</div></div>
          <div class="metric-card red"><div class="metric-icon">🚫</div><div class="metric-value">892</div><div class="metric-label">Logins bloqueados</div></div>
        </div>
        <div class="panel">
          <div class="panel-header"><div class="panel-title">Gerar Relatório</div></div>
          <div style="display:flex;gap:10px;flex-wrap:wrap;margin-bottom:16px">
            <select style="padding:9px 12px;background:var(--bg);border:1px solid var(--border);border-radius:8px;color:var(--text);font-size:13px;outline:none">
              <option>Segurança Geral</option><option>Acessos de Usuários</option><option>Ameaças Detectadas</option><option>Uso de Recursos</option>
            </select>
            <select style="padding:9px 12px;background:var(--bg);border:1px solid var(--border);border-radius:8px;color:var(--text);font-size:13px;outline:none">
              <option>Últimos 7 dias</option><option>Último mês</option><option>Último trimestre</option>
            </select>
            <button class="btn-sm">📄 Gerar PDF</button>
            <button class="btn-sm outline">📊 Exportar Excel</button>
          </div>
        </div>
      </div>

      <!-- ── TOOLS ── -->
      <div class="page" id="page-tools">
        <div class="section-title">🛠️ Ferramentas Avançadas</div>
        <div class="section-sub">Console, diagnóstico e modo desenvolvedor</div>
        <div class="panel" style="background:#0a0e0a;font-family:monospace">
          <div style="display:flex;align-items:center;gap:8px;margin-bottom:12px">
            <div style="width:12px;height:12px;border-radius:50%;background:#ef4444"></div>
            <div style="width:12px;height:12px;border-radius:50%;background:#f59e0b"></div>
            <div style="width:12px;height:12px;border-radius:50%;background:#10b981"></div>
            <span style="font-size:12px;color:var(--text3);margin-left:8px">SecureOS Shell v3.0</span>
          </div>
          <div id="console-output" style="color:#00ff41;font-size:12px;line-height:1.8;max-height:200px;overflow-y:auto">
            <div>SecureOS v3.0.0 — © 2025 Enterprise Edition</div>
            <div style="color:#888">Type 'help' for available commands.</div>
          </div>
          <div style="display:flex;gap:8px;margin-top:10px;align-items:center">
            <span style="color:#00d4ff;font-size:12px">admin@secureos:~$</span>
            <input id="console-input" onkeydown="handleConsole(event)" style="flex:1;background:transparent;border:none;color:#00ff41;font-size:12px;font-family:monospace;outline:none" placeholder="Digite um comando...">
          </div>
        </div>
        <div class="grid-3" style="margin-top:14px">
          <div class="panel" style="cursor:pointer" onclick="runDiag()"><div class="panel-title">🔍 Diagnóstico do Sistema</div><p style="font-size:12px;color:var(--text3);margin-top:6px">Verifica integridade e saúde</p></div>
          <div class="panel" style="cursor:pointer"><div class="panel-title">🧪 Teste de Penetração</div><p style="font-size:12px;color:var(--text3);margin-top:6px">Simulação de ataques internos</p></div>
          <div class="panel" style="cursor:pointer"><div class="panel-title">🔬 Modo Debug</div><p style="font-size:12px;color:var(--text3);margin-top:6px">Logs detalhados e stack traces</p></div>
        </div>
      </div>

      <!-- ── COMPLIANCE ── -->
      <div class="page" id="page-compliance">
        <div class="section-title">📜 Conformidade & LGPD/GDPR</div>
        <div class="section-sub">Status de conformidade com regulamentações de dados</div>
        <div class="grid-2">
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">LGPD (Brasil)</div>
            <div class="prog-item"><div class="prog-label"><span>Consentimento de dados</span><span style="color:var(--accent3)">100%</span></div><div class="prog-bar"><div class="prog-fill" style="width:100%;background:var(--accent3)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Portabilidade de dados</span><span style="color:var(--accent3)">90%</span></div><div class="prog-bar"><div class="prog-fill" style="width:90%;background:var(--accent3)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Direito ao esquecimento</span><span style="color:var(--warning)">75%</span></div><div class="prog-bar"><div class="prog-fill" style="width:75%;background:var(--warning)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Relatório de impacto (RIPD)</span><span style="color:var(--accent)">85%</span></div><div class="prog-bar"><div class="prog-fill" style="width:85%;background:var(--accent)"></div></div></div>
          </div>
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">GDPR (Europa)</div>
            <div class="setting-row"><div class="setting-info"><h4>Criptografia de dados pessoais</h4></div><span class="badge green">✅ OK</span></div>
            <div class="setting-row"><div class="setting-info"><h4>Retenção máxima 90 dias</h4></div><span class="badge green">✅ OK</span></div>
            <div class="setting-row"><div class="setting-info"><h4>DPO designado</h4></div><span class="badge yellow">⚠️ Pendente</span></div>
            <div class="setting-row"><div class="setting-info"><h4>Notificação de vazamento 72h</h4></div><span class="badge green">✅ OK</span></div>
          </div>
        </div>
      </div>

      <!-- ── SETTINGS ── -->
      <div class="page" id="page-settings">
        <div class="section-title">⚙️ Configurações do Sistema</div>
        <div class="section-sub">Preferências gerais, tema e integrações</div>
        <div class="grid-2">
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">Geral</div>
            <div class="setting-row"><div class="setting-info"><h4>Nome do Sistema</h4><p>SecureOS Enterprise</p></div><button class="btn-sm outline">Editar</button></div>
            <div class="setting-row"><div class="setting-info"><h4>Idioma</h4><p>Português (Brasil)</p></div><select style="padding:6px;background:var(--bg);border:1px solid var(--border);border-radius:6px;color:var(--text);font-size:12px"><option>PT-BR</option><option>EN-US</option><option>ES</option></select></div>
            <div class="setting-row"><div class="setting-info"><h4>Fuso horário</h4><p>America/Sao_Paulo (GMT-3)</p></div><button class="btn-sm outline">Alterar</button></div>
            <div class="setting-row"><div class="setting-info"><h4>Tema Escuro</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
          </div>
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">Segurança da Conta</div>
            <div class="setting-row"><div class="setting-info"><h4>Alterar Senha</h4></div><button class="btn-sm">🔑 Alterar</button></div>
            <div class="setting-row"><div class="setting-info"><h4>Sessões simultâneas</h4><p>Máximo 3 dispositivos</p></div><span class="badge blue">3</span></div>
            <div class="setting-row"><div class="setting-info"><h4>Expirar sessão</h4></div><select style="padding:6px;background:var(--bg);border:1px solid var(--border);border-radius:6px;color:var(--text);font-size:12px"><option>1 hora</option><option>4 horas</option><option>8 horas</option><option>24 horas</option></select></div>
            <div class="setting-row"><div class="setting-info"><h4>Log de atividades</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
          </div>
        </div>
      </div>

      <!-- ── SUPPORT ── -->
      <div class="page" id="page-support">
        <div class="section-title">🧑‍💻 Suporte & Sistema</div>
        <div class="section-sub">Central de ajuda e status do sistema</div>
        <div class="grid-3">
          <div class="metric-card green"><div class="metric-icon">✅</div><div class="metric-value">Online</div><div class="metric-label">Status do Sistema</div></div>
          <div class="metric-card blue"><div class="metric-icon">🎫</div><div class="metric-value">2</div><div class="metric-label">Tickets Abertos</div></div>
          <div class="metric-card purple"><div class="metric-icon">📦</div><div class="metric-value">v3.0.1</div><div class="metric-label">Versão Atual</div></div>
        </div>
        <div class="panel">
          <div class="panel-title" style="margin-bottom:14px">🎫 Tickets Recentes</div>
          <table class="data-table">
            <thead><tr><th>#</th><th>Assunto</th><th>Usuário</th><th>Prioridade</th><th>Status</th></tr></thead>
            <tbody>
              <tr><td>#1042</td><td>Não consigo acessar relatórios</td><td>maria.silva</td><td><span class="badge yellow">Média</span></td><td><span class="badge blue">Em análise</span></td></tr>
              <tr><td>#1041</td><td>MFA não está enviando SMS</td><td>pedro.ops</td><td><span class="badge red">Alta</span></td><td><span class="badge yellow">Aguardando</span></td></tr>
              <tr><td>#1040</td><td>Exportar PDF com erro</td><td>joao.tech</td><td><span class="badge gray">Baixa</span></td><td><span class="badge green">Resolvido</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── PASSWORDS ── -->
      <div class="page" id="page-passwords">
        <div class="section-title">🗝️ Gerenciamento de Senhas</div>
        <div class="section-sub">Políticas e auditoria de senhas do sistema</div>
        <div class="grid-2">
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">Políticas de Senha</div>
            <div class="setting-row"><div class="setting-info"><h4>Mínimo 8 caracteres</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Letras maiúsculas e minúsculas</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Números obrigatórios</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Caracteres especiais</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Expirar senha a cada 90 dias</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Não repetir últimas 5 senhas</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
            <div class="setting-row"><div class="setting-info"><h4>Bloquear após 5 tentativas</h4></div><label class="toggle"><input type="checkbox" checked><span class="toggle-slider"></span></label></div>
          </div>
          <div class="panel">
            <div class="panel-title" style="margin-bottom:14px">Auditoria de Senhas</div>
            <div class="prog-item"><div class="prog-label"><span>Senhas Fortes</span><span style="color:var(--accent3)">847 (66%)</span></div><div class="prog-bar"><div class="prog-fill" style="width:66%;background:var(--accent3)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Senhas Médias</span><span style="color:var(--warning)">312 (24%)</span></div><div class="prog-bar"><div class="prog-fill" style="width:24%;background:var(--warning)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Senhas Fracas</span><span style="color:var(--danger)">125 (10%)</span></div><div class="prog-bar"><div class="prog-fill" style="width:10%;background:var(--danger)"></div></div></div>
            <div class="prog-item"><div class="prog-label"><span>Expiradas</span><span style="color:var(--danger)">43 (3%)</span></div><div class="prog-bar"><div class="prog-fill" style="width:3%;background:var(--danger)"></div></div></div>
          </div>
        </div>
      </div>


      <!-- ── HACK: ALVOS INFECTADOS ── -->
      <div class="page" id="page-hack-targets">
        <canvas id="matrix-canvas"></canvas>
        <div style="display:flex;align-items:center;gap:12px;margin-bottom:6px">
          <div class="section-title" style="color:#ff0040;margin:0">🎯 Alvos Infectados</div>
          <span class="badge red" style="animation:pulse 1s infinite">● LIVE</span>
        </div>
        <div class="section-sub">Dispositivos comprometidos monitorados em tempo real</div>

        <div class="metrics-grid" style="margin-bottom:18px">
          <div class="hack-panel hack-glow" style="padding:16px;text-align:center">
            <div style="font-size:28px;font-weight:800;color:#ff0040;font-family:monospace" id="inf-count">23</div>
            <div style="font-size:11px;color:#555;text-transform:uppercase;letter-spacing:1px">Infectados Online</div>
          </div>
          <div class="hack-panel" style="padding:16px;text-align:center">
            <div style="font-size:28px;font-weight:800;color:#ff6b00;font-family:monospace">312</div>
            <div style="font-size:11px;color:#555;text-transform:uppercase;letter-spacing:1px">Bots na Rede</div>
          </div>
          <div class="hack-panel" style="padding:16px;text-align:center">
            <div style="font-size:28px;font-weight:800;color:#00ff41;font-family:monospace" id="data-stolen">4.7 GB</div>
            <div style="font-size:11px;color:#555;text-transform:uppercase;letter-spacing:1px">Dados Capturados</div>
          </div>
          <div class="hack-panel" style="padding:16px;text-align:center">
            <div style="font-size:28px;font-weight:800;color:#ff0040;font-family:monospace" id="keylog-count">8.421</div>
            <div style="font-size:11px;color:#555;text-transform:uppercase;letter-spacing:1px">Keystrokes Capturados</div>
          </div>
        </div>

        <div class="grid-2">
          <div class="hack-panel">
            <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:14px">
              <div style="font-size:13px;font-weight:600;color:#ff6b6b">Alvos Ativos</div>
              <span class="badge red" style="font-size:10px">23 online</span>
            </div>
            <div id="targets-list">
              <div class="target-card selected" onclick="selectTarget(this,'DESKTOP-K7J2X','192.168.4.12')">
                <div class="target-avatar">💻</div>
                <div class="target-info">
                  <div class="target-name">Carlos Mendes</div>
                  <div class="target-ip">192.168.4.12 · DESKTOP-K7J2X</div>
                  <div class="target-os">Windows 11 Pro · Chrome</div>
                </div>
                <div class="target-status">
                  <div class="hack-dot online"></div>
                  <span style="font-size:10px;color:#555">Ativo</span>
                </div>
              </div>
              <div class="target-card" onclick="selectTarget(this,'iMac-Fernanda','10.0.1.44')">
                <div class="target-avatar">🖥️</div>
                <div class="target-info">
                  <div class="target-name">Fernanda Ops</div>
                  <div class="target-ip">10.0.1.44 · iMac-Fernanda</div>
                  <div class="target-os">macOS Ventura · Safari</div>
                </div>
                <div class="target-status">
                  <div class="hack-dot online"></div>
                  <span style="font-size:10px;color:#555">Ativo</span>
                </div>
              </div>
              <div class="target-card" onclick="selectTarget(this,'LAPTOP-RB992','172.20.3.87')">
                <div class="target-avatar">📱</div>
                <div class="target-info">
                  <div class="target-name">Roberto Silva</div>
                  <div class="target-ip">172.20.3.87 · LAPTOP-RB992</div>
                  <div class="target-os">Windows 10 · Firefox</div>
                </div>
                <div class="target-status">
                  <div class="hack-dot idle"></div>
                  <span style="font-size:10px;color:#555">Idle</span>
                </div>
              </div>
              <div class="target-card" onclick="selectTarget(this,'Android-Juliana','192.168.1.201')">
                <div class="target-avatar">📲</div>
                <div class="target-info">
                  <div class="target-name">Juliana Adm</div>
                  <div class="target-ip">192.168.1.201 · Android</div>
                  <div class="target-os">Android 13 · Chrome Mobile</div>
                </div>
                <div class="target-status">
                  <div class="hack-dot online"></div>
                  <span style="font-size:10px;color:#555">Ativo</span>
                </div>
              </div>
              <div class="target-card" onclick="selectTarget(this,'WORKST-LUCAS','10.10.2.55')">
                <div class="target-avatar">🖥️</div>
                <div class="target-info">
                  <div class="target-name">Lucas TI</div>
                  <div class="target-ip">10.10.2.55 · WORKST-LUCAS</div>
                  <div class="target-os">Ubuntu 22.04 · Firefox</div>
                </div>
                <div class="target-status">
                  <div class="hack-dot online"></div>
                  <span style="font-size:10px;color:#555">Ativo</span>
                </div>
              </div>
            </div>
          </div>
          <div>
            <div class="hack-panel" style="margin-bottom:10px">
              <div style="font-size:12px;color:#555;margin-bottom:8px;font-family:monospace">
                ALVO SELECIONADO: <span id="sel-host" style="color:#ff6b6b">DESKTOP-K7J2X</span> · <span id="sel-ip" style="color:#00ff41">192.168.4.12</span>
              </div>
              <div style="display:flex;gap:8px;flex-wrap:wrap">
                <button class="btn-sm" style="background:#ff0040;color:#fff;font-size:11px" onclick="showPage('hack-screen',null)">🖥️ Ver Tela</button>
                <button class="btn-sm" style="background:#ff6b00;color:#fff;font-size:11px" onclick="hackAction('keylog')">⌨️ Keylogger</button>
                <button class="btn-sm" style="background:#7c3aed;color:#fff;font-size:11px" onclick="hackAction('cam')">📷 Webcam</button>
                <button class="btn-sm" style="background:#1a1a1a;color:#ff0040;border:1px solid #ff0040;font-size:11px" onclick="hackAction('files')">📂 Arquivos</button>
                <button class="btn-sm" style="background:#1a1a1a;color:#ff6b00;border:1px solid #ff6b00;font-size:11px" onclick="hackAction('mic')">🎤 Microfone</button>
                <button class="btn-sm" style="background:#1a1a1a;color:#ff0040;border:1px solid #ff0040;font-size:11px" onclick="hackAction('shutdown')">🔴 Desligar</button>
              </div>
            </div>
            <div class="hack-panel">
              <div style="font-size:12px;color:#ff6b6b;font-weight:600;margin-bottom:10px">⌨️ Keylogger ao Vivo</div>
              <div id="keylog-output" style="font-family:monospace;font-size:11px;color:#00ff41;line-height:1.8;max-height:160px;overflow-y:auto;background:#050505;padding:8px;border-radius:6px;border:1px solid rgba(0,255,65,.1)">
                <div><span style="color:#555">[10:42:03]</span> carlos · gmail.com<span style="color:#ff0040">·········</span></div>
                <div><span style="color:#555">[10:42:11]</span> senha123 <span style="color:#ff6b00">ENTER</span></div>
                <div><span style="color:#555">[10:43:22]</span> confidencial_relatorio_Q4.xlsx</div>
                <div><span style="color:#555">[10:44:01]</span> transferencia bancaria R$ 45.000 <span style="color:#ff6b00">TAB TAB ENTER</span></div>
                <div id="kl-live"></div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- ── HACK: VISUALIZAR TELA ── -->
      <div class="page" id="page-hack-screen">
        <div class="section-title" style="color:#ff0040">🖥️ Visualizador de Tela Remota</div>
        <div class="section-sub">Stream ao vivo da tela dos alvos comprometidos</div>
        <div class="grid-2" style="margin-bottom:14px">
          <div>
            <div style="font-size:12px;color:#555;font-family:monospace;margin-bottom:8px">
              CONECTADO EM: <span style="color:#ff6b6b">DESKTOP-K7J2X</span> · <span style="color:#00ff41">192.168.4.12</span> · <span id="screen-fps" style="color:#ff6b00">24 FPS</span>
            </div>
            <div class="screen-viewer" id="main-screen-viewer">
              <div class="sv-top">
                <div class="sv-dot2" style="background:#ff5f57"></div>
                <div class="sv-dot2" style="background:#febc2e"></div>
                <div class="sv-dot2" style="background:#28c840"></div>
                <span style="font-size:9px;color:#555;margin-left:6px;font-family:monospace">carlos_mendes — Área de Trabalho</span>
                <span style="margin-left:auto;font-size:9px;color:#ff0040;font-family:monospace" id="rec-label">● REC</span>
              </div>
              <div class="fake-screen">
                <div style="display:flex;gap:6px;margin-bottom:8px">
                  <div style="background:#2a2a3e;border-radius:4px;padding:4px 10px;font-size:9px;color:#7c7cff;border-bottom:2px solid #7c7cff">Gmail</div>
                  <div style="background:#1a1a2e;border-radius:4px;padding:4px 10px;font-size:9px;color:#666">Drive</div>
                  <div style="background:#1a1a2e;border-radius:4px;padding:4px 10px;font-size:9px;color:#666">Excel</div>
                </div>
                <div style="background:#16213e;border-radius:4px;padding:8px;font-size:9px;color:#ccc;margin-bottom:6px">
                  <div style="color:#888;margin-bottom:4px">De: carlos.mendes@empresa.com · Para: financeiro@empresa.com</div>
                  <div>Segue o relatório de transferências do Q4...</div>
                </div>
                <div style="display:flex;gap:4px;flex-wrap:wrap">
                  <div style="background:#0f3460;border-radius:3px;padding:3px 6px;font-size:8px;color:#7fc">📄 relatorio_q4.xlsx</div>
                  <div style="background:#0f3460;border-radius:3px;padding:3px 6px;font-size:8px;color:#7fc">🔒 senhas_banco.txt</div>
                </div>
                <div style="margin-top:8px;font-size:9px;color:#444" id="screen-typer"></div>
              </div>
              <div class="fake-taskbar">
                <div class="ftb-btn">⊞ Início</div>
                <div class="ftb-btn">🌐 Chrome</div>
                <div class="ftb-btn">📂 Docs</div>
                <div style="margin-left:auto;font-size:9px;color:#555" id="screen-clock">10:42</div>
              </div>
            </div>
          </div>
          <div style="display:flex;flex-direction:column;gap:10px">
            <div class="hack-panel">
              <div style="font-size:12px;color:#ff6b6b;font-weight:600;margin-bottom:10px">Controles Remotos</div>
              <div style="display:flex;flex-direction:column;gap:8px">
                <button class="hack-action" onclick="remoteAction('mouse')">
                  <span class="ha-icon">🖱️</span>
                  <div class="ha-info"><h4>Controlar Mouse</h4><p>Assumir controle do cursor</p></div>
                  <span class="ha-badge ready">PRONTO</span>
                </button>
                <button class="hack-action" onclick="remoteAction('keyboard')">
                  <span class="ha-icon">⌨️</span>
                  <div class="ha-info"><h4>Injetar Teclas</h4><p>Digitar remotamente</p></div>
                  <span class="ha-badge ready">PRONTO</span>
                </button>
                <button class="hack-action" onclick="remoteAction('screenshot')">
                  <span class="ha-icon">📸</span>
                  <div class="ha-info"><h4>Capturar Screenshot</h4><p>Salvar tela atual</p></div>
                  <span class="ha-badge live">LIVE</span>
                </button>
                <button class="hack-action" onclick="remoteAction('clipboard')">
                  <span class="ha-icon">📋</span>
                  <div class="ha-info"><h4>Roubar Clipboard</h4><p>Ver conteúdo copiado</p></div>
                  <span class="ha-badge live">LIVE</span>
                </button>
                <button class="hack-action" onclick="remoteAction('cam')">
                  <span class="ha-icon">📷</span>
                  <div class="ha-info"><h4>Ativar Webcam</h4><p>Stream oculto de câmera</p></div>
                  <span class="ha-badge ready">PRONTO</span>
                </button>
                <button class="hack-action" onclick="remoteAction('lock')">
                  <span class="ha-icon">🔒</span>
                  <div class="ha-info"><h4>Travar Tela</h4><p>Bloquear completamente o PC</p></div>
                  <span class="ha-badge idle2">IDLE</span>
                </button>
              </div>
            </div>
            <div class="hack-panel">
              <div style="font-size:11px;color:#ff6b6b;font-weight:600;margin-bottom:8px">Outros Alvos</div>
              <div style="display:flex;flex-direction:column;gap:6px" id="mini-targets">
                <div style="display:flex;align-items:center;gap:8px;cursor:pointer;padding:6px;border-radius:6px;background:#0a0305" onclick="switchScreenTarget('Fernanda Ops','10.0.1.44')">
                  <div class="hack-dot online"></div>
                  <span style="font-size:12px;color:#ff6b6b">Fernanda Ops</span>
                  <span style="font-size:10px;color:#444;margin-left:auto;font-family:monospace">10.0.1.44</span>
                </div>
                <div style="display:flex;align-items:center;gap:8px;cursor:pointer;padding:6px;border-radius:6px;background:#0a0305" onclick="switchScreenTarget('Roberto Silva','172.20.3.87')">
                  <div class="hack-dot idle"></div>
                  <span style="font-size:12px;color:#ff6b6b">Roberto Silva</span>
                  <span style="font-size:10px;color:#444;margin-left:auto;font-family:monospace">172.20.3.87</span>
                </div>
                <div style="display:flex;align-items:center;gap:8px;cursor:pointer;padding:6px;border-radius:6px;background:#0a0305" onclick="switchScreenTarget('Juliana Adm','192.168.1.201')">
                  <div class="hack-dot online"></div>
                  <span style="font-size:12px;color:#ff6b6b">Juliana Adm</span>
                  <span style="font-size:10px;color:#444;margin-left:auto;font-family:monospace">192.168.1.201</span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="remote-action-log" style="font-family:monospace;font-size:11px;color:#00ff41;background:#050505;border:1px solid rgba(0,255,65,.1);border-radius:6px;padding:10px;max-height:80px;overflow-y:auto"></div>
      </div>

      <!-- ── HACK: BOTNET ── -->
      <div class="page" id="page-hack-botnet">
        <div class="section-title" style="color:#ff0040">🤖 Rede de Bots (Botnet)</div>
        <div class="section-sub">Dispositivos sob controle total da rede</div>
        <div class="metrics-grid" style="margin-bottom:16px">
          <div class="hack-panel" style="text-align:center;padding:16px">
            <div style="font-size:26px;font-weight:800;color:#ff0040;font-family:monospace" id="bot-total">312</div>
            <div style="font-size:10px;color:#555;letter-spacing:1px">BOTS ATIVOS</div>
          </div>
          <div class="hack-panel" style="text-align:center;padding:16px">
            <div style="font-size:26px;font-weight:800;color:#ff6b00;font-family:monospace">18</div>
            <div style="font-size:10px;color:#555;letter-spacing:1px">PAÍSES</div>
          </div>
          <div class="hack-panel" style="text-align:center;padding:16px">
            <div style="font-size:26px;font-weight:800;color:#00ff41;font-family:monospace" id="ddos-power">48 Gbps</div>
            <div style="font-size:10px;color:#555;letter-spacing:1px">PODER DDoS</div>
          </div>
          <div class="hack-panel" style="text-align:center;padding:16px">
            <div style="font-size:26px;font-weight:800;color:#7c3aed;font-family:monospace">99.1%</div>
            <div style="font-size:10px;color:#555;letter-spacing:1px">UPTIME REDE</div>
          </div>
        </div>
        <div class="grid-2">
          <div class="hack-panel">
            <div style="font-size:12px;color:#ff6b6b;font-weight:600;margin-bottom:12px">🌎 Bots por País</div>
            <div class="bot-grid" id="bot-grid">
              <div class="bot-card active"><div class="bot-flag">🇧🇷</div><div class="bot-ip">201.x.x.x</div><div class="bot-label">BR · 87 bots</div></div>
              <div class="bot-card"><div class="bot-flag">🇺🇸</div><div class="bot-ip">104.x.x.x</div><div class="bot-label">US · 64 bots</div></div>
              <div class="bot-card"><div class="bot-flag">🇷🇺</div><div class="bot-ip">91.x.x.x</div><div class="bot-ip">RU · 41 bots</div><div class="bot-label"></div></div>
              <div class="bot-card"><div class="bot-flag">🇨🇳</div><div class="bot-ip">203.x.x.x</div><div class="bot-label">CN · 38 bots</div></div>
              <div class="bot-card"><div class="bot-flag">🇩🇪</div><div class="bot-ip">185.x.x.x</div><div class="bot-label">DE · 22 bots</div></div>
              <div class="bot-card"><div class="bot-flag">🇫🇷</div><div class="bot-ip">92.x.x.x</div><div class="bot-label">FR · 18 bots</div></div>
              <div class="bot-card"><div class="bot-flag">🇮🇳</div><div class="bot-ip">117.x.x.x</div><div class="bot-label">IN · 15 bots</div></div>
              <div class="bot-card"><div class="bot-flag">🇰🇷</div><div class="bot-ip">211.x.x.x</div><div class="bot-label">KR · 11 bots</div></div>
              <div class="bot-card"><div class="bot-flag">🇦🇷</div><div class="bot-ip">190.x.x.x</div><div class="bot-label">AR · 9 bots</div></div>
              <div class="bot-card"><div class="bot-flag">🇺🇦</div><div class="bot-ip">176.x.x.x</div><div class="bot-label">UA · 7 bots</div></div>
            </div>
          </div>
          <div style="display:flex;flex-direction:column;gap:10px">
            <div class="hack-panel">
              <div style="font-size:12px;color:#ff6b6b;font-weight:600;margin-bottom:10px">⚡ Comandos da Botnet</div>
              <div class="hack-action" onclick="botCommand('ddos')">
                <span class="ha-icon">💥</span>
                <div class="ha-info"><h4>Lançar Ataque DDoS</h4><p>Direcionar todos os bots a um alvo</p></div>
                <span class="ha-badge ready">PRONTO</span>
              </div>
              <div class="hack-action" onclick="botCommand('spam')">
                <span class="ha-icon">📧</span>
                <div class="ha-info"><h4>Campanha de Spam</h4><p>Enviar emails em massa</p></div>
                <span class="ha-badge live">ATIVO</span>
              </div>
              <div class="hack-action" onclick="botCommand('mine')">
                <span class="ha-icon">⛏️</span>
                <div class="ha-info"><h4>Cryptomining Oculto</h4><p>Minerar com CPU dos infectados</p></div>
                <span class="ha-badge live">ATIVO</span>
              </div>
              <div class="hack-action" onclick="botCommand('spread')">
                <span class="ha-icon">🦠</span>
                <div class="ha-info"><h4>Propagar Vírus</h4><p>Infectar novos dispositivos</p></div>
                <span class="ha-badge ready">PRONTO</span>
              </div>
              <div class="hack-action" onclick="botCommand('update')">
                <span class="ha-icon">🔄</span>
                <div class="ha-info"><h4>Atualizar Payload</h4><p>Enviar nova versão do malware</p></div>
                <span class="ha-badge idle2">IDLE</span>
              </div>
            </div>
            <div class="hack-panel">
              <div style="font-size:12px;color:#ff6b6b;font-weight:600;margin-bottom:8px">📊 Uso de Recursos dos Bots</div>
              <div class="prog-item"><div class="prog-label"><span style="color:#555">CPU Média</span><span style="color:#ff0040" id="bot-cpu">34%</span></div><div class="prog-bar" style="background:#1a0005"><div class="prog-fill" id="bot-cpu-bar" style="width:34%;background:#ff0040"></div></div></div>
              <div class="prog-item"><div class="prog-label"><span style="color:#555">Largura de Banda</span><span style="color:#ff6b00">28 Gbps</span></div><div class="prog-bar" style="background:#1a0500"><div class="prog-fill" style="width:58%;background:#ff6b00"></div></div></div>
              <div class="prog-item"><div class="prog-label"><span style="color:#555">Spam Enviado</span><span style="color:#7c3aed">142.000/h</span></div><div class="prog-bar" style="background:#0d001a"><div class="prog-fill" style="width:72%;background:#7c3aed"></div></div></div>
            </div>
          </div>
        </div>
      </div>

      <!-- ── HACK: FERRAMENTAS ── -->
      <div class="page" id="page-hack-tools">
        <div class="section-title" style="color:#ff0040">🔧 Ferramentas de Invasão</div>
        <div class="section-sub">Arsenal de ferramentas ofensivas disponíveis</div>
        <div class="grid-2">
          <div>
            <div class="hack-panel" style="margin-bottom:10px">
              <div style="font-size:13px;color:#ff6b6b;font-weight:600;margin-bottom:14px">🔑 Quebra de Senhas</div>
              <div class="hack-action" onclick="toolAction('bruteforce')">
                <span class="ha-icon">💥</span>
                <div class="ha-info"><h4>Brute Force SSH</h4><p>Dicionário: 14M palavras · rockyou.txt</p></div>
                <span class="ha-badge live">RODANDO</span>
              </div>
              <div class="hack-action" onclick="toolAction('hashcat')">
                <span class="ha-icon">🔓</span>
                <div class="ha-info"><h4>Hashcat GPU</h4><p>Quebrar hashes MD5/SHA/NTLM</p></div>
                <span class="ha-badge ready">PRONTO</span>
              </div>
              <div class="hack-action" onclick="toolAction('hydra')">
                <span class="ha-icon">🐍</span>
                <div class="ha-info"><h4>Hydra — Ataque em Paralelo</h4><p>SSH, FTP, HTTP, RDP, MySQL</p></div>
                <span class="ha-badge idle2">IDLE</span>
              </div>
            </div>
            <div class="hack-panel">
              <div style="font-size:13px;color:#ff6b6b;font-weight:600;margin-bottom:14px">🕵️ Exploits & Vulnerabilidades</div>
              <div class="hack-action" onclick="toolAction('metasploit')">
                <span class="ha-icon">🎯</span>
                <div class="ha-info"><h4>Metasploit Framework</h4><p>2.847 exploits disponíveis</p></div>
                <span class="ha-badge live">LIVE</span>
              </div>
              <div class="hack-action" onclick="toolAction('nmap')">
                <span class="ha-icon">📡</span>
                <div class="ha-info"><h4>Nmap — Port Scanner</h4><p>Varredura furtiva SYN scan</p></div>
                <span class="ha-badge ready">PRONTO</span>
              </div>
              <div class="hack-action" onclick="toolAction('sqlmap')">
                <span class="ha-icon">💉</span>
                <div class="ha-info"><h4>SQLMap — Injeção SQL</h4><p>Detectar e explorar SQLi automaticamente</p></div>
                <span class="ha-badge ready">PRONTO</span>
              </div>
            </div>
          </div>
          <div>
            <div class="hack-panel" style="margin-bottom:10px">
              <div style="font-size:13px;color:#ff6b6b;font-weight:600;margin-bottom:14px">📡 Interceptação</div>
              <div class="hack-action" onclick="toolAction('wireshark')">
                <span class="ha-icon">🌊</span>
                <div class="ha-info"><h4>Wireshark — Sniffer</h4><p>Capturando pacotes na rede local</p></div>
                <span class="ha-badge live">CAPTURANDO</span>
              </div>
              <div class="hack-action" onclick="toolAction('mitm')">
                <span class="ha-icon">👤</span>
                <div class="ha-info"><h4>Man-in-the-Middle</h4><p>Interceptar tráfego SSL/HTTP</p></div>
                <span class="ha-badge live">ATIVO</span>
              </div>
              <div class="hack-action" onclick="toolAction('phishing')">
                <span class="ha-icon">🎣</span>
                <div class="ha-info"><h4>Phishing Kit</h4><p>Páginas falsas de login prontas</p></div>
                <span class="ha-badge ready">PRONTO</span>
              </div>
            </div>
            <div class="hack-panel">
              <div style="font-size:13px;color:#ff6b6b;font-weight:600;margin-bottom:12px">📈 Status das Operações</div>
              <div class="scan-item"><span class="scan-ip">brute_force_ssh.py</span><span class="scan-port">PID 4421</span><span class="scan-result badge red">Rodando</span></div>
              <div class="scan-item"><span class="scan-ip">wireshark_cap.pcap</span><span class="scan-port">2.1 GB</span><span class="scan-result badge red">Gravando</span></div>
              <div class="scan-item"><span class="scan-ip">mitm_proxy.log</span><span class="scan-port">847 req</span><span class="scan-result badge red">Ativo</span></div>
              <div class="scan-item"><span class="scan-ip">metasploit_session3</span><span class="scan-port">Shell</span><span class="scan-result badge green">Aberto</span></div>
              <div class="scan-item"><span class="scan-ip">crypto_miner.bin</span><span class="scan-port">312 hosts</span><span class="scan-result badge red">Minando</span></div>
            </div>
          </div>
        </div>
      </div>

      <!-- ── HACK: TERMINAL ── -->
      <div class="page" id="page-hack-terminal">
        <div class="section-title" style="color:#ff0040">💻 Terminal de Controle Remoto</div>
        <div class="section-sub">Acesso shell direto aos alvos comprometidos</div>
        <div style="display:flex;gap:8px;margin-bottom:12px;flex-wrap:wrap">
          <button class="btn-sm" style="background:#0a0508;border:1px solid #ff0040;color:#ff6b6b;font-size:11px" onclick="setHackTarget('carlos')">💻 Carlos (192.168.4.12)</button>
          <button class="btn-sm" style="background:#0a0508;border:1px solid #333;color:#555;font-size:11px" onclick="setHackTarget('fernanda')">🖥️ Fernanda (10.0.1.44)</button>
          <button class="btn-sm" style="background:#0a0508;border:1px solid #333;color:#555;font-size:11px" onclick="setHackTarget('roberto')">💻 Roberto (172.20.3.87)</button>
          <button class="btn-sm red" style="font-size:11px;margin-left:auto" onclick="clearHackTerminal()">🗑️ Limpar</button>
        </div>
        <div class="hack-terminal" style="min-height:420px;display:flex;flex-direction:column">
          <div id="hack-terminal-output" style="flex:1;max-height:360px;overflow-y:auto;color:#00ff41;line-height:1.9">
            <div class="ht-line gray">SecureOS Remote Shell v2.4 · Conexão criptografada AES-256</div>
            <div class="ht-line">Conectando a DESKTOP-K7J2X (192.168.4.12)...</div>
            <div class="ht-line">Autenticando com implante instalado...</div>
            <div class="ht-line" style="color:#00ff41">Conexão estabelecida. Shell aberto.</div>
            <div class="ht-line gray">─────────────────────────────────────</div>
            <div class="ht-line"><span style="color:#ff6b6b">root@DESKTOP-K7J2X</span>:<span style="color:#7c7cff">~#</span> whoami</div>
            <div class="ht-line">root</div>
            <div class="ht-line"><span style="color:#ff6b6b">root@DESKTOP-K7J2X</span>:<span style="color:#7c7cff">~#</span> ls /home/carlos/Documents/</div>
            <div class="ht-line">relatorio_q4.xlsx &nbsp; senhas_banco.txt &nbsp; contrato_empresa.pdf &nbsp; fotos_pessoais/</div>
            <div class="ht-line"><span style="color:#ff6b6b">root@DESKTOP-K7J2X</span>:<span style="color:#7c7cff">~#</span> cat /home/carlos/Documents/senhas_banco.txt</div>
            <div class="ht-line yellow">Banco do Brasil: carlos.mendes · Senha: CaM@2024#01</div>
            <div class="ht-line yellow">Itaú: 02145-7 · Agência: 0021 · Senha: men4102!</div>
            <div class="ht-line yellow">NuBank: (11)99234-5678 · PIN: 4421</div>
          </div>
          <div style="display:flex;gap:8px;margin-top:12px;align-items:center;border-top:1px solid rgba(0,255,65,.1);padding-top:10px">
            <span style="font-size:12px;font-family:monospace;color:#ff6b6b;white-space:nowrap">root@DESKTOP-K7J2X:~#</span>
            <input id="hack-cmd-input" onkeydown="handleHackCmd(event)"
              style="flex:1;background:transparent;border:none;color:#00ff41;font-size:12px;font-family:monospace;outline:none"
              placeholder="Digite um comando remoto...">
            <div class="ht-cursor"></div>
          </div>
        </div>
      </div>

      <!-- ── HACK: SCANNER ── -->
      <div class="page" id="page-hack-scan">
        <div class="section-title" style="color:#ff0040">📡 Scanner de Rede</div>
        <div class="section-sub">Varredura automática de vulnerabilidades na rede</div>
        <div class="grid-2" style="margin-bottom:14px">
          <div class="hack-panel">
            <div style="font-size:12px;color:#ff6b6b;font-weight:600;margin-bottom:12px">Configurar Scan</div>
            <div class="form-group" style="margin-bottom:10px">
              <label style="font-size:11px;color:#555;margin-bottom:4px;display:block">RANGE DE IP</label>
              <input id="scan-range" value="192.168.0.0/24" style="width:100%;background:#050505;border:1px solid rgba(255,0,64,.2);border-radius:6px;padding:8px 12px;color:#ff6b6b;font-family:monospace;font-size:13px;outline:none">
            </div>
            <div style="display:flex;gap:8px;flex-wrap:wrap;margin-bottom:12px">
              <label style="display:flex;align-items:center;gap:6px;font-size:12px;color:#555;cursor:pointer"><input type="checkbox" checked style="accent-color:#ff0040"> Port Scan</label>
              <label style="display:flex;align-items:center;gap:6px;font-size:12px;color:#555;cursor:pointer"><input type="checkbox" checked style="accent-color:#ff0040"> OS Detection</label>
              <label style="display:flex;align-items:center;gap:6px;font-size:12px;color:#555;cursor:pointer"><input type="checkbox" checked style="accent-color:#ff0040"> Vuln Check</label>
              <label style="display:flex;align-items:center;gap:6px;font-size:12px;color:#555;cursor:pointer"><input type="checkbox" style="accent-color:#ff0040"> Stealth Mode</label>
            </div>
            <button class="btn-sm" style="background:#ff0040;color:#fff;width:100%" onclick="startScan()">🚀 Iniciar Scan</button>
            <div style="margin-top:10px">
              <div style="display:flex;justify-content:space-between;font-size:11px;color:#555;margin-bottom:4px">
                <span>Progresso</span><span id="scan-pct">100%</span>
              </div>
              <div class="fake-prog"><div class="fake-prog-fill" id="scan-bar" style="width:100%"></div></div>
            </div>
          </div>
          <div class="hack-panel">
            <div style="font-size:12px;color:#ff6b6b;font-weight:600;margin-bottom:10px">📊 Resumo do Último Scan</div>
            <div style="display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:12px">
              <div style="text-align:center"><div style="font-size:22px;font-weight:800;color:#ff0040;font-family:monospace">247</div><div style="font-size:10px;color:#555">Hosts encontrados</div></div>
              <div style="text-align:center"><div style="font-size:22px;font-weight:800;color:#ff6b00;font-family:monospace">89</div><div style="font-size:10px;color:#555">Vulneráveis</div></div>
              <div style="text-align:center"><div style="font-size:22px;font-weight:800;color:#7c3aed;font-family:monospace">4.312</div><div style="font-size:10px;color:#555">Portas abertas</div></div>
              <div style="text-align:center"><div style="font-size:22px;font-weight:800;color:#00ff41;font-family:monospace">23</div><div style="font-size:10px;color:#555">Exploráveis</div></div>
            </div>
          </div>
        </div>
        <div class="hack-panel">
          <div style="font-size:12px;color:#ff6b6b;font-weight:600;margin-bottom:10px">Resultados — Hosts Vulneráveis</div>
          <div id="scan-results">
            <div class="scan-item"><span class="scan-ip">192.168.0.14</span><span class="scan-port">22,80,443</span><span style="color:#555;font-size:11px">Windows 10</span><span class="scan-result badge red">CVE-2021-34527</span></div>
            <div class="scan-item"><span class="scan-ip">192.168.0.22</span><span class="scan-port">3389,445</span><span style="color:#555;font-size:11px">Windows Server</span><span class="scan-result badge red">EternalBlue</span></div>
            <div class="scan-item"><span class="scan-ip">10.0.1.44</span><span class="scan-port">22,8080</span><span style="color:#555;font-size:11px">macOS 13.2</span><span class="scan-result badge yellow">SSH Weak Key</span></div>
            <div class="scan-item"><span class="scan-ip">172.20.3.87</span><span class="scan-port">80,3306</span><span style="color:#555;font-size:11px">Ubuntu 20.04</span><span class="scan-result badge red">MySQL Open</span></div>
            <div class="scan-item"><span class="scan-ip">192.168.1.201</span><span class="scan-port">8443</span><span style="color:#555;font-size:11px">Android 13</span><span class="scan-result badge yellow">SSL v3</span></div>
            <div class="scan-item"><span class="scan-ip">10.10.2.55</span><span class="scan-port">22,5432</span><span style="color:#555;font-size:11px">Ubuntu 22.04</span><span class="scan-result badge red">Postgres Open</span></div>
          </div>
        </div>
      </div>

    </div><!-- /content -->
  </div><!-- /main -->
</div><!-- /app -->

<script>
// ── STATE ──
let currentUser = null;
let users = [
  {id:1, name:'Admin System', email:'admin@secureos.com', role:'Super Admin', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:2, name:'Maria Silva', email:'maria.silva@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 3min', mfa:true},
  {id:3, name:'João Tech', email:'joao.tech@empresa.com', role:'Moderador', status:'Ativo', lastAccess:'Há 5min', mfa:false},
  {id:4, name:'Pedro Ops', email:'pedro.ops@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 7min', mfa:true},
  {id:5, name:'Carlos Mendes', email:'carlos.mendes@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 2min', mfa:true},
  {id:6, name:'Fernanda Ops', email:'fernanda.ops@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:7, name:'Roberto Silva', email:'roberto.silva@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 1min', mfa:false},
  {id:8, name:'Juliana Adm', email:'juliana.adm@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:9, name:'Lucas TI', email:'lucas.ti@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 4min', mfa:true},
  {id:10, name:'Ana Paula RH', email:'ana.paula@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 6min', mfa:true},
  {id:11, name:'Bruno Dev', email:'bruno.dev@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 8min', mfa:false},
  {id:12, name:'Camila Souza', email:'camila.souza@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:13, name:'Diego Ramos', email:'diego.ramos@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 1min', mfa:true},
  {id:14, name:'Elisa Costa', email:'elisa.costa@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 3min', mfa:true},
  {id:15, name:'Fábio Lima', email:'fabio.lima@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 2min', mfa:false},
  {id:16, name:'Giovana Melo', email:'giovana.melo@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:17, name:'Henrique Dias', email:'henrique.dias@empresa.com', role:'Administrador', status:'Inativo', lastAccess:'Há 1h', mfa:true},
  {id:18, name:'Isabela Nunes', email:'isabela.nunes@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 5min', mfa:true},
  {id:19, name:'Jorge Batista', email:'jorge.batista@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 9min', mfa:true},
  {id:20, name:'Karla Freitas', email:'karla.freitas@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:false},
  {id:21, name:'Leonardo Pinto', email:'leonardo.pinto@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 2min', mfa:true},
  {id:22, name:'Mariana Torres', email:'mariana.torres@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 4min', mfa:true},
  {id:23, name:'Nicolás Vera', email:'nicolas.vera@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 6min', mfa:true},
  {id:24, name:'Olivia Martins', email:'olivia.martins@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:25, name:'Paulo Rodrigues', email:'paulo.rodrigues@empresa.com', role:'Administrador', status:'Inativo', lastAccess:'Há 2h', mfa:false},
  {id:26, name:'Queila Santos', email:'queila.santos@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 1min', mfa:true},
  {id:27, name:'Rafael Cunha', email:'rafael.cunha@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 3min', mfa:true},
  {id:28, name:'Sabrina Alves', email:'sabrina.alves@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:29, name:'Tiago Moreira', email:'tiago.moreira@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 7min', mfa:false},
  {id:30, name:'Ursula Campos', email:'ursula.campos@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 2min', mfa:true},
  {id:31, name:'Vinicius Rocha', email:'vinicius.rocha@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 4min', mfa:true},
  {id:32, name:'Wendy Carvalho', email:'wendy.carvalho@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:33, name:'Xavier Lima', email:'xavier.lima@empresa.com', role:'Moderador', status:'Ativo', lastAccess:'Há 5min', mfa:true},
  {id:34, name:'Yasmin Ferreira', email:'yasmin.ferreira@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 1min', mfa:false},
  {id:35, name:'Zara Oliveira', email:'zara.oliveira@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:36, name:'Alexandre Castro', email:'alexandre.castro@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 3min', mfa:true},
  {id:37, name:'Beatriz Lemos', email:'beatriz.lemos@empresa.com', role:'Administrador', status:'Inativo', lastAccess:'Há 3h', mfa:true},
  {id:38, name:'Caio Andrade', email:'caio.andrade@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 2min', mfa:true},
  {id:39, name:'Danubia Porto', email:'danubia.porto@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:false},
  {id:40, name:'Eduardo Braga', email:'eduardo.braga@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 6min', mfa:true},
  {id:41, name:'Flávia Dantas', email:'flavia.dantas@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 1min', mfa:true},
  {id:42, name:'Gustavo Teixeira', email:'gustavo.teixeira@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:43, name:'Helena Barros', email:'helena.barros@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 4min', mfa:false},
  {id:44, name:'Iago Fernandes', email:'iago.fernandes@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 2min', mfa:true},
  {id:45, name:'Juliana Siqueira', email:'juliana.siqueira@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 8min', mfa:true},
  {id:46, name:'Kevin Gomes', email:'kevin.gomes@empresa.com', role:'Administrador', status:'Inativo', lastAccess:'Ontem', mfa:true},
  {id:47, name:'Larissa Fonseca', email:'larissa.fonseca@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:48, name:'Mateus Correia', email:'mateus.correia@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 3min', mfa:false},
  {id:49, name:'Nayara Machado', email:'nayara.machado@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 5min', mfa:true},
  {id:50, name:'Otávio Guimarães', email:'otavio.guimaraes@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 1min', mfa:true},
  {id:51, name:'Patrícia Viana', email:'patricia.viana@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:52, name:'Quincy Araújo', email:'quincy.araujo@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 2min', mfa:false},
  {id:53, name:'Renata Paiva', email:'renata.paiva@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 7min', mfa:true},
  {id:54, name:'Sandro Monteiro', email:'sandro.monteiro@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 4min', mfa:true},
  {id:55, name:'Tatiane Ribeiro', email:'tatiane.ribeiro@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:56, name:'Ulisses Cardoso', email:'ulisses.cardoso@empresa.com', role:'Administrador', status:'Inativo', lastAccess:'Há 4h', mfa:false},
  {id:57, name:'Vanessa Cavalcanti', email:'vanessa.cavalcanti@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 1min', mfa:true},
  {id:58, name:'Willian Nascimento', email:'willian.nascimento@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 3min', mfa:true},
  {id:59, name:'Xênia Azevedo', email:'xenia.azevedo@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Agora', mfa:true},
  {id:60, name:'Yara Nogueira', email:'yara.nogueira@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 2min', mfa:false},
  {id:61, name:'Zeno Carvalho', email:'zeno.carvalho@empresa.com', role:'Administrador', status:'Ativo', lastAccess:'Há 6min', mfa:true},
  {id:62, name:'Alice Braga', email:'alice.braga@empresa.com', role:'Usuário', status:'Ativo', lastAccess:'Há 5min', mfa:true},
  {id:63, name:'Bernardo Cruz', email:'bernardo.cruz@empresa.com', role:'Usuário', status:'Ativo', lastAccess:'Agora', mfa:false},
  {id:64, name:'Cecília Duarte', email:'cecilia.duarte@empresa.com', role:'Usuário', status:'Ativo', lastAccess:'Há 1min', mfa:true},
  {id:65, name:'Davi Sousa', email:'davi.sousa@empresa.com', role:'Usuário', status:'Ativo', lastAccess:'Há 4min', mfa:true},
  {id:66, name:'Esther Vieira', email:'esther.vieira@empresa.com', role:'Usuário', status:'Inativo', lastAccess:'Há 2h', mfa:true},
  {id:67, name:'Flávio Teles', email:'flavio.teles@empresa.com', role:'Usuário', status:'Ativo', lastAccess:'Agora', mfa:false},
  {id:68, name:'Graça Mesquita', email:'graca.mesquita@empresa.com', role:'Usuário', status:'Ativo', lastAccess:'Há 3min', mfa:true},
  {id:69, name:'Hugo Pacheco', email:'hugo.pacheco@empresa.com', role:'Usuário', status:'Ativo', lastAccess:'Há 7min', mfa:true},
  {id:70, name:'Ingrid Leal', email:'ingrid.leal@empresa.com', role:'Usuário', status:'Ativo', lastAccess:'Há 2min', mfa:true},
];
let logData = [];
let vpnConnected = true;

// ── LOADING ──
setTimeout(() => {
  document.getElementById('loading').style.opacity = '0';
  document.getElementById('loading').style.transition = 'opacity .5s';
  setTimeout(() => document.getElementById('loading').style.display = 'none', 500);
}, 1800);

// ── AUTH ──
function switchAuthTab(tab) {
  document.querySelectorAll('.auth-tab').forEach((t,i) => t.classList.toggle('active', (tab==='login'&&i===0)||(tab==='register'&&i===1)));
  document.getElementById('login-form').style.display = tab==='login' ? 'block' : 'none';
  document.getElementById('register-form').style.display = tab==='register' ? 'block' : 'none';
  document.getElementById('auth-error').style.display = 'none';
}

function togglePass(id, btn) {
  const inp = document.getElementById(id);
  inp.type = inp.type === 'password' ? 'text' : 'password';
  btn.textContent = inp.type === 'password' ? '👁️' : '🙈';
}


function showError(msg) {
  const el = document.getElementById('auth-error');
  el.textContent = msg;
  el.style.display = 'block';
}

function doLogin() {
  const user = document.getElementById('login-user').value.trim();
  const pass = document.getElementById('login-pass').value;
  if (!user || !pass) { showError('Preencha todos os campos.'); return; }
  currentUser = { name: user.split('@')[0].replace('.',' ').replace(/\b\w/g,c=>c.toUpperCase()), email: user };
  loginSuccess();
}

function otpNext(inp, idx) {
  if (inp.value.length === 1) {
    const inputs = document.querySelectorAll('.otp-inputs input');
    if (idx < 5) inputs[idx+1].focus();
  }
}

function verifyMFA() {
  const inputs = document.querySelectorAll('.otp-inputs input');
  const code = Array.from(inputs).map(i=>i.value).join('');
  if (code === '123456') {
    document.getElementById('mfa-modal').classList.remove('open');
    loginSuccess();
  } else {
    inputs.forEach(i => { i.style.borderColor='var(--danger)'; i.value=''; });
    inputs[0].focus();
    setTimeout(() => inputs.forEach(i => i.style.borderColor=''), 1000);
  }
}

function loginSuccess() {
  document.getElementById('auth-screen').style.display = 'none';
  document.getElementById('app').classList.add('active');
  document.getElementById('user-name-display').textContent = currentUser.name;
  document.getElementById('user-avatar').textContent = currentUser.name[0].toUpperCase();
  renderUsersTable();
  startRealtime();
  startLogs();
  renderCharts();
}

function doRegister() {
  const name = document.getElementById('reg-name').value.trim();
  const email = document.getElementById('reg-email').value.trim();
  const pass = document.getElementById('reg-pass').value;
  const pass2 = document.getElementById('reg-pass2').value;
  if (!name||!email||!pass||!pass2) { showError('Preencha todos os campos.'); return; }
  if (pass !== pass2) { showError('As senhas não coincidem.'); return; }
  if (pass.length < 8) { showError('Senha muito curta (mínimo 8 caracteres).'); return; }
  users.push({id: users.length+1, name, email, role:'Usuário', status:'Ativo', lastAccess:'Agora', mfa: document.getElementById('reg-mfa').checked});
  alert('✅ Conta criada com sucesso! Faça login.');
  switchAuthTab('login');
}

function doLogout() {
  if (!confirm('Tem certeza que deseja sair?')) return;
  document.getElementById('app').classList.remove('active');
  document.getElementById('auth-screen').style.display = 'flex';
  document.querySelectorAll('.otp-inputs input').forEach(i => i.value='');
}

function checkStrength(inp) {
  const v = inp.value;
  let score = 0;
  if (v.length >= 8) score++;
  if (v.length >= 12) score++;
  if (/[A-Z]/.test(v) && /[a-z]/.test(v)) score++;
  if (/\d/.test(v)) score++;
  if (/[^A-Za-z0-9]/.test(v)) score++;
  const fill = document.getElementById('strength-fill');
  const label = document.getElementById('strength-label');
  const colors = ['','#ef4444','#f59e0b','#f59e0b','#10b981','#10b981'];
  const labels = ['','Muito fraca','Fraca','Razoável','Forte','Muito forte'];
  fill.style.width = (score*20)+'%';
  fill.style.background = colors[score]||'#ef4444';
  label.textContent = labels[score]||'Muito fraca';
  label.style.color = colors[score]||'#ef4444';
}

// ── NAVIGATION ──
function showPage(id, el) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
  const page = document.getElementById('page-'+id);
  if (page) page.classList.add('active');
  if (el) el.classList.add('active');
  const titles = {'hack-targets':'Alvos Infectados','hack-screen':'Visualizar Tela Remota','hack-botnet':'Rede de Bots','hack-tools':'Ferramentas de Invasão','hack-terminal':'Terminal Remoto','hack-scan':'Scanner de Rede',dashboard:'Dashboard',users:'Usuários & Acesso',roles:'Perfis & Permissões',sessions:'Sessões Ativas','access-log':'Histórico de Acessos','mfa-config':'MFA','encryption':'Criptografia',passwords:'Senhas',threats:'Detecção de Ameaças',iplist:'IPs Permitidos/Bloqueados',firewall:'Firewall',vpn:'VPN',network:'Rede & Conectividade',monitoring:'Monitoramento',logs:'Logs em Tempo Real',audit:'Auditoria',data:'Dados & Backup',automation:'Automação','notifications-cfg':'Notificações',reports:'Relatórios',tools:'Ferramentas Avançadas',compliance:'Conformidade',settings:'Configurações',support:'Suporte'};
  document.getElementById('page-title').textContent = titles[id]||id;
  if (id==='logs') startLogs(true);
  if (id && id.startsWith('hack-')) {
    setTimeout(startMatrix, 50);
    startKeylogTicker();
  }
}

function toggleSub(id, el) {
  const sub = document.getElementById(id);
  sub.classList.toggle('open');
  el.classList.toggle('open');
}

function toggleSidebar() {
  document.getElementById('sidebar').classList.toggle('collapsed');
}

function toggleNotif() {
  document.getElementById('notif-panel').classList.toggle('open');
}

// ── USERS TABLE ──
function renderUsersTable() {
  const tb = document.getElementById('users-tbody');
  if (!tb) return;
  tb.innerHTML = users.map(u => `
    <tr>
      <td>${u.id}</td>
      <td>${u.name}</td>
      <td>${u.email}</td>
      <td><span class="badge ${u.role==='Super Admin'?'red':u.role==='Administrador'?'yellow':u.role==='Moderador'?'blue':'gray'}">${u.role}</span></td>
      <td><span class="badge ${u.status==='Ativo'?'green':'gray'}">● ${u.status}</span></td>
      <td>${u.lastAccess}</td>
      <td>${u.mfa ? '<span class="badge green">✅ ON</span>' : '<span class="badge red">❌ OFF</span>'}</td>
      <td><button class="btn-sm outline" style="padding:3px 8px;font-size:11px">✏️</button> <button class="btn-sm red" style="padding:3px 8px;font-size:11px" onclick="deleteUser(${u.id})">🗑️</button></td>
    </tr>
  `).join('');
}

function addUser() {
  const n = document.getElementById('new-user-name').value.trim();
  const e = document.getElementById('new-user-email').value.trim();
  if (!n||!e) return alert('Preencha nome e email.');
  users.push({id:users.length+1,name:n,email:e,role:'Usuário',status:'Ativo',lastAccess:'Agora',mfa:false});
  renderUsersTable();
  document.getElementById('new-user-name').value='';
  document.getElementById('new-user-email').value='';
}

function deleteUser(id) {
  if (!confirm('Remover usuário?')) return;
  users = users.filter(u => u.id !== id);
  renderUsersTable();
}

// ── VPN ──
function toggleVPN() {
  vpnConnected = !vpnConnected;
  const globe = document.getElementById('vpn-globe');
  const name = document.getElementById('vpn-name');
  const ip = document.getElementById('vpn-ip');
  const btn = document.getElementById('vpn-btn');
  if (vpnConnected) {
    globe.classList.remove('off'); globe.textContent='🌐';
    name.textContent='🟢 Conectado — São Paulo, BR';
    ip.textContent='IP Real: 192.168.1.10 → IP VPN: 10.0.0.45 | Protocolo: WireGuard';
    btn.className='btn-vpn disconnect'; btn.textContent='⏹️ Desconectar VPN';
    document.querySelector('.nav-badge.green').textContent='ON';
  } else {
    globe.classList.add('off'); globe.textContent='🔴';
    name.textContent='🔴 Desconectado';
    ip.textContent='Sua conexão NÃO está protegida por VPN';
    btn.className='btn-vpn connect'; btn.textContent='▶️ Conectar VPN';
    document.querySelector('.nav-badge.green').textContent='OFF';
  }
}

// ── IP LIST ──
function addIP(type) {
  const input = document.getElementById(type==='allow'?'allow-ip':'block-ip');
  const val = input.value.trim();
  if (!val) return;
  const container = document.getElementById(type==='allow'?'allowed-ips':'blocked-ips');
  const el = document.createElement('div');
  el.className = 'ip-item';
  el.innerHTML = `<span class="ip-flag">🌐</span><span class="ip-addr">${val}</span><span class="badge ${type==='allow'?'green':'red'}">Manual</span><button class="btn-sm ${type==='allow'?'red':'outline'}" style="padding:3px 8px;font-size:11px;margin-left:auto" onclick="this.parentElement.remove()">✕</button>`;
  container.appendChild(el);
  input.value='';
}

// ── CHARTS ──
function buildPath(points, close=false) {
  let d = '';
  points.forEach((p,i) => d += (i===0?'M':'L')+p[0]+' '+p[1]);
  if (close) d += 'L'+points[points.length-1][0]+' 120 L'+points[0][0]+' 120 Z';
  return d;
}

function randomChartData(n, min, max) {
  const pts = [];
  let v = (min+max)/2;
  for (let i=0;i<n;i++) {
    v = Math.max(min, Math.min(max, v + (Math.random()-0.5)*15));
    pts.push([i*(400/(n-1)), 120-((v-min)/(max-min))*110]);
  }
  return pts;
}

function renderCharts() {
  const pts = randomChartData(24, 10, 90);
  document.getElementById('chart-line').setAttribute('d', buildPath(pts));
  document.getElementById('chart-area').setAttribute('d', buildPath(pts, true));
  const pts2 = randomChartData(30, 20, 95);
  if (document.getElementById('mon-line')) {
    document.getElementById('mon-line').setAttribute('d', buildPath(pts2));
    document.getElementById('mon-area').setAttribute('d', buildPath(pts2, true));
  }
}

// ── REALTIME ──
function startRealtime() {
  setInterval(() => {
    const now = new Date();
    const ts = now.toLocaleTimeString('pt-BR');
    const rtTime = document.getElementById('rt-time');
    if (rtTime) rtTime.textContent = ts;
    const monTs = document.getElementById('monitor-timestamp');
    if (monTs) monTs.textContent = ts;

    const cpu = Math.floor(50+Math.random()*40);
    const ram = Math.floor(40+Math.random()*30);
    const temp = Math.floor(45+Math.random()*20);
    const proc = Math.floor(130+Math.random()*30);
    const conn = Math.floor(30+Math.random()*20);

    setEl('cpu-val', cpu+'%'); setEl('ram-val', ram+'%');
    setEl('mon-cpu', cpu+'%'); setEl('mon-ram', ram+'%');
    setEl('mon-temp', temp+'°C'); setEl('mon-proc', proc); setEl('mon-conn', conn);
    setBar('cpu-bar', cpu, cpu>80?'var(--danger)':cpu>60?'var(--warning)':'var(--accent3)');
    setBar('ram-bar', ram, ram>80?'var(--danger)':'var(--accent)');
    setEl('rt-events', Math.floor(10+Math.random()*50)+' eventos/min');

    renderCharts();
  }, 2000);
}

function setEl(id, val) { const e=document.getElementById(id); if(e) e.textContent=val; }
function setBar(id, val, color) { const e=document.getElementById(id); if(e){e.style.width=val+'%';e.style.background=color;} }

// ── LOGS ──
const logTypes = [
  {level:'info', msgs:['Conexão TCP estabelecida de 192.168.1.55:45231','Usuário maria.silva fez login com sucesso','Verificação SSL concluída em api.secureos.com','Backup incremental iniciado','Regra de firewall #3 avaliada: ALLOW']},
  {level:'warn', msgs:['CPU acima de 75% por 3 minutos','Tentativa de acesso fora do horário comercial','Certificado expira em 68 dias','Sessão sem atividade há 55 minutos','Requisição lenta: 2.3s em /api/reports']},
  {level:'error', msgs:['Falha de autenticação — IP 203.45.12.8','Erro de conexão com banco de dados: timeout','Limite de tentativas atingido para user@test.com','Arquivo de log corrompido detectado','Certificado inválido rejeitado: expired.host.com']},
  {level:'success', msgs:['Backup concluído — 14.2 GB sem erros','IP 203.45.12.8 bloqueado automaticamente','SSL renovado com sucesso — 365 dias','Sessão encerrada normalmente: pedro.ops','Scan de segurança finalizado: 0 vulnerabilidades']},
];

function startLogs(force=false) {
  const container = document.getElementById('log-container');
  if (!container) return;
  if (force) container.innerHTML = '';
  const pushLog = () => {
    const now = new Date().toLocaleTimeString('pt-BR');
    const type = logTypes[Math.floor(Math.random()*logTypes.length)];
    const msg = type.msgs[Math.floor(Math.random()*type.msgs.length)];
    const line = document.createElement('div');
    line.className = 'log-line';
    line.dataset.level = type.level;
    line.innerHTML = `<span class="log-time">[${now}]</span><span class="log-level ${type.level}">${type.level.toUpperCase().padEnd(7,' ')}</span><span class="log-msg">${msg}</span>`;
    container.appendChild(line);
    if (container.children.length > 80) container.removeChild(container.firstChild);
    container.scrollTop = container.scrollHeight;
    logData.push({level:type.level, time:now, msg});
  };
  setInterval(pushLog, 1200);
}

function filterLog(level) {
  const container = document.getElementById('log-container');
  if (!container) return;
  Array.from(container.children).forEach(line => {
    line.style.display = (level==='all' || line.dataset.level===level) ? '' : 'none';
  });
}

function clearLogs() {
  const container = document.getElementById('log-container');
  if (container) container.innerHTML = '';
}

// ── CONSOLE ──
const cmds = {
  help: () => 'Comandos: status, ping, users, threats, vpn, backup, clear, uptime',
  status: () => '✅ Sistema: ONLINE | CPU: '+Math.floor(50+Math.random()*30)+'% | RAM: '+Math.floor(40+Math.random()*30)+'% | Uptime: 99.98%',
  ping: () => 'PING secureos.com (10.0.0.1): 64 bytes, tempo='+Math.floor(5+Math.random()*15)+'ms',
  users: () => 'Usuários ativos: '+users.filter(u=>u.status==='Ativo').length+'/'+users.length,
  threats: () => '🛡️ Ameaças bloqueadas hoje: 247 | Críticas: 3 | Médias: 12',
  vpn: () => '🌐 VPN: '+(vpnConnected?'CONECTADO — São Paulo':'DESCONECTADO')+' | Protocolo: WireGuard',
  backup: () => '🔄 Último backup: 05/04 02:00 — 14.2 GB — ✅ Sucesso',
  uptime: () => 'Sistema iniciado há 3 dias, 5 horas, 42 minutos | Uptime: 99.98%',
  clear: () => { document.getElementById('console-output').innerHTML=''; return null; },
};

function handleConsole(e) {
  if (e.key !== 'Enter') return;
  const input = document.getElementById('console-input');
  const output = document.getElementById('console-output');
  const cmd = input.value.trim().toLowerCase();
  if (!cmd) return;
  const cmdLine = document.createElement('div');
  cmdLine.innerHTML = `<span style="color:#00d4ff">admin@secureos:~$</span> <span style="color:#e2e8f0">${cmd}</span>`;
  output.appendChild(cmdLine);
  const fn = cmds[cmd];
  const result = fn ? fn() : `Comando '${cmd}' não encontrado. Digite 'help'.`;
  if (result !== null) {
    const res = document.createElement('div');
    res.style.color = fn ? '#10b981' : '#ef4444';
    res.textContent = result || '';
    output.appendChild(res);
  }
  output.scrollTop = output.scrollHeight;
  input.value = '';
}

function runDiag() {
  const output = document.getElementById('console-output');
  const lines = ['🔍 Iniciando diagnóstico do sistema...','✅ Integridade do banco de dados: OK','✅ Certificados SSL: 2/3 válidos','⚠️  Uso de disco de backup: 86% (atenção!)','✅ Regras de firewall: 6 ativas','✅ Serviços de monitoramento: ONLINE','✅ VPN: CONECTADA','✅ Diagnóstico concluído — 1 aviso encontrado'];
  let i = 0;
  const interval = setInterval(() => {
    if (i >= lines.length) { clearInterval(interval); return; }
    const el = document.createElement('div');
    el.style.color = lines[i].startsWith('⚠️') ? '#f59e0b' : '#10b981';
    el.textContent = lines[i];
    output.appendChild(el);
    output.scrollTop = output.scrollHeight;
    i++;
  }, 300);
}


// ── HACKER MODULE JS ──

// Matrix canvas
function startMatrix() {
  const canvas = document.getElementById('matrix-canvas');
  if (!canvas) return;
  const ctx = canvas.getContext('2d');
  canvas.width = canvas.offsetWidth;
  canvas.height = canvas.offsetHeight;
  const cols = Math.floor(canvas.width / 14);
  const drops = Array(cols).fill(1);
  setInterval(() => {
    ctx.fillStyle = 'rgba(0,0,0,0.05)';
    ctx.fillRect(0,0,canvas.width,canvas.height);
    ctx.fillStyle = '#00ff41';
    ctx.font = '12px monospace';
    drops.forEach((y,i) => {
      const ch = String.fromCharCode(0x30A0 + Math.random()*96);
      ctx.fillText(ch, i*14, y*14);
      if (y*14 > canvas.height && Math.random() > 0.975) drops[i] = 0;
      drops[i]++;
    });
  }, 50);
}

function selectTarget(el, host, ip) {
  document.querySelectorAll('.target-card').forEach(c => c.classList.remove('selected'));
  el.classList.add('selected');
  document.getElementById('sel-host').textContent = host;
  document.getElementById('sel-ip').textContent = ip;
}

function hackAction(type) {
  const msgs = {
    keylog:'⌨️ Keylogger ativado — capturando teclas...',
    cam:'📷 Webcam acessada — stream iniciado...',
    files:'📂 Navegando arquivos remotos...',
    mic:'🎤 Microfone ativado — gravando áudio...',
    shutdown:'🔴 Comando de desligamento enviado!'
  };
  addHackLog(msgs[type] || 'Ação executada.');
}

function addHackLog(msg) {
  const el = document.getElementById('remote-action-log');
  if (!el) return;
  const t = new Date().toLocaleTimeString('pt-BR');
  const line = document.createElement('div');
  line.innerHTML = `<span style="color:#555">[${t}]</span> <span style="color:#00ff41">${msg}</span>`;
  el.appendChild(line);
  el.scrollTop = el.scrollHeight;
}

function remoteAction(type) {
  const msgs = {
    mouse:'🖱️ Controle de mouse assumido com sucesso.',
    keyboard:'⌨️ Teclado remoto ativado — aguardando entrada.',
    screenshot:'📸 Screenshot capturado e salvo.',
    clipboard:'📋 Clipboard: "Senha@2024 · carlos123 · transferencia_pix"',
    cam:'📷 Webcam ativada — stream oculto iniciado.',
    lock:'🔒 Tela travada remotamente!'
  };
  addHackLog(msgs[type] || 'Ação executada.');
}

function switchScreenTarget(name, ip) {
  document.querySelector('.sv-top span').textContent = name + ' — Área de Trabalho';
  document.getElementById('screen-fps').textContent = Math.floor(18+Math.random()*12)+' FPS';
}

function botCommand(type) {
  const msgs = {
    ddos:'💥 Ataque DDoS iniciado! 312 bots direcionados...',
    spam:'📧 Campanha de spam ativada — 142.000 emails/h',
    mine:'⛏️ Cryptominer em execução nos 312 hosts...',
    spread:'🦠 Payload de propagação enviado para a rede...',
    update:'🔄 Atualização do malware distribuída.'
  };
  alert(msgs[type]);
}

function toolAction(tool) {
  const msgs = {
    bruteforce:'💥 Brute Force rodando: 14.200 tentativas/seg',
    hashcat:'🔓 Hashcat iniciado com 4 GPUs...',
    hydra:'🐍 Hydra: atacando 5 serviços simultaneamente',
    metasploit:'🎯 Metasploit: sessão aberta em 192.168.4.12',
    nmap:'📡 Nmap: iniciando scan SYN furtivo...',
    sqlmap:'💉 SQLMap: testando 247 endpoints...',
    wireshark:'🌊 Wireshark: 1.240 pacotes/seg capturados',
    mitm:'👤 MITM: interceptando tráfego SSL...',
    phishing:'🎣 Kit de phishing ativado em domínio falso'
  };
  alert(msgs[tool]);
}

function startScan() {
  let pct = 0;
  const bar = document.getElementById('scan-bar');
  const label = document.getElementById('scan-pct');
  bar.style.width = '0%';
  label.textContent = '0%';
  const iv = setInterval(() => {
    pct += Math.floor(2+Math.random()*5);
    if (pct >= 100) { pct=100; clearInterval(iv); }
    bar.style.width = pct+'%';
    label.textContent = pct+'%';
  }, 120);
}

// Terminal hacker
const hackCmds = {
  whoami: () => 'root',
  ls: () => 'Desktop  Documents  Downloads  senhas.txt  relatorio_q4.xlsx',
  pwd: () => '/home/carlos',
  id: () => 'uid=0(root) gid=0(root) grupos=0(root)',
  ifconfig: () => 'eth0: 192.168.4.12  inet6: ::1  ether: A4:CF:12:89:00:5F',
  ps: () => `PID 4421 backdoor.exe\nPID 4422 keylogger.dll\nPID 4423 crypto_miner.exe`,
  netstat: () => `tcp 0.0.0.0:22 LISTEN\ntcp 192.168.4.12:52341→C2:443 ESTABLISHED`,
  help: () => 'ls, pwd, whoami, id, ifconfig, ps, netstat, cat, clear',
  clear: () => { document.getElementById('hack-terminal-output').innerHTML=''; return null; },
};

function handleHackCmd(e) {
  if (e.key !== 'Enter') return;
  const input = document.getElementById('hack-cmd-input');
  const output = document.getElementById('hack-terminal-output');
  const cmd = input.value.trim().toLowerCase();
  if (!cmd) return;
  const prompt = document.createElement('div');
  prompt.className = 'ht-line';
  prompt.innerHTML = `<span style="color:#ff6b6b">root@DESKTOP-K7J2X</span>:<span style="color:#7c7cff">~#</span> ${cmd}`;
  output.appendChild(prompt);
  const fn = hackCmds[cmd.split(' ')[0]];
  const res = fn ? fn() : `bash: ${cmd}: command not found`;
  if (res !== null && res !== undefined) {
    (res+'').split('\n').forEach(line => {
      const el = document.createElement('div');
      el.className = 'ht-line' + (res.includes('backdoor')||res.includes('C2')?' yellow':'');
      el.textContent = line;
      output.appendChild(el);
    });
  }
  output.scrollTop = output.scrollHeight;
  input.value = '';
}

function clearHackTerminal() {
  document.getElementById('hack-terminal-output').innerHTML = '';
}
function setHackTarget(t) {
  const targets = {
    carlos: {name:'Carlos (192.168.4.12)', host:'DESKTOP-K7J2X', ip:'192.168.4.12'},
    fernanda: {name:'Fernanda (10.0.1.44)', host:'iMac-Fernanda', ip:'10.0.1.44'},
    roberto: {name:'Roberto (172.20.3.87)', host:'LAPTOP-RB992', ip:'172.20.3.87'},
  };
  const tgt = targets[t];
  const output = document.getElementById('hack-terminal-output');
  output.innerHTML = '';
  const el = document.createElement('div');
  el.className='ht-line'; el.style.color='#00ff41';
  el.textContent = 'Conectando a '+tgt.host+' ('+tgt.ip+')... Conectado!';
  output.appendChild(el);
}

// Live keylog animation
let klPhrases = [
  'projeto_secreto_2025', 'MinhaS3nha!', 'CPF: 123.456.789-00',
  'acesso remoto habilitado', 'contato chefe: (11) 99234-5678',
  'pix@banco.com · R$12.000', 'senha_nova: Emp@2025#', 'token: 8f3k2x9p'
];
function startKeylogTicker() {
  const el = document.getElementById('kl-live');
  if (!el) return;
  setInterval(() => {
    const phrase = klPhrases[Math.floor(Math.random()*klPhrases.length)];
    const t = new Date().toLocaleTimeString('pt-BR');
    const line = document.createElement('div');
    const colors = ['#00ff41','#ffb700','#ff6b6b'];
    line.style.color = colors[Math.floor(Math.random()*colors.length)];
    line.innerHTML = `<span style="color:#444">[${t}]</span> ${phrase}`;
    el.appendChild(line);
    if(el.children.length > 12) el.removeChild(el.firstChild);
    el.parentElement.scrollTop = el.parentElement.scrollHeight;
  }, 2200);
}

// Screen clock
function updateScreenClock() {
  const el = document.getElementById('screen-clock');
  if(el) el.textContent = new Date().toLocaleTimeString('pt-BR',{hour:'2-digit',minute:'2-digit'});
}

// Screen typer effect
let screenLines = ['Enviando relatório...','Transferência aprovada ✓','Abrindo senhas_banco.txt...','Digitando nova senha...'];
let slIdx = 0;
function screenTyper() {
  const el = document.getElementById('screen-typer');
  if(!el) return;
  el.textContent = '> ' + screenLines[slIdx % screenLines.length];
  slIdx++;
}

// Live logins feed on dashboard
let loginNames = [
  'camila.souza','diego.ramos','elisa.costa','fabio.lima','giovana.melo',
  'henrique.dias','isabela.nunes','jorge.batista','karla.freitas','leonardo.pinto',
  'mariana.torres','nicolas.vera','olivia.martins','paulo.rodrigues','queila.santos'
];
function startLoginFeed() {
  const feed = document.getElementById('login-live-feed');
  if(!feed) return;
  setInterval(() => {
    const name = loginNames[Math.floor(Math.random()*loginNames.length)];
    const ips = ['192.168.1.','10.0.0.','172.20.3.','177.23.','201.12.'];
    const ip = ips[Math.floor(Math.random()*ips.length)] + Math.floor(10+Math.random()*240);
    const t = new Date().toLocaleTimeString('pt-BR');
    const line = document.createElement('div');
    line.className = 'activity-item';
    line.innerHTML = `<div class="activity-icon success">🟢</div><div class="activity-body"><div class="activity-text">${name}@empresa.com fez login</div><div class="activity-meta">${ip}</div></div><div class="activity-time">${t}</div>`;
    feed.insertBefore(line, feed.firstChild);
    if(feed.children.length > 8) feed.removeChild(feed.lastChild);
  }, 3500);
}

// Hacker counters
function startHackCounters() {
  setInterval(() => {
    const inf = document.getElementById('inf-count');
    const kl = document.getElementById('keylog-count');
    const ds = document.getElementById('data-stolen');
    if(inf) inf.textContent = 20+Math.floor(Math.random()*8);
    if(kl) { let v = parseInt(kl.textContent.replace(/\D/g,''))+Math.floor(Math.random()*30); kl.textContent = v.toLocaleString('pt-BR'); }
    const botCpu = document.getElementById('bot-cpu');
    const botBar = document.getElementById('bot-cpu-bar');
    if(botCpu) { const v=Math.floor(25+Math.random()*40); botCpu.textContent=v+'%'; if(botBar) botBar.style.width=v+'%'; }
  }, 2500);
}

// showPage patch removido — lógica integrada na função original

// Init
renderCharts();
startHackCounters();
startLoginFeed();
setInterval(updateScreenClock,60000);
setInterval(screenTyper,4000);
</script>
</body>
</html>
