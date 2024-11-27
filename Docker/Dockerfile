FROM dockurr/windows
WORKDIR /Application
COPY . /Application
RUN apt-get update && apt-get install pulseaudio -y
RUN cp /etc/pulse/client.conf /etc/pulse/client.conf.bak
RUN cp /etc/pulse/daemon.conf /etc/pulse/daemon.conf.bak

RUN cp ./Configuration/pulseaudio/default.pa /etc/pulse/default.pa

ENV PULSE_SERVER=unix:/run/user/1000/pulse/native