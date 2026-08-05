<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
    <title>D Laser Premium</title>
    
    <meta name="theme-color" content="#0a0a0f">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    
    <link rel="stylesheet" href="style.css">
    
    <!-- Google Fonts (10 fontes padrão para gravação a laser) -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700;900&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Loading -->
    <div id="loadingOverlay">
        <div class="loader">
            <div class="loader-ring"></div>
            <p>Carregando...</p>
        </div>
    </div>

    <div class="container" id="app">
        <!-- Header com Logo -->
        <header class="header">
            <div class="header-top">
                <div class="logo-container">
                    <div class="logo">
                        <span class="logo-d">D</span>
                        <span class="logo-laser">Laser</span>
                        <span class="logo-premium">Premium</span>
                    </div>
                </div>
            </div>
            <p class="header-subtitle">⚡ Escolha sua fonte e personalize sua gravação</p>
        </header>

        <!-- Formulário -->
        <div class="form-card">
            <!-- Campo Nome -->
            <div class="form-group">
                <label for="nome" class="form-label">
                    <span class="label-icon">👤</span>
                    Digite seu nome
                </label>
                <div class="input-wrapper">
                    <input 
                        type="text" 
                        id="nome" 
                        placeholder="Ex: João Silva" 
                        maxlength="25"
                        autocomplete="off"
                        spellcheck="false"
                    >
                    <button class="clear-btn" id="clearBtn" aria-label="Limpar">✕</button>
                </div>
                <div class="input-hint">
                    <span id="charCount">0</span> / 25 caracteres
                </div>
            </div>

            <!-- Aba de Fontes -->
            <div class="form-group">
                <label class="form-label">
                    <span class="label-icon">✏️</span>
                    Escolha sua fonte
                </label>
                <div class="font-tabs" id="fontTabs">
                    <!-- As fontes serão inseridas via JavaScript -->
                </div>
            </div>

            <!-- Prévia -->
            <div class="preview-section">
                <div class="preview-label">Pré-visualização</div>
                <div class="preview-container" id="previaContainer">
                    <div class="preview-text" id="previa">JOÃO</div>
                    <span class="preview-badge">AO VIVO</span>
                </div>
            </div>

            <!-- Botão CRIAR -->
            <button class="btn-submit" id="btnEnviar">
                <span class="btn-content">
                    <span class="btn-icon">✨</span>
                    <span class="btn-text">Criar</span>
                </span>
                <span class="btn-ripple"></span>
            </button>
        </div>

        <!-- Resultado (QR Code) -->
        <div id="resultado" style="display: none;">
            <div class="result-card">
                <div class="result-animation">
                    <span class="checkmark">✅</span>
                </div>
                <h2 class="result-title">Pedido Criado!</h2>
                <p class="result-subtitle">Seu pedido foi gerado com sucesso</p>
                
                <div class="result-id">
                    <span class="id-label">Pedido</span>
                    <span class="id-number" id="pedidoId">#001</span>
                </div>

                <div class="qr-container">
                    <div class="qr-wrapper" id="qrCodeContainer"></div>
                    <div class="qr-shine"></div>
                </div>

                <p class="qr-instruction">
                    <span class="instruction-icon">📱</span>
                    Aproxime este QR Code na máquina de gravação
                </p>

                <button class="btn-new-order" id="btnNovoPedido">
                    <span class="btn-icon">🔄</span>
                    Novo Pedido
                </button>
            </div>
        </div>

        <!-- Footer -->
        <footer class="footer">
            <p>© 2026 D Laser Premium • Todos os direitos reservados</p>
        </footer>
    </div>

    <!-- Toast -->
    <div id="toast" class="toast">
        <span class="toast-icon">✅</span>
        <span class="toast-message">Pedido criado com sucesso!</span>
    </div>

    <script src="app.js"></script>
</body>
</html>
