# 🖥️ Status Técnico – Servidor Windows 2022

**Última atualização:** 29/08/2025  
**Responsável:** Samuel Cereja  
**Servidor:** Windows Server 2022 Datacenter – 64 GB RAM  

---

## 🔧 Serviços instalados
- IIS 10 com ARR e URL Rewrite ✅
- PHP 8.4 via FastCGI (IIS) ✅
- Tomcat 11 (Jakarta EE 11, JDK 24) ✅
- PostgreSQL (sistemas internos) ✅
- MariaDB 11.8 (Roundcube/hMailServer) ✅
- hMailServer 5.6.8-B2574 ✅
- Roundcube 1.7 (Webmail) ✅
- ClamAV 1.4.2 (antivírus integrado ao hMail) ✅

---

## 🌐 Rede e DNS
- Firewall Mikrotik com NAT configurado ✅
- IP público fixo: `xxx.270.657.xxx` ✅
- Domínio público: `portalauditoria.com.br` ✅
- DNS configurado no Registro.br com:
  - SPF ✅
  - DKIM ✅
  - DMARC ✅
  - A/MX/CNAME corretos ✅

---

## 🔒 Segurança
- Certificados SSL/TLS válidos (emitidos via Win-ACME) ✅
- Certificados exportáveis em `.pfx` aplicados em IIS e hMail ✅
- HSTS e cabeçalhos de segurança configurados no IIS ✅
- ClamAV integrado ao fluxo SMTP do hMail ✅

---

## 📊 Observações
- Servidor está estável em produção.  
- Todos os serviços foram validados (AMP, Roundcube, e-mail com SPF/DKIM/DMARC).  
- Próximos passos: monitoramento avançado (logs IIS/Tomcat) e publicação de APIs REST para integração com páginas AMP.
