# messaging-with-rabbitmq
MESSAGING WITH RABBITMQ
-----------------------
This was the first time I've worked with RabbitMQ. It's a simple publish-and-subscribe application using RabbitTemplate from Spring's AMQP.
The RabbitTemplate I created in the MessagingRabbitmq.java class sends a message to the queue if it has the correct routing key
(foo.bar.# in this case), and the Receiver object receives it, which I registered to recieve messages in the RabbitTemplate.
One of the difficulties I had setting this application up was getting the RabbitMQ server running correctly. The .erlang.cookie
file was not routing to the correct directory. This would give me an error and prevent the server from starting, I could not figure
out what was wrong. Eventually I found that the cookie was being placed under the SysWOW64 file, and then moved it to the RabbitMQ base 
folder which solved the problem.
This process is very similar to the simple Redis messaging application I made before this.
