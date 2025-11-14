# 📱 Página de Redirecionamento Automático — Play Store / App Store

<p align="center">
  <img src="./screen.png" alt="Page Preview" />
</p>

Uma página HTML leve e totalmente estática que detecta o sistema operacional do dispositivo do visitante e realiza automaticamente o redirecionamento para a loja apropriada.  
Ideal para campanhas de marketing, QR codes e links de download onde simplicidade e velocidade são essenciais.

🔗 **Demonstração ao vivo (GitHub Pages):**  
https://philipe-vieira.github.io/redirect-page/

📄 **Leia este README em inglês:**  
[README.md](README.md)

---

## 🎯 Objetivo

Este projeto simplifica o acesso ao seu aplicativo mobile ao redirecionar automaticamente cada dispositivo para a loja correta:

- Android → Google Play  
- iOS → App Store  
- Dispositivos não suportados ou desktop → Exibe uma mensagem informativa ao invés de redirecionar

Tudo isso usando apenas HTML, CSS e JavaScript, sem qualquer backend.

---

## 🚀 Como Funciona

O script analisa o `userAgent` do navegador para detectar:

- Dispositivos Android  
- Dispositivos iOS (incluindo iPadOS que às vezes se identifica como macOS, mas possui suporte a toque)  
- Qualquer outro ambiente  

Ao identificar o sistema operacional, a página exibe uma mensagem de status e redireciona o usuário para a loja apropriada.  
Um botão de fallback aparece caso o redirecionamento automático falhe.

---

## 🛠️ Configuração

Dentro do arquivo `index.html`, atualize estas duas constantes com os links reais do seu aplicativo:

```js
const ANDROID_APP_URL =
  "https://play.google.com/store/apps/details?id=com.android.chrome&pcampaignid=web_share";

const IOS_APP_URL =
  "https://apps.apple.com/br/app/google-chrome/id535886823";
