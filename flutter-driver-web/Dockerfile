FROM cirrusci/flutter:stable

RUN sudo apt update && sudo apt install -y gdebi-core libnss3 libgconf-2-4
COPY ./flutter-driver-web/google-chrome-stable_current_amd64.deb /tmp/google-chrome-stable_current_amd64.deb
RUN sudo gdebi -n /tmp/google-chrome-stable_current_amd64.deb

WORKDIR /app
COPY ./flutter-driver-web/chromedriver /usr/local/bin/chromedriver
RUN sudo chmod +x /usr/local/bin/chromedriver

RUN flutter doctor
