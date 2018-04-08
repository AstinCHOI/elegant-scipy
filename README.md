# elegant-scipy

## 책을 읽기 전에  
이 책은 일반 과학자 및 데이터 과학자를 위한 책이다. 역자는 과학자도 아니고 데이터 과학자도 아니다. 이 책을 번역하면서 엄청 끙끙앓았다. 또한, 번역을 마쳤으나 마음속으로 아직 찝찝한 구석이 많다. 이 책을 제대로 이해하기 위해서 많은 사전 지식이 필요하다. 선형대수학에 대한 기초가 부족하다면, 'Eigenvalue(고유벡터)'님 글의 첨부파일을 먼저 읽는 것을 추천한다. 역자는 출/퇴근시간에 이 첨부파일을 출력하여 읽었다. 또한, 이 책과 함께 '다크프로그래머'님의 블로그 글을 병행하면서 읽으면 좋을 것 같다. 개인적으로 이 책은 '다크프로그래머'님과 같은 분이 번역했으면 독자들에게 조금 더 좋았을 것 같다. 또한, 책에 나오는 어려운 용어들은 이 저장소의 '용어_x장.md'의 마크다운 파일에 간략하게 설명과 링크를 달았다. 일부 몇 장은 생물학(유전체, 유전자, DNA 등)에 대한 지식이 필요하고, 일부 몇 장은 확률론 및 선형대수학, 주파수 및 푸리에 변환에 대한 내용을 미리 알면 좋다. 불행하게도 역자는 이러한 지식이 없어서 엄청 끙끙앓으며, 모르는 내용은 위키피디아와 블로그 내용을 뒤져가면서 아주 조금 이해한 수준이다. 그리고, 이 책의 원서와 병행하면서 읽는 것을 추천한다(원서는 저자의 github 저장소에 마크다운으로 제공한다). 이 책의 구입과 이 저장소로 인해서 개인적으로 수익이 발생하는 부분은 없다. 이 저장소는 번역서를 읽는데 조금이나마 독자들에게 도움이 되기 위한 장소이며, 또한 번역 과정에서 개인적으로 모르는 부분을 간략하게 정리해놓은 저장소다(잘못된 내용이나 추가되면 좋을 것 같은 내용이 있으면 이 저장소에 'Pull Request'를 환영한다).  

* 'Eigenvalue'님의 블로그 글 (선형대수학 기초)  
http://blog.daum.net/eigenvalue/10856412  

* '다크프로그래머'님의 블로그  
http://darkpgmr.tistory.com/  

* 원서 저장소  
https://github.com/elegant-scipy  

* 이 책의 원서 마크다운 (영문)  
https://github.com/elegant-scipy/elegant-scipy/tree/master/markdown  

이 책의 코드는 아래의 실습환경에서 모두 테스트했다. 이 저장소의 'x장. [제목].ipynb' 파일의 주피터 노트북 파일을 참조한다. 마지막으로, 이 책은 온전히 내 힘으로 번역할 수 없었다는 것을 말하고 싶다. 인터넷에 좋은 글을 많이 올려주시는 블로거님들과 위키가 아니었으면 조금이라도 이해하는게 어려웠을 것이다. 이 책이 도움되었다면, 선량한 목적과 열정으로 지식을 공유하는 블로거의 공이며, 이 책의 오역과 잘못된 부분이 있다면 모두 내 탓이다.  

## 실습 환경 만들기

먼저, [http://conda.pydata.org/miniconda.html](http://conda.pydata.org/miniconda.html)에서 운영체제에 맞는 콘다를 내려받는다. 그리고, 파일에 적절한 권한을 준 후, 스크립트를 실행한다(윈도우 사용자는 exe 파일을 내려받은 후 실행한다).  

```bash
$ chmod 755 Miniconda3-latest-MacOSX-x86_64.sh
$ ./Miniconda3-latest-MacOSX-x86_64.sh
```

Yes를 입력하여 라이선스에 동의하고, Enter키를 치면 기본 경로에 설치된다. 그리고, 주피터 노트북을 설치한다.  

```bash
$ pip install jupyter 
혹은
$ pip3 install jupyter
```

책 0장에 있는 명령을 입력하여 이 책의 실습 패키지를 설치하여, 이 책에 맞는 환경을 설정한다. 그리고, 주피터 노트북을 실행한다.

```bash
$ git clone https://github.com/AstinCHOI/elegant-scipy
$ cd elegant-scipy

$ conda env create --name elegant-scipy -f environment.yml
$ source activate elegant-scipy

(elegant-scipy)$ jupyter notebook
```