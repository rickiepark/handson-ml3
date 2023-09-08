핸즈온 머신러닝 3판
=================================

이 프로젝트는 파이썬으로 머신 러닝의 기초를 배우는 것이 목표입니다. 여기에는 <[핸즈온 머신러닝 3판](https://bit.ly/homl3-home)>(한빛미디어, 2023)의 연습 문제에 대한 예제 코드와 솔루션이 포함되어 있습니다: ([교보문고](https://product.kyobobook.co.kr/detail/S000208981368), [Yes24](https://www.yes24.com/Product/Goods/122338517), [알라딘](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=324278819), [한빛미디어](https://www.hanbit.co.kr/media/books/book_view.html?p_code=B1539397165))

<a href="https://bit.ly/homl3-home"><img src="cover.png" title="book" width="500" border="1" /></a>

**참고**: 2판의 노트북은 [rickiepark/handson-ml2](https://github.com/rickiepark/handson-ml2)에 있습니다. 1판의 노트북은 [rickiepark/handson-ml](https://github.com/rickiepark/handson-ml)에 있습니다.

## 빠르게 시작하기

### 아무것도 설치하지 않고도 온라인에서 이 노트북을 실행하고 싶은가요?

* <a href="https://colab.research.google.com/github/rickiepark/handson-ml3/blob/main/" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

⚠ _코랩은 임시 환경을 제공하므로 일정 시간이 지나면 모든 작업이 삭제되므로 중요한 데이터는 반드시 다운로드하세요._

### 코드를 실행하지 않고 노트북을 빠르게 살펴보고 싶은가요?

* <a href="https://nbviewer.jupyter.org/github/rickiepark/handson-ml3/blob/main/index.ipynb"><img src="https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg" alt="Render nbviewer" /></a>

* [깃허브의 노트북 뷰어](https://github.com/rickiepark/handson-ml3/blob/main/index.ipynb)로도 볼 수 있지만 이상적이지는 않습니다. 페이지가 느리게 열리고 수학 방정식이 이따금 잘못 표시되거나 용량이 큰 노트북은 열리지 않는 경우가 많습니다.

### 이 프로젝트를 로컬 컴퓨터에 설치하고 싶은가요?

[아나콘다](https://www.anaconda.com/products/distribution)(또는 [미니콘다](https://docs.conda.io/en/latest/miniconda.html)), [깃](https://git-scm.com/downloads)을 설치하고, 텐서플로와 호환되는 GPU가 있다면 [GPU 드라이버](https://www.nvidia.com/Download/index.aspx)와 적절한 버전의 CUDA 및 cuDNN을 설치하세요(자세한 내용은 텐서플로우 설명서를 참조하세요).

그다음 터미널을 열고 다음 명령을 입력하여 이 저장소를 클론합니다(터미널 명령임을 표시하는 맨 앞의 `$` 기호는 입력하지 마세요):

    $ git clone https://github.com/rickiepark/handson-ml3.git
    $ cd handson-ml3

그다음 다음 명령을 실행합니다:

    $ conda env create -f environment.yml
    $ conda activate homl3
    $ python -m ipykernel install --user --name=python3

마지막으로 주피터를 실행합니다:

    $ jupyter notebook

더 자세한 내용은 [상세 설치 문서](INSTALL.md)를 참조하세요.

# 자주 묻는 질문

**어떤 파이썬 버전을 사용해야 하나요?**

Python 3.10을 권장합니다. 위의 설치 가이드를 따르면 이 버전이 설치됩니다. 3.7 이상 버전이면 모두 작동합니다.

**`load_housing_data()`를 호출하면 에러가 발생합니다**

HTTP 오류가 발생하면 노트북에서와 똑같은 코드를 실행하고 있는지 확인하세요(복사/붙여넣기로 다시 실행해 보세요). 문제가 지속되면 네트워크 구성을 확인하세요. SSL 오류인 경우, 다음 질문을 참조하세요.

**MacOSX에서 SSL 오류가 발생합니다**.

SSL 인증서를 설치해야 합니다([스택오버플로 질문](https://stackoverflow.com/questions/27835619/urllib-and-ssl-certificate-verify-failed-error) 참조하세요). 공식 웹사이트에서 파이썬을 다운로드한 경우, 터미널에서 `/Applications/Python\ 3.10/Install\ Certificates.command`를 실행합니다(`3.10`을 설치한 버전으로 변경). MacPorts를 사용하여 파이썬을 설치한 경우, 터미널에서 `sudo port install curl-ca-bundle`을 실행합니다.

**이 프로젝트를 로컬에 설치했습니다. 최신 버전으로 업데이트하려면 어떻게 해야 하나요?**

[INSTALL.md](INSTALL.md)를 참고하세요.

**아나콘다를 사용할 때 파이썬 라이브러리를 최신 버전으로 업데이트하려면 어떻게 해야 하나요?**

[INSTALL.md](INSTALL.md)를 참고하세요.

## 도움을 주신 분들

유용한 피드백을 제공하거나 이슈를 제기하거나 풀 리퀘스트를 보내는 등 이 프로젝트에 기여해 주신 모든 분들께 감사의 말씀을 드립니다. 특별히 [박해선](https://github.com/rickiepark)과 Ian Beauregard에게 감사드립니다. 전체 노트북을 리뷰했을 뿐만 아니라 일부 연습문제 해답에 대한 도움을 주고, 많은 PR을 보내주었습니다. 연습문제 해답에 도움을 준 깃허브 사용자 SuperYorio에게 감사합니다. 많은 오류 수정이 포함된 훌륭한 PR을 많이 보내준 Victor Khaustov에게 감사드립니다. 마지막으로 구글 클라우드 크레딧을 제공하여 이 작업을 지원해주신 구글 ML 개발자 프로그램 팀에게도 감사드립니다.
