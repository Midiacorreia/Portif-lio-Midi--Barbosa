Thanks for downloading this template!

Template Name: FolioOne
Template URL: https://bootstrapmade.com/folioone-bootstrap-portfolio-website-template/
Author: BootstrapMade.com
License: https://bootstrapmade.com/license/


- Retirar a página "Resume"; "Droopedaw" ; 
- Incrementar a página de services em um espçao da página SOBRE MIM 
- Editat o Portifólio 
- Editar o Contact 

No fim limpar o códgo .... mostrar para o chat oque poderia ser retirado e deixar o código limpo.


-------------------PRÓXIMO PASSO--------------
- Cadastrar os projetos na vercel para poder mandar para o link Resultado
- Adequar o formulário PHP

 


VERSÃO QUE O CHAT DEU : o problema é :
-O erro “405 Method Not Allowed” acontece porque você está tentando acessar um arquivo PHP usando o Live Server do VS Code (porta 5500) — e isso NÃO funciona, porque:

🚫 O Live Server não interpreta PHP
🚫 O PHP só funciona em um servidor que suporte processamento backend
🚫 O navegador está tentando fazer uma requisição POST para um arquivo que o servidor não sabe processar

Ou seja:

❌ Você NÃO pode rodar esse formulário PHP usando:

Live Server (127.0.0.1:5500)

Arquivo HTML aberto direto no navegador

GitHub Pages

Vercel (sem serverless escrito para isso)

Netlify

✅ COMO RESOLVER

Você tem 3 opções:

✅ OPÇÃO 1 — Rodar localmente com PHP

Use um servidor local que suporte PHP:

1.1 Instale o PHP (se ainda não tiver)

🔗 https://www.php.net/downloads.php

1.2 No terminal, navegue até a pasta do seu site e rode:
php -S localhost:8000

1.3 Acesse no navegador:
http://localhost:8000


Agora o contact.php vai funcionar sem erro 405.

✅ OPÇÃO 2 — Hospedar em um servidor com PHP

Coloque seu portfólio em qualquer serviço que aceite PHP:

✔ Hostinger
✔ InfinityFree (gratuito)
✔ 000webhost (gratuito)
✔ cPanel de qualquer hospedagem
✔ OVH
✔ Locaweb
✔ KingHost

Apenas envie sua pasta via FTP.

✅ OPÇÃO 3 — Usar email sem PHP (via Formspree, Google Forms, Netlify Forms etc.)

Se você não quiser backend, posso converter seu formulário para:

Formspree (o mais simples)

EmailJS (JS + SMTP sem servidor)

Netlify Forms

Google Firebase Functions

Quer essa opção?

⚠️ Por que o erro 405 aparece?

Porque neste ambiente:

http://127.0.0.1:5500/forms/contact.php


O arquivo .php não está sendo processado
→ O navegador tenta enviar um POST
→ O "servidor" do Live Server rejeita
→ Resultado: 405 Method Not Allowed