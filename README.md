<img src="https://img.shields.io/badge/Insomnia-5849be?style=for-the-badge&logo=Insomnia&logoColor=white"/> <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=Postman&logoColor=white"/> <img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=Selenium&logoColor=white"/> <img src= "https://img.shields.io/badge/IntelliJIDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white"/> <img src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E"/> <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=Swagger&logoColor=white"/>






# Welcome! Scripts de Automação de Teste README.md Roger Drumond

Aqui inicio minha jornada na elaboraçao de scripts de automaçao de Teste, usando Selenium WebDriver

📱 Autor: ​Roger Drumond | Analista de Projetos I<br>
Certified ITIL V3 | COBIT 4.1 | ISO/IEC-20000 | <a href="https://www.bstqb.org.br/verificador-certificado?field_certificado_numero_value=13-CTFL-02452-BR">CTFL</a> | HDI-SCA | <a href="https://www.scrumstudy.com/certification/verify?type=SFC&number=888750">SFC-Scrum</a> | <a href="http://165.227.93.41/cgitar/certificado.php?hash=09101ac13f5106d2f5b2c7960be24192">API Rest-Test</a><br><a href="https://www.instagram.com/venomroger/"><br>
  <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white"/>
</a>
<a href="https://www.linkedin.com/in/drumondroger/">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
<a href="https://open.spotify.com/user/225ftlajwacbj5xxgj26cmktq?si=7fb5b1281fd44229">
  <img src="https://img.shields.io/badge/Spotify-1ED760?&style=for-the-badge&logo=spotify&logoColor=white"/>
  </a>
<a href="https://psnprofiles.com/venomroger">
  <img src="https://img.shields.io/badge/PlayStation-003791?style=for-the-badge&logo=playstation&logoColor=white"/>
  </a>
  <a href="https://twitter.com/drumondroger">
  <img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white"/>
  </a>



## Menu
   - [💻 Script1](#-script1-) - Download do Log
   - [💻 Script2](#-script2-) - Cadastro de Produto
   - [💻 Script3](#-script3-) - Cadastro de Tipo de Operação
   - [💻 Script4](#-script4-) - Taskit - Criaçao de User + Login
   - [💻 Fontes](#-fontes-)
   - [💻 Tools](#-tools-)







## 💻 Script1 [🔝](#welcome-scripts-de-automação-de-teste-readmemd-roger-drumond)

Script de Teste 1 - Acessar a tela de Administraçao do Servidor e fazer download do log  

   script: <a href= "https://github.com/venomroger/Test-automation-SKOM/commit/a0977fa2105cf257991665e9fd2a04eb64184f18">Create download_do_log</a>


   Desafios Mapeados:

## 💻 Script2 [🔝](#welcome-scripts-de-automação-de-teste-readmemd-roger-drumond)

Script de Teste 2 - Abrir navegador Chrome, logar com SUP, navegar pelo Menu ate a tela de Cadastro de Produto e efetuar o cadastro de um produto

   script: <a href="https://github.com/venomroger/Test-automation-SKOM/commit/2d156859985e0ecfc112fdb4c9c529fa5a6e8e2c">Cadastro_Produto</a>
   
   
   Desafios Mapeados na Jornada:
   
   #D1:-Menu do Sistema SKOM: Nao possui 'name', 'Id' ou 'Tag'
   
   ![image](https://user-images.githubusercontent.com/98754939/152168310-6795a56c-aec7-440a-8dda-f3b2eb6885e3.png)![image](https://user-images.githubusercontent.com/98754939/152169151-b96ddf2e-0b3a-416c-a037-839b03723791.png)

Os atributos disponiveis estao dispostos acima.
Portanto ao utilizar o atributo 'orig-title ='Menu do Sistema' , retorna: Unable to locate element, entao foi necessario utilizar o atributo do Cssselector

//Acessar o Menu
        
        navegador.findElement(By.xpath("//div[@class='Taskbar-icon icon-menu']")).click();

   #D2:-Navegação na Arvore de Menu: popupContent, as opções da arvore do Menu esta dentro de um Pop-up, entao é preciso encontrar primeiro a classe deste pop-up, para depois encontrar os valores dentro dele.
   
        navegador.findElement(By.cssSelector(".popupContent"));

        navegador.findElement(By.xpath("//div[contains(text(),'Cadastros')]")).click();
        
   #D3-O uso do metodo Thread.sleep, foi usado no script de teste, porque os SKOM tem loading para acessar as telas do sistema e os metodos implicito e explicito nao geraram resultados esperados no primeiro momento (POSTERIORMENTE IREI TESTA-LO NOVAMENTE)     
   
    ::Trecho em que eu espero 20000 milisegundos, apos logar no sistema
    navegador.findElement(By.xpath("//*[contains(text(), 'Entrar')]")).click();

        Thread.sleep(20000);
   
   #D4-O mapeamento dos campos de uma tela: Exemplo Cadastro de Parceiro: Nao possui 'name', 'Id' ou 'Tag'
      
    Exemplo:  Campo: Cód. Fabricante: - xpath: //input[@class='form-control ng-pristine ng-valid ng-empty ng-valid-maxlength ng-valid-required ng-touched'] sua tagname: input
              Campo: Fabricante: - xpath: //sk-text-input[@sk-field-name='FABRICANTE']//input[@type='text']
   
   
   
   
## 💻 Script3 [🔝](#welcome-scripts-de-automação-de-teste-readmemd-roger-drumond)

  Script de Teste 3 - Abrir navegador Chrome, logar com SUP, navegar pelo Menu ate a tela de Cadastro de Tipo de Operação e efetuar o cadastro de um Tipo de Operação
  
  script: <a href="https://github.com/venomroger/Test-automation-SKOM/commit/294e6f1f6e3c672ff42d31ef599be922fef8b536">cadastro_tipmov</a>


  Desafios Mapeados na Jornada:
  #D1:-Arvore do Menu Lateral: Do tipo dropdown, metodos utilizados com insucesso
  
      navegador.findElement(By.name("Todas")).click();
      navegador.findElement(By.className("tree-icon glyphicon collapse glyphicon-chevron-right")).click();
      navegador.findElement(By.xpath("//i[@class='tree-icon glyphicon collapse glyphicon-chevron-right']")).click();
      
  Solução: Tornar o Menu 'TODAS' do Inicio da arvore de Tipo de Movimento 'clicavel' e mapea-los.
  
![botao_Todas_da_arvore_tipomov](https://user-images.githubusercontent.com/98754939/152402572-e04ef8d6-6078-4c5e-85d4-9267fa05b645.gif)


## 💻 Script4 [🔝](#welcome-scripts-de-automação-de-teste-readmemd-roger-drumond)
  
  Script de Teste 4 - Abrir navegador Chrome, acessar o site /taskit, criar novo usuario e logar
  Script: 



## 💻 Fontes [🔝](#welcome-scripts-de-automação-de-teste-readmemd-roger-drumond)

   -<a href="https://chromedriver.chromium.org/downloads">ChromeDriver- WebDriver for Chrome</a><br>
   -<a href="https://selectorshub.com/">Extensao HUB Selector for Chrome</a><br>
   -<a href="https://www.lambdatest.com/blog/types-of-waits-in-selenium/">Blog Lambda Test</a><br>
    
## 💻 Tools [🔝](#welcome-scripts-de-automação-de-teste-readmemd-roger-drumond)

  -<a href="https://www.jetbrains.com/pt-br/idea/download/">IntellijIDEA</a><br>
  -<a href="https://jmeter.apache.org/download_jmeter.cgi">Apache JMeter</a><br>
  -<a haref="https://www.postman.com/downloads/">PostMan Rest</a><br>
  -<a href="https://insomnia.rest/download">Insomnia Rest</a><br>
  
 
