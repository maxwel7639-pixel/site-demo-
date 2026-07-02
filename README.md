# Mentoria MX Digital — Landing page

Landing page estática (dark + roxo, serif Cormorant + Montserrat) importada do
Claude Design e implementada como HTML/CSS/JS puro. Deploy direto na Vercel — sem build.

## Rodar localmente

Basta abrir `index.html` no navegador, ou servir a pasta:

```powershell
npx serve .
# ou
python -m http.server 8000
```

## Configuração (editar em `index.html`, bloco `CONFIG` no final)

| Campo | O que é |
|-------|---------|
| `whatsappNumber` | **⚠️ Placeholder `5551999999999` — troque pelo número real** (DDI+DDD, só dígitos). Todos os botões de WhatsApp usam este valor. |
| `guaranteeDays` | `'7 dias'` ou `'14 dias'` — texto da garantia. |
| `ebookCheckoutUrl` | Link de checkout do Ebook. Vazio = botão cai no WhatsApp. |
| `mentoriaCheckoutUrl` | Link de checkout da Mentoria. Vazio = botão cai no WhatsApp. |

## ⚠️ Imagens pendentes (2)

O importador do Claude Design tem limite de 256 KiB por arquivo. As imagens maiores
vieram truncadas, mas 4 delas foram recuperadas dos screenshots originais no disco
(`hero-bg`, `benditas`, `cristiana`, `infosul`).

Faltam **2**, que só existiam dentro do projeto de design com nome próprio. Enquanto
não forem adicionadas, esses 2 cards aparecem com um fundo escuro elegante (sem quebrar
o layout — são `background-image`, sem ícone de imagem quebrada):

- `assets/mary-fialho.png` — card do portfólio + mockup do Passo 04 (Site no ar)
- `assets/neuro-design.png` — card do portfólio

Já incluídas e funcionando (11): `logo.png`, `hero-bg.png`, `portfolio-bg.png`,
`preco-bg.png`, `cta-bg.png`, `rosangela.png`, `benditas.png`, `cristiana.png`,
`infosul.png` (+ ícone do Claude em SVG inline).

## Deploy na Vercel

```powershell
vercel        # preview
vercel --prod # produção
```
Como é um site estático, não precisa de configuração — a Vercel detecta o `index.html`.
