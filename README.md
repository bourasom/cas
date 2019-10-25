# cas
Conf eXo SAML2 with CAS
## Build cas image
cd docker
docker build -t apero/cas-ldap:5.3.10 .
## Run docker cas
docker run -p 80:8080 -p 443:8443 -d --name="cas" -v PATH/TO/thekeystore:/etc/cas/thekeystore -v PATH/TO/config:/etc/cas/config -v PATH/TO/services:/etc/cas/services -v PATH/TO/saml:/etc/cas/saml -ti --rm apero/cas-ldap:5.3.10-
