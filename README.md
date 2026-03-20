CRUD App atividade (Flutter)
Aplicação Flutter para gerenciamento de **clientes** e **produtos**, com operações de CRUD (criar, listar, editar e remover), organizada em camadas para separar interface, regras de negócio e acesso a dados.
## Visão geral
Este projeto utiliza uma arquitetura simples em camadas:
- `views`: telas da aplicação
- `components`: widgets reutilizáveis de UI
- `providers`: gerenciamento de estado e comunicação com a interface
- `services`: regras de negócio e orquestração de operações
- `models`: entidades, DAOs e implementação de persistência
- `data`: dados padrão/iniciais
- `routes`: definição de rotas da aplicação
- `main.dart`: ponto de entrada do app
## Estrutura principal
``text
lib/
  main.dart
  routes/
    routes.dart
  views/
    inicial.dart
    clients_list.dart
    produto_list.dart
    formulaire.dart
    formulario_produto.dart
  components/
    client_widget.dart
    produto_widget.dart
  providers/
    client_provider.dart
    produto_provider.dart
  services/
    client_service.dart
    produto_service.dart
  models/
    client.dart
    produto.dart
    client_dao.dart
    produto_dao.dart
    client_dao_impl.dart
    produto_dao_impl.dart
    exception.dart
    dbCreationClientes.sql
    dbCreationProdutos.sql
  data/
    standard_client.dart
    standard_produto.dart


Fluxo da aplicação
De forma geral, o fluxo segue esta ordem:

A tela (views) dispara uma ação do usuário (ex.: salvar cliente).
O provider recebe a ação e atualiza o estado da UI.
O service aplica regras de negócio/validação.
O DAO (models/*_dao_impl.dart) executa acesso aos dados.
A resposta volta para o provider, que atualiza a interface.
Funcionalidades
Cadastro de clientes
Listagem de clientes
Edição e remoção de clientes
Cadastro de produtos
Listagem de produtos
Edição e remoção de produtos
Pré-requisitos
Flutter SDK
Dart SDK (incluído com Flutter)
Android Studio, VS Code ou Cursor com suporte a Flutter
Emulador Android/iOS ou dispositivo físico
Como executar
Instale as dependências:
flutter pub get
Execute o aplicativo:
flutter run
Comandos úteis
Analisar o projeto:
flutter analyze
Rodar testes:
flutter test
Limpar build:
flutter clean
Observações
Os scripts SQL em lib/models/dbCreationClientes.sql e lib/models/dbCreationProdutos.sql representam a criação das estruturas de dados usadas pela aplicação.
O projeto possui separação de responsabilidades para facilitar manutenção e evolução.
