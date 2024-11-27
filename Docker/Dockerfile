FROM dockurr/windows
WORKDIR /Application
RUN apt-get update && apt-get install pulseaudio -y
ENV PULSE_SERVER=unix:/run/user/1000/pulse/native