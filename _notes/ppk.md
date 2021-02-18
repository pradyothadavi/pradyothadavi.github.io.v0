brew install putty

puttygen privatekey.ppk -O private-openssh -o privatekey.pem

ssh -i privatekey.pem user@my.server.com

chmod go-rw privatekey.pem