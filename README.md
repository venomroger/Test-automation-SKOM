<img src="https://img.shields.io/badge/Insomnia-5849be?style=for-the-badge&logo=Insomnia&logoColor=white"/> <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=Postman&logoColor=white"/> <img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=Selenium&logoColor=white"/> <img src= "https://img.shields.io/badge/IntelliJIDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white"/> <img src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E"/> <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=Swagger&logoColor=white"/>



<a href="https://www.instagram.com/venomroger/">
  <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white"/>
</a>
<a href="https://www.linkedin.com/in/drumondroger/">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
<a href="https://open.spotify.com/user/225ftlajwacbj5xxgj26cmktq?si=7fb5b1281fd44229">
  <img src="https://img.shields.io/badge/Spotify-1ED760?&style=for-the-badge&logo=spotify&logoColor=white"/>
  </a>


# Welcome! Scripts de Automação de Teste README.md Roger Drumond

Aqui inicio minha jornada na elaboraçao de scripts de automaçao de Teste, usando Selenium WebDriver

Autor: Roger Macedo Drumond


## Menu
   - [1️⃣ Script1](#-script1-) - Download do Log
   - [2️⃣ Script2](#-script2-) - Cadastro de Produto
   - [💻 Script3](#-script3-)







## 1️⃣ script1 [🔝](#welcome-scripts-de-automação-de-teste-readmemd-roger-drumond)

Script de Teste 1 - Acessar a tela de Administraçao do Servidor e fazer download do log  

   script: <a href= "https://github.com/venomroger/Test-automation-SKOM/commit/a0977fa2105cf257991665e9fd2a04eb64184f18">Create download_do_log</a>


   Desafios Mapeados:

## 2️⃣ script2 [🔝](#welcome-scripts-de-automação-de-teste-readmemd-roger-drumond)

Script de Teste 2 - Abrir navegador Chrome, logar com SUP, navegar pelo Menu ate a tela de Cadastro de Produto e efetuar o cadastro de um produto

   script: <a href="https://github.com/venomroger/Test-automation-SKOM/commit/2d156859985e0ecfc112fdb4c9c529fa5a6e8e2c">Cadastro_Produto</a>
   
   
   Desafios Mapeados na Jornada:
   
   -Menu do Sistema SKOM: Nao possui 'name', 'Id' ou 'Tag'
   
   ![image](https://user-images.githubusercontent.com/98754939/152168310-6795a56c-aec7-440a-8dda-f3b2eb6885e3.png)![image](https://user-images.githubusercontent.com/98754939/152169151-b96ddf2e-0b3a-416c-a037-839b03723791.png)

Os atributos disponiveis estao dispostos acima.
Portanto ao utilizar o atributo 'orig-title ='Menu do Sistema' , retorna: Unable to locate element, entao foi necessario utilizar o atributo do Cssselector

//Acessar o Menu
        navegador.findElement(By.xpath("//div[@class='Taskbar-icon icon-menu']")).click();


## 💻 Script3 [🔝](#welcome-scripts-de-automação-de-teste-readmemd-roger-drumond)

Script de Teste 3 - Não iniciado...
