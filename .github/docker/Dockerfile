FROM rocker/r-ver:3.6.3

RUN \
	echo "deb http://statmath.wu.ac.at/AASC/debian testing main non-free" > /etc/apt/sources.list.d/rcheckserver.list && \
	apt-get -y update && \
	DEBIAN_FRONTEND=noninteractive apt-get -yq install rcheckserver
