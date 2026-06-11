# Apresentação — Maconha (Cannabis sativa) · Seminário de Psicologia

- **`maconha-seminario-1080p.pdf`** — a apresentação pronta, 9 páginas vetoriais em 16:9 Full HD (1920×1080), uma por slide: texto nítido em qualquer zoom e selecionável. No CSS de impressão, os degradês translúcidos são trocados por equivalentes opacos (zero máscaras de transparência no PDF), o que elimina o travamento ao virar páginas em leitores fracos. Abra, ative o modo de apresentação/tela cheia e passe com as setas.
- **`maconha-seminario.html`** — a versão interativa (navegação por setas/clique/swipe, contador de slides, botão de tela cheia — tecla `F`). Arquivo 100% autocontido: fontes embutidas, ilustrações em SVG, nenhuma requisição externa — abre offline em qualquer navegador moderno com visual idêntico.
- **`original.html`** — o arquivo original recebido, mantido como referência.

## Como regenerar o PDF

Abra `maconha-seminario.html` no Chrome ou Edge e imprima (`Ctrl+P`) → destino "Salvar como PDF" → Guardar. O tamanho de página (1920×1080), as margens zero e a impressão das cores de fundo já estão forçados pelo CSS (`print-color-adjust: exact`) — não é preciso marcar "Imagens em segundo plano".

## O que foi corrigido em relação ao original

1. **Conteúdo estourando o quadro 16:9**: os slides 2 ("O que é a maconha?", +27px), 3 ("THC × CBD", +126px — a nota "Atenção" saía cortada) e 9 ("Fontes", +9px) tinham mais conteúdo do que a altura do palco. Espaçamentos, cartões e diagramas foram reequilibrados para tudo caber com folga.
2. **Molduras de foto que colapsavam**: a proporção estava declarada na `<img>`, não no contêiner — quando a foto remota falhava, a moldura sumia. Agora os contêineres têm proporção fixa.
3. **Sem imagens externas**: fotos do Wikimedia substituídas por ilustrações SVG no estilo do deck; as estruturas químicas do THC e do CBD foram redesenhadas à mão em SVG esquemático (fundo de papel, traço de diagrama químico).
4. **Fontes embutidas** (Fraunces, Inter, IBM Plex Mono em woff2/base64, subset latino) — sem dependência do Google Fonts.
5. **Contador de slides e botão de tela cheia** adicionados à barra superior; auto-ajuste de segurança reduz proporcionalmente qualquer slide que volte a estourar após edições futuras.
6. **PDF de exportação** em 1920×1080 exatos (antes 1600×900), com `print-color-adjust: exact` para o tema escuro sobreviver ao Ctrl+P e pintura 100% opaca (0 máscaras de transparência, ~107 ms/página).
