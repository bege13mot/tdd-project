FROM python:3.6.1

# set working directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# add requirements (to leverage Docker cache)
ADD ./requirements.txt /usr/src/app/requirements.txt

# install requirements
RUN pip install -r requirements.txt --quiet

# add entrypoint.sh
ADD ./entrypoint.sh /usr/src/app/entrypoint.sh

# add app
ADD . /usr/src/app

# run server
CMD ["./entrypoint.sh"]