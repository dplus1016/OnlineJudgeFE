# 득쌤의 온라인저지 프론트 엔드

## 설치 방법

`$ cd ~` -- 계정의 상위 폴더로 이동

`$ sudo apt install git` -- git 

`$ sudo apt install nodejs:i386` -- nodejs 설치

`$ sudo apt install npm`

`$ sudo npm clean cache -f`

`$ sudo npm install -g n`

`$ sudo n 6.11`

`$ sudo node -v` -- 버전확인 v6.11.5를 확인

여기까지.. nodejs 6.11 설치 완료

`$ mkdir OnlineJudge` -- OnlineJudge 폴더 생성

`$ cd OnlineJudge` -- OnlineJudge 폴더로 이동

`$ git clone https://github.com/dplus1016/OnlineJudgeFE` -- OnlineJudge 폴더에 FrontEnd 소스코드 다운로드

`$ cd OnlineJudgeFE` -- OnlineJudgeFE 폴더로 이동

`$ sudo npm install` 

`$ NODE_ENV=development sudo npm run build:dll`

`$ export TARGET=http://0.0.0.0/`

`$ npm run dev`

`http://0.0.0.0:8080` 에 접속 -- 온라인저지 사이트가 한글화 되어 있는 것을 확인 할 수 있음

다음 내용은 주피터 노트북을 활용하여 실시간으로 수정할 수 있도록 하는 것임

`$ pip install jupyter`

`$ sudo apt install jupyter-notebook`

이제 ip주소만 알면 되는데...ip주소를 확인하려면...

`$ sudo apt install net-tools`

`$ ifconfig`

출력 내용 중에서...ens로 구분되는 내용의 ip주소(inet)를 확인

`$ jupyter-notebook --ip='000.000.000.000'`

위의 주소부분에 자신의 ip주소를 입력

주피터 노트북에 접속한 후에 OnlineJudge/OnlineJudgeFE 폴더에 있는 다양한 파일들을 확인하면서 수정하면,

온라인저지 사이트에 즉시 반영됨

## 오픈소스 라이센스

[MIT](http://opensource.org/licenses/MIT)
