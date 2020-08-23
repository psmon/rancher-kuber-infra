우분투에서 패키지를 설치할 때 사용하는 mirror를 kakao mirror로 변경하여 다운로드 속도를 더 빠르게 해보자.

/etc/apt/sources.list 에 기본 mirror 주소가 설정되어있고, 이를 변경하면 된다.

우선 vi로 파일을 연다.
$ sudo vi /etc/apt/sources.list
파일 내에 있는 모든 저장소 주소를 mirror.kakao.com으로 변경해주면 된다.

%s/(변경할 대상)/(변경할 값) 명령어를 사용하면 된다.
:%s/kr.archive.ubuntu.com/mirror.kakao.com
다 됐으면 apt-get update를 통해 이를 적용하자.
$ sudo apt-get update