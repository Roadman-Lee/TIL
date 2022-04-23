# 바운드와 블로킹

## 바운드란?

: 특정한 자원에 의해서 제한됨.

여러가지 바운드가 있지만 CPU-바운드와 I/O-바운드에 대해서 알아보자

### CPU 바운드

1. 프로그램이 실행될 때 실행 속도가 CPU 속도에 의해 제한됨을 의미한다.
2. 복잡한 수학 수식을 계산하는 경우에 컴퓨터의 실행속도가 느려진다.
예) 무한 루프에 가까운 for문, 머신러닝 모델

### I/O 바운드

1. I는 Input을 O는 Output을 의미한다
2. 프로그램이 실행될 때 실행 속도가 I/O에 의해 제한됨을 의미한다.
3. 사용자가 키보드로 숫자를 입력하는 경우 뿐만 아니라, 컴퓨터와 컴퓨터끼리 통신을 할 때에도 I/O 바운드가 발생한다.   
예) 어떤 프로그램에서 특정 웹에 요청을 하여 응답을 기다리는 코드가 있다고 하면 요청을 하는 것이 I가 응답을 하는 것이 O가 되는 I/O 바운드

### 블로킹이란?

: 바운드에 의해 코드가 멈추게 되는 현상이 일어나는 것