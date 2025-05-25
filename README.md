from pathlib import Path

# Novo conteúdo HTML com a frase "você é incrível demais", corações e lírios (representados por emoji para simplicidade)
html_content_custom = """
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Você é Incrível Demais!</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #fff0f5;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
      position: relative;
    }
    .message {
      text-align: center;
      z-index: 10;
    }
    .message h1 {
      color: #d63384;
      font-size: 2.8em;
    }
    .float {
      position: absolute;
      font-size: 2em;
      animation: floatUp 7s linear infinite;
      opacity: 0.8;
    }
    @keyframes floatUp {
      0% {
        transform: translateY(100vh);
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="message">
    <h1>Você é incrível demais! 💖</h1>
  </div>
  <script>
    const symbols = ["❤️", "💗", "💖", "💐", "🌸", "🌺", "🌷", "🌼", "🪷"]; // corações e lírios/florais
    for (let i = 0; i < 50; i++) {
      const elem = document.createElement('div');
      elem.className = 'float';
      elem.style.left = Math.random() * 100 + 'vw';
      elem.style.animationDuration = (Math.random() * 3 + 4) + 's';
      elem.innerText = symbols[Math.floor(Math.random() * symbols.length)];
      document.body.appendChild(elem);
    }
  </script>
</body>
</html>
"""

# Criar novo arquivo HTML com a personalização
custom_file_path = Path("/mnt/data/voce_e_incrivel_demais.html")
custom_file_path.write_text(html_content_custom, encoding='utf-8')
custom_file_path
