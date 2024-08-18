# docker-ubuntu-xorg

Dockerfile for Ubuntu 22.04 with xorg.

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

## License

Copyright (c) 2024 University of Kitakyushu

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at [http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
