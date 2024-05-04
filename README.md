# webacademy-docker


> Fabrício da Costa Guimarães

## Instalação

Após fazer o pull no repositório, abra o terminal no diretório dos arquivos. Contando que o Docker já esteja instalado, faça o seguinte comando:

Windows:

    docker compose --build up -d

Linux:

    sudo docker compose --build up -d


## Verificando Containers

Para verificar se funcionou, faça o seguinte comando:

Windows:

    docker ps

Linux:

    sudo docker ps

## Imagem, Contêineres, Volumes e Rede

Nessa aplicação, foram utilizado de algumas imagens, sejam elas o frontend, backend, banco de dados, PHP My Admin. Para guardar informações, foram criados dois volumes, um para o banco de dados e outro para os logs do backend. Assim como uma rede que faz com que os contêineres conversem entre si utlizando o nome de cada serviço.

