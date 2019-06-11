# pyred-hello

Piecing together a multi-service(?) kubernetes app (deployment?) just to learn how the pieces all fit together

After much gnashing of teeth and rending of hair, I got a single `pod` able to run both the flask app and redis, installing the right things and talking to each other

However, when trying to add replication sets, I didn't quite think through and just made a deployment with 3 replicas
  - now, I have 3 pods, each of which have a flask app _and their own redis_; so no data is getting shared.
