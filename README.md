<h1>Hourly - Um sistema de gerenciamento e agendamento voltado para barbearias</h1> 

<h2>Descrição</h2> 

<p>O sistema Hourly foi desenvolvido com o ituito de ser uma plataforma simples e funcional voltado para micro e pequenos empresários do ramo de beleza masculina que possuem barbearias. O mercado de beleza masculina vem ganhando reconhecimento internacional sendo um mercado em ascensão e atraindo uma série de novos empresários e clientes. Novas barbearias são abertas todos os meses e os empresários buscam por um modo de fazer uma gestão simples dos seus atendimento e fornece para seus clientes mais autonomia.

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
<p>O sistema Hourly oferece para os seus usuários as seguintes funcionaldiades:</p>
<ul>
  <li>Agendamento de horários: O sistema de agendamento desenvolvido na plataforma Hourly permite que os usuários os empreendedores consigam gerir de melhor forma seus agendamentos. Para os usuários a plataforma oferece uma maneira simples e intuitiva de agendar os horários na barbearia desejada e com o profissional desejado. Já para os empresários, o sistema de agendamento possui inteligência para otimizar o tempo dos atendimentos, evitando ociosidade e garantindo um melhor aproveitamento do dia do profissional.</li>
  <li>Fila online: Os usuários que tem a necessidade de realizar um serviço e preferem não agendar um horário, podem entrar em uma fila online e garantir seu atendimento assim que possível. O sistema de fila foi pensado para que não há acumulo de pessoas dentro da barbearia e que os clientes não fiquem aguardando no estabelecimento sem a real necessidade. Com isso, os empresários também conseguem otimizar o seu tempo e garantir que espaços do dia que ficariam vazios sejam preenchidos por esses clientes.</li>
  <li>Avaliação de serviços: Os usuários podem dar notas de 0 - 5 para os atendimentos recebidos e também deixar um breve comentários sobre as suas impressões. Isso auxília o empresário a garantir que os serviços entregues dentro do seu estabelecimento estejam sempre da melhor forma possível para os seus clintes, pois é através desses feedbacks manter o que está dando certo e melhorar pontos que julgar necessário.</li>
  <li>Fidelização: O estabelecimento pode criar um plano de fidelização para os seus clientes, fazendo com que os mesmos recebam uma porcentagem de desconto depois de um determinado número de serviços executados. Isso faz com que os clientes se tornem assiduos do estabelecimento</li>
</ul>
<h2>Tecnologias Utilizadas</h2>
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
