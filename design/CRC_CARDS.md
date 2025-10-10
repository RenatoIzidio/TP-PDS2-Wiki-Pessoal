# Cartões CRC - Wiki Pessoal

---
**Classe:** JanelaPrincipal
**Responsabilidades:**
- Apresentar a interface principal ao usuário.
- Coordenar os principais componentes visuais da aplicação.
- Exibir informações sobre o estado atual do sistema.
- Receber as intenções do usuário (entrada de dados, cliques).
- Delegar as ações do usuário para as classes de controle.
- Servir como o espaço dedicado a outros elementos da UI.
**Colaboradores:**
- GerenciadorDeNotas
- EditorTextoView
- ListaNotasView

---
**Classe:** GerenciadorBancoDados
**Responsabilidades:**
- Gerenciar o salvamento dos dados (notas, títulos e etc).
- Garantir a integridade dos dados durante as operações de salvamento.
- Abstrair os detalhes do mecanismo de armazenamento do resto do sistema.
- Fornecer uma interface para operações de dados (ex: Criar, Ler, Atualizar, Deletar).
- Lidar com a conexão e transações com a fonte de dados.
**Colaboradores:**
- GerenciadorDeNotas
- Documento

---
**Classe:** Documento
**Responsabilidades:**
- Representar a nota gerada pelo usuário.
- Encapsular os dados e as regras associadas a uma nota.
- Conhecer sua própria informação (título, conteúdo, etc.).
- Garantir a validade de seu próprio estado (ex: título não pode ser vazio).
- Servir como um modelo de dados para os gerenciadores de funções.
- Ser facilmente transferível entre as camadas do sistema.
**Colaboradores:**
- GerenciadorDeNotas
- GerenciadorBancoDados

---
**Classe:** GerenciadorDeNotas (Controller/Service)
**Responsabilidades:**
- Gerenciar as operações e a lógica de anotação do sistema.
- Mediar a comunicação entre a interface e a camada de dados.
- Manter o estado da sessão do usuário (ex: qual nota está ativa).
- Coordenar a resposta do sistema às ações do usuário.
- Garantir que as regras de anotação sejam aplicadas.
- Gerenciar o ciclo de vida dos objetos de modelo (`Documento`).
**Colaboradores:**
- JanelaPrincipal
- GerenciadorBancoDados
- Documento

---
**Classe:** EditorTextoView
**Responsabilidades:**
- Fornecer uma interface para a visualização e edição de texto.
- Apresentar o conteúdo de um `Documento` de forma editável.
- Permitir a manipulação de texto pelo usuário.
- Sinalizar eventos de interação do usuário com o texto.
- Visualizar formatações ou destaques especiais no texto.
- Representar o estado do documento que está sendo editado.
**Colaboradores:**
- JanelaPrincipal
- GerenciadorDeNotas

---
**Classe:** ListaNotasView
**Responsabilidades:**
- Apresentar uma coleção de documentos disponíveis para o usuário.
- Permitir a navegação e seleção de um documento da coleção.
- Refletir o estado atual do conjunto de documentos (adições, remoções).
- Sinalizar a intenção do usuário de interagir com um documento (seleção).
- Oferecer ações de gerenciamento para a lista de notas (ex: iniciar criação/deleção).
**Colaboradores:**
- JanelaPrincipal
- GerenciadorDeNotas
