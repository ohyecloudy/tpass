FROM ubuntu

RUN apt-get update && apt-get install -y pass unzip vim

RUN  >~/gen-key-script echo "Key-Type: 1" && \
    >>~/gen-key-script echo "Key-Length: 2048" && \
    >>~/gen-key-script echo "Subkey-Type: 1" && \
    >>~/gen-key-script echo "Subkey-Length: 2048" && \
    >>~/gen-key-script echo "Name-Real: user b" && \
    >>~/gen-key-script echo "Name-Email: user_b@mail.com" && \
    >>~/gen-key-script echo "Expire-Date: 0"
RUN gpg-agent --daemon && gpg --gen-key --batch ~/gen-key-script
