# Redis python example 

Real-time Pub/Sub system using Redis (key-value store): https://redis.io/download

![image.png](attachment:cfaa5a5c-0402-41fd-a5f9-c52d37444c7e.png)

## library

- Python3, can install miniconda or anaconda
- Python Redis client: pip install redis



```python
!pip install redis
```

## Key Value Example


```python
# Set a key-value
import redis
r = redis.Redis(host='localhost', port=6379, db=0)
r.set('bigdatakey', 'Hey, It is working!')
```


```python
# Getting a value from a key
import redis
r = redis.Redis(host='localhost', port=6379, db=0)
r.get('bigdatakey')
```

### From terminal, you can type: 
*redis-cli get bigdatakey*

## Pub-Sub Example


```python
# Publisher

import redis
publisher = redis.Redis(host = 'localhost', port = 6379)
message=""
channel = "bigdataclass"
while(message!="exit"):
    message = input("")
    send_message = message
    publisher.publish(channel, send_message)
```


```python

```
