# Set up a trojan server
```
apt install nginx socat -y
systemctl stop nginx

# install xray
bash -c "$(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh)" @ install -u root

# https://github.com/acmesh-official/acme.sh/wiki/How-to-issue-a-cert
curl https://get.acme.sh | sh

# make sure tcp port 80 is opened or use zerossl
~/.acme.sh/acme.sh --issue -d yourdomain.com --standalone --server letsencrypt
...
```
