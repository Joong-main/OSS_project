
# 휠체어 인식을 통한 역무원 자동 호출 시스템

</br>

## 배경

엘레베이터가 미설치된 역에서 휠체어 이용객이 휠체어 리프트를 이용하기 위해선 역무원 호출을 해야함.

</br>

## 기존 휠체어 리프트 호출 방식의 문제점
<li>리프트 이용을 위해 역무원 호출시 7분 이상의 시간이 소요됨</li>
<li>중증 장애인의 경우 역무원 호출 버튼을 누르기 어려움</li>
<li>역무원 호출 버튼을 누르는 과정에서 안전사고 발생함</li>
<br/>

## 목표
<li>휠체어 리프트 이용객 편의 증진 (이용 대기 시간 7분 감축) 및 안전 확보 </li>

<br/>
<img src="https://github.com/Joong-main/OSS_project/blob/main/doc/img/%EC%84%9C%EB%B9%84%EC%8A%A4%20%EA%B0%9C%EC%84%A0.PNG"></img>


## 운용방식
<ol>1. 카메라애서 서버로 영상전송</ol>
<ol>2.서버에서 휠체어 탐지</ol>
<ol>3. 탐지 정보 웹페이지 업로드</ol>
<ol>4. 휠체어 리프트 담당 역무원 배치</ol>
<br/>
<br/>

### 웹 인터페이스 
<img src="https://github.com/Joong-main/OSS_project/blob/main/doc/img/%EB%AA%A8%EB%B0%94%EC%9D%BC%20%EC%9B%B9.PNG"> </img>
<li>웹기반 실시간 알림 서비스 지원</li>
</br>
</br>


### 서버
<img src="https://github.com/Joong-main/OSS_project/blob/main/doc/img/%EC%84%9C%EB%B2%84%20%ED%8C%90%EB%B3%84.PNG"></src>
<li> 지도학습으로 학습된 휠체어 인식 알고리즘을 통해 휠체어 탐지</li>

</br>
</br>

### 프로토 타입 제작 방안
<li> open cv와 웹캠을 통해 프레임별 데이터 생성하도록 코드 작성</li>
<li> 캐글 데이터셋 + 크롤링을 통해 확보한 휠체어 학습 데이터와 티처블머신을 통해 알고리즘 생성</li>
<li>프레임별 데이터를 티처블 머신으로 생성한 알고리즘에 넣어 휠체어를 실시간 판별하도록 함</li>
<li>휄체어 탐지시 웹페이지에 알림을 생성하도록 웹페이지를 제작</li>

### 사용예정 라이브러리 및 오픈소스
<ul>Numpy</ul>
