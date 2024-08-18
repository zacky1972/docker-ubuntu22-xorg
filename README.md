# docker-ubuntu-xorg

## Installation

1. `brew install orbstack xquartz`
2. `open -a XQuartz`
3. Open the XQuartz setting in Security, allow connections from network clients.
4. Restart macOS.
7. `git clone https://github.com/zacky1972/docker-ubuntu-xorg.git`
8. `cd docker-ubuntu-xorg`
9. `docker image build --rm --no-cache --pull -t zacky1972/ubuntu-xorg .`

## Usage (to run `xclock`)

1. `open -a XQuartz`
2. `xhost + localhost`
3. `docker run --env="DISPLAY=host.docker.internal:0" --detach zacky1972/ubuntu-xorg xclock`

