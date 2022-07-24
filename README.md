# Dashy

https://github.com/Lissy93/dashy

```wrap
mkdir -p dashy/{public,icons}

nano docker-run.txt

nano public/conf.yml

appConfig:
  theme: colorful
  layout: auto
  iconSize: medium
  language: en
pageInfo:
  title: HJCOM
  description: Welcome to My Dashboard!
  navLinks:
    - title: GitHub
      path: https://github.com/Lissy93/dashy
    - title: Documentation
      path: https://dashy.to/docs
  footerText: ''
sections:
  - name: Starter
    icon: fas fa-server
    items:
      - title: Google
        description: Search
        url: https://google.com

docker run -d \
  -p 8086:80 \
  --volume /home/jassa/docker/dashy/public/conf.yml:/app/public/conf.yml \
  --volume /home/jassa/docker/dashy/icons:/app/public/item-icons/icons \
  --name dashy \
  --restart=unless-stopped \
  lissy93/dashy:latest
 
 ```
```wrap
git clone https://github.com/walkxcode/dashboard-icons.git
