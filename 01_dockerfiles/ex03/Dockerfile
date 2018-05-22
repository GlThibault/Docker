FROM 		debian
ENV 		DEBIAN_FRONTEND noninteractive
RUN 		apt-get update && apt-get install -y sudo curl openssh-server ca-certificates
ENV 		EXTERNAL_URL="localhost"
RUN  		adduser --disabled-login --gecos 'Gitlab' git
RUN 		curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | bash
RUN 		sudo apt-get install -y gitlab-ce
RUN 		echo "external url $EXTERNAL_URL" > /etc/gitlab/gitlab.rb
EXPOSE 		2222 80
CMD 		gitlab-ctl reconfigure
