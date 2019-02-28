# Build your kernel driver

In order to build any driver yourself, go on your docker host and use follwing shell commands to build it:

```
mkdir driver-iwlwifi

cd driver-iwlwifi

git clone https://github.com/xcp-ng/xcp-ng-build-env

git clone https://github.com/rushikeshjadhav/iwlwifi

chown 1000 ./iwlwifi/ -R

./xcp-ng-build-env/run.py -b 7.6 --build-local iwlwifi/ --rm
```
