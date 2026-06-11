# Apresentação — Álcool (Etanol) · Seminário de Psicologia

- **`alcool-seminario-1080p.pdf`** — a apresentação pronta, 10 páginas em 16:9 Full HD (1920×1080), uma por slide. Abra em qualquer leitor de PDF, ative o modo de apresentação/tela cheia e passe com as setas.
- **`alcool-seminario.html`** — a versão interativa corrigida (navegação por setas/clique/swipe, contador de slides, botão de tela cheia — tecla `F`).
- **`original.html`** — o arquivo original recebido, mantido como referência.

## Como regenerar o PDF

Abra `alcool-seminario.html` no Chrome e imprima (`Ctrl+P`) → destino "Salvar como PDF" → margens "Nenhuma" → ativar "Imagens de fundo". O tamanho de página 1920×1080 já está definido no CSS de impressão.

## O que foi corrigido em relação ao original

1. **Colisão de classe CSS `.stage`**: os rótulos do slide 6 ("Da desinibição ao coma") usavam a mesma classe do contêiner de fundo (`position:fixed; inset:0`), o que cobria o slide inteiro com painéis pretos. Os rótulos foram renomeados para `.stg`.
2. **Conteúdo estourando o quadro 16:9**: os slides 3, 4, 7 e 10 tinham mais conteúdo do que a altura do palco (até +142px), cortando elementos. Espaçamentos, cartões e diagramas foram reequilibrados para tudo caber com folga.
3. **Fotos remotas** (Wikimedia) trocadas por ilustrações SVG embutidas — o arquivo funciona offline e o visual fica consistente.
4. **PDF de exportação** agora sai em 1920×1080 exatos (antes 1600×900) e há um auto-ajuste de segurança que reduz proporcionalmente qualquer slide que volte a estourar após edições futuras.
