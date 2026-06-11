# Apresentação — Álcool (Etanol) · Seminário de Psicologia

- **`alcool-seminario-1080p.pdf`** — a apresentação pronta, 10 páginas em 16:9 Full HD (1920×1080), uma por slide. Abra em qualquer leitor de PDF, ative o modo de apresentação/tela cheia e passe com as setas.
- **`alcool-seminario.html`** — a versão interativa corrigida (navegação por setas/clique/swipe, contador de slides, botão de tela cheia — tecla `F`). As fontes tipográficas estão embutidas no arquivo: abre offline em qualquer navegador moderno com o visual idêntico.
- **`original.html`** — o arquivo original recebido, mantido como referência.

## Fotos reais das bebidas (slide 3)

O HTML carrega as fotos reais do Wikimedia Commons quando há internet. Sem internet (ou se uma foto sair do ar), entram automaticamente as ilustrações no mesmo estilo do deck — nunca aparece ícone de imagem quebrada.

O PDF deste repositório foi gerado em um ambiente sem acesso ao Wikimedia, então mostra as ilustrações. Para gerar o PDF com as fotos: abra o HTML em um PC com internet e imprima (veja abaixo).

## Como regenerar o PDF

Abra `alcool-seminario.html` no Chrome ou Edge, espere o slide 3 mostrar as fotos e imprima (`Ctrl+P`) → destino "Salvar como PDF" → Guardar. O tamanho de página (1920×1080), as margens zero e a impressão das cores de fundo já estão forçados pelo CSS (`print-color-adjust: exact`) — não é preciso marcar "Imagens em segundo plano".

## O que foi corrigido em relação ao original

1. **Colisão de classe CSS `.stage`**: os rótulos do slide 6 ("Da desinibição ao coma") usavam a mesma classe do contêiner de fundo (`position:fixed; inset:0`), o que cobria o slide inteiro com painéis pretos. Os rótulos foram renomeados para `.stg`.
2. **Conteúdo estourando o quadro 16:9**: os slides 3, 4, 7 e 10 tinham mais conteúdo do que a altura do palco (até +142px), cortando elementos. Espaçamentos, cartões e diagramas foram reequilibrados para tudo caber com folga.
3. **Fontes embutidas** (Fraunces, Inter, IBM Plex Mono em woff2/base64, subset latino) — sem dependência do Google Fonts.
4. **Fotos com fallback**: as imagens remotas ganharam ilustrações SVG de reserva acionadas por `onerror`.
5. **PDF de exportação** agora sai em 1920×1080 exatos (antes 1600×900) e há um auto-ajuste de segurança que reduz proporcionalmente qualquer slide que volte a estourar após edições futuras.
