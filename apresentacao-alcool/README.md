# Apresentação — Álcool (Etanol) · Seminário de Psicologia

- **`alcool-seminario-1080p.pdf`** — a apresentação pronta, 10 páginas em 16:9 Full HD (1920×1080), uma por slide. Cada página é uma imagem achatada em alta resolução (3840×2160), o que torna a navegação instantânea em qualquer leitor de PDF — os PDFs vetoriais do Chrome ficavam lentos por causa dos degradês e transparências do tema. Abra, ative o modo de apresentação/tela cheia e passe com as setas.
- **`alcool-seminario.html`** — a versão interativa (navegação por setas/clique/swipe, contador de slides, botão de tela cheia — tecla `F`). Arquivo 100% autocontido: fontes embutidas, ilustrações em SVG, nenhuma requisição externa — abre offline em qualquer navegador moderno com visual idêntico.
- **`original.html`** — o arquivo original recebido, mantido como referência.

## Como regenerar o PDF

Abra `alcool-seminario.html` no Chrome ou Edge e imprima (`Ctrl+P`) → destino "Salvar como PDF" → Guardar. O tamanho de página (1920×1080), as margens zero e a impressão das cores de fundo já estão forçados pelo CSS (`print-color-adjust: exact`) — não é preciso marcar "Imagens em segundo plano".

## O que foi corrigido em relação ao original

1. **Colisão de classe CSS `.stage`**: os rótulos do slide 6 ("Da desinibição ao coma") usavam a mesma classe do contêiner de fundo (`position:fixed; inset:0`), o que cobria o slide inteiro com painéis pretos. Os rótulos foram renomeados para `.stg`.
2. **Conteúdo estourando o quadro 16:9**: os slides 3, 4, 7 e 10 tinham mais conteúdo do que a altura do palco (até +142px), cortando elementos. Espaçamentos, cartões e diagramas foram reequilibrados para tudo caber com folga.
3. **Sem imagens externas**: as fotos remotas do Wikimedia foram substituídas por ilustrações SVG no estilo do deck (decisão de design — modelo sem fotos).
4. **Fontes embutidas** (Fraunces, Inter, IBM Plex Mono em woff2/base64, subset latino) — sem dependência do Google Fonts.
5. **PDF de exportação** em 1920×1080 exatos (antes 1600×900), com `print-color-adjust: exact` para o tema escuro sobreviver ao Ctrl+P, e um auto-ajuste de segurança que reduz proporcionalmente qualquer slide que volte a estourar após edições futuras.
