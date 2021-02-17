## :chess_pawn: Estrutura para o angular :chess_pawn:

<p align="center">:black_circle: Proposta inicial de criar uma seed para centralizar e desacoplar cada responsabilidade, permitindo o gerenciamento de paginas, componentes e regras de negócio para projetos de larga escala e voltado a squads com a finalidade de reduzir efeitos colaterais, aumentar a reutilização e garantir entregas mais integras. :black_circle:</p>

- /app
  - /componentes
    - componentes reutilizaveis para toda aplicação.
  - /directives
    - diretivas da aplicação.
  - /guards
    - middleware de paginas. 
  - /layouts
    - estrutura comum entre páginas, ex: header e menu lateral, vao ser comuns entre todas a paginas. 
  - /mocks
    - dados fixos ex: lista de usuarios padrão para alguma finalidade temporaria.
  - /modules
    - /nome_do_modulo
      - /components
        - componentes reutilizaveis dentro de um contexto especifico, ou nesse caso do modulo em especifico.
      - /helpers
        - codígos reutilizaveis dentro de um contexto especifico, ou nesse caso do modulo em especifico, ex: validações, metódos, etc.
      - /pages
        - /criar
          - /helpers
            - codígos exclusivos com a finalidade de serem reaproveitados dentro das partições ou dos componentes inteligentes de uma página, e também para reduzir o tamanho e a responsabilidade do arquivo principal da pagina.
          - /partials
            - crie componentes inteligentes com a finalidade de segregar e diminuir as responsabilidades do arquivo principal da página.
          types.ts //armazena tipagem de parametro ou dados da pagina em especifico.
          main-file.ts
          main-file.html
      types.ts //armazena tipagem de parametro ou dados do modulo.
      nome_do_module.module.ts
      nome_do_module.route.ts
    - /outro-modulo
  - /pipes
    - crie seus pipes para RxJS
  - /services
    - /nome_do_servico 
      - arquivos com as funcionalidades de acordo com o serviço
    - /user
      - crud.ts
      - permissões.ts // gerencia a comunicação com a api de permissões da tela que um usuario pode acessar  
      - galeria-fotos.ts // gerencia a comunicação com a api de galeria de fotos do usuario.