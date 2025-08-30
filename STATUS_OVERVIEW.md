# 📊 Status Técnico Geral – Portal Auditoria

**Última atualização:** 29/08/2025  
**Responsável:** Samuel Cereja  

Este documento resume o estado atual de todos os serviços implantados no servidor **Windows Server 2022 Datacenter**.

---

## 🖥️ Servidor Base
| Serviço / Software   | Status        | Observações |
|----------------------|---------------|-------------|
| Windows Server 2022  | ✅ Ativo      | Datacenter, 64 GB RAM, estável |
| IIS 10 + ARR/Rewrite | ✅ Ativo      | Proxy reverso p/ Tomcat, SSL habilitado |
| PHP 8.4 (FastCGI)    | ✅ Ativo      | Validado com Roundcube, ini revisado |
| Tomcat 11 + JDK 24   | ✅ Ativo      | Rodando em 8080, atrás do IIS |
| MariaDB 11.8         | ✅ Ativo      | Roundcube + hMailServer integrados |
| PostgreSQL           | ✅ Ativo      | Suporte a sistemas internos |

---

## 📧 E-mail e Webmail
| Serviço / Software | Status         | Observações |
|-------------------|----------------|-------------|
| hMailServer 5.6.8 | ✅ Ativo       | SPF/DKIM/DMARC configurados, filtros globais ativos |
| Roundcube 1.7     | ✅ Ativo       | Webmail funcional em `/webmail` |
| ClamAV 1.4.2      | ✅ Ativo       | Integrado ao hMailServer, atualizações via Agendador |
| Anti-spam         | ✅ Ativo       | Regras + EventHandlers.vbs → 90% redução de spam |

---

## 🔐 Segurança
| Serviço / Software     | Status         | Observações |
|------------------------|----------------|-------------|
| Certificados SSL/TLS   | ✅ Ativo       | Emitidos via Win-ACME, exportáveis .pfx |
| HSTS + Headers IIS     | ✅ Ativo       | Segurança reforçada, nota A+ no SSL Labs |
| SPF                    | ✅ Validado    | `v=spf1 a mx ip4:167.250.65.254 -all` |
| DKIM                   | ✅ Validado    | `default._domainkey.portalauditoria.com.br` |
| DMARC                  | ✅ Validado    | `rua=mailto:dmarc@portalauditoria.com.br` |

---

## 📊 Observações Gerais
- Todos os serviços estão **ativos, estáveis e validados** em produção.  
- Integração **IIS ↔ Tomcat ↔ PHP ↔ hMail ↔ Roundcube** concluída.  
- Antivírus e filtros de spam estão operando sem alertas.  
- Certificados e DNS de autenticação de e-mail validados externamente.  

---

## 🚀 Próximos Passos
- Publicar APIs REST (`/api/servicos`, `/api/noticias`) para consumo via AMP.  
- Monitoramento de logs (IIS, Tomcat, hMail) com alertas centralizados.  
- Revisão periódica de relatórios DMARC e métricas de spam.  
