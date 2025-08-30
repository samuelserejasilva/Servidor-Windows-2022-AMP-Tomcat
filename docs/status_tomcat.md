# ☕ Status Técnico – Tomcat 11 + JDK 24 (Jakarta EE)

**Última atualização:** 29/08/2025  
**Responsável:** Samuel Cereja  
**Servidor:** Windows Server 2022 Datacenter  

---

## 🔧 Configuração do Tomcat
- Versão instalada: **Apache Tomcat 11.0.x** ✅  
- Executando com **JDK 24 (Java SE 24, 64-bit)** ✅  
- Porta de serviço: **8080 (localhost only)** ✅  
- Configurado atrás do **IIS + ARR** → rotas `/app/*` e `/api/*` ✅  
- Conector HTTPS **desabilitado no Tomcat** (IIS cuida do SSL/TLS) ✅  

---

## 📂 Estrutura de implantação
- Aplicação principal: **Portal Auditoria (AMP + JSP/Servlets)** ✅  
- Diretório de deploy: `C:\Tomcat\webapps\portal-auditoria`  
- Rotas AMP: servidas por JSP dinâmico ✅  
- Rotas API: `/api/servicos`, `/api/noticias` (planejadas) ✅  
- Logs: `C:\Tomcat\logs` (catalina, localhost, manager) ✅  

---

## 🔒 Integração com IIS (ARR + URL Rewrite)
- IIS recebe HTTPS (`443`) e repassa para Tomcat (`127.0.0.1:8080`).  
- Variáveis de proxy:
  - `X-Forwarded-Proto: https`
  - `X-Forwarded-Host: {HTTP_HOST}`
- Regra de bypass para `/webmail` configurada ✅  

---

## 🔒 Segurança
- Tomcat **não exposto externamente** (apenas localhost:8080) ✅  
- Autenticação do `Manager` e `Host-Manager` desabilitada em produção ✅  
- Senhas administrativas removidas dos configs padrão ✅  
- Conexão ao DB (MariaDB/PostgreSQL) configurada via `context.xml` com usuários dedicados ✅  

---

## 📊 Observações
- Tomcat está rodando estável e integrado ao IIS.  
- Próximos passos:
  - Publicar APIs REST de exemplo (serviços/notícias).  
  - Implementar monitoramento de logs (catalina.out, GC).  
  - Avaliar uso de Spring Boot para endpoints futuros.

