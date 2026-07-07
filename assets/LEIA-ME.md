# Assets do protótipo

`brasao-sjc.png` — brasão oficial de São José dos Campos (Wikimedia Commons,
"Brasão de São José dos Campos.svg", render 250px). Usado no header; se o arquivo
sumir, o HTML cai num escudo genérico de fallback.

`seu-jose-<pose>.mp4` — vídeo opcional do Seu José por tela/pose (ex.: `seu-jose-boasvindas.mp4`
já existe e roda no hero da home). Cada tela PODE ter o seu; se não houver `.mp4` para a pose,
cai no `seu-jose-<pose>.png` (e no desenho vetorial por último). Ao trocar de tela, o vídeo
anterior para e o da tela atual começa do início. O som é controlado por um único botão no
header (junto ao A+); começa mudo (autoplay + etiqueta de totem). Poses: boasvindas, apontando,
celular, pensando, comemorando — basta soltar `seu-jose-apontando.mp4` etc. para dar vídeo àquela tela.

`anderson-neutro.jpg` / `anderson-sorrindo.jpg` — fotos reais do munícipe (Anderson)
usadas na simulação de biometria facial (tela s-c4): a neutra durante o "Analisando…"
e a sorrindo na confirmação (crossfade). Recorte no rosto é feito por CSS
(`.bio .bio-photo` — object-fit:cover + transform:scale/origin no terço superior);
se as duas fotos tiverem o mesmo enquadramento, a troca sério→sorrindo fica perfeita.
Se os arquivos sumirem, a biometria cai no emoji de fallback (🙂/😄).

# Seu José — imagens do guia do totem

O protótipo (`../index.html`) procura os PNGs abaixo nesta pasta. Enquanto o arquivo
não existir, ele mostra automaticamente uma ilustração vetorial de fallback — ou seja,
o protótipo funciona com ou sem as imagens. Basta salvar os PNGs aqui com o nome exato
e recarregar a página.

| Arquivo | Pose | Onde aparece |
|---|---|---|
| `seu-jose-boasvindas.png` | Acenando, sorridente | Tela inicial (destaque grande) e biometria |
| `seu-jose-apontando.png` | Apontando para o lado/frente | Identificação, teclados, imóvel, boletos, e-mail |
| `seu-jose-celular.png` | Segurando o celular | Conta Munícipe, código WhatsApp/SMS, Pix, WhatsApp |
| `seu-jose-pensando.png` | Mão no queixo, pensativo | Escolha da forma de pagamento |
| `seu-jose-comemorando.png` | Polegar para cima, comemorando | Telas de sucesso |

**Atalho:** as duas imagens que já temos servem direto —
o recorte circular acenando → `seu-jose-boasvindas.png`;
a imagem segurando o celular → `seu-jose-celular.png`.

Formato ideal: PNG quadrado (~800×800), personagem centralizado do peito para cima,
fundo transparente ou círculo azul-claro (#DCEBFB). A moldura do totem é circular,
então deixe margem nas bordas.

## Prompt base para o ChatGPT (anexar a imagem de referência)

> Using the attached reference image, generate a new pose of the EXACT same 3D Pixar-style
> character: a friendly elderly Brazilian man ("Seu José"), gray combed hair, thick black
> rounded glasses, white/gray mustache, warm smile, beige polo shirt with light suspenders.
> Keep identical face, proportions, materials and lighting as the reference.
> Square image, chest-up framing, centered, plain white/transparent background,
> soft studio lighting, high resolution.
>
> Pose: **[POSE]**

Substitua **[POSE]** por uma das linhas abaixo (uma imagem por vez):

1. `seu-jose-boasvindas.png` — *waving hello with one hand raised, big welcoming smile*
2. `seu-jose-apontando.png` — *pointing forward/sideways with index finger, as if showing a button on a screen, encouraging expression*
3. `seu-jose-celular.png` — *holding a dark smartphone with both hands and showing its screen towards the viewer*
4. `seu-jose-pensando.png` — *hand on chin, thoughtful but friendly expression, slightly tilted head*
5. `seu-jose-comemorando.png` — *both thumbs up, celebrating with joyful open-mouth smile, eyes slightly closed with happiness*
