```bash
cd SBW-ATM

docker build . -f docker/Dockerfile -t sbw-atm-website

docker run -p 8080:80 sbw-atm-website
```
