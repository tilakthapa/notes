# Running RabbitMQ on Docker
- install docker
  - for windows - https://hub.docker.com/editions/community/docker-ce-desktop-windows
- ``docker --version``
- download RabbitMQ image with management plugin in order to be able to view server-side GUI. ``docker pull rabbitmq:3-management``
- run ``docker run -d -p 15672:15672 -p 5672:5672 --name TT rabbitmq:3-management``
- go to http://localhost:15672/#/ and login. username/password - ``guest/guest``
