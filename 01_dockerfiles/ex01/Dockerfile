#docker build -t ts3 .
#docker run -d --name ts3 -p 9987:9987/udp -p 30033:30033/tcp -p 10011:10011/tcp ts3
FROM debian
EXPOSE 9987/udp
EXPOSE 10011/tcp
EXPOSE 30033/tcp
ADD http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2 ./
RUN mv teamspeak3-server_linux_amd64 /opt/teamspeak && useradd teamspeak && mkdir -p /opt/teamspeak/data && chown teamspeak:teamspeak /opt/teamspeak/data
VOLUME /opt/teamspeak/data
USER teamspeak
CMD /opt/teamspeak/ts3server_minimal_runscript.sh start