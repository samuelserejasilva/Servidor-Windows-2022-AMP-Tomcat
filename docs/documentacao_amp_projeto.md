# 📘 Documentação AMP + JSP

**Objetivo**: páginas AMP validadas consumindo dados de **APIs** via `amp-list`, servidas por **IIS** (proxy) → **Tomcat**.

## Pilares
- **AMP Cache** (ganhos de performance/SEO)
- **CORS** somente para o domínio do site
- **noindex** em staging/dev
- **URL Rewrite/ARR** para rotear `/app` e `/api` ao Tomcat

## Cabeçalhos (exemplo)

## AMP + `amp-list`
```html
<!doctype html>
<html ⚡ lang="pt-BR">
  <head>
    <meta charset="utf-8" />
    <title>Serviços – Portal Auditoria</title>
    <meta name="viewport" content="width=device-width,minimum-scale=1,initial-scale=1" />
    <script async src="https://cdn.ampproject.org/v0.js"></script>
    <script async custom-element="amp-list" src="https://cdn.ampproject.org/v0/amp-list-0.1.js"></script>
    <style amp-custom>.card{padding:12px;border:1px solid #eee;margin:8px 0}</style>
  </head>
  <body>
    <h1>Serviços</h1>
    <amp-list width="auto" height="120" layout="fixed-height"
              src="https://api.seu-dominio.com/api/servicos">
      <template type="amp-mustache">
        <div class="card">
          <h3>{{nome}}</h3>
          <p>{{descricao}}</p>
        </div>
      </template>
    </amp-list>
  </body>
</html>
```
