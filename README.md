# Catálogo de Ferramentas de Dobradeira

Site de consulta desenvolvido pela **Engenharia de Processo** para centralizar informações técnicas de punções, matrizes e ferramentas especiais utilizadas em dobradeiras.

O catálogo permite consultar famílias de ferramentas, códigos, dimensões, fabricantes e desenhos técnicos. Usuários autorizados também podem atualizar o conteúdo diretamente pela interface.

## Acesso ao site

Após ativar o GitHub Pages, o catálogo ficará disponível em:

**https://otavioschraiberpena-cmyk.github.io/Matriz-de-dobradeira/**

## Funcionalidades

- Consulta pública das famílias de ferramentas.
- Pesquisa por código, dimensão, ângulo ou fabricante.
- Navegação pelo índice lateral e pelos botões de famílias.
- Visualização ampliada dos desenhos técnicos.
- Impressão e geração de PDF pelo navegador.
- Login para usuários autorizados.
- Criação, edição e exclusão de ferramentas.
- Criação, edição, exclusão e reordenação de famílias.
- Inclusão e exclusão de imagens nas famílias.
- Gerenciamento de usuários nas configurações.
- Armazenamento e sincronização dos dados com o Supabase.
- Atualização automática dos dados para computadores em modo de consulta.
- Tela de carregamento enquanto os dados ainda não foram sincronizados.

## Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript
- Supabase Database
- Supabase JavaScript Client
- GitHub Pages

## Estrutura do repositório

```text
Matriz-de-dobradeira/
├── index.html
└── README.md
```

O arquivo `index.html` contém a interface, os estilos e os scripts necessários para executar o catálogo.

## Publicação no GitHub Pages

1. Abra o repositório no GitHub.
2. Entre em **Settings**.
3. No menu lateral, clique em **Pages**.
4. Em **Source**, selecione **Deploy from a branch**.
5. Selecione a branch **main**.
6. Selecione a pasta **/ (root)**.
7. Clique em **Save**.
8. Aguarde a conclusão da publicação na aba **Actions**.

## Atualização do site

Para publicar uma nova versão:

1. Renomeie o novo arquivo para `index.html`.
2. Substitua o `index.html` existente no repositório.
3. Confirme a alteração em **Commit changes**.
4. Aguarde o GitHub Pages concluir uma nova publicação.
5. Atualize o navegador com `Ctrl + F5` caso a versão anterior ainda apareça.

## Banco de dados

O site utiliza o Supabase para armazenar:

- Dados das famílias e ferramentas.
- Imagens associadas às famílias.
- Data e usuário da última atualização.
- Usuários autorizados a editar o catálogo.

Enquanto a leitura inicial do Supabase não for concluída, o catálogo permanece oculto e apresenta somente a tela **Carregando**.

## Uso administrativo

Depois do login, o usuário autorizado pode:

- Editar e excluir ferramentas.
- Adicionar novas ferramentas.
- Criar e reorganizar famílias.
- Alterar nomes e colunas das famílias.
- Adicionar ou apagar imagens.
- Gerenciar acessos em **Configurações**.
- Salvar as alterações no banco de dados.

## Segurança

Este projeto utiliza uma chave pública do Supabase no navegador, como é esperado em aplicações web cliente. Entretanto, a versão atual utiliza login controlado pela própria página e políticas públicas de acesso ao banco.

Por esse motivo:

- Não armazene dados pessoais, confidenciais ou estratégicos no catálogo.
- Nunca coloque a chave `service_role`, senha do banco ou chave secreta no `index.html`.
- Para uma publicação com maior proteção, recomenda-se migrar o login administrativo para o Supabase Auth e limitar as operações de escrita por políticas RLS para usuários autenticados.

## Responsável

**Engenharia de Processo**

## Licença

Uso interno. A distribuição, alteração ou reutilização deve seguir as diretrizes da organização responsável pelo catálogo.
