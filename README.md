# LP Notorium · Diagnóstico gratuito

Landing page de captação da Agência Notorium. Publicada em **lp.agencianotorium.com.br** (Vercel).

Página única em HTML (`index.html`), sem build. Imagens em `img/`.

## Configuração (topo do `index.html`, bloco `LP_CONFIG`)

- `whatsapp`: número que recebe os leads na tela de obrigado.
- `webhookUrl`: função `webhook-leads` do CRM Notorium (Supabase `NOTORIUM-crm`). Cada envio cria contato + negócio no funil **Inbound → Leads**, com origem `lp-diagnostico`. Investimento e prioridade vão no campo "motivo"; UTMs ficam no payload salvo em `webhook_leads`.
- `metaPixelId`: mesmo Pixel do site agencianotorium.com.br. Dispara `PageView` e `Lead`.

## Pendências

- Página `politica-de-privacidade.html` (o link já aponta para ela; a Meta exige).
- Confirmar os números de 2026 (+R$ 10 mi, +100 empresas, +3 mi pessoas/mês).
- Frase do Renan: trocar por "revisa cada campanha antes de ir ao ar" se valer para todos os clientes.

## No anúncio

Objetivo **Cadastros**, conversão no **Site**, evento **Lead**. UTMs no link:

```
?utm_source=meta&utm_medium=paid&utm_campaign=diagnostico&utm_content={{ad.name}}
```
