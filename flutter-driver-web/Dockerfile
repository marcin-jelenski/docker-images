FROM cirrusci/flutter:2.0.1

RUN sudo apt update && sudo apt install -y gdebi-core libnss3 libgconf-2-4
ADD ./flutter-driver-web/google-chrome-stable_current_amd64.deb /tmp/google-chrome-stable_current_amd64.deb
RUN sudo gdebi -n /tmp/google-chrome-stable_current_amd64.deb

WORKDIR /
ADD ./flutter-driver-web/chromedriver ./chromedriver
RUN sudo chmod +x chromedriver

RUN flutter config --enable-web && flutter doctor