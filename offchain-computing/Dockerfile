FROM python:3.7-alpine3.10

### install some python3 dependencies
RUN apk --no-cache --update-cache add gcc libc-dev
RUN SCONE_MODE=sim pip3 install eth_abi

### copy the code inside the image
COPY src /app

ENTRYPOINT ["python3", "/app/app.py"]
