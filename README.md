# elegant-scipy

## 실습 환경 설정하기

역자는 맥 사용자이므로 맥 기준으로 포스팅한다.  

[http://conda.pydata.org/miniconda.html](http://conda.pydata.org/miniconda.html)에서 운영체제에 맞는 콘다를 내려받는다. 그리고, 파일에 적절한 권한을 준 후, 스크립트를 실행한다(윈도우 사용자는 exe 파일을 내려받은 후 실행한다).  

```bash
$ chmod 755 Miniconda3-latest-MacOSX-x86_64.sh
$ ./Miniconda3-latest-MacOSX-x86_64.sh
```

Yes를 입력하여 라이선스에 동의하고, Enter키를 치면 기본 경로에 설치된다. 책 0장에 있는 명령을 입력하여 이 책의 실습 패키지를 설치한 후, 여기에 접속한다.

```bash
$ git clone https://github.com/AstinCHOI/elegant-scipy
$ cd elegant-scipy

$ conda env create --name elegant-scipy -f environment.yml
$ source activate elegant-scipy
```


