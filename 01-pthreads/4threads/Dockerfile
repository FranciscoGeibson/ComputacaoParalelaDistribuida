# Usar uma imagem base do Ubuntu
FROM ubuntu:20.04

# Definir o diretório de trabalho dentro do container
WORKDIR /app

# Definir as variáveis de ambiente para o fuso horário e evitar configuração interativa
ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=UTC

# Instalar pacotes necessários
RUN apt-get update && \
    apt-get install -y \
    g++ \
    make \
    cmake \
    wget \
    libjsoncpp-dev \
    git

# Baixar diretamente o json.hpp do repositório do GitHub
RUN wget https://raw.githubusercontent.com/nlohmann/json/develop/include/nlohmann/json.hpp -P /usr/local/include/json

# Copiar o código C++ para dentro do container
COPY . .

# Comando para compilar o código C++ (assumindo que o arquivo é main.cpp)
RUN g++ -o my_program 4threads.cpp -std=c++11 -pthread

# Comando para rodar o programa compilado
CMD ["./my_program"]
