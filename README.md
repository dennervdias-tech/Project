# Bichinho de Bolso

Um bichinho virtual estilo Tamagotchi pra iPhone, feito como web app instalável (PWA).

## Como funciona

- Toque no ovo algumas vezes pra ele chocar.
- Cuide de 4 coisas: **Barriga**, **Alegria**, **Energia** e **Higiene**.
- O tempo passa mesmo com o app fechado: ele sente fome, fica com sono e faz cocô.
- **Brincar** abre um minijogo: pegue as estrelinhas antes que sumam.
- Toque no bichinho pra fazer carinho.
- Ele cresce: Bebê (1º dia), Jovem (até o 4º dia) e Adulte.
- No ✎ dá pra mudar nome, cor e acessório (laço, óculos, coroa ou bandeirinha).

O progresso fica salvo no próprio aparelho (`localStorage`).

## Instalar no iPhone

1. Publique o site (veja abaixo) e abra o link no **Safari**.
2. Toque em **Compartilhar** → **Adicionar à Tela de Início**.
3. Pronto: ele abre em tela cheia, com ícone próprio, e funciona offline.

## Publicar no GitHub Pages

O workflow `.github/workflows/pages.yml` publica o app a cada push na `main`.
Pra ativar: no repositório, vá em **Settings → Pages → Build and deployment → Source** e escolha **GitHub Actions**.
O link fica `https://<seu-usuário>.github.io/<repositório>/`.

## Arquivos

- `index.html`: o app inteiro (visual, lógica e desenho do bichinho em SVG)
- `manifest.webmanifest`: nome, cores e ícones pra instalação
- `sw.js`: guarda os arquivos pra funcionar sem internet
- `icons/`: ícones da tela de início
