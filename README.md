# 득쌤의 온라인저지 프론트 엔드

## npdejs 6.11 설치

`$ cd ~` -- 계정의 상위 폴더로 이동

`$ sudo apt-get update`

`$ sudo apt install nodejs` -- nodejs 설치

`$ sudo apt install npm`

`$ sudo npm clean cache -f`

`$ sudo npm install -g n`

`$ sudo n 6.11`

`$ sudo node -v` -- 버전확인 v6.11.5를 확인

여기까지.. nodejs 6.11 설치 완료

## FrontEnd 서버 구동

`$ mkdir OnlineJudge && cd OnlineJudge` -- OnlineJudge 폴더 생성 및 이동

`$ git clone https://github.com/dplus1016/OnlineJudgeFE` -- OnlineJudge 폴더에 FrontEnd 소스코드 다운로드

`$ cd OnlineJudgeFE` -- OnlineJudgeFE 폴더로 이동

`$ sudo npm install` 

`$ NODE_ENV=development sudo npm run build:dll`

`$ export TARGET=http://0.0.0.0/`

`$ npm run dev` -- FrontEnd 서버 구동(터미널을 꺼버리면 FrontEnd 서버도 멈춤)

`http://0.0.0.0:8080` 에 접속 -- 온라인저지 사이트가 한글화 되어 있는 것을 확인 할 수 있음

## 주피터 노트북 활용

이번 내용은 주피터 노트북을 활용하여 실시간으로 수정할 수 있도록 하는 것임

앞서 진행했던 터미널을 그대로 둔 상태(FrontEnd 서버 구동 중)에서...

터미널을 추가로 실행함 (shift 키를 누른 상태에서 터미널 클릭)

`$ pip install jupyter`

`$ sudo apt install jupyter-notebook`

이제 ip주소만 알면 되는데...ip주소를 확인하려면...

`$ sudo apt install net-tools` 

`$ ifconfig` -- ip주소 정보를 확인

출력 내용 중에서...ens로 구분되는 내용의 ip주소(inet)를 확인

`$ jupyter-notebook --ip='000.000.000.000'` -- 위에서 확인한 주소를 입력하면 주피터 노트북에 접속이 됨

- 이때, 터미널 창에서 `http://000.000.000.000:8888/?token=2020dd78379a5d80419ec27afa3ad4eb8bd83877c6e6c0ed` 이런 형태의 코드가 링크되어 있는 것을 알 수 있음 / 이 링크를 클릭하거나 복사해서 사용해도 주피터 노트북에 접속이 가능함

- 주피터 노트북의 OnlineJudgeFE 폴더에 있는 파일들을 수정한 후에 저장하면 온라인저지 사이트에 즉시 반영됨

- 예) OnlineJudge - OnlineJudgeFE - src - pages - oj 폴더에서 App.vue 파일을 클릭하면 소스코드를 볼 수 있는데...
- `Copyright &copy; <a href="https://www.naver.com">반갑습니다~^^ </a> All right reserved.` 의 부분을...
- `Copyright &copy; <a href="https://www.naver.com">안득하</a> All right reserved.` 로 수정한 후에...
- `File - Save` 혹은 `Ctrl+s` 하면 저장되고 사이트에 반영이 됨

참고 : [유튜브 강좌] https://www.youtube.com/watch?v=i5z5YrGyMZY&list=PLRx0vPvlEmdCSBgU29ZEmxqTr4ge-MoN_&index=6

## 오픈소스 라이센스

[MIT](http://opensource.org/licenses/MIT)
