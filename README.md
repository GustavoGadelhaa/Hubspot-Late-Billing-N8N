# Automação de Lembretes de Projetos

## 🛠 Stacks Utilizadas
- **n8n**: Orquestração de automações.
- **PostgreSQL**: Banco de dados.
- **HubSpot API**: Consulta de projetos e usuários.
- **Evolution API**: Envio de mensagens via WhatsApp.
- **Gmail API**: Envio de e-mails.
- **JavaScript**: Transformação de dados e formatação de mensagens.



## 🔄 Fluxo de Automação (resumido)

1. **Trigger Agendado**: Dispara a automação semanalmente.  
2. **Consulta HubSpot**: Busca projetos e informações dos consultores.  
3. **Tratamento de Dados**: Calcula dias sem atualização e organiza informações.  
4. **Filtragem**: Seleciona projetos sem atualizações há mais de 7 dias.  
5. **Merge e Preparação**: Une dados de usuários e projetos, formata a mensagem.  
6. **Envio**: Mensagens automáticas enviadas via WhatsApp e e-mail.  
> ⚠️ Substitua todas as chaves de API (HubSpot, Evolution e Gmail) pelas suas credenciais.

---

## 📷 Visual do fluxo no n8n

![Exemplo de fluxo no n8n](imagemn8n.png)

---

## ✉️ Mensagem enviada (WhatsApp / E-mail)

![Msg formatada WhatsApp](ImagemExemploWPP.png)
------



## ✉️ Mensagem Fomatada no E-mail (Usando HTML)

![Msg formatada G-mail](msgHTML.png)

----------

# 🛠️ Estrutura HTML:

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8" />
  <title>Lembrete de Projetos</title>
</head>
<body style="background-color: #ffffff; padding: 20px; font-family: Arial, sans-serif; color: #333;">
  <div style="max-width: 600px; margin: auto; border-radius: 8px; border: 1px solid #ddd; padding: 24px; text-align: left;">
    <h1 style="color: #1a73e8; font-size: 22px; font-weight: bold; margin-bottom: 20px;">
      Olá, João Silva! 👋
    </h1>
    <div style="font-size: 15px; line-height: 1.6;">
      <p>Notamos que alguns dos seus projetos estão sem atualizações no HubSpot. Dá uma olhadinha neles pra gente? 😄👇</p>
      <p>📌 <b>Projeto Alpha</b> — <b>34 dias</b> sem atualização.</p>
      <p>📌 <b>Projeto Beta</b> — <b>56 dias</b> sem atualização.</p>
      <p>🛠️ Lembrando que é importante atualizar os projetos no Hubspot. Consegue atualizar ainda hoje?</p>
      <p>🚀 Contamos com você pra resolver isso o quanto antes!</p>
    </div>
  </div>
</body>
</html>
```

