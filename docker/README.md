```bash
cd SBW-ATM

docker build . -f docker/Dockerfile -t sbw-atm-website

docker run -d -p 127.0.0.1:8888:80 sbw-atm-website --name sbw-atm-website
```
