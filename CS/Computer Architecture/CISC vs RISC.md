## CISC vs RISC

* CISC (Complex Instruction Set Computing, intel)
	* 여러 동작을 한꺼번에 할 수 있는 여러 가지의 명령어들을 제공
	* 명령어들의 형식과 길이가 다양하고, 주소 지정 방식도 다양
	* 주로 마이크로프로그램 제어 방식의 프로세서로 구성
	
**CISC가 명령어가 많아지고 복잡해져서 성능 향상에 걸림돌이 된다!**

* RISC (Reduced Instruction Set Computing, ARM)
	* CISC보다 늦게 나옴
	* 고정된 길이의 최소 종류의 명령어 제공
	* 주소 지정 방식 최소화, Load/Store 방식의 메모리 접근
	* 한 클록 사이클에 하나의 명령을 실행할 수 있도록 설계
	* Performance <= Throughput 기준
	![[Pasted image 20240806095524.png]]
	하나의 프로그램이 실행하는데 몇 개의 명령어가 필요한가? -> CISC 유리
	하나의 명령어가 실행되는데 몇 싸이클이 필요한가? -> RISC 유리
		왜? CISC는 복잡한 명령어, 여러 연산 및 저장 명령어의 집합
		하지만 RISC는 하나의 명령어에 하나의 연산 혹은 저장만!
		따라서 RISC는 1 클록 사이클이고 CISC는 RISC보다 복잡하므로 그보다 더 많은 클록 사이클이 소요됨
	하나의 사이클에 몇 초가 걸리는가? => ex. 2.4Ghz 3.2Ghz 등등 숫자가 높을수록 성능이 높음