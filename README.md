#Heroku Kafka to Postgres Consumer

<br>
This demo application is written in ASP.NET Core and is intended to consume a "web traffic data stream" from a Heroku Kafka Topic and write all messages to a Heroku Postgres database. It has 2 brother apps, one is the Kafka Producer which generates the simulated Web Traffic for our Kafka Topic, and another which finds specific messages and flips them in Postgres for Heroku Connect to Sync to Salesforce. <br><br>
Obviously you need Heroku Kafka in order to use this app as well, in addition to the following Heroku App Config VARs:<br>
<br><p>
- ClientID (if using the default code, value should be set to 29481765 as this is the "Tracking ID" we key off of for the final/3rd app)
- DATABASE_URL (Heroku Postgres-provisioned DB URL)
- KAFKA_REST_API_URL (should be set to the Kafka Rest API URL...similar to http://kafka-rest-app.herokuapp.com/api/messages)
- KAFKA_TOPIC (should be set to the exact name of the Kafka Topic to write messages to)
<br><p>
The other Config VARs are set when you provision Heroku Kafka and include:
<br>
- KAFKA_CLIENT_CERT
- KAFKA_CLIENT_CERT_KEY
- KAFKA_JMX_URL
- KAFKA_PLAINTEXT_URL (if in a Private Space)
- KAFKA_TRUSTED_CERT
- KAFKA_URL
- KAFKA_ZOOKEEPER_JMX_URL
- KAFKA_ZOOKEEPER_URL
- SECURITY_PROTOCOL_CONFIG
<br><p>

Deploy this App to Heroku by clicking the button below:

<a href="https://heroku.com/deploy?template=https://github.com/herokumx/kafka-to-postgres"> <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy">
</a>
