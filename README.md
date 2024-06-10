# Gerenciamento de Livros
  
> Fabrício da Costa Guimarães

## Sobre

Aplicação Full Stack com:

- FrontEnd: Uso do React em TypeScript
- BackEnd: Uso do ExpressJs e Sequelize em TypeScript.
- Banco de Dados: MySQL
- Deploy: Docker e Docker Compose (Services, Volumes, Networks, Environments e etc)


## Instalação

Após fazer o pull no repositório, abra o terminal no diretório dos arquivos. Contando que o Docker já esteja instalado, faça o seguinte comando:

Windows:

    docker compose up --build -d

Linux:

    sudo docker compose up --build -d


## Verificando os Contêineres

Para verificar se funcionou, faça o seguinte comando e veja os contêineres que foram criados:

Windows:

    docker ps

Linux:

    sudo docker ps

## Imagem, Contêineres, Volumes e Rede

Nessa aplicação, foram utilizadas algumas imagens, sejam elas o frontend, backend, banco de dados e o phpMyAdmin. Para guardar informações, foram criados dois volumes, um para o banco de dados e outro para os logs do backend. Assim como uma rede que faz com que os contêineres conversem entre si utlizando o nome de cada serviço.

## Como testar?

Para testar a funcionalidade da aplicação, abra o navegador no host localhost, na porta do frontend. Ou seja,  http://localhost:8000/. Nessa página terá a opção de ***Adicionar Novos Livros*** (usando os exemplos de [dados-livros.txt](https://github.com/abriciof/webacademy-docker/blob/main/mysql/dados-livros.txt)). 

Após feita a adição de livros, o backend irá receber a resposta do formulário e irá salvar no banco de dados, o que faz com que a página inicial mostre os livros adicionados. 

Você pode verificar separadamente se o livro foi salvo em dois outros lugares, no phpMyAdmin (http://localhost:8080/) acessando o database ***Livraria*** e verificando os registros da tabela **Livros** e também direto no serviço de api do backend, que tem a rota principal do modelo de livros em http://localhost:4444/api/livros. 

Em todos esses casos, é possível verificar a interação entre os contêineres. Em caso de remoção dos contêiners e imagens, todos os dados do banco ficam salvos no volume criado, que pode facilmente recuperar o estado da aplicação.

