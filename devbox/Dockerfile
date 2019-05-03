FROM x11docker/lxde

RUN apt update

# 7zip
RUN apt install -y p7zip

# Firefox + ublock
RUN apt install -y firefox-esr xul-ext-ublock-origin

# SublimeText
RUN apt install -y wget gnupg && wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | apt-key add - \
	&& echo "deb https://download.sublimetext.com/ apt/stable/" | tee /etc/apt/sources.list.d/sublime-text.list \
	&& apt update && apt install -y sublime-text

# Git
RUN apt install -y git

# IntelliJ
# RUN wget https://download-cf.jetbrains.com/idea/ideaIU-2019.1.1.tar.gz
