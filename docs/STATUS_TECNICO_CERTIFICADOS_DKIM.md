# 🔑 Certificados & Autenticação de E-mail – Status Técnico

## ⚙️ Configuração atual
- Certificados ativos:
  - Emitidos via **Win-ACME (Let's Encrypt)** ✅
  - Exportáveis em **.pfx**, aplicados no **IIS** e no **hMailServer** ✅
- Chaves privadas armazenadas com segurança fora do repositório Git.  
- Certificado público validado em **SSL Labs** com nota **A+**.  

---

## 📧 SPF, DKIM e DMARC
- **SPF**:
  - Registro publicado em DNS:  
    ```
    v=spf1 a mx ip4:167.250.65.254 -all
    ```
  - Validação: **OK**
- **DKIM**:
  - Selector configurado: `default._domainkey.portalauditoria.com.br` ✅  
  - Registro TXT publicado e validado em [dkimcore.org](https://dkimcore.org/tools/keycheck.html).  
  - Validação: **OK**
- **DMARC**:
  - Registro publicado:  
    ```
    v=DMARC1; p=none; rua=mailto:dmarc@portalauditoria.com.br
    ```
  - Caixa `dmarc@portalauditoria.com.br` criada e monitorada.  
  - Validação: **OK**

---

## 📊 Observações
- Certificados e autenticações DNS ativos e funcionando sem alertas.  
- E-mails enviados passam em **SPF, DKIM e DMARC** nas ferramentas de teste.  
- Melhorias anti-spam foram observadas em conjunto com:
  - **Filtros globais no hMailServer**
  - **Scripts EventHandlers.vbs** (blacklist + whitelist)  
  - Resultando em **~90% de redução de spam** ✅  

---

## 🚀 Próximos passos
- Manter ciclo de renovação automática do Win-ACME (a cada 60–90 dias).  
- Revisar relatórios DMARC periodicamente.  
- Avaliar políticas mais restritivas no DMARC (`p=quarantine` ou `p=reject`) após monitoramento.  
