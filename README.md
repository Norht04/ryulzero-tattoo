# RyulZero 零 — Tattoo

Site de portfólio do tatuador **Ryulz** (São Paulo — BR), especializado em tatuagem **oriental**, **anime** e **blackwork**.
Página única, autoral, com identidade visual inspirada em tinta, carimbos japoneses e no traço do próprio artista.

**🔗 Ver o site no ar: https://norht04.github.io/ryulzero-tattoo/**

## Destaques do projeto

- **Abertura animada**: o kanji 零 é "pintado" com pincel enquanto brasas e partículas de tinta são atraídas para ele (canvas 2D com camadas de profundidade).
- **Hero em 3D**: desenho autoral (Mahoraga) girando em 3D com camadas em profundidades diferentes, logo em camadas com efeito de carimbo, glitch e paralaxe com o mouse.
- **Destaques**: carrossel automático com navegação por setas, bolinhas e gesto de arrastar no celular.
- **Portfólio** com abas **Tatuagens / Artes**, filtros por estilo, "Ver mais" para reduzir a rolagem e cartas com inclinação 3D estilo *Steam cards*.
- **Visualizador com zoom**: roda do mouse, clique, pinça e arrastar; carrega a versão em alta definição só quando o visitante amplia.
- **Formulário de orçamento** que monta a mensagem pronta para o WhatsApp.
- **Easter egg** escondido no site 🥚

## Desempenho

- Imagens com transparência servidas como **JPG + máscara PNG** (até 70% mais leves que PNG).
- Miniaturas, versões normais e em alta definição separadas (`-sm`, normal, `-hd`), com `srcset` e carregamento sob demanda.
- Fonte japonesa carregada apenas com os caracteres usados no site.
- Animações pausam quando a seção sai da tela; efeitos pesados de GPU desligados no celular.
- Respeita `prefers-reduced-motion`.

## Tecnologias

- HTML, CSS e JavaScript puros (sem framework, sem etapa de build)
- [GSAP](https://gsap.com/) + ScrollTrigger — animações
- [Lenis](https://lenis.darkroom.engineering/) — rolagem suave
- Google Fonts (IBM Plex Sans, Pirata One, Noto Serif JP/KR) + fontes próprias em `/fonts`

## Como rodar

O site é estático. Abra a pasta no VS Code e use a extensão **Live Server** (botão *Go Live*),
ou qualquer servidor local, por exemplo:

```bash
npx serve .
```

> Abra sempre por um servidor (`http://`), não com duplo clique no `index.html`:
> as máscaras de recorte das imagens são bloqueadas pelo navegador quando o arquivo é aberto direto do disco (`file://`).

## Estrutura

```
index.html            página única (HTML, CSS e JS)
assets/               imagens do site
  portfolio/          artes (nome-sm.jpg, nome.jpg, nome-hd.jpg)
  tatuagens/          fotos de tatuagens feitas (mesmo padrão)
fonts/                fontes próprias (Death Font, Downcome, Old London)
```

## Créditos

Arte, desenhos e tatuagens: **Ryulz** — Instagram [@ryulztattoo](https://instagram.com/ryulztattoo) · TikTok [@ryulzeroo](https://www.tiktok.com/@ryulzeroo)

© Todos os direitos sobre as imagens e artes pertencem ao artista. O uso das imagens fora deste projeto não é permitido sem autorização.
