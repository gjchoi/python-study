# python-study
파이썬 스크랩핑 스터디


## Indtoducing Python (처음 시작하는 파이썬)

## Web Scraping with Python (파이썬으로 웹 크롤러 만들기)


## MAC OS에 Python 환경설치

### Python3 (3.5)설치
기본적으로 mac에 2.7버젼이 깔려있다. (homebrew를 통해서 설치함)

~~~
brew install python3
~~~


테스트

scrapertest.py
~~~
from urllib.request import urlopen
html = urlopen("http://pythonscraping.com/pages/page1.html")
print(html.read());
~~~

를 만든뒤 실행해본다.

~~~
python3 ./scrapertest.py
~~~


python명령어가 python3.5버젼을 바라보게 하고 싶다면 (기본적으로 2.7) .bashrc(or .bash_profile에 phython 명령어 alias를 준다.

.bash_profile
~~~
....
alias python='/usr/local/bin/python3'
~~~


### pip설치

python의 라이브러리를 다운로드 받을 수 있게 해주는 모듈

~~~
sudo easy_install pip
~~~


#### pip를 통해서 Beautifulsoup4 모듈다운

크롤링을 편하게 해주는 
라이브러리 다운


~~~
sudo pip install beautifulsoup4
~~~

이렇게 하면 2.7로 설치된다.

~~~
sudo pip3 install beautifulsoup4
~~~

3.x버젼용 모듈을 받기 위해서는 위와 같이 실행


### beautifulsoup 테스트

beautifulsoup_test.py 를 만들어 수행해본다

~~~
from urllib.request import urlopen
from bs4 import BeautifulSoup
html = urlopen("http://www.pythonscraping.com/pages/page1.html")
bsObj = BeautifulSoup(html.read(), "html.parser")
print(bsObj.h1)
~~~

~~~
python3 beatifulsoup_test.py
~~~
