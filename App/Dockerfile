# FROM palavra-chave requer um nome de imagem de contêiner do Docker
FROM mcr.microsoft.com/dotnet/aspnet:7.0 

#O comando COPY informa ao Docker para copiar a pasta especificada em seu computador para uma pasta no contêiner. 
#Neste exemplo, a pasta de publicação é copiada para uma pasta chamada App no contêiner.
COPY bin/Release/net7.0/publish/ App/

#O comando WORKDIR altera o WORKDIR dentro do contêiner para o aplicativo.
WORKDIR /App

#O comando ENTRYPOINT informa ao Docker para configurar o contêiner para ser executado como um executável. 
#Quando o contêiner é iniciado, o comando ENTRYPOINT é executado. 
#Quando esse comando terminar, o contêiner será interrompido automaticamente.
ENTRYPOINT ["dotnet", "DotNet.Docker.dll"]


#gerando imagem docker
#docker build -t counter-image -f Dockerfile .

#criando container com a imagem gerada
#docker create --name core-counter counter-image

#docker start para iniciar o contêiner
#docker start core-counter

#docker attach para conectar ao container e ver a saida
#docker attach --sig-proxy=false core-counter

#docker stop para iniciar o contêiner
#docker stop core-counter