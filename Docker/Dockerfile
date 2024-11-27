FROM dockurr/windows
WORKDIR /Application
RUN apt-get update && apt-get install pulseaudio -y
RUN cp /etc/pulse/client.conf /etc/pulse/client.conf.bak
RUN cp /etc/pulse/daemon.conf /etc/pulse/daemon.conf.bak

RUN cd . && du -h > /Application/du.txt

RUN cp ./Win11pro/Configuration/pulseaudio/default.pa /etc/pulse/default.pa

ENV PULSE_SERVER=unix:/run/user/1000/pulse/native