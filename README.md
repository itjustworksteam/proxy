# proxy
a simple proxy for docker containers

You can simple use this image using docker-compose:

```
version: '2'

services:
  app:
    image: therickys93/telegrambot
    environment:
      - TELEGRAM_BOT_TOKEN=your_token
      - TELEGRAM_SERVER_TOKEN=123
      - PORT=80
  proxy:
    image: therickys93/proxy
    ports:
      - "80:80"
```

The ```app``` is a key name and must be listen on port ```80```
