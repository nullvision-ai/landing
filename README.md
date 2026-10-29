# Landing page — nullvision

Página única (`index.html`) de apresentação e contato da nullvision: "o que você imagina, pronto pra tela."
Sem formulário: todo contato vai para o WhatsApp, com uma mensagem pronta que diz de qual parte da
página a pessoa veio (cada card de serviço tem a sua). Há também um link de e-mail no fecho.

**No ar em:** https://nullvision-ai.github.io/projectbriefing/ — é esse o link da bio do Instagram.
Domínio próprio previsto: `nullvisionai.com` (a registrar).

## Medição

Meta Pixel `2061112354570345`, no `<head>`:

| Evento | Quando |
|---|---|
| `PageView` | toda visita |
| `ViewContent` | a pessoa rolou até os trabalhos |
| `Contact` | clique em qualquer botão de WhatsApp ou no e-mail (`content_name` diz qual) |

Os números aparecem no Gerenciador de Eventos do Meta Business Suite. Links com `?utm_source=...`
anexam a origem à mensagem do WhatsApp.

## Arquivos

| Arquivo | O que é |
|---|---|
| `index.html` | a página inteira (HTML, CSS e JS, sem build) |
| `assets/v/` | trechos curtos do portfólio, sem áudio, ~5 MB no total, com um `.jpg` de capa cada |
| `og-image.png` | imagem de prévia (1200×630) ao compartilhar o link |
| `nullvision_brand_identity_v2.html` | referência de identidade visual |
| `nullvision_graphic_elements.html` | elementos gráficos da marca |

Os vídeos só carregam quando aparecem na tela. Para trocar um trecho, gere um MP4 novo com o mesmo
nome (topo: 432×768; cards: 480×600; H.264, CRF 30, sem áudio, `+faststart`) e a capa `.jpg`.

O código que corre ao fundo do topo, nas margens e no fecho é o código real do filme
"tudo começa com uma ideia" (`motion-testes/nullvision-ideia/film/index.html`).

## Publicar uma alteração

A pasta local é um clone deste repositório, então publicar é commitar e dar push:

```bash
git add -A
git commit -m "descrição do que mudou"
git push
```

O GitHub Pages republica sozinho em ~1 minuto. Não subir arquivo pela interface web do GitHub: foi
assim que a versão local e a publicada acabaram divergindo sem ninguém perceber.

Depois de mexer no `<head>` ou na `og-image.png`, vale limpar o cache de prévia do WhatsApp/Facebook em
[developers.facebook.com/tools/debug](https://developers.facebook.com/tools/debug/) — senão a prévia
antiga fica grudada por dias.

## Repositório antigo

`contatomateusaraujom-ctrl/nullvision-briefing` só redireciona para esta página. Não usar.
