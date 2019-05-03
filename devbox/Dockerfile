FROM x11docker/lxde

RUN apt update

# package management
RUN apt install -y snapd

# Firefox + adblock
RUN apt install -y firefox-esr xul-ext-ublock-origin

# SublimeText
RUN apt install -y wget gnupg && wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | apt-key add - \
	&& echo "deb https://download.sublimetext.com/ apt/stable/" | tee /etc/apt/sources.list.d/sublime-text.list \
	&& apt update && apt install -y sublime-text
