FROM verdverm/pypge-base

RUN sudo apt-get update \
	&& \
	sudo apt-get install -y --no-install-recommends \
	libpng-dev \
	libfreetype6-dev \
	python3-setuptools \
	python3-dev \
	python3-pip \
	python3-pandas \
	python3-scipy \
	&& \
	/scripts/clean-apt.sh

WORKDIR /pycode

COPY requirements.txt /pycode/requirements.txt
RUN pip3 install -r /pycode/requirements.txt
	 
COPY ./ /pycode/
RUN python3 /pycode/setup.py install


