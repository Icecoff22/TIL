## 운영체제
컴퓨터 시스템이 살아가기 위하여 반드시 필요한 소프트웨어

* 역할
	* 컴퓨터 시스템의 자원을 관리
		* 프로세서 시간, 메모리 공간, 입출력 장치, 파일 등
		* 위의 자원은 무조건 운영체제를 통해 접근해야함
	* 사용자에게 시스템 자원을 활용할 수 있는 기능 제공
		* 단일 사용자 시스템의 경우, 다소 간단
		* 다중 사용자 시스템의 경우, 다소 복잡
운영체제의 분류
* 운용 대상 시스템이 어떤 종류의 것인가?
	* 범용/내장형
* 여러 사용자들에 대해 서비스 제공할건가?
	* 단일 사용자/다중 사용자
	* 우리가 지금 마주하는 대부분 운영체제는 다중 사용자이다.
* 여러 개의 중앙처리장치로 이루어진 시스템을 지원할 것인가?
	* 단일 프로세서/다중 프로세서
	* 요즘은 다중 프로세서
* 어떤 방식으로 복수의 작업을 행할 것인가?
	* 시분할 방식(batch processing)/다중 프로그래밍(multiprogramming)
	* 시분할은 옛날 방식
	* 요즘은 다중 프로그래밍, 여러 개의 프로그램이 동시에 실행되는 것처럼 보이는 것
운영체제의 역할
* 컴퓨터 시스템의 자원 관리
	* 프로세스 관리, 메모리 관리, 파일 시스템 관리, 입출력 장치 관리
* 사용자에게 시스템 활용 도구 제공(운영체제로 보는 경우도, 아닌 경우도 있음)
	* 텍스트 에디터
	* 시스템 관리 도구
	* 소프트웨어 개발 도구(환경)
	* 웹 브라우저(?)


### 운영체제 커널
운영체제의 핵심(core) 부분에 위치
* 시스템 모든 측면에 대한 완전한 권한 보유
* 사용자 (및 프로세스) 간 충돌 또는 침해로부터 보호와 함께 효율적이면서 공정한 자원 공유(배분) 담당
시스템 자원에 대한 완전한 제어권을 구사하기 위해서 하드웨어의 지원이 필요
* User mode vs kernel mode, exception levels
커널 외의 부분 ("사용자"라고 부름)을 이루는 코드는 시스템 자원 접근을 위해서 커널의 서비스를 이용
* 대표적으로 시스템 콜

### 시스템 콜
운영체제 커널이 제공하는 서비스에 대한 응용 프로그램의 요청을 가능하게 하기 위한 프로그래밍 인터페이스
응용 프로그램은 보통 고급 API (라이브러리) 함수들을 통하여 시스템 호출에 접근
시스템 콜의 호출은 프로세서의 실행 문맥(context) 을 특권 모드(privileged mode)로 전환시킴