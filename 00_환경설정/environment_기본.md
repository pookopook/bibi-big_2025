# 파이썬 설치하기

## 1. 아나콘다(Anaconda) 또는 미니콘다(Miniconda) 설치

아나콘다 또는 미니콘다를 설치해야 합니다. 아래 링크에서 다운로드할 수 있습니다.

- [아나콘다 또는 미니콘다 다운로드 링크크](https://www.anaconda.com/download/success)

설치 후, 터미널(또는 명령 프롬프트)에서 아래 명령어를 입력하여 정상적으로 설치되었는지 확인합니다.

```sh
conda --version
```
## 2. environment.yml 다운로드
GitHub 저장소에서 environment.yml 파일을 다운로드합니다.
## 3. environment.yml을 사용한 Conda 환경 추가
다운로드한 environment.yml 파일을 사용하여 새로운 Conda 환경을 생성합니다.

Anaconda Prompt를 실행합니다.

```sh
# 기본 경로에 환경 설치 (#으로 시작하는 구문은 주석입니다.)
conda env create -f environment.yml
```


환경이 정상적으로 생성되었는지 확인하려면 다음 명령어를 실행하세요.
``` sh
conda env list
```

새로 생성된 환경이 보이면 다음 명령어로 활성화할 수 있습니다.
``` sh
# conda activate {환경이름}
conda activate bibiml
```

# 주피터 기본 폴더 설정하기

먼저 파이썬 환경의 기본 폴더를 확인합니다.
주피터 노트북에 다음과 같이 입력하여 경로를 확인할 수 있습니다.
``` python
# 주피터의 현재 기본 폴더 확인하기
import os
os.getcwd()
```

콘솔(Anaconda Prompt)에서 다음 명령어를 실행합니다.
``` sh
jupyter lab --generate-config
# 주피터노트북을 사용하는 경우
## jupyter notebook --generate-config 
```
위 명령어를 실행하면, config 파일의 경로가 출력됩니다. 파일을 찾아 메모장으로 엽니다.

config 파일에 다음 구문을 추가합니다.
먼저 폴더를 먼저 만들고, 그 경로를 복사합니다. 
``` yml
# c.ServerApp.root_dir = ''  <-- 이 부분을 찾아서 주석을 해제하고
c.ServerApp.root_dir = r'D:\jupyter\bibiml' #예시 경로입니다.
```

주피터 랩을 재시작하고 기본 경로를 확인해보세요.