FROM rocker/r-ver:3.6.3

RUN \
	apt-get update && \
	apt-get -y dist-upgrade && \
	DEBIAN_FRONTEND=noninteractive apt-get -yq install \
	locales cloc curl parallel debian-keyring \
	libnode-dev libarchive-dev texlive-extra-utils python3

RUN curl "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0xfe6b0f6d941769e0b8ee7c3c3b1c3b572302bcb1" | APT_KEY_DONT_WARN_ON_DANGEROUS_USAGE=1 apt-key add -

RUN \
	echo "deb http://statmath.wu.ac.at/AASC/debian testing main non-free" > /etc/apt/sources.list.d/rcheckserver.list && \
	apt-get -y update && \
	DEBIAN_FRONTEND=noninteractive apt-get -yq install rcheckserver
