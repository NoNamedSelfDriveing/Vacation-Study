USART
=============
- USART란?
	- 범용 동기/비동기 송수신 방식을 말한다.

- USART의 특징
	- 송수신을 할 수 있는 전이중 통신 가능하다.
		- 전이중 방식  :  두 대의 단말기가 데이터를 송수신하기 위해 동시에 각각 독립된 회선을 사용하는 통식 방식이다.
	- 멀티 프로세서 통신 모드 동작이 가능하다.
	- 에러율이 적은  Baud Rate Generator 내장되어 있다.

- 통신 방법
	- 병렬 통신
		- 고속데이터 전송이 필요한 곳에서 이루어진다.
		- 여러 개의 라인에서 동시에 이루어진다.
		- 직렬 통신에 배해 전송 속도가 빠르다.
	- 직렬 통신
		- 한 라인에서 이루어진다.
		- 데이터의 전송 속도가 병렬 통신에 비해 느리다.	
		- 동기식과 비동기식이 있다.
			- 동기식
				- 기준 클럭에 동기를 맞추어 데이터를 순차적으로 전송
				- 높은 전송 효율을 필요로 한다.
				- 장거리 전송에 유리하다.


				- 대량의 데이터를 고속으로 전송할 때 사용한다.
				- 클럭을 이용하기 때문에 클럭선을 하나 추가해야 된다는 단점이 있다.
			- 비동기식
				- 동기 클럭 없이 데이터의 전송 속도를 정하여 전송 하는 방식
				- 약속된 Baud rate에 따라서 양쪽의 송/수신기가 데이터를 주고 받는다.
				- 선이 적은 장점이 있다.
				- 대부분의 통신은 비동기식 통신을 이용한다.

- 동기식과 비동기식의 차이점
	- 데이터를 송수신 할때 데이터를 기준 동기 클럭에 맞추어 보내 것과 클럭에 상관 없이 정한 속도로 보내는 것에 차이가 있다.

- Parity Bit란?
	- 정보의 전달 과정에서 오류가 생겼는지를 검사하기 위해 추가된 비트이다.
	- 전송하고자 하는 데이터 끝에 1비트를 더하여 전송하는 방법
	- 2가지 종류의 패리티 비트 홀수,짝수가 있다.

- 짝수 패리티 
	- 송신하고자 하는 데이터의 각 비트의 값 중에서 1의 개수가 짝수가 되게 패리티 비트를 정하는 것이다.
	- 안정적 통신을 위한 보호장치라 볼 수 있다.
		- Ex) 실제 전송하고자 하는 데이터에 1의 개수가 3개일땐 1이 붙게되고 1의 개수가 4개이면 0이 붙게된다.

-홀수 패리티
	- 송신하고자 하는 데이터의 각 비트의 값 중에서 1의 개수가 홀수가 되게 패리티 비트를 정하는 것이다.
		- Ex) 실제 전송하고자 하는 데이터에 1의 개수가 4개일 땐 1이 붙고 3개일땐 0이 붙는다.

	* 짝수 패리티라고 0으로 값 고정하거나 홀수 패리티라 값을 1로 고정하는 것이 아니다.

- 패리티 비트 추가해 송수신 하는 이유
	- 데이터를 송수신 할 때는 각 비트를 단위시간당 하나씩 보내게 되어있다한다. 이때 알 수 없는 요인에 이해 비트의 값이 틀어지게 되면 그것을 확인할 수 있다.
		- Ex) 0=>1 , 1 => 0
	- 패리티 비트 정하여 데이터 보내면 받는 쪽에서 수신된 데이터 전체 계산하여 패리티 비트 다시 계산하게 되어 데이터 오류 발생하게 되면 알 수 있다고 한다.
	- 오류 발생 여부만을 알 수 있고 오류를 수정할 수 없다는 단점이 있다.