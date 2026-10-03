# J.A.R.V.I.S — Web Edition

Esta é uma adaptação do projeto Python original para funcionar diretamente no navegador.

## Como usar

Abra `index.html` em um navegador moderno, ou publique a pasta em Netlify/GitHub Pages/Vercel. Não é necessário instalar Python, pip, PyAudio, OpenCV, Tesseract ou outras dependências locais.

**Chrome/Edge** são recomendados para reconhecimento de voz e câmera.

## Funções adaptadas
- Comandos por texto e voz
- Resposta por voz usando Speech Synthesis do navegador
- Hora
- Clima usando geolocalização + Open-Meteo
- Wikipedia
- YouTube/Google/Amazon/Stack Overflow/GitHub
- Busca no Google e YouTube
- Notícias
- Piadas
- Dicionário local (`data.json`)
- Memória persistente via localStorage
- Informações de sistema que o navegador permite expor
- Captura de tela com permissão do navegador
- Música por arquivo escolhido pelo usuário
- E-mail via `mailto:`
- Câmera
- OCR com Tesseract.js carregado por CDN

## Limitações do navegador
O Python original tinha acesso privilegiado ao computador. Um site não pode, por segurança, desligar o PC, abrir programas locais, enviar e-mail silenciosamente ou baixar vídeos do YouTube como um programa desktop. Essas funções foram convertidas para alternativas seguras no navegador.

A autenticação facial original usava OpenCV + `trainer.yml`. Esse modelo Python não é diretamente compatível com o navegador; a página mantém câmera/OCR e sinaliza essa diferença em vez de fingir que a autenticação original continua igual.
