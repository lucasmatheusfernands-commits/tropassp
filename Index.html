<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Central da Tropa v2</title>
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="theme-color" content="#FF6B00">
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
    <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

    <style>
        :root { 
            --bg-color: #0f1115; --card-bg: #1c1f26; --primary: #FF6B00; --text-light: #f1f1f1; 
            --text-muted: #8b949e; --success: #25D366; --danger: #ff4444; --warning: #ffc107; 
            --info: #1877F2; --progress-bg: #30363d; 
        }
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Roboto, sans-serif; }
        body { background-color: var(--bg-color); color: var(--text-light); padding: 15px; padding-bottom: 120px; transition: 0.3s; }
        body.modo-extremo { --bg-color: #000000; --card-bg: #000000; --primary: #39ff14; --text-light: #39ff14; --text-muted: #228b22; --success: #39ff14; }
        body.modo-extremo .card, body.modo-extremo .menu-item { border: 1px solid var(--primary); box-shadow: none; }
        body.modo-extremo .btn-calc { background-color: var(--primary); color: #000; }
        .top-bar { display: flex; align-items: center; justify-content: space-between; margin-bottom: 15px; }
        .btn-voltar { display: none; background: none; border: none; color: var(--primary); font-size: 16px; font-weight: bold; cursor: pointer; }
        .btn-night { background: transparent; border: 1px solid var(--primary); color: var(--primary); padding: 5px 10px; border-radius: 6px; font-size: 12px; font-weight: bold; cursor: pointer; }
        .header { flex-grow: 1; text-align: center; }
        .header h1 { color: var(--primary); font-size: 20px; text-transform: uppercase; letter-spacing: 1px; }
        .header p { color: var(--text-muted); font-size: 11px; margin-top: 2px; }
        .xp-badge { background: rgba(255,107,0,0.1); border: 1px solid var(--primary); padding: 6px 12px; border-radius: 20px; font-size: 12px; font-weight: bold; color: var(--primary); text-align: center; margin-bottom: 15px; display: inline-block; width: 100%; }
        
        .moto-setup { background: rgba(255,107,0,0.05); border: 1px dashed var(--primary); padding: 10px; border-radius: 10px; margin-bottom: 15px; display: flex; align-items: center; justify-content: space-between; font-size: 13px; }
        .moto-setup select { background: #0f1115; color: var(--text-light); border: 1px solid var(--primary); padding: 4px 8px; border-radius: 6px; font-weight: bold; outline: none; }
        
        .weather-home-card { background: var(--card-bg); border: 1px solid var(--primary); border-radius: 12px; padding: 15px; margin-bottom: 15px; box-shadow: 0 4px 15px rgba(255, 107, 0, 0.1); }
        .weather-home-title { font-size: 12px; color: var(--primary); font-weight: bold; text-transform: uppercase; margin-bottom: 8px; display: flex; justify-content: space-between; align-items: center; }
        .weather-hora { font-size: 12px; background: rgba(255,107,0,0.25); padding: 3px 8px; border-radius: 6px; color: var(--text-light); font-weight: bold; letter-spacing: 0.5px; }
        .weather-select { width: 100%; background-color: #0f1115; border: 1px solid var(--primary); border-radius: 6px; padding: 8px; color: var(--text-light); font-size: 13px; margin-bottom: 10px; font-weight: bold; outline:none;}
        .weather-desc { font-size: 12px; color: var(--text-muted); }
        .weather-links { display: flex; justify-content: space-between; gap: 10px; margin-top: 10px; border-top: 1px dashed #30363d; padding-top: 10px; }
        .weather-link-btn { background: rgba(24, 119, 242, 0.1); border: 1px solid var(--info); color: var(--info); padding: 6px 10px; border-radius: 6px; text-decoration: none; font-size: 11px; font-weight: bold; text-align: center; flex: 1; }
        
        .menu-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; }
        .menu-item { background-color: var(--card-bg); border: 1px solid #30363d; border-radius: 12px; padding: 12px; display: flex; flex-direction: column; align-items: center; text-align: center; cursor: pointer; transition: 0.2s; min-height: 95px; justify-content: center; }
        .menu-item:active { transform: scale(0.96); }
        .menu-icon { font-size: 26px; margin-bottom: 4px; }
        .menu-text h3 { font-size: 12px; color: var(--text-light); margin-bottom: 2px; font-weight: bold; }
        .menu-text p { font-size: 9px; color: var(--text-muted); line-height: 1.1; }
        
        .tela-app { display: none; }
        .card { background-color: var(--card-bg); border-radius: 12px; padding: 15px; margin-bottom: 12px; border: 1px solid #30363d; }
        .help-box { background-color: rgba(255, 107, 0, 0.05); border: 1px dashed var(--primary); padding: 10px; border-radius: 8px; margin-bottom: 12px; font-size: 12px; color: #ffd2b2; line-height: 1.3; }
        .input-group { margin-bottom: 12px; }
        .input-group label { display: block; font-size: 12px; color: var(--text-muted); margin-bottom: 4px; font-weight: 500; }
        .input-group input, .input-group select, .input-group textarea { width: 100%; background-color: #0f1115; border: 1px solid #30363d; border-radius: 8px; padding: 10px; color: var(--text-light); font-size: 14px; outline: none; }
        .btn-calc { width: 100%; background-color: var(--primary); color: white; border: none; padding: 12px; border-radius: 8px; font-size: 14px; font-weight: bold; text-transform: uppercase; cursor: pointer; margin-top: 8px; transition: 0.3s; display: inline-block; text-decoration: none; text-align: center; }
        .btn-calc:active { opacity: 0.8; }
        
        .tab-bar { display: flex; gap: 8px; margin-bottom: 15px; border-bottom: 1px solid #30363d; padding-bottom: 8px; }
        .tab-btn { background: transparent; border: none; color: var(--text-muted); font-size: 12px; font-weight: bold; padding: 6px 12px; cursor: pointer; border-radius: 4px; }
        .tab-btn.active { background: rgba(255, 107, 0, 0.15); color: var(--primary); }

        .result-box { display: none; text-align: center; margin-top: 15px; padding-top: 15px; border-top: 1px dashed #30363d; }
        .result-item span { display: block; font-size: 11px; color: var(--text-muted); text-transform: uppercase; }
        .result-item strong { font-size: 24px; color: var(--success); }
        .veredito-box { padding: 10px; border-radius: 6px; margin-top: 10px; font-size: 14px; font-weight: bold; text-transform: uppercase; text-align: center; }
        .status-ok { background-color: rgba(37, 211, 102, 0.15); color: var(--success); border: 1px solid var(--success); }
        .status-danger { background-color: rgba(255, 68, 68, 0.15); color: var(--danger); border: 1px solid var(--danger); }
        .status-alert { background-color: rgba(255, 193, 7, 0.15); color: var(--warning); border: 1px solid var(--warning); }
        
        .log-item { background: #0f1115; border: 1px solid #30363d; padding: 10px; border-radius: 8px; margin-bottom: 8px; font-size: 12px; display: flex; justify-content: space-between; align-items: center; }
        .log-left { display: flex; flex-direction: column; gap: 2px; }
        .log-tag { display: inline-block; padding: 2px 5px; font-size: 9px; font-weight: bold; border-radius: 4px; align-self: flex-start; }
        .btn-del { background: transparent; border: none; color: var(--danger); font-weight: bold; font-size: 13px; cursor: pointer; padding: 4px 8px; }

        .qg-item { background: #0f1115; padding: 10px; border-radius: 8px; border: 1px solid #30363d; margin-bottom: 8px; text-align: left; }
        .progress-container { width: 100%; background-color: var(--progress-bg); border-radius: 8px; margin-top: 8px; height: 10px; overflow: hidden; }
        .progress-bar { height: 100%; background-color: var(--success); width: 0%; transition: width 0.5s; }
        .check-item-container { display: flex; align-items: center; padding: 8px 0; border-bottom: 1px solid #30363d; font-size: 13px; }
        .check-item-container input[type="checkbox"] { width: 18px; height: 18px; margin-right: 12px; accent-color: var(--primary); }
        .maint-item { display: flex; flex-direction: column; padding: 10px 0; border-bottom: 1px dashed #30363d; }
        .status-badge { padding: 3px 8px; border-radius: 20px; font-size: 10px; font-weight: bold; display: inline-block; }
        
        .game-area { width: 100%; min-height: 200px; background: #000; border: 2px solid var(--primary); border-radius: 12px; position: relative; overflow: hidden; display: flex; align-items: center; justify-content: center; flex-direction: column; padding: 12px; text-align: center; }
        .grid-4x4 { display: grid; grid-template-columns: repeat(4, 1fr); gap: 4px; width: 100%; max-width: 280px; margin: 0 auto; }
        .grid-btn { background: var(--card-bg); border: 1px solid #30363d; color: #fff; font-size: 16px; font-weight: bold; padding: 10px 0; border-radius: 6px; cursor: pointer; display: flex; align-items: center; justify-content: center; border:none; }
        
        .mapa-container { height: 250px; border-radius: 8px; z-index: 1; border: 1px solid #30363d; margin-top: 10px; }
        #toast { visibility: hidden; min-width: 250px; background-color: var(--success); color: white; text-align: center; border-radius: 8px; padding: 12px; position: fixed; z-index: 10000; left: 50%; bottom: 80px; transform: translateX(-50%); font-size: 13px; font-weight: bold; }
        #toast.show { visibility: visible; animation: fadein 0.3s, fadeout 0.3s 2.5s; }
        @keyframes fadein { from {bottom: 0; opacity: 0;} to {bottom: 80px; opacity: 1;} }
        @keyframes fadeout { from {bottom: 80px; opacity: 1;} to {bottom: 0; opacity: 0;} }
        
        .footer-feedback { position: fixed; bottom: 0; left: 0; width: 100%; background-color: var(--card-bg); border-top: 1px solid #30363d; padding: 8px 12px; display: flex; justify-content: space-around; align-items: center; z-index: 999; gap: 6px; }
        .footer-btn { padding: 8px 4px; border-radius: 6px; font-size: 10px; font-weight: bold; cursor: pointer; text-decoration: none; text-align: center; flex: 1; border: 1px solid var(--primary); color: var(--primary); background: transparent; }
        .btn-call { display: block; width: 100%; background-color: var(--danger); color: white; border: none; padding: 8px; border-radius: 6px; font-size: 13px; font-weight: bold; text-decoration: none; text-align: center; margin-top: 5px; }
    </style>
</head>
<body>

    <div id="toast">✅ Concluído!</div>

    <div class="top-bar">
        <button id="btn-voltar" class="btn-voltar" onclick="voltarContexto()">⬅ Voltar</button>
        <div class="header">
            <h1 id="titulo-pagina">A TROPA</h1>
            <p id="subtitulo-pagina">Ferramentas de asfalto.</p>
        </div>
        <button class="btn-night" onclick="toggleModoExtremo()">🦇 Extremo</button>
    </div>

    <!-- MOTO SETUP GERAL -->
    <div class="moto-setup">
        <span>🏍️ <strong>Sua Moto:</strong></span>
        <select id="seletor-moto-geral" onchange="alterarMotoGeral()">
            <option value="Honda CG 160 Titan">Honda CG 160 Titan</option>
            <option value="Honda CG 160 Fan">Honda CG 160 Fan</option>
            <option value="Honda CG 160 Start">Honda CG 160 Start</option>
            <option value="Honda Pop 110i">Honda Pop 110i</option>
            <option value="Honda Biz 125">Honda Biz 125</option>
            <option value="Honda NXR 160 Bros">Honda NXR 160 Bros</option>
            <option value="Mottu Sport 110i">Mottu Sport 110i</option>
            <option value="Yamaha Factor 150">Yamaha Factor 150</option>
            <option value="Yamaha Factor 125">Yamaha Factor 125</option>
            <option value="Honda XRE 190">Honda XRE 190</option>
            <option value="Honda CB 300F Twister">Honda CB 300F Twister</option>
            <option value="Yamaha Fazer 150">Yamaha Fazer 150</option>
            <option value="Yamaha FZ15 Fazer">Yamaha FZ15 Fazer</option>
            <option value="Honda Sahara 300">Honda Sahara 300</option>
            <option value="Yamaha Lander 250">Yamaha Lander 250</option>
            <option value="Yamaha Crosser 150">Yamaha Crosser 150</option>
            <option value="Honda Elite 125">Honda Elite 125</option>
            <option value="Honda PCX 150">Honda PCX 150</option>
            <option value="Shineray Worker 125">Shineray Worker 125</option>
            <option value="Suzuki Intruder 125">Suzuki Intruder 125</option>
        </select>
    </div>

    <!-- TELA 0: MENU -->
    <div id="tela-menu" class="tela-app" style="display: block;">
        <div class="xp-badge" id="hud-xp">XP DA TROPA: 0</div>
        
        <div class="weather-home-card">
            <div class="weather-home-title">
                <span>🌦️ Clima SP e Radar</span>
                <span id="relogio-atual" class="weather-hora">--:--:--</span>
            </div>
            <select id="seletor-regiao" class="weather-select" onchange="atualizarClimaRegiao()">
                <option value="centro">📍 Centro / Paulista - 19°C (Nublado)</option>
                <option value="norte">📍 Zona Norte - 18°C (Nublado)</option>
                <option value="sul">📍 Zona Sul - 17°C (Nublado)</option>
                <option value="leste">📍 Zona Leste - 19°C (Nublado)</option>
                <option value="oeste">📍 Zona Oeste - 19°C (Nublado)</option>
            </select>
            <div class="weather-desc">Chuvas e umidade monitoradas ao vivo em São Paulo.</div>
            <div class="weather-links">
                <a href="https://radar.sodamobi.com/" target="_blank" class="weather-link-btn">🛰️ Radar Chuva Ao Vivo</a>
                <a href="https://www.climatempo.com.br/radar/grande-sao-paulo" target="_blank" class="weather-link-btn">🌦️ Climatempo Radar</a>
            </div>
        </div>

        <div class="menu-grid">
            <!-- 🚀 OPERAÇÃO -->
            <div class="menu-item" onclick="abrirTela('tela-radar')"><div class="menu-icon">⚖️</div><div class="menu-text"><h3>Radar Tropa</h3><p>Avaliar Corridas</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-teclado')"><div class="menu-icon">💬</div><div class="menu-text"><h3>Teclado Ninja</h3><p>Mensagens Prontas</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-alerta')"><div class="menu-icon">📡</div><div class="menu-text"><h3>Alerta Tropa</h3><p>Enviar aos Grupos</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-sos')"><div class="menu-icon">🚨</div><div class="menu-text"><h3>SOS / Roubos</h3><p>Suporte e Alertas</p></div></div>

            <!-- 💰 FINANCEIRO -->
            <div class="menu-item" onclick="abrirTela('tela-metas')"><div class="menu-icon">🎯</div><div class="menu-text"><h3>Metas Ninja</h3><p>Diária/Semanal/Mensal</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-raiox')"><div class="menu-icon">💰</div><div class="menu-text"><h3>Raio-X</h3><p>Calculadora Lucro</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-comunidade')"><div class="menu-icon">🤝</div><div class="menu-text"><h3>Compras</h3><p>Grupo Atacado</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-feirao')"><div class="menu-icon">♻️</div><div class="menu-text"><h3>Feirão do Rolo</h3><p>Classificados</p></div></div>
            
            <!-- 🔧 MECÂNICA -->
            <div class="menu-item" onclick="abrirTela('tela-diagnosticos')"><div class="menu-icon">🩺</div><div class="menu-text"><h3>Doutor Motor</h3><p>Diagnóstico Local</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-trocas')"><div class="menu-icon">🔧</div><div class="menu-text"><h3>Controle Mecânico</h3><p>Manutenção e Histórico</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-barulhos')"><div class="menu-icon">🔊</div><div class="menu-text"><h3>Barulhos</h3><p>Defeitos Comuns</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-pneus')"><div class="menu-icon">🛞</div><div class="menu-text"><h3>Vida Pneu</h3><p>Calculadora TWI</p></div></div>

            <!-- 📍 APOIO -->
            <div class="menu-item" onclick="abrirTela('tela-qgs')"><div class="menu-icon">📍</div><div class="menu-text"><h3>Bases & QGs</h3><p>Apoio na Rua</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-postos')"><div class="menu-icon">⛽</div><div class="menu-text"><h3>Mapa Postos</h3><p>Qualidade de Postos</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-bomba')"><div class="menu-icon">🧪</div><div class="menu-text"><h3>Bomba Flex</h3><p>Álcool x Gasolina</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-parceiros')"><div class="menu-icon">🍔</div><div class="menu-text"><h3>Parceiros</h3><p>Descontos e Dicas</p></div></div>
            
            <!-- ⏳ EXTRA -->
            <div class="menu-item" onclick="abrirTela('tela-checklist')"><div class="menu-icon">🎒</div><div class="menu-text"><h3>Check de Saída</h3><p>Inspeção Rápida</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-cha')"><div class="menu-icon">⏳</div><div class="menu-text"><h3>Chá de Cadeira</h3><p>Espera Produtiva</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-ct')"><div class="menu-icon">🧠</div><div class="menu-text"><h3>CT Ninja</h3><p>10 Jogos Treino</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-bloco')"><div class="menu-icon">📝</div><div class="menu-text"><h3>Bloco de Notas</h3><p>Agenda e Tarefas</p></div></div>

            <!-- 🧘 SAÚDE & DIREITOS -->
            <div class="menu-item" onclick="abrirTela('tela-direitos')"><div class="menu-icon">⚖️</div><div class="menu-text"><h3>Direitos Tropa</h3><p>Leis e Regras</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-alongamento')"><div class="menu-icon">🤸</div><div class="menu-text"><h3>Alongamento</h3><p>Exercícios Farol</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-sono')"><div class="menu-icon">💤</div><div class="menu-text"><h3>Sono Ninja</h3><p>Ciclos e Horários</p></div></div>
            <div class="menu-item" onclick="abrirTela('tela-mantra')"><div class="menu-icon">🙏</div><div class="menu-text"><h3>Mantra</h3><p>Partida com Foco</p></div></div>

            <!-- CONFIGURAÇÕES E MANUAL (BACKUP FICA AQUI!) -->
            <div class="menu-item" onclick="abrirTela('tela-manual')" style="grid-column: span 2; border: 2px solid var(--warning); background-color: rgba(255, 193, 7, 0.05);"><div class="menu-icon" style="font-size:24px;">⚙️</div><div class="menu-text"><h3>Manual & Backup</h3><p>Instruções e Salvar Conta</p></div></div>
        </div>
    </div>

    <!-- ======================================================== -->
    <!-- TELAS DETALHADAS -->
    <!-- ======================================================== -->

    <!-- TELA RADAR: AVALIAR CORRIDA -->
    <div id="tela-radar" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:10px;">⚖️ Configuração do Seu Alvo (R$/km)</h3>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:12px;">Defina os limites de ganho ideais do seu bolso para avaliar as corridas oferecidas.</p>
            <div style="display:flex; gap:8px;">
                <div class="input-group" style="flex:1;"><label>Bom R$/km</label><input type="number" id="radar-bom" value="3.0" step="0.1" onchange="salvarParamsRadar()"></div>
                <div class="input-group" style="flex:1;"><label>Médio R$/km</label><input type="number" id="radar-medio" value="2.0" step="0.1" onchange="salvarParamsRadar()"></div>
                <div class="input-group" style="flex:1;"><label>Ruim R$/km</label><input type="number" id="radar-ruim" value="1.5" step="0.1" onchange="salvarParamsRadar()"></div>
            </div>
        </div>
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:15px;">🔍 Dados da Corrida do App</h3>
            <div class="input-group"><label>Valor Oferecido (R$)</label><input type="number" id="corrida-valor" placeholder="Ex: 24.50" step="0.01"></div>
            <div class="input-group"><label>Distância Total (Km)</label><input type="number" id="corrida-km" placeholder="Ex: 8.5" step="0.1"></div>
            <div class="input-group"><label>Tempo Estimado (Minutos)</label><input type="number" id="corrida-tempo" placeholder="Ex: 25"></div>
            <button class="btn-calc" onclick="avaliarCorridaCompleta()">Analisar Corrida</button>
            <div class="result-box" id="radar-resultado">
                <div style="display:flex; justify-content:space-around; margin-bottom:12px;">
                    <div class="result-item"><span>Ganho por KM</span><strong id="res-valorkm">R$ 0,00</strong></div>
                    <div class="result-item"><span>Média por Hora</span><strong id="res-valorhora" style="color:var(--text-light);">R$ 0,00</strong></div>
                </div>
                <div id="radar-veredito" class="veredito-box status-ok">ACEITAR</div>
                <div class="qg-item" style="margin-top:12px; font-size:11px; color:var(--text-muted);" id="radar-coment">Análise baseada nos seus custos operacionais.</div>
            </div>
        </div>
    </div>

    <!-- TELA TECLADO NINJA -->
    <div id="tela-teclado" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:12px;">💬 Mensagens Rápidas Ninja</h3>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:15px;">Toque para copiar ou crie novas respostas para envio rápido no aplicativo de entregas.</p>
            <div style="display:flex; gap:8px; margin-bottom:15px;">
                <input type="text" id="novo-msg-texto" placeholder="Nova resposta personalizada..." style="flex:1; background:#0f1115; color:#fff; border:1px solid #30363d; padding:10px; border-radius:6px; font-size:13px;">
                <button class="btn-calc" style="width:auto; margin:0; padding:10px 15px;" onclick="addMensagemNinja()">➕</button>
            </div>
            <div id="container-mensagens"></div>
        </div>
    </div>

    <!-- TELA ALERTA -->
    <div id="tela-alerta" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:12px;">📡 Avisar a Tropa de Ocorrências</h3>
            <div class="input-group"><label>Tipo de Ocorrência</label><select id="alerta-tipo"><option>Blitz / Operação</option><option>Alagamento / Temporal</option><option>Acidente Grave</option><option>Trânsito Parado</option></select></div>
            <div class="input-group"><label>Rua / Bairro / Referência</label><input type="text" id="alerta-local" placeholder="Ex: Av. Ataliba Leonel, alt 1200"></div>
            <button class="btn-calc" style="background:var(--success);" onclick="dispararAlertaGrupo()">📲 Enviar WhatsApp</button>
        </div>
    </div>

    <!-- TELA SOS / ROUBOS -->
    <div id="tela-sos" class="tela-app">
        <div class="card">
            <h3 style="color:var(--danger); margin-bottom:12px;">🚨 Pânico e Emergências</h3>
            <p style="font-size:12px; color:var(--text-muted); margin-bottom:15px;">Canais rápidos abaixo para socorro.</p>
            <div class="qg-item"><h4>🚓 Polícia Militar</h4><a href="tel:190" class="btn-call" style="background:var(--info);">Ligar 190</a></div>
            <div class="qg-item"><h4>🚑 SAMU</h4><a href="tel:192" class="btn-call" style="background:var(--danger);">Ligar 192</a></div>
            <div class="qg-item"><h4>🚒 Bombeiros</h4><a href="tel:193" class="btn-call" style="background:#8b949e;">Ligar 193</a></div>
        </div>
        <div class="card" style="border-color:var(--danger);">
            <h3 style="color:var(--danger); margin-bottom:10px;">🏍️ Alerta de Moto Roubada</h3>
            <div class="input-group"><label>Sua Moto</label><input type="text" id="sos-moto" placeholder="Modelo e Cor"></div>
            <div class="input-group"><label>Placa</label><input type="text" id="sos-placa" placeholder="Placa da Moto"></div>
            <div class="input-group"><label>Região / Detalhes</label><input type="text" id="sos-local" placeholder="Onde foi?"></div>
            <button class="btn-calc" style="background:var(--danger);" onclick="dispararRouboWhatsApp()">🚨 Alertar Grupos</button>
        </div>
    </div>

    <!-- TELA METAS NINJA -->
    <div id="tela-metas" class="tela-app">
        <div class="tab-bar">
            <button class="tab-btn active" id="btn-meta-dia" onclick="alterarMetaTab('dia')">DIÁRIA</button>
            <button class="tab-btn" id="btn-meta-semana" onclick="alterarMetaTab('semana')">SEMANAL</button>
            <button class="tab-btn" id="btn-meta-mes" onclick="alterarMetaTab('mes')">MENSAL</button>
        </div>
        <div class="card" id="card-metas-input">
            <h3 id="meta-titulo-aba" style="color:var(--primary); margin-bottom:12px;">🎯 Planejar Meta</h3>
            <div class="input-group"><label id="label-meta-alvo">Valor Alvo (R$)</label><input type="number" id="meta-valor-alvo" placeholder="0.00" onchange="salvarMetasTropa()"></div>
            <div class="input-group"><label id="label-meta-dias">Número de Dias</label><input type="number" id="meta-dias" placeholder="Quantidade" onchange="salvarMetasTropa()"></div>
            <div class="input-group"><label id="label-meta-feito">Já Faturado (R$)</label><input type="number" id="meta-faturado" placeholder="0.00" onchange="salvarMetasTropa()"></div>
            <div class="input-group"><label id="label-meta-diasfeitos">Dias/Horas Trabalhados</label><input type="number" id="meta-diasfeitos" placeholder="Corridos" onchange="salvarMetasTropa()"></div>
            <button class="btn-calc" onclick="calcularMetasTropa()">Calcular Progresso</button>
            
            <div class="result-box" id="metas-resultado">
                <div class="result-item"><span>Falta por período</span><strong id="metas-valor-necessario">R$ 0,00</strong></div>
                <p style="font-size:12px; margin-top:10px; color:var(--warning);" id="metas-res-desc">Mantenha a frequência.</p>
                <div class="progress-container"><div class="progress-bar" id="metas-progresso-bar" style="width: 0%;"></div></div>
                <div id="metas-porcento" style="font-size:11px; text-align:right; color:var(--text-muted); margin-top:4px;">0%</div>
            </div>
        </div>
    </div>

    <!-- TELA RAIO-X -->
    <div id="tela-raiox" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:12px;">💰 Raio-X de Faturamento</h3>
            <div class="input-group">
                <label>Selecione o Aplicativo</label>
                <select id="raiox-app">
                    <option value="iFood">iFood 🍔</option>
                    <option value="Lalamove">Lalamove 📦</option>
                    <option value="Uber">Uber 🚗</option>
                    <option value="99">99 🛵</option>
                    <option value="Rappi">Rappi 🎒</option>
                    <option value="Outros">Outros / Particular 🤝</option>
                </select>
            </div>
            <div style="display:flex; gap:8px;">
                <div class="input-group" style="flex:1;"><label>Faturamento (R$)</label><input type="number" id="raiox-fat" placeholder="0.00"></div>
                <div class="input-group" style="flex:1;"><label>Km Rodados</label><input type="number" id="raiox-km" placeholder="0"></div>
            </div>
            <div style="display:flex; gap:8px;">
                <div class="input-group" style="flex:1;"><label>Gasolina (R$)</label><input type="number" id="raiox-gas" placeholder="0.00"></div>
                <div class="input-group" style="flex:1;"><label>Consumo (km/L)</label><input type="number" id="raiox-consumo" value="35"></div>
            </div>
            <div class="input-group"><label>Gasto Extra / Almoço (R$)</label><input type="number" id="raiox-extras" placeholder="0.00"></div>
            <button class="btn-calc" onclick="calcularESalvarRaioX()">Calcular e Salvar Lucro</button>
        </div>
        <div class="card">
            <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:10px;">
                <h3 style="color:var(--success); font-size:14px;">📋 Histórico do Corre</h3>
                <button onclick="limparHistoricoRaioX()" style="background:transparent; border:none; color:var(--danger); font-size:12px; cursor:pointer;">Limpar tudo</button>
            </div>
            <div id="historico-raiox-lista"></div>
        </div>
    </div>

    <!-- TELA COMUNIDADE / FEIRÃO / PARCEIROS -->
    <div id="tela-comunidade" class="tela-app">
        <div class="card" style="text-align:center;">
            <h3 style="color:var(--primary); margin-bottom:15px;">🤝 Compras no Atacado</h3>
            <p style="font-size:13px; margin-bottom:15px;">A união faz a força! Compre pneus e óleos direto de fornecedores para economizar.</p>
            <a href="https://chat.whatsapp.com/BF03y8eivFdDoyNrKk9nCk" target="_blank" class="btn-calc" style="background:var(--success);">🟢 Entrar no Grupo Atacado</a>
        </div>
    </div>
    <div id="tela-feirao" class="tela-app">
        <div class="card" style="text-align:center;">
            <h3 style="color:var(--primary); margin-bottom:10px;">♻️ Feirão do Rolo</h3>
            <p style="font-size:12px; color:var(--text-muted); margin-bottom:15px;">Classificados exclusivos da comunidade para desapego de peças.</p>
            <a href="https://www.facebook.com/share/g/1F9pkLnkJe/" target="_blank" class="btn-calc" style="background:var(--info);">📘 Entrar no Facebook</a>
        </div>
    </div>
    <div id="tela-parceiros" class="tela-app">
        <div class="card" style="text-align: center;">
            <h3 style="color:var(--primary); margin-bottom:10px;">🍔 Parceiros da Tropa</h3>
            <div class="veredito-box status-alert" style="margin-bottom: 15px;">🚧 EM DESENVOLVIMENTO</div>
            <p style="font-size:13px; color:var(--text-light); margin-bottom:15px; text-align:left; background:rgba(255,107,0,0.1); padding:12px; border-left:4px solid var(--primary); border-radius:8px;">
                A ideia aqui é montar um clube de vantagens. Fechar parcerias com lanchonetes, restaurantes, lojas de peças ou parceiros que fazem trampo extra (manutenção, barbeiro).
            </p>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:15px;">Conhece um lugar bom? Manda a dica pra nós cadastrarmos!</p>
            <a href="https://wa.me/?text=Salve%20Lucas,%20tenho%20uma%20sugest%C3%A3o%20de%20parceria" target="_blank" class="btn-calc" style="background:var(--success); text-decoration:none;">🤝 Indicar Parceria</a>
        </div>
    </div>

    <!-- TELA DOUTOR MOTOR E TROCAS -->
    <div id="tela-diagnosticos" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:12px;">🩺 Doutor Motor</h3>
            <div class="help-box">Descubra falhas comuns baseado nos sintomas da Tropa.</div>
            <div class="input-group">
                <label>Sintoma do Motor</label>
                <select id="diag-sintoma" onchange="gerarDiagnosticoDoutorMotor()">
                    <option value="">Escolha uma queixa comum...</option>
                    <option value="partida">Não dá partida (tec tec / apaga)</option>
                    <option value="fumaça">Fumaça branca constante no escape</option>
                    <option value="falhando">Engasga, falha ao acelerar</option>
                    <option value="freio">Manete/pedal de freio baixo (borrachudo)</option>
                    <option value="embreagem">Motor gira forte mas moto não anda (patinando)</option>
                </select>
            </div>
            <div id="diag-resultado" style="display:none;" class="qg-item"></div>
        </div>
    </div>

    <div id="tela-trocas" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:12px;">🔧 Controle Geral de Trocas</h3>
            <div class="input-group">
                <label>KM Atual do Painel</label>
                <input type="number" id="mecanico-km-atual" placeholder="Ex: 45320" onchange="salvarKMAntigos()">
            </div>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:15px;">Adicione o histórico de troca para acompanhar o prazo limite.</p>
            
            <div class="maint-item">
                <div style="display:flex; justify-content:space-between; align-items:center;">
                    <h4>🛢️ Óleo (1.000km)</h4><span class="status-badge status-ok" id="mecanico-badge-oleo">Aguardando</span>
                </div>
                <button class="btn-calc" style="padding:6px; font-size:11px; background:#30363d;" onclick="registrarTrocaPeca('oleo', 1000)">Substituir Óleo</button>
            </div>
            <div class="maint-item">
                <div style="display:flex; justify-content:space-between; align-items:center;">
                    <h4>🛢️ Óleo Sint. (3.000km)</h4><span class="status-badge status-ok" id="mecanico-badge-oleosint">Aguardando</span>
                </div>
                <button class="btn-calc" style="padding:6px; font-size:11px; background:#30363d;" onclick="registrarTrocaPeca('oleosint', 3000)">Substituir Sintético</button>
            </div>
            <div class="maint-item">
                <div style="display:flex; justify-content:space-between; align-items:center;">
                    <h4>💨 Filtro (10.000km)</h4><span class="status-badge status-ok" id="mecanico-badge-filtro">Aguardando</span>
                </div>
                <button class="btn-calc" style="padding:6px; font-size:11px; background:#30363d;" onclick="registrarTrocaPeca('filtro', 10000)">Substituir Filtro</button>
            </div>
            <div class="maint-item">
                <div style="display:flex; justify-content:space-between; align-items:center;">
                    <h4>⚡ Vela (12.000km)</h4><span class="status-badge status-ok" id="mecanico-badge-vela">Aguardando</span>
                </div>
                <button class="btn-calc" style="padding:6px; font-size:11px; background:#30363d;" onclick="registrarTrocaPeca('vela', 12000)">Substituir Vela</button>
            </div>
            <div class="maint-item">
                <div style="display:flex; justify-content:space-between; align-items:center;">
                    <h4>⚙️ Relação (20.000km)</h4><span class="status-badge status-ok" id="mecanico-badge-relacao">Aguardando</span>
                </div>
                <button class="btn-calc" style="padding:6px; font-size:11px; background:#30363d;" onclick="registrarTrocaPeca('relacao', 20000)">Substituir Relação</button>
            </div>
            <div class="maint-item" style="border-bottom:none;">
                <div style="display:flex; justify-content:space-between; align-items:center;">
                    <h4>🛑 Freios (8.000km)</h4><span class="status-badge status-ok" id="mecanico-badge-freios">Aguardando</span>
                </div>
                <button class="btn-calc" style="padding:6px; font-size:11px; background:#30363d;" onclick="registrarTrocaPeca('freios', 8000)">Substituir Pastilhas</button>
            </div>
        </div>
        <div class="card">
            <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:10px;">
                <h3 style="color:var(--success); font-size:14px;">📋 Histórico</h3>
                <button onclick="limparHistoricoTrocas()" style="background:transparent; border:none; color:var(--danger); font-size:12px; cursor:pointer;">Limpar tudo</button>
            </div>
            <div id="historico-trocas-lista"></div>
        </div>
    </div>

    <!-- TELA BARULHOS E PNEUS -->
    <div id="tela-barulhos" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:10px;">🔊 Biblioteca de Barulhos</h3>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:12px;">Identifique ruidos comuns da moto.</p>
            <div class="qg-item"><h4>🛠️ Tec-Tec constante do cabeçote</h4><p style="font-size:11px;">Causa: Folga nas válvulas. Ação: Regulagem no mecânico.</p></div>
            <div class="qg-item"><h4>🛑 Assobio agudo ao usar o freio</h4><p style="font-size:11px;">Causa: Pastilhas gastas (no ferro). Ação: Troca urgente.</p></div>
            <div class="qg-item"><h4>⛓️ Estalos secos ao rodar</h4><p style="font-size:11px;">Causa: Corrente frouxa/seca. Ação: Esticar e lubrificar.</p></div>
            <div style="background:rgba(255, 107, 0, 0.05); border: 1px dashed var(--primary); border-radius: 8px; padding: 12px; text-align: center; margin-top:15px;">
                <span style="font-size:24px;">🎧</span>
                <h4 style="color:var(--primary); margin-top:5px; font-size:12px;">EM BREVE: SONS GRAVADOS REAIS</h4>
                <p style="font-size:10px; color:var(--text-muted);">Diagnósticos baseados em áudios reais da rua.</p>
            </div>
        </div>
    </div>

    <div id="tela-pneus" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:10px;">🛞 Teste de Desgaste (TWI)</h3>
            <p style="font-size:12px; color:var(--text-muted); margin-bottom:12px;">Calcula a segurança do pneu com base na moto definida no painel superior.</p>
            <div class="input-group"><label>KM no momento da troca do pneu anterior</label><input type="number" id="pneu-km-anterior" placeholder="Ex: 35000"></div>
            <button class="btn-calc" onclick="calcularVidaPneu()">Estimar Desgaste</button>
            <div class="result-box" id="pneus-resultado">
                <div class="result-item"><span>Previsão de Vida Restante</span><strong id="pneu-porcento">0%</strong></div>
                <div class="progress-container" style="margin-top:10px;"><div class="progress-bar" id="pneus-barra" style="width: 0%;"></div></div>
                <div id="pneu-estado" class="veredito-box status-ok" style="margin-top:10px;">SEGURO</div>
                <div class="qg-item" style="margin-top:10px; font-size:11px; color:var(--text-muted);">
                    <strong>💡 Prevenção:</strong> O cálculo monitora o risco de pneu careca, evitando multas e quedas na chuva. Confirme visualmente a marcação do friso (TWI).
                </div>
            </div>
        </div>
    </div>

    <!-- TELA QGS E POSTOS (LEAFLET HTML) -->
    <div id="tela-qgs" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:10px;">📍 Bases e Apoios</h3>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:12px;">Toque no mapa ou escreva o endereço abaixo.</p>
            <div id="map-bases" class="mapa-container"></div>
            <div class="input-group" style="margin-top:12px;"><label>Nome / Referência</label><input type="text" id="qg-endereco" placeholder="Ex: Praça X"></div>
            <div class="input-group"><label>Facilidades</label><input type="text" id="qg-desc" placeholder="Ex: Tomadas liberadas"></div>
            <button class="btn-calc" onclick="salvarQGLive()">Adicionar Ponto</button>
            <div id="qg-salvos-lista" style="margin-top:12px;"></div>
        </div>
    </div>

    <div id="tela-postos" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:10px;">⛽ Postos Parceiros</h3>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:12px;">Toque no mapa ou escreva o endereço abaixo.</p>
            <div id="map-postos" class="mapa-container"></div>
            <div class="input-group" style="margin-top:12px;"><label>Nome do Posto</label><input type="text" id="posto-endereco" placeholder="Ex: Shell Av. Paulista"></div>
            <div style="display:flex; gap:8px;">
                <div class="input-group" style="flex:1;"><label>Preço (R$)</label><input type="number" id="posto-preco" placeholder="0.00" step="0.01"></div>
                <div class="input-group" style="flex:1;"><label>Avaliação</label><select id="posto-nota"><option value="Boa">Boa ⭐⭐⭐</option><option value="Média">Média ⭐⭐</option><option value="Ruim">Ruim ⭐</option></select></div>
            </div>
            <button class="btn-calc" onclick="salvarPostoLive()">Adicionar Posto</button>
            <div id="postos-salvos-lista" style="margin-top:12px;"></div>
        </div>
    </div>

    <!-- TELA BOMBA FLEX E CHECKLIST -->
    <div id="tela-bomba" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:10px;">🧪 Bomba Flex</h3>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:12px;">Saiba qual vale a pena hoje.</p>
            <div class="input-group"><label>Gasolina (R$)</label><input type="number" id="bomba-gasolina" placeholder="Ex: 5.49" step="0.01"></div>
            <div class="input-group"><label>Etanol (R$)</label><input type="number" id="bomba-etanol" placeholder="Ex: 3.89" step="0.01"></div>
            <button class="btn-calc" onclick="calcularBombaFlex()">Calcular Relação</button>
            <div class="result-box" id="bomba-resultado">
                <div class="result-item"><span>Custo Proporcional do Etanol</span><strong id="bomba-porcento">0%</strong></div>
                <div id="bomba-veredito" class="veredito-box status-ok">VAI DE GASOLINA</div>
                <div class="qg-item" style="margin-top:10px; font-size:11px; color:var(--text-muted);">
                    <strong>💡 Regra dos 70%:</strong> Motores pequenos aproveitam ~70% do rendimento do etanol. Se o etanol for mais caro que 70% da gasolina, a gasolina rende mais no final do dia.
                </div>
            </div>
        </div>
    </div>

    <div id="tela-checklist" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:12px;">🎒 Check de Saída Ninja</h3>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:12px;">Vistoria de 1 min antes de rodar.</p>
            <div class="check-item-container"><input type="checkbox" id="chk-checklist-1" onchange="salvarCheckListEstático('1')"><label for="chk-checklist-1">📱 Powerbank e cabo ok</label></div>
            <div class="check-item-container"><input type="checkbox" id="chk-checklist-2" onchange="salvarCheckListEstático('2')"><label for="chk-checklist-2">🌧️ Capa e polainas no baú</label></div>
            <div class="check-item-container"><input type="checkbox" id="chk-checklist-3" onchange="salvarCheckListEstático('3')"><label for="chk-checklist-3">🛞 Pneus calibrados / Sem rasgos</label></div>
            <div class="check-item-container"><input type="checkbox" id="chk-checklist-4" onchange="salvarCheckListEstático('4')"><label for="chk-checklist-4">🔒 Trava de disco / Cadeado</label></div>
            <div class="check-item-container"><input type="checkbox" id="chk-checklist-5" onchange="salvarCheckListEstático('5')"><label for="chk-checklist-5">💧 Garrafa de água cheia</label></div>
            <div class="check-item-container"><input type="checkbox" id="chk-checklist-6" onchange="salvarCheckListEstático('6')"><label for="chk-checklist-6">⛓️ Lubrificação da corrente visual</label></div>
            <button class="btn-calc" style="background:var(--success);" onclick="salvarChecklistCompleto()">Tudo OK! Partiu.</button>
        </div>
    </div>

    <!-- TELA CHÁ DE CADEIRA E CT -->
    <div id="tela-cha" class="tela-app">
        <div class="card" style="text-align:center;">
            <h3 style="color:var(--primary); margin-bottom:10px;">⏳ Chá de Cadeira na Loja</h3>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:15px;">Foco nos 15 min de espera.</p>
            <div style="font-size:48px; font-weight:bold; margin:15px 0;" id="cha-display">15:00</div>
            <div style="display:flex; gap:10px; margin-bottom:15px;">
                <button class="btn-calc" style="background:var(--success); margin:0;" onclick="iniciarCronometroCha()">▶ Iniciar</button>
                <button class="btn-calc" style="background:var(--warning); color:#000; margin:0;" onclick="pausarCronometroCha()">⏸ Pausar</button>
                <button class="btn-calc" style="background:var(--danger); margin:0;" onclick="zerarCronometroCha()">⏹ Zerar</button>
            </div>
            <div class="qg-item" style="text-align:left; border-left:3px solid var(--warning);">
                <h4>🧠 Sugestões Produtivas:</h4>
                <p style="font-size:11px; margin-top:5px; color:#ffd2b2;">
                    - Avaliar TWI e corrente da moto.<br>
                    - Jogar no <strong>CT Ninja</strong> (Treino mental).<br>
                    - Revisar e organizar metas do dia.<br>
                    - Ler os Direitos da Tropa e beber água.
                </p>
            </div>
        </div>
    </div>

    <div id="tela-ct" class="tela-app">
        <div class="card">
            <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:15px;">
                <h3 style="color:var(--primary);">🧠 CT Ninja</h3><span class="xp-badge" style="width:auto; margin:0;" id="ct-xp-badge">0 XP</span>
            </div>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:15px;">10 Simuladores de asfalto.</p>
            <div id="ct-lista-jogos"></div>
        </div>
    </div>

    <!-- TELA JOGO ATIVO -->
    <div id="tela-jogo-ativo" class="tela-app">
        <div class="card">
            <h3 id="game-title" style="color:var(--primary); text-align:center; margin-bottom:5px;">Jogo</h3>
            <p id="game-desc" style="font-size:11px; color:var(--text-muted); text-align:center; margin-bottom:15px;"></p>
            <div class="stats-bar" style="display:flex; justify-content:space-between; font-size:12px; color:var(--warning); margin-bottom:10px; font-weight:bold;">
                <span>🏆 Rec: <span id="game-recorde">0</span></span><span>⭐ Pts: <span id="game-score">0</span></span>
            </div>
            <div id="game-canvas" class="game-area"></div>
            <div id="game-over-screen" style="display:none; text-align:center; margin-top:20px; padding-top:15px; border-top:1px dashed #30363d;">
                <h4 style="color:var(--success); font-size:18px; margin-bottom:5px;">FIM DE TREINO</h4>
                <p style="font-size:14px; margin-bottom:10px;">Pontos: <strong id="go-score">0</strong></p>
                <div class="qg-item" style="background:rgba(255,107,0,0.1); border:none;">
                    <strong style="color:var(--primary); font-size:12px;">🏍️ Pra que serve:</strong>
                    <p id="go-benefit" style="font-size:11px; color:var(--text-light); margin-top:4px;"></p>
                </div>
                <div style="display:flex; gap:10px; margin-top:15px;">
                    <button class="btn-calc" style="background:var(--primary); color:#000;" onclick="reiniciarJogoAtual()">Jogar De Novo</button>
                    <button class="btn-calc" style="background:#30363d;" onclick="voltarContexto()">Voltar ao CT</button>
                </div>
            </div>
        </div>
    </div>

    <!-- TELA BLOCO DE NOTAS -->
    <div id="tela-bloco" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:12px;">📝 Agenda de Tarefas e Notas</h3>
            <textarea id="bloco-texto" placeholder="Anotações livres..." style="width:100%; height:100px; background:#0f1115; color:#fff; border:1px solid #30363d; border-radius:8px; padding:10px; margin-bottom:10px;" onkeyup="salvarBlocoTexto()"></textarea>
            <div style="display:flex; gap:8px; margin-bottom:15px;">
                <input type="text" id="novo-tarefa" placeholder="Lembrete de tarefa..." style="flex:1; background:#0f1115; color:#fff; border:1px solid #30363d; padding:10px; border-radius:8px;">
                <button class="btn-calc" style="width:auto; margin:0;" onclick="addTarefaTropa()">➕</button>
            </div>
            <div id="tarefas-lista"></div>
        </div>
    </div>

    <!-- TELA GESTOR -->
    <div id="tela-gestor" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:10px;">👔 Gestor MEI</h3>
            <p style="font-size:12px; margin-bottom:12px;">O DAS (tributo do motofretista MEI) vence todo dia 20.</p>
            <a href="https://www.gov.br/empresas-e-negocios/pt-br/empreendedor" target="_blank" class="btn-calc" style="background:var(--info);">Acessar Portal do Empreendedor</a>
        </div>
    </div>

    <!-- TELA DIREITOS, ALONGAMENTO, SONO E MANTRA -->
    <div id="tela-direitos" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:12px;">⚖️ Direitos da Tropa</h3>
            <p style="font-size:11px; margin-bottom:15px;">Leis e regras essenciais de operação e segurança.</p>
            <div id="direitos-container"></div>
        </div>
    </div>

    <div id="tela-alongamento" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:12px;">🤸 Alongamento no Farol</h3>
            <div class="qg-item"><h4>Pescoço e Cervical</h4><p style="font-size:11px;">Incline a cabeça para os lados segurando por 10 seg.</p></div>
            <div class="qg-item"><h4>Costas e Braços</h4><p style="font-size:11px;">Entrelace os dedos e estique os braços à frente por 15 seg.</p></div>
            <div class="qg-item"><h4>Lombar e Quadril</h4><p style="font-size:11px;">Apoiado na moto, incline levemente o tronco para trás.</p></div>
        </div>
    </div>

    <div id="tela-sono" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:12px;">💤 Sono Ninja (Ciclos)</h3>
            <p style="font-size:11px; margin-bottom:15px;">Calcule o ciclo para não acordar grogue.</p>
            <div class="input-group"><label>Que horas você pretende deitar?</label><input type="time" id="sono-dormir-hora"></div>
            <button class="btn-calc" onclick="calcularSonoNinja()">Calcular 3 Ciclos de Sono</button>
            <div id="sono-resultado" style="margin-top:15px; display:none;">
                <div class="qg-item" style="border-left:3px solid var(--success);">
                    <h4>🛌 Sono Excelente (7h30m / 5 ciclos)</h4>
                    <p style="font-size:12px;">Acorde às: <strong id="sono-bom" style="color:var(--success);">--:--</strong></p>
                </div>
                <div class="qg-item" style="border-left:3px solid var(--warning);">
                    <h4>🛏️ Sono Médio (6h00m / 4 ciclos)</h4>
                    <p style="font-size:12px;">Acorde às: <strong id="sono-medio" style="color:var(--warning);">--:--</strong></p>
                </div>
                <div class="qg-item" style="border-left:3px solid var(--info);">
                    <h4>⚡ Cochilo Rápido (3h00m / 2 ciclos)</h4>
                    <p style="font-size:12px;">Acorde às: <strong id="sono-curto" style="color:var(--info);">--:--</strong></p>
                </div>
            </div>
        </div>
    </div>

    <div id="tela-mantra" class="tela-app">
        <div class="card" style="text-align:center;">
            <h3 style="color:var(--primary); margin-bottom:15px;">🙏 Mantra de Partida</h3>
            <p style="font-size:15px; font-style:italic; line-height:1.4; text-align:left; background:rgba(255,107,0,0.1); padding:15px; border-left:4px solid var(--primary); border-radius:8px;">
                "Minha mente é atenta, meu freio é preciso. O asfalto não é pista, é de onde tiro meu sustento. Volto pra casa íntegro, volto pra quem me espera. Com responsabilidade e coragem, eu assumo o controle da rua."
            </p>
            <button class="btn-calc" style="margin-top:20px;" onclick="adicionarXP(10, 'Partida'); voltarContexto()">Mantra Ativado. Fui!</button>
        </div>
    </div>

    <!-- TELA MANUAL E BACKUP REFORMULADA -->
    <div id="tela-manual" class="tela-app">
        <div class="card">
            <h3 style="color:var(--primary); margin-bottom:15px;">📖 Manual e Instruções</h3>
            <div class="qg-item"><strong>Radar Tropa:</strong> Defina seus parâmetros de lucro por km e avalie se a corrida compensa.</div>
            <div class="qg-item"><strong>Teclado Ninja:</strong> Mensagens rápidas editáveis para enviar no chat do cliente.</div>
            <div class="qg-item"><strong>Raio-X:</strong> Calcule o lucro real diário descontando gasolina e alimentação.</div>
            <div class="qg-item"><strong>Metas Ninja:</strong> Acompanhe o progresso das suas metas de ganho diário, semanal e mensal.</div>
            <div class="qg-item"><strong>Doutor Motor & Trocas:</strong> Controle de KM das peças e diagnóstico de falhas comuns.</div>
            <div class="qg-item"><strong>Bases & Postos:</strong> Mapa interativo para guardar locais seguros e parceiros. Toca no mapa ou digita a rua para pesquisar.</div>
            <div class="qg-item"><strong>Chá de Cadeira & CT Ninja:</strong> Cronômetro para o restaurante e 10 minijogos para treinar o cérebro.</div>
        </div>
        
        <div class="card" style="border-color:var(--warning);">
            <h3 style="color:var(--warning); margin-bottom:10px;">💾 Backup e Restauro de Dados</h3>
            <p style="font-size:11px; color:var(--text-muted); margin-bottom:15px;">Vai trocar de telemóvel ou quer guardar o seu histórico? Extraia o seu código de segurança abaixo.</p>
            
            <button class="btn-calc" style="background:var(--warning); color:#000;" onclick="exportarDadosApp()">📤 EXTRAIR MEUS DADOS (COPIAR)</button>
            
            <div style="margin-top:20px; border-top:1px dashed #30363d; padding-top:15px;">
                <p style="font-size:11px; color:var(--text-light); margin-bottom:10px;">Colar dados de outro aparelho:</p>
                <textarea id="input-backup" placeholder="Cole o código do backup aqui..." style="width:100%; height:80px; background:#0f1115; color:#fff; border:1px solid #30363d; border-radius:8px; padding:10px; font-size:12px; margin-bottom:10px;"></textarea>
                <button class="btn-calc" style="background:var(--success);" onclick="importarDadosApp()">📥 RESTAURAR DADOS</button>
            </div>
        </div>
    </div>    <!-- ======================================================== -->
    <!-- PARTE 2: INTELIGÊNCIA DO APLICATIVO (JAVASCRIPT)         -->
    <!-- ======================================================== -->
    <script>
        // --- VARIÁVEIS GLOBAIS E ESTADOS ---
        let xpTropa = parseInt(localStorage.getItem('tropa_xp')) || 0;
        let historicoTelas = ['tela-menu'];
        let metaAtivaAba = 'dia';
        let scrollPosMenu = 0; 
        
        let mapB = null; let mapP = null;
        let marcadoresBases = JSON.parse(localStorage.getItem('t_bases_m')) || [];
        let marcadoresPostos = JSON.parse(localStorage.getItem('t_postos_m')) || [];

        // Variáveis temporárias para o clique no ecrã (mapa)
        let tempMarkB = null; let latSelB = null; let lngSelB = null;
        let tempMarkP = null; let latSelP = null; let lngSelP = null;

        // --- INICIALIZAÇÃO (ONLOAD) ---
        window.onload = () => {
            inicializarRelogio();
            carregarConfiguracoesGerais();
            carregarMensagensNinja();
            carregarLogRaioX();
            carregarHistoricoTrocas();
            carregarNotasYTarefas();
            carregarBasesMap();
            carregarPostosMap();
            carregarDireitosTropa();
            carregarJogosCT();
            carregarMetasTropa();
            
            // Popula Parâmetros do Radar salvos
            document.getElementById('radar-bom').value = localStorage.getItem('t_rad_bom') || 3.0;
            document.getElementById('radar-medio').value = localStorage.getItem('t_rad_med') || 2.0;
            document.getElementById('radar-ruim').value = localStorage.getItem('t_rad_ruim') || 1.5;

            adicionarXP(0, 'Início');
        };

        // --- SISTEMA CORE (NAVEGAÇÃO, RELÓGIO, XP, MODO ESCURO) ---
        function inicializarRelogio() {
            setInterval(() => {
                let d = new Date();
                document.getElementById('relogio-atual').innerText = d.toLocaleTimeString('pt-BR');
            }, 1000);
        }

        function mostrarToast(msg) {
            let t = document.getElementById("toast");
            t.innerText = msg;
            t.className = "show";
            setTimeout(() => { t.className = t.className.replace("show",""); }, 3000);
        }

        function adicionarXP(pts, motivo) {
            xpTropa += pts; 
            localStorage.setItem('tropa_xp', xpTropa);
            document.getElementById('hud-xp').innerText = `XP DA TROPA: ${xpTropa}`;
            let el = document.getElementById('ct-xp-badge'); 
            if (el) el.innerText = `${xpTropa} XP`;
            if (pts > 0) mostrarToast(`+${pts} XP (${motivo})`);
        }

        function carregarConfiguracoesGerais() {
            let mt = localStorage.getItem('t_moto_g') || 'Honda CG 160 Titan';
            document.getElementById('seletor-moto-geral').value = mt;
        }

        function alterarMotoGeral() {
            let m = document.getElementById('seletor-moto-geral').value;
            localStorage.setItem('t_moto_g', m);
            mostrarToast("Moto definida para " + m + "!");
        }

        function abrirTela(id) {
            if (historicoTelas[historicoTelas.length - 1] === id) return;
            if (historicoTelas[historicoTelas.length - 1] === 'tela-menu') scrollPosMenu = window.scrollY;
            
            document.querySelectorAll('.tela-app').forEach(t => t.style.display = 'none');
            document.getElementById('btn-voltar').style.display = 'block';
            
            let alvo = document.getElementById(id);
            if (alvo) {
                alvo.style.display = 'block'; 
                window.scrollTo(0, 0);
                historicoTelas.push(id);
            }
            if (id === 'tela-qgs') initMapaBases();
            if (id === 'tela-postos') initMapaPostos();
        }

        function voltarContexto() {
            if (historicoTelas.length > 1) {
                historicoTelas.pop();
                let anterior = historicoTelas[historicoTelas.length - 1];
                document.querySelectorAll('.tela-app').forEach(t => t.style.display = 'none');
                let prev = document.getElementById(anterior);
                if (prev) {
                    prev.style.display = 'block';
                    if (anterior === 'tela-menu') {
                        document.getElementById('btn-voltar').style.display = 'none';
                        window.scrollTo(0, scrollPosMenu);
                    } else {
                        window.scrollTo(0, 0);
                    }
                }
                pararGameLoops();
            }
        }

        function toggleModoExtremo() {
            document.body.classList.toggle('modo-extremo');
            document.querySelector('.btn-night').innerText = document.body.classList.contains('modo-extremo') ? "☀ Normal" : "🦇 Extremo";
        }

        function atualizarClimaRegiao() {}

        // --- SISTEMA DE BACKUP E RESTAURO ---
        function exportarDadosApp() {
            let backup = {};
            for (let i = 0; i < localStorage.length; i++) {
                let key = localStorage.key(i);
                if (key.startsWith('t_') || key.startsWith('tropa_')) {
                    backup[key] = localStorage.getItem(key);
                }
            }
            // Encripta o JSON para base64 seguro
            let codigo = btoa(encodeURIComponent(JSON.stringify(backup)));
            navigator.clipboard.writeText(codigo).then(() => {
                mostrarToast("📦 Código copiado! Guarde-o nas suas notas ou no WhatsApp.");
            }).catch(err => {
                mostrarToast("Erro ao copiar. Selecione o código e copie manualmente.");
                document.getElementById('input-backup').value = codigo;
            });
        }

        function importarDadosApp() {
            let val = document.getElementById('input-backup').value.trim();
            if (!val) { 
                mostrarToast("Cole o código na caixa primeiro!"); 
                return; 
            }
            try {
                let backup = JSON.parse(decodeURIComponent(atob(val)));
                for (let key in backup) {
                    localStorage.setItem(key, backup[key]);
                }
                mostrarToast("✅ Dados restaurados com sucesso! A reiniciar...");
                setTimeout(() => location.reload(), 1500);
            } catch(e) {
                mostrarToast("❌ Código inválido ou corrompido.");
            }
        }

        // --- 1. RADAR TROPA (AVALIAÇÃO DE CORRIDAS) ---
        function salvarParamsRadar() {
            localStorage.setItem('t_rad_bom', document.getElementById('radar-bom').value);
            localStorage.setItem('t_rad_med', document.getElementById('radar-medio').value);
            localStorage.setItem('t_rad_ruim', document.getElementById('radar-ruim').value);
            mostrarToast("Parâmetros atualizados!");
        }

        function avaliarCorridaCompleta() {
            let valor = parseFloat(document.getElementById('corrida-valor').value) || 0;
            let km = parseFloat(document.getElementById('corrida-km').value) || 1;
            let tempo = parseFloat(document.getElementById('corrida-tempo').value) || 1;
            
            let kmBom = parseFloat(document.getElementById('radar-bom').value) || 3.0;
            let kmMed = parseFloat(document.getElementById('radar-medio').value) || 2.0;
            let kmRuim = parseFloat(document.getElementById('radar-ruim').value) || 1.5;
            
            let ganhoKM = valor / km;
            let ganhoHora = (valor / tempo) * 60;

            document.getElementById('res-valorkm').innerText = "R$ " + ganhoKM.toFixed(2);
            document.getElementById('res-valorhora').innerText = "R$ " + ganhoHora.toFixed(2);
            document.getElementById('radar-resultado').style.display = 'block';

            let b = document.getElementById('radar-veredito');
            let c = document.getElementById('radar-coment');

            if (ganhoKM >= kmBom) {
                b.className = "veredito-box status-ok"; b.innerText = "Excelente 🟢";
                c.innerText = "A margem está ótima! Pegue sem hesitar.";
            } else if (ganhoKM >= kmMed) {
                b.className = "veredito-box status-alert"; b.innerText = "Razoável 🟡";
                c.innerText = "Abaixo do topo de ganhos, mas compensa o corre do dia.";
            } else if (ganhoKM > kmRuim) {
                b.className = "veredito-box status-danger"; b.innerText = "Fique Atento 🟠";
                c.innerText = "Quase não cobre a manutenção. Só pegue se for caminho de volta.";
            } else {
                b.className = "veredito-box status-danger"; b.innerText = "Não Vale a Pena 🔴";
                c.innerText = "Prejuízo na certa. Melhor recusar e aguardar.";
            }
        }

        // --- 2. TECLADO NINJA (MENSAGENS EDITÁVEIS) ---
        let msgNinjaPadrao = [
            "Olá! Já estou no endereço, no ponto de entrega. 📍",
            "Salve! Peguei trânsito carregado, estou a caminho. 🏍️",
            "Endereço incompleto. Pode confirmar o bloco ou número? ❓",
            "Por segurança não subo no AP. Te aguardo aqui na portaria! 🚫",
            "Estou aguardando a liberação do seu pedido na loja. ⏳",
            "Pedido coletado com sucesso! Já estou indo para você. 🚀",
            "Cheguei com sua entrega! Estarei na portaria de moto. 🏁",
            "Por favor, tenha o código de confirmação em mãos. 📲",
            "Obrigado pelas boas vindas e pela gorjeta! Abraços. 🙏",
            "Sem possibilidade de parada segura na frente, estou de lado. ⚠️",
            "Atenção, o aplicativo está instável. Aguarde um instante por favor.",
            "Já estou finalizando a entrega anterior e vou direto pro seu.",
            "Desculpe, pneu furado a caminho. Informei o suporte. 🔧",
            "Por favor, acione a portaria para me liberar a entrada se puder.",
            "Gostaria de uma embalagem extra se necessário, ou algo mais?"
        ];

        function carregarMensagensNinja() {
            let salvos = JSON.parse(localStorage.getItem('t_ninja_m'));
            if(!salvos || salvos.length === 0) {
                salvos = msgNinjaPadrao;
                localStorage.setItem('t_ninja_m', JSON.stringify(salvos));
            }
            let c = document.getElementById('container-mensagens');
            c.innerHTML = '';
            salvos.forEach((m, i) => {
                c.innerHTML += `
                    <div class="log-item">
                        <div class="log-left" style="cursor:pointer;" onclick="copiarTexto('${m.replace(/'/g, "\\'")}')">
                            <span style="color:#fff; font-size:13px;">${m}</span>
                        </div>
                        <div>
                            <button class="btn-del" onclick="removerMensagemNinja(${i})">🗑️</button>
                        </div>
                    </div>`;
            });
        }

        function addMensagemNinja() {
            let txt = document.getElementById('novo-msg-texto').value.trim();
            if (txt) {
                let salvos = JSON.parse(localStorage.getItem('t_ninja_m')) || [];
                salvos.unshift(txt);
                localStorage.setItem('t_ninja_m', JSON.stringify(salvos));
                document.getElementById('novo-msg-texto').value = '';
                carregarMensagensNinja();
                mostrarToast("Mensagem adicionada!");
            }
        }

        function removerMensagemNinja(idx) {
            let salvos = JSON.parse(localStorage.getItem('t_ninja_m')) || [];
            salvos.splice(idx, 1);
            localStorage.setItem('t_ninja_m', JSON.stringify(salvos));
            carregarMensagensNinja();
            mostrarToast("Mensagem excluída.");
        }

        function copiarTexto(t) {
            navigator.clipboard.writeText(t);
            mostrarToast("Copiado com Sucesso!");
        }

        // --- 3. ALERTAS E SOS (WHATSAPP) ---
        function dispararAlertaGrupo() {
            let tipo = document.getElementById('alerta-tipo').value;
            let local = document.getElementById('alerta-local').value;
            if(local) {
                let msg = `🚨 *ALERTA DA TROPA* 🚨\n\n*Tipo:* ${tipo}\n*Local:* ${local}\n\n_Atenção no asfalto!_`;
                window.open(`https://api.whatsapp.com/send?text=${encodeURIComponent(msg)}`, '_blank');
            } else mostrarToast("Digite o local do ocorrido!");
        }

        function dispararRouboWhatsApp() {
            let m = document.getElementById('sos-moto').value;
            let p = document.getElementById('sos-placa').value;
            let l = document.getElementById('sos-local').value;
            if(m && p && l) {
                let msg = `🚨 *ALERTA DE MOTO ROUBADA* 🚨\n\n*Moto:* ${m}\n*Placa:* ${p}\n*Onde foi:* ${l}\n\nAjude a tropa! Quem tiver informações, acione. 🙏`;
                window.open(`https://api.whatsapp.com/send?text=${encodeURIComponent(msg)}`, '_blank');
            } else mostrarToast("Preencha todos os campos do roubo!");
        }

        // --- 4. METAS NINJA (DIÁRIA, SEMANAL, MENSAL) ---
        function alterarMetaTab(aba) {
            metaAtivaAba = aba;
            document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
            document.getElementById('btn-meta-' + aba).classList.add('active');
            
            if (aba === 'dia') {
                document.getElementById('meta-titulo-aba').innerText = "🎯 Planejar Meta Diária";
                document.getElementById('label-meta-alvo').innerText = "Meta Diária Desejada (R$)";
                document.getElementById('label-meta-dias').innerText = "Dias da Semana Trabalhados";
                document.getElementById('label-meta-feito').innerText = "Faturado Hoje (R$)";
                document.getElementById('label-meta-diasfeitos').innerText = "Dias (ou horas) já rodados";
            } else if (aba === 'semana') {
                document.getElementById('meta-titulo-aba').innerText = "📅 Planejar Meta Semanal";
                document.getElementById('label-meta-alvo').innerText = "Meta Semanal Desejada (R$)";
                document.getElementById('label-meta-dias').innerText = "Dias de trampo na semana";
                document.getElementById('label-meta-feito').innerText = "Faturado na semana (R$)";
                document.getElementById('label-meta-diasfeitos').innerText = "Dias trabalhados na semana";
            } else {
                document.getElementById('meta-titulo-aba').innerText = "📆 Planejar Meta Mensal";
                document.getElementById('label-meta-alvo').innerText = "Meta Mensal Desejada (R$)";
                document.getElementById('label-meta-dias').innerText = "Dias de trampo no mês";
                document.getElementById('label-meta-feito').innerText = "Faturado no mês (R$)";
                document.getElementById('label-meta-diasfeitos').innerText = "Dias corridos já trabalhados";
            }
            carregarMetasTropa();
        }

        function salvarMetasTropa() {
            localStorage.setItem(`t_meta_v_${metaAtivaAba}`, document.getElementById('meta-valor-alvo').value);
            localStorage.setItem(`t_meta_d_${metaAtivaAba}`, document.getElementById('meta-dias').value);
            localStorage.setItem(`t_meta_f_${metaAtivaAba}`, document.getElementById('meta-faturado').value);
            localStorage.setItem(`t_meta_df_${metaAtivaAba}`, document.getElementById('meta-diasfeitos').value);
        }

        function carregarMetasTropa() {
            document.getElementById('meta-valor-alvo').value = localStorage.getItem(`t_meta_v_${metaAtivaAba}`) || '';
            document.getElementById('meta-dias').value = localStorage.getItem(`t_meta_d_${metaAtivaAba}`) || '';
            document.getElementById('meta-faturado').value = localStorage.getItem(`t_meta_f_${metaAtivaAba}`) || '';
            document.getElementById('meta-diasfeitos').value = localStorage.getItem(`t_meta_df_${metaAtivaAba}`) || '';
            document.getElementById('metas-resultado').style.display = 'none';
        }

        function calcularMetasTropa() {
            let alvo = parseFloat(document.getElementById('meta-valor-alvo').value) || 0;
            let diasTot = parseFloat(document.getElementById('meta-dias').value) || 1;
            let feito = parseFloat(document.getElementById('meta-faturado').value) || 0;
            let diasFeitos = parseFloat(document.getElementById('meta-diasfeitos').value) || 0;
            
            let diasRestantes = Math.max(1, diasTot - diasFeitos);
            let valorFaltante = Math.max(0, alvo - feito);
            let diarioNecessario = valorFaltante / diasRestantes;

            document.getElementById('metas-valor-necessario').innerText = "R$ " + diarioNecessario.toLocaleString('pt-BR', {minimumFractionDigits: 2});
            document.getElementById('metas-resultado').style.display = 'block';
            
            let prog = Math.min(100, (feito / (alvo || 1)) * 100);
            document.getElementById('metas-progresso-bar').style.width = prog + '%';
            document.getElementById('metas-porcento').innerText = prog.toFixed(0) + '%';
            
            let desc = document.getElementById('metas-res-desc');
            if (prog >= 100) desc.innerText = "🔥 Meta batida! Parabéns, tropa!";
            else if (prog >= 50) desc.innerText = "🚀 Metade do caminho já foi. Continua firme!";
            else desc.innerText = "🏃 Mais asfalto para bater a meta planejada.";
        }

        // --- 5. RAIO-X FINANCEIRO (LUCRO E HISTÓRICO) ---
        function calcularESalvarRaioX() {
            let app = document.getElementById('raiox-app').value;
            let fat = parseFloat(document.getElementById('raiox-fat').value) || 0;
            let km = parseFloat(document.getElementById('raiox-km').value) || 0;
            let gasCost = parseFloat(document.getElementById('raiox-gas').value) || 0;
            let extras = parseFloat(document.getElementById('raiox-extras').value) || 0;
            
            let descTotalGasto = gasCost + extras;
            let lucroReal = fat - descTotalGasto;
            
            let hist = JSON.parse(localStorage.getItem('t_raiox_l')) || [];
            hist.unshift({ data: new Date().toLocaleDateString('pt-BR'), app, fat, gasto: descTotalGasto, lucro: lucroReal, km });
            localStorage.setItem('t_raiox_l', JSON.stringify(hist));
            
            document.getElementById('raiox-fat').value='';
            document.getElementById('raiox-gas').value='';
            
            carregarLogRaioX(); 
            mostrarToast("Lucro calculado e salvo no Histórico!");
        }

        function carregarLogRaioX() {
            let hist = JSON.parse(localStorage.getItem('t_raiox_l')) || [];
            let div = document.getElementById('historico-raiox-lista'); div.innerHTML = '';
            hist.forEach((h, i) => {
                div.innerHTML += `
                    <div class="log-item">
                        <div class="log-left">
                            <span class="log-tag" style="background:var(--primary); color:#000;">${h.app}</span>
                            <span style="color:#fff; font-size:12px; font-weight:bold; margin-top:2px;">Faturamento: R$ ${h.fat.toFixed(2)}</span>
                            <span style="font-size:10px; color:var(--text-muted);">${h.data} • Rodou: ${h.km} km</span>
                        </div>
                        <div style="text-align:right;">
                            <strong style="color:var(--success); font-size:14px;">Lucro: R$ ${h.lucro.toFixed(2)}</strong>
                            <br><button class="btn-del" onclick="deletarItemRaioX(${i})" style="margin-top:5px;">🗑️ Excluir</button>
                        </div>
                    </div>`;
            });
        }

        function deletarItemRaioX(idx) {
            let hist = JSON.parse(localStorage.getItem('t_raiox_l')) || [];
            hist.splice(idx, 1); localStorage.setItem('t_raiox_l', JSON.stringify(hist));
            carregarLogRaioX(); mostrarToast("Excluído.");
        }

        function limparHistoricoRaioX() {
            if(confirm("Tem certeza que deseja apagar todo o histórico de faturamento?")) {
                localStorage.removeItem('t_raiox_l'); carregarLogRaioX(); mostrarToast("Histórico limpo!");
            }
        }

        // --- 6. DOUTOR MOTOR (DIAGNÓSTICOS) ---
        const diagDB = {
            partida: {
                causa: "Bateria arriada, fusível mestre de partida queimado ou mau contato no relé.",
                detalhes: "Caso o painel se apague por completo na hora da partida, ou você apenas ouça um estalo metálico debaixo do assento (tec tec), a energia não está alcançando o motor de arranque.",
                procedimento: "Verifique se a buzina e os faróis funcionam normais; caso estejam sem força, o problema é bateria. Tente dar tranco (2ª marcha) para chegar na oficina."
            },
            fumaça: {
                causa: "Queima indesejada de óleo lubrificante na câmara de combustão (desgaste de anéis/retentores).",
                detalhes: "A emissão de fumaça azulada ou branca contínua indica que a moto está consumindo óleo de motor, o que pode causar o travamento completo se faltar óleo.",
                procedimento: "Verifique o nível na vareta diariamente. Evite rodar sem o nível correto e agende uma retífica (troca de cilindro/anéis)."
            },
            falhando: {
                causa: "Combustível batizado, vela de ignição desgastada ou entupimento na injeção/carburador.",
                detalhes: "O engasgo indica falha de queima elétrica ou falta de fluxo regular de combustível quando é exigido maior torque no acelerador.",
                procedimento: "Verifique e limpe a vela ou o filtro de ar. Se o sintoma for logo após o abastecimento, esvazie o tanque e troque de posto."
            },
            freio: {
                causa: "Presença de bolhas de ar no circuito hidráulico ou desgaste total das pastilhas/lonas.",
                detalhes: "Freios esponjosos, que afundam muito até o limite sem frear, perdem eficácia de resposta, o que gera grande risco de colisão e queda.",
                procedimento: "Faça o sangramento (tirar ar) do sistema de óleo de freio ou substitua a lona traseira se já tiver passado da marcação de desgaste."
            },
            embreagem: {
                causa: "Queima ou desgaste total dos discos de embreagem ou desregulagem extrema do cabo.",
                detalhes: "Quando a embreagem está patinando, a potência do motor não se converte em tração traseira, fazendo a moto girar frouxo e gastar mais combustível.",
                procedimento: "Ajuste a folga no manete ou lá embaixo no motor. Se não resolver, agende a troca do Kit Embreagem (Discos e Separadores)."
            }
        };

        function gerarDiagnosticoDoutorMotor() {
            let s = document.getElementById('diag-sintoma').value;
            let r = document.getElementById('diag-resultado');
            if (diagDB[s]) {
                r.style.display = 'block';
                r.innerHTML = `
                    <h4 style="color:var(--primary); margin-bottom:5px;">🔍 Análise do Doutor Motor</h4>
                    <p style="font-size:12px; margin-bottom:8px;"><strong>Provável Causa:</strong> ${diagDB[s].causa}</p>
                    <p style="font-size:11px; color:var(--text-muted); margin-bottom:10px;">${diagDB[s].detalhes}</p>
                    <p style="font-size:11px; border-top:1px dashed #30363d; padding-top:8px;"><strong>🛠️ O que fazer:</strong> ${diagDB[s].procedimento}</p>`;
            } else r.style.display = 'none';
        }

        // --- 7. CONTROLE MECÂNICO (HISTÓRICO E PRAZOS) ---
        function salvarKMAntigos() {
            let km = parseInt(document.getElementById('mecanico-km-atual').value) || 0;
            localStorage.setItem('t_km_a', km); 
            atualizarVistoriaPrazoManutencao();
        }

        function atualizarVistoriaPrazoManutencao() {
            let atual = parseInt(localStorage.getItem('t_km_a')) || 0;
            document.getElementById('mecanico-km-atual').value = atual > 0 ? atual : '';
            
            let itens = ['oleo', 'oleosint', 'filtro', 'vela', 'relacao', 'freios'];
            itens.forEach(it => {
                let uTroca = parseInt(localStorage.getItem(`t_manu_u_${it}`)) || 0;
                let limite = parseInt(localStorage.getItem(`t_manu_l_${it}`)) || 1000;
                let bg = document.getElementById(`mecanico-badge-${it}`);
                
                if (uTroca === 0) {
                    bg.className = "status-badge status-alert"; bg.innerText = "Sem registro";
                } else {
                    let rodados = atual - uTroca;
                    let resto = limite - rodados;
                    if (resto > 0) {
                        bg.className = "status-badge status-ok"; bg.innerText = `Faltam ${resto} km`;
                    } else {
                        bg.className = "status-badge status-danger"; bg.innerText = `Passou ${Math.abs(resto)} km!`;
                    }
                }
            });
        }

        function registrarTrocaPeca(item, limite) {
            let atual = parseInt(document.getElementById('mecanico-km-atual').value) || 0;
            if (atual === 0) { mostrarToast("Insira o seu KM Atual no painel acima primeiro!"); return; }
            
            let moto = localStorage.getItem('t_moto_g') || 'Moto Tropa';
            let antKm = parseInt(localStorage.getItem(`t_manu_u_${item}`)) || 0;
            
            localStorage.setItem(`t_manu_u_${item}`, atual);
            localStorage.setItem(`t_manu_l_${item}`, limite);
            
            let hist = JSON.parse(localStorage.getItem('t_manu_log')) || [];
            hist.unshift({ data: new Date().toLocaleDateString('pt-BR'), item, km: atual, anterior: antKm, moto });
            localStorage.setItem('t_manu_log', JSON.stringify(hist));
            
            carregarHistoricoTrocas(); 
            atualizarVistoriaPrazoManutencao();
            mostrarToast("Manutenção Registrada com Sucesso!"); 
            adicionarXP(25, 'Cuidou da Máquina');
        }

        function carregarHistoricoTrocas() {
            atualizarVistoriaPrazoManutencao();
            let hist = JSON.parse(localStorage.getItem('t_manu_log')) || [];
            let div = document.getElementById('historico-trocas-lista'); div.innerHTML = '';
            hist.forEach((h, i) => {
                let antStr = h.anterior > 0 ? `Trocado antes no KM: ${h.anterior}` : "Primeiro registro inserido";
                div.innerHTML += `
                    <div class="log-item">
                        <div class="log-left">
                            <span class="log-tag" style="background:#30363d; color:#fff;">${h.moto}</span>
                            <strong style="color:var(--primary); font-size:12px; margin-top:2px;">Substituição: ${h.item.toUpperCase()}</strong>
                            <span style="font-size:10px; color:var(--text-muted);">${h.data} • KM atualizado: ${h.km}</span>
                            <span style="font-size:9px; color:#555;">(${antStr})</span>
                        </div>
                        <div>
                            <button class="btn-del" onclick="deletarItemTroca(${i})">🗑️</button>
                        </div>
                    </div>`;
            });
        }

        function deletarItemTroca(idx) {
            let hist = JSON.parse(localStorage.getItem('t_manu_log')) || [];
            hist.splice(idx, 1); localStorage.setItem('t_manu_log', JSON.stringify(hist));
            carregarHistoricoTrocas(); mostrarToast("Registro apagado.");
        }

        function limparHistoricoTrocas() {
            if(confirm("Deseja apagar todo o histórico de manutenção mecânica?")) {
                localStorage.removeItem('t_manu_log'); 
                carregarHistoricoTrocas(); 
                mostrarToast("Histórico limpo!");
            }
        }

        // --- 8. VIDA DO PNEU (TWI) ---
        function calcularVidaPneu() {
            let mAnterior = parseInt(document.getElementById('pneu-km-anterior').value) || 0;
            let mAtual = parseInt(localStorage.getItem('t_km_a')) || 0;
            
            if (mAnterior === 0 || mAtual === 0) { 
                mostrarToast("Insira o seu KM Atual lá na aba de Controle Mecânico!"); 
                return; 
            }
            
            let rodado = Math.max(0, mAtual - mAnterior);
            let limiteEst = 12000; // Média para motos pequenas urbanas
            let rest = Math.max(0, 100 - ((rodado / limiteEst) * 100));
            
            document.getElementById('pneu-porcento').innerText = rest.toFixed(0) + "% (Rodado: " + rodado + "km)";
            document.getElementById('pneus-barra').style.width = rest + "%";
            document.getElementById('pneus-resultado').style.display = 'block';
            
            let b = document.getElementById('pneu-estado');
            if (rest >= 50) { 
                b.className = "veredito-box status-ok"; b.innerText = "PNEU SEGURO 🟢"; 
            } else if (rest >= 20) { 
                b.className = "veredito-box status-alert"; b.innerText = "ALERTA (MEIO USO) 🟡"; 
            } else { 
                b.className = "veredito-box status-danger"; b.innerText = "PERIGO (LIMITE TWI) 🔴"; 
            }
        }

        // --- 9. MAPAS (LEAFLET.JS) COM GPS, CLIQUE E BUSCA DE ENDEREÇO ---
        // ================= BASES E QGs =================
        function initMapaBases() {
            if(!mapB) {
                mapB = L.map('map-bases').setView([-23.5505, -46.6333], 13);
                L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png').addTo(mapB);
                
                // GPS Automático
                if ("geolocation" in navigator) {
                    navigator.geolocation.getCurrentPosition(pos => {
                        let lat = pos.coords.latitude;
                        let lng = pos.coords.longitude;
                        mapB.setView([lat, lng], 15);
                        L.circleMarker([lat, lng], {color: '#1877F2', radius: 8, fillOpacity: 0.8}).addTo(mapB).bindPopup("Você está aqui!");
                    }, err => { console.log("Acesso ao GPS negado."); });
                }

                // Permite clicar no mapa para gerar um pino provisório
                mapB.on('click', function(e) {
                    latSelB = e.latlng.lat;
                    lngSelB = e.latlng.lng;
                    if(tempMarkB) mapB.removeLayer(tempMarkB);
                    tempMarkB = L.marker([latSelB, lngSelB]).addTo(mapB);
                    mostrarToast("📍 Local marcado no mapa!");
                });
            }
            setTimeout(()=> { mapB.invalidateSize(); carregarPontosNoMapa(mapB, marcadoresBases); }, 300);
        }

        async function salvarQGLive() {
            let end = document.getElementById('qg-endereco').value;
            let desc = document.getElementById('qg-desc').value;
            
            if(!end || !desc) {
                mostrarToast("Preencha a morada e os detalhes da Base.");
                return;
            }

            let lat = latSelB;
            let lng = lngSelB;

            // Se o utilizador digitou a rua mas não tocou no mapa, faz a pesquisa por satélite!
            if (!lat || !lng) {
                mostrarToast("A procurar a morada no satélite...");
                try {
                    let res = await fetch(`https://nominatim.openstreetmap.org/search?format=json&q=${encodeURIComponent(end + ', Brasil')}`);
                    let data = await res.json();
                    if (data && data.length > 0) {
                        lat = parseFloat(data[0].lat);
                        lng = parseFloat(data[0].lon);
                    } else {
                        mostrarToast("Morada não encontrada! Toca no mapa para marcar.");
                        return;
                    }
                } catch(e) {
                    mostrarToast("Erro na pesquisa. Toca no mapa!");
                    return;
                }
            }
            
            let markerObj = {lat, lng, title: "Base/QG: " + end, desc};
            marcadoresBases.push(markerObj); 
            localStorage.setItem('t_bases_m', JSON.stringify(marcadoresBases));
            
            document.getElementById('qg-endereco').value = '';
            document.getElementById('qg-desc').value = '';
            latSelB = null; lngSelB = null;
            if(tempMarkB) { mapB.removeLayer(tempMarkB); tempMarkB = null; }
            
            carregarBasesMap();
            if(mapB) {
                mapB.setView([lat, lng], 15);
                carregarPontosNoMapa(mapB, marcadoresBases);
            }
            
            mostrarToast("Base adicionada no local exato!"); 
            adicionarXP(15, 'Mapeamento Local');
        }

        function carregarBasesMap() {
            let l = document.getElementById('qg-salvos-lista'); l.innerHTML = '';
            marcadoresBases.forEach((b, i) => {
                l.innerHTML += `
                    <div class="log-item">
                        <div class="log-left">
                            <strong>📍 ${b.title}</strong>
                            <span style="font-size:11px; color:var(--text-muted);">${b.desc}</span>
                        </div>
                        <div><button class="btn-del" onclick="removerBaseMap(${i})">🗑️</button></div>
                    </div>`;
            });
        }

        function removerBaseMap(idx) {
            marcadoresBases.splice(idx, 1); 
            localStorage.setItem('t_bases_m', JSON.stringify(marcadoresBases));
            carregarBasesMap();
            if(mapB) {
                mapB.eachLayer(layer => { if(layer instanceof L.Marker) mapB.removeLayer(layer); });
                carregarPontosNoMapa(mapB, marcadoresBases);
            }
            mostrarToast("Base removida.");
        }

        // ================= POSTOS DE COMBUSTÍVEL =================
        function initMapaPostos() {
            if(!mapP) {
                mapP = L.map('map-postos').setView([-23.5505, -46.6333], 13);
                L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png').addTo(mapP);
                
                if ("geolocation" in navigator) {
                    navigator.geolocation.getCurrentPosition(pos => {
                        let lat = pos.coords.latitude;
                        let lng = pos.coords.longitude;
                        mapP.setView([lat, lng], 15);
                        L.circleMarker([lat, lng], {color: '#1877F2', radius: 8, fillOpacity: 0.8}).addTo(mapP).bindPopup("Você está aqui!");
                    }, err => { console.log("GPS negado."); });
                }

                mapP.on('click', function(e) {
                    latSelP = e.latlng.lat;
                    lngSelP = e.latlng.lng;
                    if(tempMarkP) mapP.removeLayer(tempMarkP);
                    tempMarkP = L.marker([latSelP, lngSelP]).addTo(mapP);
                    mostrarToast("📍 Local do posto marcado no mapa!");
                });
            }
            setTimeout(()=> { mapP.invalidateSize(); carregarPontosNoMapa(mapP, marcadoresPostos); }, 300);
        }

        async function salvarPostoLive() {
            let end = document.getElementById('posto-endereco').value;
            let preco = parseFloat(document.getElementById('posto-preco').value) || 0;
            let nota = document.getElementById('posto-nota').value;
            
            if (!end || preco <= 0) {
                mostrarToast("Preencha o nome/rua e o preço do posto.");
                return;
            }

            let lat = latSelP;
            let lng = lngSelP;

            // Satélite caso o utilizador não toque no mapa
            if (!lat || !lng) {
                mostrarToast("A procurar a morada no satélite...");
                try {
                    let res = await fetch(`https://nominatim.openstreetmap.org/search?format=json&q=${encodeURIComponent(end + ', Brasil')}`);
                    let data = await res.json();
                    if (data && data.length > 0) {
                        lat = parseFloat(data[0].lat);
                        lng = parseFloat(data[0].lon);
                    } else {
                        mostrarToast("Posto não encontrado! Toca no mapa para marcar.");
                        return;
                    }
                } catch(e) {
                    mostrarToast("Erro na pesquisa. Toca no mapa!");
                    return;
                }
            }

            let markerObj = {lat, lng, title: "Posto: " + end, desc: `Gasolina: R$ ${preco.toFixed(2)} | Qualidade: ${nota}`};
            marcadoresPostos.push(markerObj); 
            localStorage.setItem('t_postos_m', JSON.stringify(marcadoresPostos));
            
            document.getElementById('posto-endereco').value = '';
            document.getElementById('posto-preco').value = '';
            
            latSelP = null; lngSelP = null;
            if(tempMarkP) { mapP.removeLayer(tempMarkP); tempMarkP = null; }
            
            carregarPostosMap();
            if(mapP) {
                mapP.setView([lat, lng], 15);
                carregarPontosNoMapa(mapP, marcadoresPostos);
            }
            mostrarToast("Posto adicionado com localização exata!"); 
            adicionarXP(15, 'Posto Parceiro cadastrado');
        }

        function carregarPostosMap() {
            let l = document.getElementById('postos-salvos-lista'); l.innerHTML = '';
            marcadoresPostos.forEach((p, i) => {
                l.innerHTML += `
                    <div class="log-item">
                        <div class="log-left">
                            <strong>⛽ ${p.title}</strong>
                            <span style="font-size:11px; color:var(--text-muted);">${p.desc}</span>
                        </div>
                        <div><button class="btn-del" onclick="removerPostoMap(${i})">🗑️</button></div>
                    </div>`;
            });
        }

        function removerPostoMap(idx) {
            marcadoresPostos.splice(idx, 1); 
            localStorage.setItem('t_postos_m', JSON.stringify(marcadoresPostos));
            carregarPostosMap();
            if(mapP) {
                mapP.eachLayer(layer => { if(layer instanceof L.Marker) mapP.removeLayer(layer); });
                carregarPontosNoMapa(mapP, marcadoresPostos);
            }
        }

        // Renderizador de PINOS reais
        function carregarPontosNoMapa(mapObj, list) {
            list.forEach(m => { 
                L.marker([m.lat, m.lng]).addTo(mapObj)
                 .bindPopup(`<b>${m.title}</b><br>${m.desc}`)
                 .openPopup(); 
            });
        }

        // --- 10. BOMBA FLEX ---
        function calcularBombaFlex() {
            let gas = parseFloat(document.getElementById('bomba-gasolina').value) || 0;
            let alc = parseFloat(document.getElementById('bomba-etanol').value) || 0;
            if (gas > 0 && alc > 0) {
                let perc = (alc / gas) * 100;
                document.getElementById('bomba-porcento').innerText = perc.toFixed(0) + "%";
                document.getElementById('bomba-resultado').style.display = "block";
                
                let b = document.getElementById('bomba-veredito');
                if (perc < 70) { 
                    b.className = "veredito-box status-ok"; b.innerText = "ABASTEÇA ETANOL! 🌿"; 
                } else { 
                    b.className = "veredito-box status-danger"; b.innerText = "ABASTEÇA GASOLINA! ⛽"; 
                }
            } else {
                mostrarToast("Insira os preços primeiro!");
            }
        }

        // --- 11. CHECKLIST DE SAÍDA ---
        function salvarCheckListEstático(id) {
            let ch = document.getElementById('chk-checklist-' + id).checked;
            localStorage.setItem('t_check_est_' + id, ch);
        }

        function salvarChecklistCompleto() {
            mostrarToast("Inspeção Concluída! Boa sorte no corre.");
            adicionarXP(10, 'Prevenção Diária'); 
            voltarContexto();
        }

        // --- 12. CHÁ DE CADEIRA (CRONÔMETRO) ---
        let cTimer = null; 
        let tRestante = 900; // 15 Minutos Padrão
        
        function iniciarCronometroCha() {
            if (cTimer) return;
            cTimer = setInterval(() => {
                if (tRestante > 0) {
                    tRestante--;
                    let m = Math.floor(tRestante / 60); 
                    let s = tRestante % 60;
                    document.getElementById('cha-display').innerText = `${String(m).padStart(2, '0')}:${String(s).padStart(2, '0')}`;
                } else {
                    zerarCronometroCha(); 
                    mostrarToast("Pronto! Já deu 15 min. Pode cobrar a taxa!");
                    adicionarXP(30, 'Paciência de Monge');
                }
            }, 1000);
        }

        function pausarCronometroCha() { 
            clearInterval(cTimer); 
            cTimer = null; 
        }

        function zerarCronometroCha() { 
            pausarCronometroCha(); 
            tRestante = 900; 
            document.getElementById('cha-display').innerText = "15:00"; 
        }

        // --- 13. CT NINJA (10 JOGOS DE TREINO MENTAL) ---
        const listaJogosCT = [
            { id: "j_reflexo", ic: "🟢", nome: "Reação Rápida", hab: "Reflexo", desc: "Meça seu tempo de resposta. Ajuda a treinar freagens de emergência e reação rápida no trânsito.", c: "var(--danger)" },
            { id: "j_visao", ic: "👀", nome: "Visão Periférica", hab: "Foco Visual", desc: "Encontre os números em ordem rápida. Melhora a agilidade de ler placas, números e prever atalhos.", c: "var(--primary)" },
            { id: "j_calculo", ic: "🧮", nome: "Matemática", hab: "Troco", desc: "Cálculos mentais de troco para não errar dinheiro nem tomar prejuízo na correria do dia a dia.", c: "var(--warning)" },
            { id: "j_memoria", ic: "🧠", nome: "Memória Genial", hab: "Rotas", desc: "Decore o padrão de luzes que piscar. Estimula o cérebro a decorar ruas, senhas de portão e caminhos.", c: "#1877F2" },
            { id: "j_impulso", ic: "🚦", nome: "Controle de Impulso", hab: "Paciência", desc: "Sinal verde passa, vermelho para. Treina a ansiedade de querer furar o semáforo antes da hora.", c: "var(--success)" },
            { id: "j_perigos", ic: "⚠️", nome: "Rastreio de Risco", hab: "Defesa", desc: "Ache o emoji de perigo no meio dos carros. Estimula o foco em prever buracos e portas a abrir.", c: "#ff4444" },
            { id: "j_alvos", ic: "🎯", nome: "Foco Fixo", hab: "Atenção", desc: "Acerta só no alvo certo e ignora distrações em movimento. Mantém sua visão onde interessa rodando.", c: "#1DB954" },
            { id: "j_seq", ic: "🧩", nome: "Padrões Lógicos", hab: "Lógica", desc: "Descubra qual cor segue a sequência lógica da rua e preveja padrões de trânsito em movimento.", c: "#9b59b6" },
            { id: "j_dir", ic: "🧭", nome: "Bússola Exata", hab: "Espaço", desc: "Lembra para onde apontava a seta? Melhora o seu GPS mental para não depender do telemóvel o tempo todo.", c: "#34495e" },
            { id: "j_dif", ic: "🔎", nome: "Ponto Cego", hab: "Detalhes", desc: "Ache o veículo diferente no meio da manada. Melhora a percepção rápida no retrovisor e em pontos cegos.", c: "#e67e22" }
        ];

        function carregarJogosCT() {
            let div = document.getElementById('ct-lista-jogos'); 
            div.innerHTML = '';
            listaJogosCT.forEach(j => {
                div.innerHTML += `
                    <div class="qg-item" style="border-left: 4px solid ${j.c};">
                        <div style="display:flex; justify-content:space-between; align-items:center;">
                            <h4 style="color:var(--text-light);">${j.ic} ${j.nome}</h4>
                            <span style="font-size:10px; background:#30363d; padding:3px 6px; border-radius:4px;">${j.hab}</span>
                        </div>
                        <p style="font-size:11px; color:var(--text-muted); margin-top:4px;">${j.desc}</p>
                        <button class="btn-calc" style="background:${j.c}; ${j.c === 'var(--warning)' ? 'color:#000;' : ''} padding:8px; font-size:12px; margin-top:8px;" onclick="iniciarJogo('${j.id}')">🎮 COMEÇAR TREINO</button>
                    </div>`;
            });
        }

        let loopG = null; 
        let jgAt = {};
        
        function pararGameLoops() {
            if(loopG) clearTimeout(loopG); 
            if(loopG) clearInterval(loopG);
            let gs = document.getElementById('game-over-screen'); 
            if(gs) gs.style.display = 'none';
            let cv = document.getElementById('game-canvas');
            if(cv) { 
                cv.style.pointerEvents = 'auto'; 
                cv.innerHTML = ''; 
                cv.style.backgroundColor = '#000'; 
                cv.style.color = '#fff'; 
                cv.onclick = null; 
            }
        }

        function iniciarJogo(id) {
            jgAt = listaJogosCT.find(x => x.id === id); 
            abrirTela('tela-jogo-ativo'); 
            pararGameLoops();
            
            document.getElementById('game-title').innerText = jgAt.ic + " " + jgAt.nome;
            document.getElementById('game-desc').innerText = "Treino de: " + jgAt.hab;
            document.getElementById('game-recorde').innerText = localStorage.getItem('t_rec_' + id) || 0;
            document.getElementById('game-score').innerText = '0';
            
            if (id === 'j_reflexo') startJogoReflexo();
            else if (id === 'j_visao') startJogoSchulte();
            else if (id === 'j_calculo') startJogoTroco();
            else if (id === 'j_memoria') startJogoMemoria();
            else if (id === 'j_impulso') startJogoImpulso();
            else if (id === 'j_perigos') startJogoPerigo();
            else if (id === 'j_alvos') startJogoAlvo();
            else if (id === 'j_seq') startJogoSeq();
            else if (id === 'j_dir') startJogoDir();
            else if (id === 'j_dif') startJogoDif();
        }

        function finalizarJogo(pts) {
            let rec = parseInt(localStorage.getItem('t_rec_' + jgAt.id)) || 0;
            if (pts > rec) {
                localStorage.setItem('t_rec_' + jgAt.id, pts);
                mostrarToast("🏆 NOVO RECORDE BATIDO!"); 
                document.getElementById('game-recorde').innerText = pts;
            }
            document.getElementById('game-canvas').style.pointerEvents = 'none';
            document.getElementById('go-score').innerText = pts;
            document.getElementById('go-benefit').innerText = jgAt.desc;
            document.getElementById('game-over-screen').style.display = 'block';
            
            // Recompensa XP
            adicionarXP(Math.max(1, Math.floor(pts / 10)), 'Treino no CT Ninja');
        }

        function reiniciarJogoAtual() { iniciarJogo(jgAt.id); }

        // --- Simuladores Ninja Lógicas ---
        
        let refTimeout, refStart;
        function startJogoReflexo() {
            let cv = document.getElementById('game-canvas'); 
            cv.style.backgroundColor = 'var(--danger)'; 
            cv.innerHTML = '<h2 style="font-size:24px;">AGUARDE...</h2><p style="font-size:12px; margin-top:10px;">Toque no ecrã quando ficar VERDE.</p>';
            
            cv.onclick = () => { 
                clearTimeout(refTimeout); 
                cv.style.backgroundColor = '#30363d'; 
                cv.innerHTML = '<h2>QUEIMOU A LARGADA!</h2>'; 
                cv.onclick=null; 
                setTimeout(() => finalizarJogo(0), 1000); 
            };
            
            refTimeout = setTimeout(() => { 
                cv.style.backgroundColor = 'var(--success)'; 
                cv.innerHTML = '<h1 style="font-size:40px;">💥 FREIA!!! 💥</h1>'; 
                refStart = Date.now(); 
                cv.onclick = () => { 
                    let ms = Date.now() - refStart; 
                    cv.onclick = null; 
                    cv.style.backgroundColor = '#111'; 
                    cv.innerHTML = `<h2>Tempo: ${ms} ms</h2>`; 
                    setTimeout(() => finalizarJogo(Math.max(0, 1000 - ms)), 1200); 
                }; 
            }, Math.floor(Math.random()*3000) + 1200);
        }

        function startJogoSchulte() {
            let cv = document.getElementById('game-canvas'); 
            cv.innerHTML = '<div class="grid-4x4" id="s-grid"></div><p style="font-size:12px; margin-top:15px;">Toque nos números em ordem do 1 ao 16 rapidamente.</p>';
            let curr = 1; let st = Date.now(); 
            let nums = Array.from({length: 16}, (_, i) => i + 1).sort(() => Math.random() - 0.5);
            
            nums.forEach(n => { 
                let btn = document.createElement('button'); 
                btn.className = 'grid-btn'; 
                btn.innerText = n; 
                btn.onclick = () => { 
                    if(n === curr) { 
                        btn.style.opacity = '0.1'; curr++; 
                        document.getElementById('game-score').innerText = curr - 1; 
                        if(curr > 16) { 
                            let t = (Date.now() - st)/1000; 
                            finalizarJogo(Math.max(0, Math.floor(1000 - (t*15)))); 
                        } 
                    } 
                }; 
                document.getElementById('s-grid').appendChild(btn); 
            });
        }

        function startJogoTroco() {
            let cv = document.getElementById('game-canvas'); let pts = 0; let rod = 4;
            function run() {
                if(rod===0) return finalizarJogo(pts*100);
                let v = Math.floor(Math.random()*40)+15; 
                let p = 50; while(p<v) p+=50; 
                let tc = p-v;
                
                cv.innerHTML = `
                    <h4>Faltam: ${rod} rondas</h4>
                    <div class="veredito-box" style="background:#1c1f26; border:1px dashed var(--warning); color:var(--text-light); margin:15px 0;">
                        O Pedido deu <strong>R$ ${v}</strong> <br> Pagou com nota de <strong>R$ ${p}</strong>
                    </div>
                    <p style="font-size:12px; margin-bottom:10px;">Qual é o troco certo?</p>
                    <div class="grid-4x4" id="t-g" style="grid-template-columns:1fr 1fr; gap:5px;"></div>`;
                
                let opc = [tc, tc+3, tc-4>0?tc-4:tc+6, tc+12].sort(()=>Math.random()-0.5);
                opc.forEach(o => { 
                    let b = document.createElement('button'); b.className = 'grid-btn'; b.innerText = `R$ ${o}`; 
                    b.onclick = () => { 
                        if(o===tc) { pts++; document.getElementById('game-score').innerText = pts*100; } 
                        rod--; run(); 
                    }; 
                    document.getElementById('t-g').appendChild(b); 
                });
            } run();
        }

        function startJogoMemoria() {
            let cv = document.getElementById('game-canvas'); 
            cv.innerHTML = '<div class="grid-4x4" id="m-g" style="grid-template-columns:1fr 1fr; gap:10px;"></div><p id="m-msg" style="margin-top:15px; font-size:12px; font-weight:bold;">Presta atenção na ordem!</p>';
            let c = ['#FF6B00', '#25D366', '#1877F2', '#ffc107']; 
            let g = document.getElementById('m-g'); 
            let seq = []; let pSeq = []; let r = 1;
            
            c.forEach((color, i) => { 
                let d = document.createElement('div'); 
                d.style.width='60px'; d.style.height='60px'; d.style.background='#30363d'; d.style.borderRadius='8px'; 
                d.id='cb-'+i; d.onclick = () => uC(i); g.appendChild(d); 
            });
            
            function playSeq() { 
                document.getElementById('m-msg').innerText = "A decorar o caminho..."; g.style.pointerEvents = 'none'; 
                seq.push(Math.floor(Math.random()*4)); pSeq = []; let i = 0; 
                let int = setInterval(() => { 
                    let b = document.getElementById('cb-'+seq[i]); b.style.background = c[seq[i]]; 
                    setTimeout(()=> b.style.background='#30363d', 400); i++; 
                    if(i >= seq.length) { 
                        clearInterval(int); 
                        setTimeout(()=>{ document.getElementById('m-msg').innerText = "Sua Vez! Repita."; g.style.pointerEvents = 'auto';}, 500); 
                    } 
                }, 800); 
            }
            function uC(idx) { 
                let b = document.getElementById('cb-'+idx); b.style.background = c[idx]; setTimeout(()=> b.style.background='#30363d', 200); 
                pSeq.push(idx); 
                if(pSeq[pSeq.length-1] !== seq[pSeq.length-1]) { finalizarJogo((r-1)*100); return; } 
                if(pSeq.length === seq.length) { document.getElementById('game-score').innerText = r*100; r++; setTimeout(playSeq, 1000); } 
            } setTimeout(playSeq, 1000);
        }

        function startJogoImpulso() {
            let cv = document.getElementById('game-canvas'); 
            let colors = ['🔴', '🟡', '🟢']; let pts = 0; let act = true;
            cv.innerHTML = '<h2 id="i-t" style="font-size:70px;">🔴</h2><p style="font-size:12px; margin-top:15px; color:var(--text-muted);">Toque APENAS quando for o Sinal Verde (🟢).</p>';
            
            cv.onclick = () => { 
                if(!act) return; 
                let t = document.getElementById('i-t').innerText; 
                if(t === '🟢') { 
                    pts+=100; document.getElementById('game-score').innerText = pts; 
                } else { 
                    act = false; finalizarJogo(pts); 
                } 
            };
            function next() { 
                if(!act) return; 
                let c = colors[Math.floor(Math.random()*colors.length)]; 
                document.getElementById('i-t').innerText = c; 
                loopG = setTimeout(next, Math.floor(Math.random()*700)+550); 
            } next();
        }

        function startJogoPerigo() {
            let cv = document.getElementById('game-canvas'); let pts = 0; let r = 4;
            function run() {
                if(r===0) return finalizarJogo(pts*100);
                cv.innerHTML = '<div class="grid-4x4" id="p-g" style="font-size:32px;"></div><p style="font-size:12px; margin-top:15px;">Encontre o perigo na rua: ⚠️</p>'; 
                let arr = Array(15).fill('🚗'); arr.push('⚠️'); arr.sort(()=>Math.random()-0.5);
                arr.forEach(i => { 
                    let b = document.createElement('div'); b.style.cursor="pointer"; b.innerText = i; 
                    b.onclick = () => { 
                        if(i==='⚠️') { pts++; document.getElementById('game-score').innerText=pts*100; r--; run(); } 
                        else { finalizarJogo(pts*100); } 
                    }; 
                    document.getElementById('p-g').appendChild(b); 
                });
            } run();
        }

        function startJogoAlvo() {
            let cv = document.getElementById('game-canvas'); 
            let emojis = ['🔴','🟡','🔵']; let pts = 0; let act = true;
            cv.innerHTML = '<h2 id="a-t" style="font-size:70px;">🔴</h2><p style="font-size:12px; margin-top:15px;">Toque APENAS na bola Azul (🔵).</p>';
            cv.onclick = () => { 
                if(!act) return; 
                let t = document.getElementById('a-t').innerText; 
                if(t === '🔵') { pts+=100; document.getElementById('game-score').innerText = pts; } 
                else { act = false; finalizarJogo(pts); } 
            };
            function next() { 
                if(!act) return; 
                document.getElementById('a-t').innerText = emojis[Math.floor(Math.random()*emojis.length)]; 
                loopG = setTimeout(next, Math.floor(Math.random()*700)+500); 
            } next();
        }

        function startJogoSeq() {
            let cv = document.getElementById('game-canvas'); let pts = 0; let r = 4;
            function run() {
                if(r===0) return finalizarJogo(pts*100);
                cv.innerHTML = `<h2 style="letter-spacing:10px;">🔴🔵🟢🔴🔵 ?</h2><p style="font-size:12px; margin-top:10px;">Qual é a lógica do próximo farol?</p><div style="display:flex; gap:20px; margin-top:15px;" id="s-opts"></div>`;
                ['🔴','🔵','🟢'].sort(()=>Math.random()-0.5).forEach(o => { 
                    let b = document.createElement('button'); b.className='grid-btn'; b.style.width='60px'; b.innerText=o; 
                    b.onclick=()=>{ 
                        if(o==='🟢') { pts++; document.getElementById('game-score').innerText=pts*100; r--; run(); } 
                        else { finalizarJogo(pts*100); } 
                    }; 
                    document.getElementById('s-opts').appendChild(b); 
                });
            } run();
        }

        function startJogoDir() {
            let cv = document.getElementById('game-canvas'); let r = 1;
            function run() {
                let seq = []; let setas = ['⬆️','➡️','⬇️','⬅️']; 
                for(let i=0; i<3; i++) seq.push(setas[Math.floor(Math.random()*4)]);
                
                cv.innerHTML = `<h2>Decore a SEGUNDA seta!</h2><h1 id="d-t" style="font-size:60px; margin-top:20px;">⏳</h1>`;
                let i=0; 
                let show = setInterval(()=>{ 
                    document.getElementById('d-t').innerText = seq[i]; i++; 
                    if(i>=3){ 
                        clearInterval(show); 
                        setTimeout(()=>{ 
                            cv.innerHTML = `<h2>Qual foi a direção da 2ª seta?</h2><div style="display:flex; gap:10px; margin-top:20px;" id="d-opts"></div>`; 
                            setas.forEach(s => { 
                                let b = document.createElement('button'); b.className='grid-btn'; b.style.width='60px'; b.innerText=s; 
                                b.onclick=()=>{ 
                                    if(s===seq[1]) { document.getElementById('game-score').innerText=r*100; r++; run(); } 
                                    else { finalizarJogo((r-1)*100); } 
                                }; 
                                document.getElementById('d-opts').appendChild(b); 
                            }); 
                        }, 1000); 
                    } 
                }, 800);
            } run();
        }

        function startJogoDif() {
            let cv = document.getElementById('game-canvas'); let pts = 0; let r = 4;
            function run() {
                if(r===0) return finalizarJogo(pts*100);
                cv.innerHTML = '<div class="grid-4x4" id="d-g" style="font-size:32px;"></div><p style="font-size:12px; margin-top:15px;">Ache a pequena scooter no meio das motos.</p>'; 
                let arr = Array(15).fill('🏍️'); arr.push('🛵'); arr.sort(()=>Math.random()-0.5);
                arr.forEach(i => { 
                    let b = document.createElement('div'); b.style.cursor="pointer"; b.innerText = i; 
                    b.onclick = () => { 
                        if(i==='🛵') { pts++; document.getElementById('game-score').innerText=pts*100; r--; run(); } 
                        else { finalizarJogo(pts*100); } 
                    }; 
                    document.getElementById('d-g').appendChild(b); 
                });
            } run();
        }

        // --- 14. BLOCO DE NOTAS E TAREFAS ---
        function salvarBlocoTexto() { 
            localStorage.setItem('t_bloco_t', document.getElementById('bloco-texto').value); 
        }
        
        function addTarefaTropa() {
            let txt = document.getElementById('novo-tarefa').value.trim();
            if(txt) {
                let list = JSON.parse(localStorage.getItem('t_tarefas')) || [];
                list.push({id:Date.now(), text:txt}); 
                localStorage.setItem('t_tarefas', JSON.stringify(list));
                document.getElementById('novo-tarefa').value = ''; 
                carregarNotasYTarefas();
            }
        }

        function carregarNotasYTarefas() {
            document.getElementById('bloco-texto').value = localStorage.getItem('t_bloco_t') || '';
            let list = JSON.parse(localStorage.getItem('t_tarefas')) || [];
            let div = document.getElementById('tarefas-lista'); div.innerHTML = '';
            list.forEach(t => {
                div.innerHTML += `
                    <div class="log-item">
                        <span>📝 ${t.text}</span>
                        <button class="btn-del" onclick="removerTarefaTropa(${t.id})">❌</button>
                    </div>`;
            });
        }

        function removerTarefaTropa(id) {
            let list = JSON.parse(localStorage.getItem('t_tarefas')) || [];
            list = list.filter(t => t.id !== id); 
            localStorage.setItem('t_tarefas', JSON.stringify(list));
            carregarNotasYTarefas();
        }

        // --- 15. DIREITOS DA TROPA (Biblioteca Legal Expandida) ---
        const direitosTropa = [
            {t: "Adicional de Periculosidade", d: "A lei garante 30% a mais no salário base para quem trabalha de moto via CLT, pelo risco constante no trânsito urbano."},
            {t: "Subir no Apartamento?", d: "A entrega é finalizada na portaria, ou no primeiro ponto de controle. Você não tem obrigação legal nem contratual (segundo as regras do Ifood) de subir."},
            {t: "Mostrar a Tela do App", d: "Seguranças ou porteiros não podem obrigá-lo a mostrar a tela do telemóvel por causa da Lei Geral de Proteção de Dados (LGPD). É uma questão de privacidade, mostre apenas por cortesia se desejar."},
            {t: "Atraso no Restaurante", d: "Restaurantes não podem reter o estafeta. Após 15 a 20 minutos de espera, você tem o direito de solicitar o cancelamento ao suporte e cobrar a taxa de deslocação."},
            {t: "Gorjeta é 100% Sua", d: "É ilegal qualquer aplicativo ou restaurante reter o valor repassado como gorjeta pelo cliente de forma alguma."},
            {t: "Local de Descanso (Ex: SP)", d: "Por leis municipais aprovadas em diversas capitais (como São Paulo), os aplicativos devem garantir pontos de apoio físicos ou parcerias com casas de banho e água."},
            {t: "Direito de Recusa a Áreas de Risco", d: "O profissional autónomo tem o direito de recusar chamadas que o direcionem para áreas de conhecido risco de segurança sem sofrer bloqueio permanente."},
            {t: "Bloqueio Injusto / Desativado", d: "Os apps são obrigados a fornecer o motivo claro em caso de bloqueio. Desativação sem notificação prévia e justificativa fundamentada gera direito a indemnização judicial."},
            {t: "Peso Máximo do Baú", d: "Você não é obrigado a transportar mercadorias com pesos excessivos ou volumes que ultrapassem as regras do CONTRAN (não pode exceder a largura do guiador e tem um limite geral de 20kg na traseira)."},
            {t: "Abordagem e Identificação Policial", d: "Durante uma operação stop/blitz, a PM tem o direito de solicitar os documentos (Doc e CNH). Mantenha a calma, retire o capacete para identificação fácil e mantenha as mãos visíveis; é procedimento padrão de segurança."}
        ];

        function carregarDireitosTropa() {
            let c = document.getElementById('direitos-container');
            c.innerHTML = '';
            direitosTropa.forEach(dir => {
                c.innerHTML += `
                <div class="qg-item" style="border-left: 3px solid var(--info);">
                    <h4 style="color:var(--text-light); margin-bottom:5px;">${dir.t}</h4>
                    <p style="font-size:11px; color:var(--text-muted); line-height:1.4;">${dir.d}</p>
                </div>`;
            });
        }

        // --- 16. SONO NINJA (CICLOS BIOLÓGICOS) ---
        function calcularSonoNinja() {
            let val = document.getElementById('sono-dormir-hora').value;
            if(!val) { mostrarToast("Insira o horário que vai deitar primeiro!"); return; }
            
            let [h,m] = val.split(':').map(Number); 
            let d = new Date(); d.setHours(h,m,0); 
            
            // O tempo médio para adormecer é de 14 minutos (adicionado ao cálculo).
            let adormecer = 14 * 60000;
            
            // Ciclos ideais: 5 (ótimo), 4 (médio) e 2 (cochilo de emergência)
            let sBom = new Date(d.getTime() + adormecer + (5 * 90 * 60000));
            let sMedio = new Date(d.getTime() + adormecer + (4 * 90 * 60000));
            let sCurto = new Date(d.getTime() + adormecer + (2 * 90 * 60000));

            function format(date) { return String(date.getHours()).padStart(2,'0') + ":" + String(date.getMinutes()).padStart(2,'0'); }

            document.getElementById('sono-bom').innerText = format(sBom);
            document.getElementById('sono-medio').innerText = format(sMedio);
            document.getElementById('sono-curto').innerText = format(sCurto);
            
            document.getElementById('sono-resultado').style.display = 'block';
            mostrarToast("Horários de despertar calculados!");
        }

    </script>
</body>
</html>
