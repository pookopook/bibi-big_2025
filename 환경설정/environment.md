# GitHub에 아나콘다 환경 설정하기

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
```sh
conda env create -f environment.yml
```

환경이 정상적으로 생성되었는지 확인하려면 다음 명령어를 실행하세요.
``` sh
conda env list
```

새로 생성된 환경이 보이면 다음 명령어로 활성화할 수 있습니다.
``` sh
conda activate 환경이름
```
