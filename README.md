# mop_docker_image

After downloading this repository, run the following command:
```
cd v1_2X_X
docker build -t mop-stable:v1.2X.X .
```
Environment for build:
```
$ cat /etc/os-release
PRETTY_NAME="Ubuntu 24.04.3 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.3 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo
$ docker version --format '{{.Server.Version}}'
29.1.5
$ uname -m
x86_64
$ docker inspect --format='{{index .RepoDigests 0}}' mop-stable:v1.20.8
mop-stable@sha256:92ac6bb0feea57698a4707165851c1efde326e449794dd444dfa0fff66655d1d
$ docker inspect --format='{{index .RepoDigests 0}}' mop-stable:v1.20.9
mop-stable@sha256:8d5bc7098ce656ab55c42e8aa543bea9a9957595b5b446321d48651c23ae978e
$ docker inspect --format='{{index .RepoDigests 0}}' mop-stable:v1.21.0
mop-stable@sha256:6a742e9438ca0cb06d2e445d96a31dd1cf5c219f1a5042725e747ac5c26a3474
```
