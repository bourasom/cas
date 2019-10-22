# cas
Conf eXo SAML2 with CAS
## Build cas image
cd docker
docker build -t apereo/cas:v5.3.10 .
## Run docker cas
docker run -p 80:8080 -p 443:8443 -d --name="cas" -v PATH/TO/thekeystore:/etc/cas/thekeystore -v PATH/TO/CONFIG:/etc/cas/config -ti --rm apereo/cas:v5.3.10
