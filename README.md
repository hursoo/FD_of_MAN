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
* keywords : TF/TF-IDF 기준 시기별 키워드. 단어-단어 네트워크 매트릭스
* model : 시계열 토픽 모델링 model 파일
* plot : 토픽 內 단어변화 플롯 및 연도별 상위 20개 단어와 토픽-토픽 네트워크 매트릭스
* riss : RISS에서 다운로드 받은 서지정보 예시 파일

---

## 0. 서지정보 데이터 다운로드
#### [데이터 안내(필독)](https://github.com/ByungjunKim/DDMKL/blob/main/data/DATA.md)
#### [data 폴더](https://github.com/ByungjunKim/DDMKL/tree/main/data)

## 1. 데이터 수집 및 개괄  
~~Selenium 을 활용한 RISS 서지정보 자동 내려받기 (2024년 현재 작동 불가)~~  
~~00RissCrawling.ipynb (RISS 서지정보 자동수집, [코드 활용안내 튜토리얼](https://youtu.be/3A7EKg9XyMU))~~  
~~01RissParsing.ipynb (RISS에서 다운로드 받은 서지정보 엑셀파일 합치기)~~  
~~[크롬 드라이버 다운로드](https://chromedriver.chromium.org/downloads)~~  
#### Riss 사이트에서 서지정보 스크래핑 (2024년 4월 업데이트 완료)
#### 01RissScraping.ipynb

## 2. 데이터 전처리 & 형태소 분석
#### 02Preprocess.ipynb ([구글 Colab 링크](https://colab.research.google.com/drive/1x8DIFh5LMjIC7E3Qezy9emWp_-EpMqEO?usp=sharing))
* Pandas를 활용한 데이터 전처리
* 사용자 사전 구축
* Khaiii 형태소 분석기
* 불용어 처리

## 3. 기술 통계량 & 키워드 추출
#### 03Keywords.ipynb ([구글 Colab 링크](https://colab.research.google.com/drive/1bGebwCdiwY1g-0aMEUqQbZ1QMptSkDc7?usp=sharing))
* 기술 통계량
* TF, TF-IDF 기준 키워드 추출
* 시기별 키워드 추출

## 4. 시계열 토픽 모델링
#### 04Model.ipynb ([구글 Colab 링크](https://colab.research.google.com/drive/15A9sNGjogSm23yYmT_KVkwWd6YHxfvur?usp=sharing))
[Dynamic Topic Model 바이너리 Github](https://github.com/magsilva/dtm)  
[Dynamic Topic Model 바이너리 다운로드(윈도우64)](https://github.com/magsilva/dtm/raw/master/bin/dtm-win64.exe)  
[Dynamic Topic Model 바이너리 다운로드(리눅스64)](https://github.com/magsilva/dtm/raw/master/bin/dtm-linux64)  
* 모델링
* 시간에 따른 토픽별 주요단어 변화
* 모델링 결과 시각화
* 토픽-토픽 네트워크
