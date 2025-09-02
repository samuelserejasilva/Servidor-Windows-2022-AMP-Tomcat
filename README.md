[![📖 Ver documentação](https://img.shields.io/badge/📖-Documentação-blue?style=for-the-badge)](docs/README.md)

<details>
  <summary><b>📑 Índice rápido</b></summary>

- [Visão Geral](#anc-visao-geral)
- [📂 Estrutura](#anc-estrutura)
- [🔗 Exemplos de uso](#anc-exemplos)
- [🛡️ Segurança](#anc-seguranca)
- [👤 Autor](#anc-autor)

</details>

---

<a id="anc-visao-geral"></a>
## 🚀 Portal Auditoria – Projeto Técnico AMP + Servidor Windows 2022

Este repositório documenta a **infraestrutura e configuração do servidor** utilizada para hospedar e integrar diferentes tecnologias, incluindo:

- **Aplicações Java (JSP/Servlets) com Tomcat**
- **AMP (Accelerated Mobile Pages)**
- **PHP (FastCGI/IIS)** — ex.: Roundcube, WordPress, Joomla, Drupal, Laravel
- **Aplicações .NET e ASP.NET Core** (nativamente suportadas pelo IIS)
- **Aplicações Node.js** (via proxy reverso pelo IIS + ARR)
- **Aplicações Python (Flask/Django)** (via proxy reverso)
- **Bancos de dados** — MariaDB/MySQL e PostgreSQL
- **E-mail corporativo** com hMailServer + ClamAV
- **Integrações seguras via IIS + ARR + URL Rewrite**
- **Front-ends estáticos modernos** (HTML, CSS, JS, Vue, React, Angular)

O foco é mostrar como projetar, configurar e operar um ambiente de servidor Windows 2022 preparado para múltiplas aplicações modernas, com segurança e escalabilidade.

---

<a id="anc-estrutura"></a>
## 📂 Estrutura

- `docs/` – documentação (AMP + guia técnico do servidor)  
- `webconfig/` – exemplos prontos de **web.config** (raiz e `/webmail`)  
- `api/examples/` – JSON de exemplo para `amp-list`  
- `css/` – estilos base (para injetar inline em AMP no build)  

---

<a id="anc-exemplos"></a>
## 🔗 Exemplos de uso

- AMP consumindo API com `amp-list` (CORS habilitado)  
- Proxy IIS → Tomcat para `/app/*` e `/api/*`  
- Roundcube em `/webmail` com títulos de segurança  

---

<a id="anc-seguranca"></a>
## 🛡️ Segurança

Veja `SECURITY.md` e `GUIA_DE_SEGREDOS.md`.  
Nada sensível (senhas, `.pfx`, chaves DKIM) é versionado aqui.  

---

<a id="anc-autor"></a>
## 👤 Autor

**Samuel Cereja** — Administrador de Sistemas e Programador  

Windows Server, IIS/ARR, Tomcat, Java (JSP/Servlets), PHP (FastCGI), Mikrotik, AMP.  

🌐 [https://www.portalauditoria.com.br](https://www.portalauditoria.com.br)
