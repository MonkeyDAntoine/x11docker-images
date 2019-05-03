FROM x11docker/lxde

RUN apt update

# 7zip
RUN apt install -y p7zip-full

# Firefox + ublock
RUN apt install -y firefox-esr xul-ext-ublock-origin

# SublimeText
RUN apt install -y wget gnupg && wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | apt-key add - \
	&& echo "deb https://download.sublimetext.com/ apt/stable/" | tee /etc/apt/sources.list.d/sublime-text.list \
	&& apt update && apt install -y sublime-text

# Git
RUN apt install -y git

# Java
RUN apt install -y default-jdk && export JAVA_HOME=$(readlink -f /usr/bin/java | sed "s:bin/java::")

# IntelliJ
RUN wget --output-document /tmp/ideaIU.tar.gz https://download-cf.jetbrains.com/idea/ideaIU-2019.1.1.tar.gz
RUN tar -xzf /tmp/ideaIU.tar.gz -C /opt \
	&& rm /tmp/ideaIU.tar.gz \
	&& ln -s /opt/idea-IU* /opt/idea \
	&& ln -s /opt/idea/bin/idea.sh /usr/bin/idea \
	&& chmod 777 -R /opt/idea*
