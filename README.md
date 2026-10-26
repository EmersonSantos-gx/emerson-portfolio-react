# Emerson Santos — Portfólio & Gxcodev (React JS)

Aplicação web em **React (JavaScript)** totalmente componentizada, mantendo fielmente o visual, animações, responsividade, acessibilidade e interações do seu portfólio original e já com a sua foto de perfil configurada.

## Estrutura do Projeto

```text
emerson-portfolio-react/
├── index.html                             # HTML base com fontes Space Grotesk/Mono, Font Awesome e Tailwind CDN
├── package.json                           # Scripts e dependências React 18 + Vite
├── vite.config.js                         # Configuração do bundler suportando JSX em arquivos .js
├── public/
│   └── perfil.jpg                         # Sua foto de perfil recortada em alta resolução (800x800)
└── src/
    ├── index.js                           # Inicialização ReactDOM.createRoot
    ├── App.js                             # Orquestração dos componentes, estados dos modais e Toast
    ├── styles/
    │   └── global.css                     # Estilos completos (variáveis CSS, story-ring, glass, mini-UIs, modais)
    ├── config/
    │   └── portfolioData.js               # Objeto CONFIG centralizado + foto de perfil (/perfil.jpg e fallback Base64)
    ├── utils/
    │   └── helpers.js                     # Utilitários (safeURL, whatsappURL, publicPortfolioURL, vCard 3.0)
    └── components/
        ├── AmbientBackground.js           # Barra de progresso de leitura, partículas, grid e código decorativo
        ├── Topbar.js                      # Assinatura emerson.dev_ e indicador pulsante de disponibilidade
        ├── HeroSection.js                 # Avatar com anel giratório, foto de perfil, bio, localização e menu de seções
        ├── SocialBar.js                   # Links rápidos (Instagram, WhatsApp, LinkedIn, GitHub) com tooltips
        ├── StackSection.js                # 01 / Stack & Aprendizado (acordeões nativos <details>)
        ├── ProjectsSection.js             # 02 / Portfólio de Projetos (filtros por categoria, contador e grid)
        ├── ProjectPreview.js              # Maquetes vetoriais em HTML/CSS (escalas, financas, studio, bot) + fallback de imagem
        ├── StudioSection.js               # 03 / Estúdio Digital Gxcodev com borda animada e pilares
        ├── Footer.js                      # Compartilhamento nativo, download de vCard (.vcf), CNPJ e voltar ao topo
        ├── FloatingElements.js            # Botão flutuante (FAB) do WhatsApp e Toast de notificação
        └── modals/
            ├── ProjectModal.js            # Modal 1: Detalhes completos do projeto
            ├── BriefingModal.js           # Modal 2: Briefing interativo para WhatsApp
            └── CopyLinkModal.js           # Modal 3: Fallback para copiar link manualmente
```

## Como Rodar Localmente

1. Extraia o arquivo `emerson-portfolio-react.zip`.
2. No terminal, dentro da pasta do projeto, instale as dependências:
   ```bash
   npm install
   ```
3. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```
4. Acesse o endereço exibido no terminal (geralmente `http://localhost:5173`).

## Foto de Perfil

- O arquivo `public/perfil.jpg` já contém a sua foto recortada em alta resolução.
- Além disso, `src/config/portfolioData.js` traz a constante `PROFILE_PHOTO_BASE64` como fallback automático: caso `public/perfil.jpg` não seja encontrado em algum ambiente de preview online (como CodeSandbox ou StackBlitz), o componente `HeroSection.js` carrega automaticamente a versão em Base64 sem quebrar a foto.
