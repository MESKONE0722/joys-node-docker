FROM ubuntu:18.04
LABEL version="9.0"

RUN apt-get update && apt-get install --yes software-properties-common apt-utils
RUN add-apt-repository ppa:ethereum/ethereum
RUN apt-get update && apt-get install geth --yes

#ADD http://boot.joys.digital/genesis.json /root/
#ADD http://boot.joys.digital/fork1.json /root/
ADD http://boot.joys.digital/fork2.json /home/Joys/
ADD http://boot.joys.digital/static-nodes.json /home/Joys/

ADD start.sh /Joys/start.sh
RUN chmod +x /Joys/start.sh

EXPOSE 30303
EXPOSE 30303/udp
EXPOSE 8545

ENTRYPOINT /Joys/start.sh
