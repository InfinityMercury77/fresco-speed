# Fresco Speed Mobile

PWA responsiva para celular, feita com React, TypeScript e Vite.

## Executar no computador
Requer Node.js 20+.
```bash
npm install
npm run dev
```
Para testar no celular na mesma rede Wi-Fi, abra o endereço de rede mostrado pelo Vite (por exemplo `http://192.168.x.x:5173`). O navegador pode bloquear câmera/PWA em HTTP na rede local; use HTTPS para instalar e acessar recursos seguros.

## Gerar versão de produção
```bash
npm run build
npm run preview
```
Publique o conteúdo da pasta `dist` em um serviço HTTPS estático como Vercel, Netlify ou GitHub Pages configurado para SPA.

## Instalar no celular
- Android/Chrome: abra a URL HTTPS publicada, menu ⋮ e "Instalar app" ou "Adicionar à tela inicial".
- iPhone/Safari: abra a URL, toque em Compartilhar e "Adicionar à Tela de Início".

## Funcionalidades
- Layout projetado para telas pequenas, navegação inferior e botões de toque.
- Importação de vídeo e seletor que pode oferecer gravação pela câmera.
- Marcação manual da bolinha em quadros do vídeo.
- Cálculo experimental de velocidade por escala simples.
- Dois atletas, registro de golpes e quedas.
- Exportação de dados em JSON.
- Manifesto PWA, ícone e service worker para cache básico da interface.

## Limitações
A detecção automática da bola não está implementada nesta versão. O seletor `capture` pode abrir a câmera ou apenas o seletor de arquivos dependendo do navegador/dispositivo; ele não garante análise de vídeo ao vivo. A velocidade é estimativa e a calibração simples não corrige perspectiva nem movimento em profundidade. O service worker armazena o shell da interface, não os vídeos ou os dados da sessão. A sessão ainda não persiste ao fechar/recarregar a página.
