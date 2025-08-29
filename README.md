# 🚀 Portal Auditoria – Projeto Técnico AMP + Servidor Windows 2022

Repositório **público de documentação e exemplos** do ambiente Portal Auditoria, focado em:
- **Windows Server 2022 + IIS 10** com **ARR** e **URL Rewrite**
- **Java (JDK 24) + Tomcat 11 (Jakarta)** para rotas dinâmicas /app e /api
- **PHP 8.4 (FastCGI/IIS)** para apps como **Roundcube**
- **E-mail corporativo** com **hMailServer** + **ClamAV**
- **AMP (Accelerated Mobile Pages)** para páginas rápidas e validadas

> **Código-fonte da aplicação** (JSP/AMP) é comercial e permanece privado.  
> Este repo mostra *como eu projeto e opero a infraestrutura* e *como integrar AMP + APIs* com segurança.

## 📂 Estrutura
- `docs/` – documentação (AMP + guia técnico do servidor)
- `webconfig/` – exemplos prontos de `web.config` (raiz e `/webmail`)
- `api/examples/` – JSON de exemplo para `amp-list`
- `css/` – estilos base (para injetar inline em AMP no build)

## 🔗 Exemplos de uso
- AMP consumindo API com `amp-list` (CORS habilitado)
- Proxy **IIS → Tomcat** para `/app/*` e `/api/*`
- Roundcube em `/webmail` com cabeçalhos de segurança

## 🛡️ Segurança
Veja `SECURITY.md` e `SECRETS_GUIDE.md`.  
Nada sensível (senhas, .pfx, chaves DKIM) é versionado aqui.

## 👤 Autor
**Samuel Cereja** — Administrador de Sistemas & Programador  
Windows Server, IIS/ARR, Tomcat, Java (JSP/Servlets), PHP (FastCGI), Mikrotik, AMP.  
🌐 https://www.portalauditoria.com.br

