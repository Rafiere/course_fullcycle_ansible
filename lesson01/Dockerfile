FROM ubuntu:latest

RUN apt-get update && apt-get install vim ssh ansible -y
RUN echo 'root:fullcycle' | chpasswd

# Estamos dando a permissão para o usuário root acessar o SSH como "root".
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -i 's/#Port 22/Port 2222/' /etc/ssh/sshd_config #Estamos habilitando a porta 22.
RUN sed -i 's/#PubkeyAuthentication/PubkeyAuthentication/' /etc/ssh/sshd_config # Estamos permitindo a utilização com public key
RUN sed -i 's/#PasswordAuthentication/PasswordAuthentication/' /etc/ssh/sshd_config # Estamos permitindo a utilização com senha