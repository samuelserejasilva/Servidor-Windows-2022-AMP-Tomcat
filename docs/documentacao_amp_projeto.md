# 📘 Documentação AMP + JSP

**Objetivo**: páginas AMP validadas consumindo dados de **APIs** via `amp-list`, servidas por **IIS** (proxy) → **Tomcat**.

## Pilares
- **AMP Cache** (ganhos de performance/SEO)
- **CORS** somente para o domínio do site
- **noindex** em staging/dev
- **URL Rewrite/ARR** para rotear `/app` e `/api` ao Tomcat

## Cabeçalhos (exemplo)

