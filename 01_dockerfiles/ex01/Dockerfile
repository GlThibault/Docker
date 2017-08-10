#docker run -d --name ts3 --publish=9987:9987/udp --publish=30033:30033/tcp --publish=10011:10011/tcp $IID
FROM debian
RUN useradd teamspeak
WORKDIR /home/teamspeak
EXPOSE 9987/udp
EXPOSE 10011/tcp
EXPOSE 30033/tcp
ADD http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_x86-3.0.13.8.tar.bz2 ./
RUN chown teamspeak:teamspeak
USER teamspeak
CMD teamspeak3-server_linux_x86/ts3server_startscript.sh start
