# 설치

## 저장소 다운로드
컴퓨터에 이 저장소를 다운로드하고 주피터 노트북을 실행하려면 먼저 git이 필요합니다. 이미 설치되어 있을 수 있습니다. 터미널을 열고 `git` 명령을 타이핑하여 확인해 보세요. 만약 git이 없다면 [git-scm.com](https://git-scm.com/)에서 다운로드할 수 있습니다.

그다음 이 저장소를 클론하기 위해 터미널을 열고 다음 명령을 타이핑하세요(맨 앞의 `$` 기호는 타이핑하지 마세요. 이 기호는 파이썬 코드가 아니라 터미널 프롬프트로 관례상 표시합니다):

    $ cd $HOME  # 또는 각자 원하는 다른 개발 디렉토리
    $ git clone https://github.com/rickiepark/handson-ml3.git
    $ cd handson-ml3

git을 설치하고 싶지 않다면 [master.zip](https://github.com/rickiepark/handson-ml3/archive/main.zip) 파일을 다운로드하여 압축을 풀고 디렉토리 이름을 `handson-ml2`로 바꾸어 주세요. 그다음 원하는 개발 디렉토리로 옮깁니다.

## 아나콘다 설치
다음으로 파이썬 3과 여러 가지 파이썬 라이브러리가 필요합니다. 가장 쉬운 설치 방법은 [아나콘다를 다운로드하고 설치](https://www.anaconda.com/distribution/)하는 것입니다. 아나콘다는 과학 컴퓨팅을 위한 훌륭한 파이썬 배포판으로 여러 플랫폼에서 사용할 수 있습니다. 넘파이, 판다스, 맷플롯립, 사이킷런 등과 같은 많은 과학 라이브러리를 포함하고 있기 때문에 용량이 큽니다. 작은 용량의 아나콘다 배포판가 필요하다면 `conda` 패키지 도구를 실행하기 위한 최소 기능을 담고 있는 [미니콘다를 설치](https://docs.conda.io/en/latest/miniconda.html)하세요. 꼭 최신 버전의 아나콘다(또는 미니콘다)를 설치해야 합니다.

MacOS와 리눅스에 설치할 때 `conda init` 명령을 실행하여 아나콘다를 초기화할지 묻습니다. 이를 수락하면 터미널을 열 때마다 `conda` 명령을 사용하도록 쉘 스크립트를 업데이트합니다. 설치가 끝나면 터미널을 닫고 새로운 터미널을 열어 잘 적용되었는지 확인해 보세요.

윈도우에서 설치할 때 `PATH` 환경 변수를 업데이트할지 묻습니다. 이것은 다른 소프트웨어와 충돌할 수 있기 때문에 권장되지 않습니다. 대신 설치가 끝난 후에 아나콘다를 사용하려면 시작 메뉴를 열고 Anaconda Shell을 실행하세요.

아나콘다(또는 미니콘다)가 설치되면 다음 명령을 실행하여 `conda` 패키지 도구를 최신 버전으로 업데이트합니다:

    $ conda update -n base -c defaults conda

> **노트**: 어떤 이유로 아나콘다를 좋아하지 않는다면 수동으로 파이썬 3을 설치하고 pip를 사용해 필요한 라이브러리를 설치할 수 있습니다(구체적인 내용에 대해 잘 알지 못한다면 권장하는 방법이 아닙니다). 일부 라이브러리는 아직 파이썬 3.8이나 3.9를 지원하지 않기 때문에 파이썬 3.7을 권장합니다.


## GPU 드라이버와 라이브러리 설치
텐서플로 호환 GPU 카드(Compute Capability ≥ 3.5인 NVidia 카드)를 가지고 있고 텐서플로에서 사용하려면 [nvidia.com](https://www.nvidia.com/Download/index.aspx?lang=en-us)에서 해당 카드에 맞는 최신 드라이버를 다운로드하고 설치해야 합니다. 또한 NVidia CUDA와 cuDNN 라이브리가 필요합니다. 다행히 아나콘다에서 tensorflow-gpu 패키지를 설치할 때 자동으로 설치됩니다. 하지만 아나콘다를 사용하지 않으면 수동으로 설치해야 합니다. 설치에 어려움이 있다면 텐서플로 [GPU 설치 가이드](https://tensorflow.org/install/gpu)를 참고하세요.

## `homl3` 환경 만들기
그다음 `handson-ml3` 디렉토리 안에서 다음 명령을 실행하세요. 이 명령은 노트북을 실행하기 위해 필요한 모든 라이브러리를 포함한 새로운 `conda` 환경을 만듭니다(기본적으로 이 환경의 이름은 `homl3`이지만 `-n` 옵션으로 바꿀 수 있습니다):

    $ conda env create -f environment.yml

그다음 새로운 환경을 활성화합니다:

    $ conda activate homl3


## 주피터 시작
거의 다 되었습니다! `homl3` 콘다 환경을 주피터에 등록해야 합니다. 이 프로젝트의 노트북은 기본적으로 `python3` 이름의 환경을 사용합니다. 따라서 이 환경을 `python3`로 등록하는 것이 좋습니다(다른 이름으로 등록하고 싶다면 노트북을 열 때마다 주피터에서 "Kernel > Change kernel..." 메뉴를 선택해야 합니다):

    $ python3 -m ipykernel install --user --name=python3

이제 끝났습니다! 다음 명령으로 주피터를 실행할 수 있습니다:

    $ jupyter notebook

브라우저가 열리고 주피터가 현재 디렉토리의 목록을 보여줍니다. 브라우저가 자동으로 열리지 않는다면 [localhost:8888](http://localhost:8888/tree)에 접속해 보세요. `index.ipynb`를 클릭하여 시작합니다.

축하합니다! 머신러닝을 배우고 실습할 준비를 마쳤습니다!

주피터 작업을 마치려면 주피터를 실행한 터미널 윈도에서 Ctrl-C를 타이핑하여 종료할 수 있습니다. 이 프로젝트를 사용할 때마다 터미널을 열고 다음을 실행합니다:

    $ cd $HOME # 또는 설치한 다른 디렉토리
    $ cd handson-ml3
    $ conda activate homl3
    $ jupyter notebook

## 프로젝트와 라이브러리 업데이트하기
이슈를 해결하고 새로운 라이브러리를 지원하기 위해 정기적으로 노트북을 업데이트합니다. 따라서 업데이트된 프로젝트를 받는 것이 좋습니다.

이렇게 하려면 터미널을 열고 다음을 실행하세요:

    $ cd $HOME # 또는 설치한 다른 디렉토리
    $ cd handson-ml3 # 프로젝트 디렉토리로 이동
    $ git pull

에러가 난다면 아마도 노트북이 수정되었기 때문입니다. 이런 경우에 `git pull`을 실행하기 전에 먼저 수정한 내용을 커밋해야 합니다. 이 작업은 별도의 브랜치에서 진행하는 것이 좋습니다. 그렇지 않으면 충돌이 발생할 것입니다:

    $ git checkout -b my_branch # 원하는 브랜치 이름
    $ git add -u
    $ git commit -m "수정 내용"
    $ git checkout master
    $ git pull

그다음 라이브러리를 업데이트해 보죠. 먼저 `conda` 자체를 업데이트합니다:

    $ conda update -c defaults -n base conda

그다음 `homl3` 환경을 삭제합니다:

    $ conda activate base
    $ conda env remove -n homl3

그리고 환경을 새로 만듭니다:

    $ conda env create -f environment.yml

마지막으로 환경을 다시 활성화 하고 주피터를 시작합니다:

    $ conda activate homl3
    $ jupyter notebook
