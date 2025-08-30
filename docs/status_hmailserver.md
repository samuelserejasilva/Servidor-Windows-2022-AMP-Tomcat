# 📧 Status Técnico – hMailServer 5.6.8

**Última atualização:** 29/08/2025  
**Responsável:** Samuel Cereja  
**Servidor:** Windows Server 2022 Datacenter  

---

## 🔧 Configuração do hMailServer
- Versão instalada: **hMailServer 5.6.8-B2574** ✅  
- Banco de dados: **MariaDB 11.8** (base `hmailserver`) ✅  
- Serviços ativos:
  - SMTP (25, 465, 587)  
  - IMAP (143, 993)  
  - POP3 (110, 995) ✅  
- Contas configuradas:  
  - `contabil@portalauditoria.com.br`  
  - `luciane@portalauditoria.com.br` ✅  
- Integração com **Roundcube 1.7** funcionando ✅  

---

## 🔒 Segurança e Antivírus
- **ClamAV 1.4.2** integrado via `clamd` (porta 3310) ✅  
- Teste com **EICAR** bem-sucedido (bloqueio) ✅  
- Certificado SSL exportável (.pfx) aplicado no hMail ✅  
- SPF, DKIM e DMARC ativos no domínio `portalauditoria.com.br` ✅  
- STARTTLS habilitado em portas 143 e 587 ✅  

---

## 🌐 DNS e Entregabilidade
- Registros DNS:
  - SPF: `v=spf1 a mx ip4:167.250.65.254 -all` ✅  
  - DKIM: `default._domainkey` publicado e validado ✅  
  - DMARC: `dmarc@portalauditoria.com.br` monitorado ✅  
- Testes externos:  
  - Validação em [dkimcore.org](https://dkimcore.org/tools/keycheck.html) ✅  
  - SSL Labs: certificado válido e sem duplicatas ✅  

---

## 📊 Observações
- hMailServer estável e validado em produção.  
- ClamAV ocasionalmente gera timeout (HM5400), mas sem impacto crítico.  
- Próximos passos:
  - Implementar regras globais (filtros de spam e financeiros).  
  - Configurar monitoramento de fila SMTP para envios em massa.
