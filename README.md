# The Formation and Diversity of Modern Academic Norms during the Japanese Colonial Period (FD_of_MAN)  
  *A Quantitative Analysis of the Formal Aspects of Articles in Jindanhakbo*   

## 소개
1934년에서 1941년까지 발행된 진단학보 1~14호 수록 글 중 59편 논설을 분석하여 
근대 학술 규범의 초기 양상을 살펴본 연구의 데이터 및 파이썬 코드, 이미지 파일입니다.
논문의 문제의식, 데이터 정보, 분석 절차 및 결론에 관한 자세한 내용은 아래 논문을 참고하십시오.  
논문이나 코드관련 문의는 아래 저자 소개에 있는 이메일로 연락주시거나 깃허브 issue 페이지를 통해 받겠습니다.  
#### [일제 식민지 시기 근대 학술 규범의 형성과 다양성 -『진단학보』 논설 형태에 대한 정량적 분석- (인문논총 82-5, 2025.5.31.)]( )
#### [논문 Wiki 페이지](...)

## 저자
* 허  수(서울대학교 역사학부 교수, crctaper@snu.ac.kr)

## 코드 활용
Jupyter lab 코드(ipynb)를 다운받아 로컬에서 활용하면 됩니다.

## 폴더 설명
* data : 

---

## 실행 환경 및 설정 가이드 (Execution Environment & Setup Guide)

이 프로젝트는 **Anaconda** 배포판을 사용하여 관리되는 파이썬 가상환경에서 실행되었습니다. 아래 명시된 환경 정보와 설정 방법을 따르면 안정적으로 코드를 재현할 수 있습니다.

### 1. 환경 요약 (Environment Summary)

* **운영체제 (OS):** Windows
* **Python 배포판 (Distribution):** Anaconda
* **Python 버전:** 3.11
* **가상환경 이름 (Environment Name):** `py-project`
* **주요 라이브러리 (Main Libraries):**
    * `numpy` (1.26.x)
    * `pandas`
    * `scikit-learn`
    * `matplotlib`
    * `seaborn`
    * `jupyter`

### 2. 설정 방법 (Setup Instructions)

아래 단계를 따라 프로젝트 실행에 필요한 가상환경을 설정합니다.

#### **필수 조건**

* [Anaconda](https://www.anaconda.com/download)가 컴퓨터에 설치되어 있어야 합니다.

#### **설정 단계**

1.  **Anaconda Prompt 실행**
    시작 메뉴에서 `Anaconda Prompt`를 찾아 실행합니다.

2.  **Conda 가상환경 생성**
    아래 명령어를 실행하여 프로젝트를 위한 `py-project`라는 이름의 가상환경을 생성합니다. 이 과정에서 Python 3.11이 설치됩니다.
    ```bash
    conda create -n py-project python=3.11
    ```
    실행 중 `Proceed ([y]/n)?` 라고 물으면 `y`를 입력하고 Enter를 누릅니다.

3.  **가상환경 활성화**
    아래 명령어를 실행하여 새로 만든 가상환경으로 들어갑니다.
    ```bash
    conda activate py-project
    ```
    이후의 모든 명령어는 이 가상환경 안에서 실행됩니다. (터미널 맨 앞에 `(py-project)`가 표시됩니다.)

4.  **필수 라이브러리 설치**
    아래 명령어를 실행하면, `conda`가 Python 3.11 환경에 호환되는 안정적인 버전의 라이브러리들을 자동으로 찾아 한 번에 설치해 줍니다.
    ```bash
    conda install numpy=1.26 pandas scikit-learn matplotlib seaborn jupyter
    ```

5.  **Jupyter Notebook 실행**
    설치가 완료되면, 현재 터미널에서 아래 명령어를 실행하여 Jupyter Notebook을 시작합니다.
    ```bash
    jupyter notebook
    ```
    웹 브라우저에서 Jupyter Notebook이 열리면, 이 저장소에 있는 `.ipynb` 파일을 열어 코드를 실행할 수 있습니다.

### 3. 참고: 패키지 목록 파일 (environment.yml)

- 이곳에는 `environment.yml` 파일이 포함되어 있습니다. 
- 이 파일을 사용하면 위 2, 4번 단계를 한 번에 실행할 수 있어 더욱 편리합니다.
