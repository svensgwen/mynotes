

sudo apt install webp libwebp-dev libwebpdemux2 libwebpmux3

sudo apt install qt6-base-dev-tools


## Yarn Install

curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update

sudo apt install yarn

yarn -v


