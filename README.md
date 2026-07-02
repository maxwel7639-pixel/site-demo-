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

## ⚠️ Imagens pendentes (6)

O importador do Claude Design tem limite de 256 KiB por arquivo, então 6 imagens
maiores não puderam ser baixadas e vieram truncadas — elas foram removidas. Enquanto
não forem adicionadas, esses blocos aparecem com um fundo escuro elegante (sem quebrar
o layout — são todos `background-image`, sem ícone de imagem quebrada).

Coloque os arquivos originais em `assets/` com **exatamente estes nomes**:

- `assets/hero-bg.png` — fundo da seção Hero
- `assets/mary-fialho.png` — card do portfólio + mockup do Passo 04
- `assets/benditas.png` — card do portfólio
- `assets/cristiana.png` — card do portfólio
- `assets/infosul.png` — card do portfólio
- `assets/neuro-design.png` — card do portfólio

Já incluídas e funcionando: `logo.png`, `portfolio-bg.png`, `preco-bg.png`,
`cta-bg.png`, `rosangela.png`.

## Deploy na Vercel

```powershell
vercel        # preview
vercel --prod # produção
```
Como é um site estático, não precisa de configuração — a Vercel detecta o `index.html`.
