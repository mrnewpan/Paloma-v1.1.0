## Paloma-v1.1.0

git clone https://github.com/palomachain/paloma.git

cd paloma

git checkout v1.1.0

make build

mv build/palomad /usr/local/bin/


### Pigeon-v1.1.0

wget -O - https://github.com/palomachain/pigeon/releases/download/v1.1.0/pigeon_Linux_x86_64.tar.gz | \
tar -C /usr/local/bin -xvzf - pigeon

chmod +x /usr/local/bin/pigeon



### Restart
sudo systemctl start pigeond

sudo systemctl start palomad

sudo journalctl -u palomad -f --no-hostname -o cat



## palomad version

palomad version --long

commit: 7067342b87e3fbee74d5b247d399e9c876ccf84c

cosmos_sdk_version: v0.47.1

go: go version go1.19.4 linux/amd64

name: paloma

server_name: palomad

version: 1.1.0



## pigeon version

pigeon version

App version: v1.1.0

Build commit hash: c301c73fef9aee128fe43231b8e525b4a1612c4a
