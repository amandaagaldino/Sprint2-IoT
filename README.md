# SOSLocaliza - IoT
## Evolução do projeto em relação à Sprint 1

O projeto evoluiu significativamente da fase de concepção teórica, apresentada na Sprint 1, para a implementação de um protótipo funcional. Enquanto a primeira sprint focou em definir o problema, o público-alvo e a solução macro, **a Sprint 2 concentrou-se em materializar essas ideias em uma aplicação inicial.**

O escopo original foi mantido, mas o foco prático nos permitiu validar a viabilidade da integração entre a interface de usuário e o banco de dados, **transformando os conceitos planejados em funcionalidades tangíveis.**

## Ferramentas e tecnologias exploradas 

Para o desenvolvimento do protótipo, as seguintes ferramentas e tecnologias, planejadas na Sprint 1, foram exploradas, formando uma arquitetura integrada e escalável: 

  - **Oracle APEX (Application Express):** Oracle APEX é uma plataforma de desenvolvimento low-code nativa do Oracle para criar aplicações web e móveis modernas, seguras e escaláveis de forma rápida.

    - Utilizado para a criação rápida e eficiente da interface web do protótipo, permitindo a construção de formulários para       registro e consulta das denúncias. 

  - **Oracle Database integrado:** o Oracle APEX utiliza uma arquitetura encapsulada em banco de dados, baseada em metadados, que garante acesso aos dados com zero latência, além de oferecer escalabilidade e excelente desempenho.
    
    - O banco de dados Oracle é utilizada não apenas para persistência, mas também para processamento de toda lógica de negócio através de PL/SQL.   

  - **OpenStreetMap:** O OpenStreetMap (OSM) não é uma única API, mas sim um banco de dados de mapas aberto e gratuito, como uma "Wikipedia dos Mapas".
    
    - O OpenStreetMap é usada para mostrar visualmente o mapa e onde futuramente o alerta de emergência aparecerá. 


## Funcionalidades do protótipo
O protótipo atual, desenvolvido no **Oracle APEX**, já possui as seguintes funcionalidades implementadas e em execução: 

  - **Acesso a conta:** Permite que usuários já existentes acessem o aplicativo usando seu email e senha.
  <img src="./img/imgEntrar.png" alt="Imagem">

  - **Formulário de registro de usuário:** Permite que novos usuários criem uma conta. Os campos solicitados são: Nome Completo, Email, Data de Nascimento, CPF, Senha e Confirmação de Senha.
    <img src="./img/imgCadastro.png" alt="Imagem">

  - **Formulário cadastro de CEP:** uma interface web permite que o usuário insira o nome e um CEP, essas informações ficaram salvas e nas proxima vesão (Sprint 3) o usuario receberar alertas dessa região.
  <img src="./img/imgCEP.png" alt="Imagem">

  - **Pagina de orientações:** O app possui uma seção detalhada com guias sobre como agir em diferentes tipos de "eventos adversos". O exemplo mostrado é "Orientações para Enchentes", que é dividido em três fases:
    - Antes da Enchente (Ex: preparar kit de emergência, identificar rotas de fuga).
    - Durante a Enchente (Ex: evitar áreas alagadas, não usar equipamentos elétricos).
    - Após a Enchente (Ex: aguardar autorização para retornar, verificar danos estruturais).

  <img src="./img/imgOrientacoes.png" alt="Imagem">

  - **Mapa (Sprint 3):** Mapa é usada para mostrar visualmente o mapa e onde futuramente o alerta de emergência aparecerá. 

   - **Envio de SMS (Sprint 3):** Há um botão de destaque ("Enviar SMS") para usuários que "estão em uma área de risco", indicando uma forma rápida de pedir ajuda ou contatar serviços de emergência.

  <img src="./img/imgMapa.png" alt="Imagem">


## Integrações que já puderam ser testadas ou implementadas

A principal integração implementada e testada com sucesso nesta sprint foi:

- **Integração entre Oracle APEX e Oracle Database (banco de dados integrado):** a conexão entre a interface do protótipo e o banco de dados embutido no APEX estão totalmente funcionais. Os formulários criados no APEX conseguem inserir CEP e consultar dados diretamente nas tabelas do banco de dados, garantindo a persistência das informações.

- Adicionalmente, **foi realizado um teste preliminar (prova de conceito) de consumo da API do SMS**, confirmando a viabilidade técnica de enviar da mensagem.

## Próximos passos até a versão final 

Para as próximas sprints, os passos planejados para a evolução do projeto são: 

  1. **Integração contínua da IA:** implementar de forma definitiva a chamada à **API de análise** para que toda novo alerta seja automaticamente classificada e marcada no banco de dados.
     
  2. **Desenvolvimento do módulo de análise de dados:** criar o back-end que analisará os dados armazenados para identificar padrões e tendências suspeitas.
     
  3. **Intregração com a API de SMS:** implementar de forma definitiva a **API de SMS** desenvolvida em java utilizando o Twilio.
     
  4. **Refinamento da interface (UI/UX):** melhorar a experiência do usuário no protótipo com base em feedbacks e testes de usabilidade.

## Vídeo de demonstração

Segue abaixo o link do vídeo apresentando a evolução do projeto e demonstrando o funcionamento do protótipo: 

> 🎬 Clique na imagem abaixo para assistir no YouTube

[![Assista ao vídeo](https://img.youtube.com/vi/UewdXhF_TZ8/maxresdefault.jpg)](https://youtu.be/ctzDoaCnXF4?si=H6sil0fHTgRDbUEb) 
