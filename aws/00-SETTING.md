# WSL 윈도우준비

인프라는 리눅스로 단일화가 되어가고 있으며, 그로 인해 리눅스 베이스인 맥이 개발장비로 필수였으나

윈도우에서 WSL의 등장으로 리눅스를 활용하는 개발장비의 불편함이 사라졌으며 OS의 경계는 큰 의미가 없어졌습니다.

- https://www.44bits.io/ko/post/wsl2-install-and-basic-usage

# WSL2 준비

WSL2가 1에비해 성능및, 윈도우시스템에서 도커 사용과 통합되었다. (Docker Proxy사용 안해도됨)

윈도우에서 리눅스 개발환경으로 wSL2를 추천합니다. 



  wsl.exe -l -v

    NAME                   STATE           VERSION
  * Ubuntu                 Running         1
    Ubuntu-18.04           Running         2
    docker-desktop         Running         2
    docker-desktop-data    Running         2

  wsl.exe --set-version Ubuntu-18.04 2

  wsl.exe --set-default-version 2

  wsl --set-default Ubuntu-18.04

# PIP준비

  sudo apt-get update

  sudo apt-get install python3-pip

# AWS CLI 설치

  pip3 install awscli

  aws --version

  which aws


# AWS Credential

  Region : ap-northeast-2

  aws configure  
  
  aws ecr get-login --no-include-email --region ap-northeast-2

  aws ecr get-login-password --region ap-northeast-2 | docker login --username AWS --password-stdin 825765832343.dkr.ecr.ap-northeast-2.amazonaws.com

