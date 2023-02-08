# RabbitMQ

RabbitMQ is an implementation of the AMQP message model. With this type of message model, the producer, the service that produces the messages, instead of producing directly to a message queue, it's going to produce to an exchange. It's going to receive all the messages and then distribute them according to whom they're addressed to.

There are several reasons why this message queue is so widely used:
The flexibility with the way the messages move through the system.
One advantage of this message model is the flexibility with which the messages can move through the system. And that flexibility is largely in part to the different types of exchanges available.
This message broker, or message brokers in general, is also going to help with scalability.
It is cloud friendly, easy to containerise, and supports SASL, LDAP and TLS for authentication and authorization.

In this application, the message is sent to RabbitMQ, the direct exchange is used for publishing the message to RabbitMQ, and this RabbitMQ message is then consumed by the spring boot application.

Setup:
1.Download and install ERlang  http://erlang.org/download/
2.Downlaod and install RabbitMQ  https://www.rabbitmq.com/install-windows.html#installer
3.Go to RabbitMQ Server install Directory C:\Program Files\RabbitMQ Server\rabbitmq_server-3.x.x\sbin
4.Set the environment as the following: 
ERLANG_HOME = C:\Program Files\Erlang OTP
RABBITMQ_BASE = C:\Program Files\RabbitMQ Server\rabbitmq_server-3.x.x
5.Run command rabbitmq-plugins enable rabbitmq_management
6.Open browser and enter http://localhost:15672/ to redirect to RabbitMQ Dashboard
7.Login page default username and password is guest, guest
8.After successfully login you should see RabbitMQ Home page


In case the rabbitmq server is not working, check the RabbitMQ/Erlang version compatibility:
https://www.rabbitmq.com/which-erlang.html

Open the command prompt and run the following commands one by one:

cd c:\Program Files\RabbitMQ Server\rabbitmq_server-3.x.x\sbin

rabbitmq-service remove
rabbitmq-service install
rabbitmq-service start
rabbitmq-server.bat start
