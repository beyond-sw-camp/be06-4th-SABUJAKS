# 🐈 사부작즈 DevOps 프로젝트 🐿️
<br><br>



<div align=center>
	<h4>
    <!--이미지 넣기? 폴더예시:<img src="https://github.com/beyond-sw-camp/be06-1st-ketchop-mojal/blob/dev/assets/image/project_background.PNG" width="60%" /> -->
 		자동화된 프로세스를 통해 반복 작업을 최소화하고 <br> 개발 속도를 향상시키기 위한 데브옵스 환경 구성 프로젝트입니다. 블라블라
	</h4>
</div>
<br><br><br>



# 🧑‍🔧 팀원
<h4>🐹구은주</h4>
<h4>🐱박종성</h4> 
<h4>🐸서시현</h4> 
<h4>🐻서재은</h4> 
<h4>🦉장유정</h4>
<br><br><br><br>



# 🛠 기술 스택
<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=GitHub&logoColor=white" /></a>
<img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=Git&logoColor=white&color=ffa500"></a>
<img src="https://img.shields.io/badge/GitHub Actions-2088FF?style=flat&logo=GitHub Actions&logoColor=white&color=gray"></a>
&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://img.shields.io/badge/Jenkins-D24939?style=flat&logo=jenkins&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=black&color=blue"/></a>
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=Kubernetes&logoColor=blue&color=skyblue"/></a>
&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://img.shields.io/badge/vuejs-%2335495e.svg?style=flat&logo=vuedotjs&logoColor=%234FC08D"/></a>
<img src="https://img.shields.io/badge/SpringBoot-181717?style=flat&logo=SpringBoot&logoColor=6DB33F&color=white"></a>
<br><br><br><br><br>



# ⛳ CI/CD 프로젝트 목표
작성즁
<br><br><br><br><br>



# 🌳 운영 환경
### ⚙️ 서버 구성
Kubernetes Master server 1 <br>
Kubernetes Worker server 4 <br>
Jenkins server 1 <br>
쿠버네티스의 클러스터 노드 구성입니다. <br>
추가 예정
<br><br><br><br>



### ⚙️ 시스템 아키텍처
이미지 업로드 예정
<br>

**구성 요소 간의 연결**

- **젠킨스 <-> 깃허브**: 웹훅을 통해 젠킨스가 깃허브에서 변경 사항을 감지하고 파이프라인을 시작합니다.
- **젠킨스 <-> 도커**: 젠킨스는 도커를 사용하여 애플리케이션의 빌드를 자동화하고, 빌드된 이미지를 도커 허브에 저장합니다.
- **젠킨스 <-> 쿠버네티스**: 젠킨스는 쿠버네티스 클러스터와의 연결을 위해 SSH를 사용하여 디플로이먼트를 적용합니다.
- **쿠버네티스**: 클러스터 내부에서는 마스터 서버가 디플로이먼트를 관리하고, 워커 서버들이 실제로 애플리케이션을 호스팅합니다.
<br><br><br><br>



### 🎬 시나리오
1. **개발자의 코드 푸시**
    - 개발자가 새로운 코드를 깃허브에 푸시하면 이벤트가 트리거됩니다.
      
2. **젠킨스 CI/CD 파이프라인**
    - 젠킨스가 깃허브 푸시 이벤트를 감지하고 파이프라인이 시작됩니다.
    - 젠킨스 파이프라인이 다음 단계들을 처리합니다.
        1. **깃허브 클론**: 젠킨스가 깃허브로부터 최신 코드를 클론합니다.
        2. **프론트엔드 & 백엔드 빌드**: 클론된 코드를 기반으로 각각의 빌드 작업을 수행합니다. 이 과정에서 도커 이미지를 생성합니다.
        3. **도커 허브 푸시**: 빌드된 도커 이미지를 도커 허브에 푸시합니다.
           
3. **쿠버네티스 배포**
    - 젠킨스가 빌드 완료 후 SSH를 통해 쿠버네티스 마스터 서버에 접근하여 디플로이먼트를 만듭니다.
    - 디플로이먼트는 기존 버전을 유지하면서 새로운 버전을 배포합니다. 여기서 **블루-그린 배포** 방식을 사용하여, 새로운 버전이 문제없이 작동하는지 확인한 후 트래픽을 전환합니다.
<br><br><br><br>



### 📦 배포 방식
블루/그린 배포 선택 이유 <br>
추가 예정
<br><br><br><br><br>



# 💡 CI/CD 테스트 및 결과
무중단 배포 gif 업로드 예정
<!--예시 [시연영상](https://youtu.be/rzBV5B_kKbU)-->
<br><br><br><br><br>


