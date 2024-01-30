# FROM <image-name>:<tag> que é versão ou tipo
# WORKDIR <diretorio-padrao-para-executar-os-comandos>
# ARG <nome-variavel>=<valor> essa variavel é aplicada em tempo de compilação da imagem, na hora que cria a imagem
# ENV <nome-variavel>=<valor> essa variavel é aplicada dentro do container, na hora que cria o container
# EXPOSE <porta> mostra de forma explicita em qual porta está rodando a aplicação onde dps para rodar o container será mais facil de descobrir
# COPY <diretorio-remetente> <diretorio-destinatario> exemplo: COPY . . usar assim vai mandar para dentro do diretorio de destino que foi escolhido no WORKDIR
# RUN <comando> comando para ser instalado na etapa de criação da imagem
# ENTRYPOINT <comando> comando para executar a aplicação dentro do container
FROM node:14
WORKDIR /app-node
ARG PORT_BUILD=6000
ENV PORT=$PORT_BUILD
EXPOSE $PORT_BUILD
COPY . .
RUN npm install
ENTRYPOINT npm start