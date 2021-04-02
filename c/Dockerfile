FROM cirrusci/flutter:2.0.3

RUN sudo apt update && sudo apt install -y gdebi-core libnss3 libgconf-2-4
ADD ./google-chrome-stable_current_amd64.deb ./google-chrome-stable_current_amd64.deb
RUN sudo gdebi -n google-chrome-stable_current_amd64.deb

WORKDIR /
ADD ./chromedriver ./chromedriver
RUN sudo chmod +x chromedriver

RUN flutter config --enable-web && flutter doctor