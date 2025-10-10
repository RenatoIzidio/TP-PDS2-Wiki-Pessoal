# User Stories - Wiki Pessoal

## US-01: Criação de Nova Nota
* **Descrição:** Como um **usuário**, quero **criar uma nova nota com um título e conteúdo**, para poder **registrar novas informações**.
* **Critérios de aceitação:**
    1.  O sistema deve solicitar um título para a nova nota.
    2.  O sistema deve validar que o título informado ainda não existe.
    3.  O sistema deve fornecer uma área de texto para inserção do conteúdo.
    4.  O sistema deve salvar a nova nota no banco de dados.

## US-02: Interligação Automática de Notas
* **Descrição:** Como um **usuário**, quero que o **sistema identifique e transforme em links os títulos de outras notas que eu menciono no texto**, para que eu possa **navegar facilmente entre ideias conectadas**.
* **Critérios de aceitação:**
    1.  O sistema deve escanear o conteúdo da nota ativa em busca de texto, no banco de dados, que corresponda exatamente a títulos de outras notas.
    2.  O texto correspondente a um link deve ser exibido com formatação diferente (ex: azul e sublinhado).
    3.  Clicar em um link deve carregar e exibir o conteúdo da nota correspondente na área de edição.

## US-03: Navegação e Visualização de Notas
* **Descrição:** Como um **usuário**, quero **ver uma lista com os títulos de todas as minhas notas**, para poder **ter uma visão geral do meu conhecimento e selecionar uma para ler ou editar**.
* **Critérios de aceitação:**
    1.  A lista de títulos de notas deve estar sempre visível em um painel lateral.
    2.  A lista deve ser atualizada automaticamente quando uma nota é criada ou deletada.
    3.  Clicar em um título na lista deve carregar seu conteúdo na área de edição principal.
    4.  A lista deve ser ordenada alfabeticamente.

## US-04: Exclusão de Nota
* **Descrição:** Como um **usuário organizador**, quero **poder apagar uma nota que não é mais relevante**, para **manter meu workspace limpo e focado**.
* **Critérios de aceitação:**
    1.  O sistema deve fornecer uma opção para deletar uma nota a partir da lista de notas.
    2.  O sistema deve solicitar uma confirmação antes de apagar permanentemente a nota.
    3.  Após a exclusão, a nota deve ser removida do banco de dados e da lista de visualização.

## US-05: Busca por Conteúdo
* **Descrição:** Como um **usuário pesquisador**, quero **buscar por uma palavra-chave no título e no conteúdo de todas as notas**, para **encontrar rapidamente todas as informações que possuo sobre um tópico específico**.
* **Critérios de aceitação:**
    1.  O sistema deve possuir um campo de busca na interface.
    2.  A busca deve retornar uma lista de títulos de notas que contêm a palavra-chave.
    3.  Clicar em um resultado da busca deve abrir a nota correspondente.

## US-06: Renomear uma Nota
* **Descrição:** Como um **usuário editor**, quero **poder renomear o título de uma nota**, para **corrigir erros de digitação ou refinar o nome de um conceito**.
* **Critérios de aceitação:**
    1.  O sistema deve fornecer uma opção para renomear uma nota.
    2.  O sistema deve impedir que o novo título seja igual a um título já existente.
    3.  A mudança de título deve ser refletida imediatamente na lista de notas e no banco de dados.
