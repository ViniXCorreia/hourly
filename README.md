<h1>Hourly - Um sistema de gerenciamento e agendamento voltado para barbearias</h1> 

<h2>Descrição</h2> 

<p>O sistema Hourly foi desenvolvido com o intuito de ser uma plataforma simples e funcional, voltada para micro e pequenos empresários do ramo de beleza masculina que possuem barbearias. O mercado de beleza masculina vem ganhando reconhecimento internacional, sendo um mercado em ascensão e atraindo uma série de novos empresários e clientes. Novas barbearias são abertas todos os meses e os empresários buscam por um modo de fazer uma gestão simples dos seus atendimentos, com o objetivo de fornecer mais autonomia aos seus clientes.

<h2>Equipe:</h2> 

<table>
  <tbody><tr>
    <td align="center">
      <a href="https://github.com/ViniXCorreia">
        <img src="https://avatars.githubusercontent.com/u/79664002?v=4" width="100px" height="100px" alt="ViniXCorreia" style="max-width: 100%;">
        <br>
        <sub><b>Vinícius Martins Correia</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/Matteus777">
        <img src="https://avatars.githubusercontent.com/u/41447631?v=4" width="100px" height="100px" alt="Matteus777" style="max-width: 100%;">
        <br>
        <sub><b>Matteus Camargo de Almeida</b></sub>
      </a>
    </td>
  </tr>
</table>

<h2>Funcionalidades</h2>
<p>O sistema Hourly oferece para os seus usuários as seguintes funcionalidades:</p>
<ul>
  <li><b>Agendamento de horários:</b> O sistema de agendamento desenvolvido na plataforma Hourly, permite que os usuários e os empreendedores consigam gerir de melhor forma seus agendamentos. Para os usuários, a plataforma oferece uma maneira simples e intuitiva de agendar seus serviços, na barbearia desejada e com o profissional da sua preferência. Para os empresários, o sistema de agendamento possui inteligência para otimizar o tempo dos atendimentos, evitando ociosidade e garantindo um melhor aproveitamento do dia do profissional.</li>
  <li><b>Fila online:</b> Os usuários que tem a necessidade de realizar um serviço e preferem não agendar um horário, podem entrar em uma fila online e garantir seu atendimento assim que possível. O sistema de fila foi pensado, para que não haja acúmulo de pessoas dentro da barbearia e que os clientes não fiquem aguardando no estabelecimento, sem a real necessidade. Com isso, os empresários também conseguem otimizar o tempo da sua equipe e garantir que espaços do dia, os quais ficariam vazios, sejam preenchidos por esses clientes.</li>
  <li><b>Avaliação de serviços:</b> Os usuários podem dar notas de 0 - 5 para os atendimentos recebidos e também deixar um breve comentários, sobre as suas impressões. Isso auxilia o empresário, a garantir que os serviços prestados dentro do seu estabelecimento, estejam sempre com a melhor qualidade possível, para os seus clintes, pois é através desses feedbacks que tudo se manterá dando certo, além de oportunizar um espaço de comunicação e melhoria em situações que julgar necessário.</li>
  <li><b>Fidelização:</b> O estabelecimento pode criar um plano de fidelização para os seus clientes, fazendo com que os mesmos recebam uma porcentagem de desconto depois de um determinado número de serviços executados. Isso faz com que os clientes se tornem assíduos do estabelecimento.</li>
</ul>
<h2>Tecnologias Utilizadas</h2>
-> Sugiro incluir aqui, os logotipos das tecnologias utilizadas, mantendo as descrições existentes abaixo de cada imagem.
<ul>
  <li>FrontEnd: HTML, CSS, Javascript associados ao framework Angular</li>
  <li>Backend: Node.js utilizando framework NestJs</li>
  <li>Banco de dados: PostgreSQL</li>
</ul>
<h2>Estrutura do backend do projeto</h2>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>src
├───infra
│   └───database
│       ├───entities
│       ├───migration
│       └───proxy
├───_modules
│   ├───collaborator
│   │   ├───infra
│   │   │   └───dtos
│   │   └───useCases
│   │       ├───closeSchedule
│   │       ├───createCollaborator
│   │       ├───deleteCollaborator
│   │       ├───findAllCollaborators
│   │       ├───findAllCollaboratorSchedules
│   │       ├───getCollaboratorQueueHistory
│   │       ├───getCollaboratorScheduleHistory
│   │       ├───getOneById
│   │       ├───getOneByToken
│   │       ├───getReports
│   │       ├───getServicesFromCompany
│   │       └───updateCollaborator
│   ├───company
│   │   ├───infra
│   │   │   ├───controller
│   │   │   └───dto
│   │   └───useCases
│   │       ├───clearQueue
│   │       ├───createCompany
│   │       ├───deleteCompany
│   │       ├───findAllCollaboratorsLoggedCompany
│   │       ├───findAllCompanyCollaborators
│   │       ├───findAllCompanySchedules
│   │       ├───findAllCompanyServices
│   │       ├───findAllServicesLoggedCompany
│   │       ├───findCompanyById
│   │       ├───findCompanyLike
│   │       ├───getAllCompanies
│   │       ├───getCompanyConfig
│   │       ├───getCompanyQueue
│   │       ├───getCompanyRatings
│   │       ├───getReports
│   │       └───updateCompany
│   ├───customer
│   │   ├───dto
│   │   ├───infra
│   │   └───useCase
│   │       ├───cancelQueue
│   │       ├───enterQueue
│   │       ├───getCustomerSchedule
│   │       ├───getHistory
│   │       ├───getOneByToken
│   │       ├───getQueue
│   │       ├───ratingSchedule
│   │       ├───setQueueStarted
│   │       └───updatedCustomer
│   ├───person
│   │   ├───infra
│   │   │   ├───controller
│   │   │   └───dto
│   │   └───useCase
│   │       ├───changePassword
│   │       ├───createPerson
│   │       ├───deletePerson
│   │       ├───findAllPersons
│   │       ├───findOnePersonByDocumentNumber
│   │       ├───findOnePersonByEmail
│   │       ├───findOnePersonById
│   │       ├───findOnePersonByName
│   │       ├───forgotPassword
│   │       ├───login
│   │       ├───recoveryPassoword
│   │       ├───setRoleToken
│   │       ├───updatePerson
│   │       └───validatePerson
│   ├───schedule
│   │   ├───infra
│   │   │   ├───controller
│   │   │   └───dto
│   │   └───useCases
│   │       ├───createSchedule
│   │       ├───deleteScheduleBy
│   │       ├───findAllSchedulesByCompany
│   │       ├───findScheduleById
│   │       ├───finishSchedule
│   │       ├───getAvailableSchedule
│   │       ├───notAttend
│   │       ├───ratingSchedule
│   │       ├───returnScheduelFinish
│   │       ├───scheduleCron
│   │       └───updateSchedule
│   └───service
│       ├───infra
│       │   ├───controller
│       │   └───dto
│       └───useCase
│           ├───createService
│           ├───findAllServicesByCompanyId
│           ├───findServiceById
│           ├───removeServiceById
│           └───updateServiceById
└───_shared
    ├───auth
    ├───crypto
    ├───mailModule
    └───protocols
        └───dto
</code></pre> 
<h2>Explicação da estrutura do backend</h2>
<ul>
  <li>infra: Pasta responsável por armazenar todas as entidades, dados de conexão, migrações e configuração do banco de dados do projeto; </li>
  <li>shared: Local onde foram desenvolvidas todas as funcionalidades que são comuns a todos os demais módulos do sistema, como a parte de criptografia, envio de emails e padrões de respostas;</li>
  <li>_modules: Cada entidade do sistema possui o seu módulo, que é a parte onde ficam localizados todos os casos de uso de cada um deles. Todos os endpoints são criados dentro das classes de controle (controllers) auxiliados pelas classes de acesso aos dados (dtos) relacionados. Cada ação do módulo é separado dentro de um useCase, facilitando localizar e desenvolver uma funcionalidade sem interferir nas demais.</li>
</ul>
<h2>Estrutura do frontend do projeto</h2>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>
src
├───app
│   ├───dtos
│   ├───entities
│   ├───interceptor
│   ├───services
│   ├───shared
│   │   └───directives
│   └───_modules
│       ├───auth
│       │   ├───forgot-password
│       │   └───login
│       └───pages
│           ├───collaborator
│           │   ├───edit
│           │   └───list
│           ├───company
│           │   ├───edit
│           │   └───list
│           ├───customer
│           │   ├───company-view
│           │   ├───create-schedule
│           │   ├───enter-queue
│           │   ├───find-company
│           │   ├───history
│           │   └───view-queue
│           ├───layout
│           │   ├───api
│           │   └───service
│           ├───profile
│           │   ├───change-password
│           │   ├───profile-collaborator
│           │   ├───profile-company
│           │   └───profile-customer
│           ├───queue
│           │   └───queue-history
│           ├───reports
│           │   ├───collaborator-report
│           │   └───company-report
│           ├───schedule
│           │   └───schedule-history
│           └───service
│               ├───edit
│               └───list
├───assets
│   ├───demo
│   │   ├───data
│   │   ├───images
│   │   │   ├───access
│   │   │   ├───avatar
│   │   │   ├───blocks
│   │   │   │   ├───hero
│   │   │   │   └───logos
│   │   │   ├───error
│   │   │   ├───flag
│   │   │   ├───galleria
│   │   │   ├───landing
│   │   │   ├───login
│   │   │   ├───nature
│   │   │   ├───notfound
│   │   │   └───product
│   │   └───styles
│   │       └───flags
│   └───layout
│       ├───images
│       │   └───themes
│       └───styles
│           ├───layout
│           └───theme
└───environments
</code></pre> 
<h2>Explicação da estrutura do frontend</h2>
<ul>
  <li>entities: Mapeamento das entidades utilizadas pelo sistema;</li>
  <li>interceptor: Interceptadores para validações de códigos https e apresentações de erros;</li>
  <li>services: Onde são montadas as requisições para a API do backend;</li>
  <li>shared: Onde são hospedados os serviços e as diretivas para se utilizar em todo o projeto;</li>
  <li>_modules: Todas as páginas do sistema, com cada tela separada e toda a sua estrutura e funcionalidades;</li>
  <li>assets: Imagens e padrões de layout utilizados dentro do sistema;</li>
  <li>environments: Onde ficam definidas as variáveis de ambiente, que indicam se o sistema está apontando para o ambiente de desenvolvimento ou para o ambiente de produção.</li>
</ul>
