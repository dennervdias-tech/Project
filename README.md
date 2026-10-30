# Bichinho de Bolso

Um bichinho virtual estilo Tamagotchi pra iPhone, feito como web app instalável (PWA).

## Como funciona

- Toque no ovo (ou sacuda o celular) pra ele chocar.
- Cuide de 4 coisas: **Barriga**, **Alegria**, **Energia** e **Higiene**.
- O tempo passa mesmo com o app fechado: ele sente fome, fica com sono, se suja e faz cocô.
- O corpo é de "gelatina": amassa ao cair, balança quando você mexe e reage à física.
- O céu acompanha o horário de verdade (amanhecer, dia, pôr do sol, noite com estrelas).
- Ele cresce: Bebê (1º dia), Jovem (até o 4º dia) e Adulte.
- No ✎ dá pra mudar nome, cor, acessório (laço, óculos, coroa ou bandeirinha), sons e vibração.

## Gestos

| Gesto | O que acontece |
| --- | --- |
| Tocar | "Boop": ele ri e solta coraçõezinhos |
| Tocar duas vezes | Ele pula |
| Deslizar o dedo nele | Carinho (fecha os olhinhos e ronrona) |
| Segurar | Pega no colo; solte com força pra arremessar |
| Chacoalhar no colo | Ele fica tontinhe |
| Sacudir o celular | Balança, acorda assustado ou fica tonto |
| Inclinar o celular | Ele escorrega pro lado e olha pra ladeira |
| Tocar no cocô | Limpa |
| Banho + esfregar | Faz espuma e tira a sujeira |

Os olhos seguem seu dedo, e quando você volta pro app ele percebe e reage
(de madrugada, de manhã, depois de muito tempo longe…).

O progresso fica salvo no próprio aparelho (`localStorage`).

### Sobre o iPhone

- **Sacudir e inclinar** usam os sensores de movimento; o iPhone pede permissão no primeiro toque.
- **Vibração**: o Safari não tem API de vibração; o app usa o "tique" do interruptor nativo do iOS 18+.
- **Live Activity / Dynamic Island / widget** não são possíveis em web app: exigem um app nativo em Swift.

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
