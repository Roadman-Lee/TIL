## 변수(Variable) **가변적인**

컴퓨터가 어떠한 일을 하기위해서는 모든 데이터가 보조기억장치(SSD,HDD,USB 등)에서 주기억 장치(RAM)로 읽혀져야만 중앙 처리장치(CPU)가 주기억 장치의 내용을 읽어서 데이터를 가공처리한다.

그런데 이 주기억장치는 Byte마다 번지가 지정되어 있다.

번지는 숫자이므로 프로그램을 작성하려면 “10번지의 값을 읽어서 20번지의 값과 더하여 30번지의 값에 저장하여라" 등의 명령어를 내리게 된다.

프로그래머가 모든 번지를 제어하기 힘들기 때문에, 번지에 별명을 붙인것이 **“변수”**이다.

메모리 관리는 OS가 맡아서 하므로 프로그래머가 메모리가 필요하면 변수를 선언하고 값을 할당하면 된다.

그러면 OS가 현재 사용하지 않는 메모리를 확보해서 그곳에 변수명을 할당한다.

### **메모리 관리원칙**

- 메모리 관리의 주체는 운영체제입니다.
- 운영체제는 메모리가 있는 한은 할당 요청을 거절하지 않습니다.
- 한 번 할당된 메모리 공간은 절대로 다른 목적을 위해 재할당되지 않습니다.
- 응용 프로그램이 할당된 메모리를 해제하면 운영체제는 이 공간을 빈 영역으로 인식하고 다른 목적을 위해 사용할 수 있도록 합니다.

결론적으로 변수는 문자나 **숫자 같은 값을 담는 컨테이너**이다.

변수는 항상 맨 마지막에 저장한 값만을 저장한다. 

다시말하면 변수는 **값을 저장하는 그릇**과 같다.

## ****상수(constant) *일정한***

상수는 항상 똑같은 값을 저장하고 있는 곳이라 할 수 있다.

프로그래머나 시스템에 의해 미리 정해져 있는 것으로, 복잡한 수자의 값을 인지하기 쉬운 문자로 변경하여 사용하고자 할 때 주로 사용한다.

실제로 파이썬에서 상수를 사용하지 않는다.

클레스를 사용하여 상수를 만들 수는 있다.

```python
import sys

class _constant2:
    def __setattr__(self, name, value):
        if name in self.__dict__:
            raise Exception('변수에 값을 할당할 수 없습니다.')
        self.__dict__[name] = value

    def __delattr__(self, name):
        if name in self.__dict__:
            raise Exception('변수를 삭제할 수 없습니다.')

sys.modules[__name__] = _constant2()
```

```python
import constant2

constant2.PI = 3.14
constant2.MAX = 1000
print(constant2.PI)
print(constant2.MAX)

constant2.PI = 3.141592
constant2.MAX = 2000
print(constant2.PI)
print(constant2.MAX)

### 실행 결과 ###
3.14
Traceback (most recent call last):
1000
  File "C:/PyThonProjects/Ex01/basic04/Ex08_constant2.py", line 8, in <module>
    constant2.PI = 3.141592
  File "C:\PyThonProjects\Ex01\basic04\constant2.py", line 4, in __setattr__
    raise Exception('변수에 값을 할당할 수 없습니다.')
Exception: 변수에 값을 할당할 수 없습니다.
```

## ****리터럴(literal) *정확한***

데이터 그 자체를 뜻한다. 

리터럴은 “값" 그 자체로, 고정된 값을 표현하는 것을 의미한다. 

리터럴은 변수 초기화에 종종 사용된다.

정리하자면 **상수는 변하지 않는 변수**를 의미하며(메모리 위치) 메모리 값을 변경할 수 없다.

**리터럴은 변수의 값이 변하지 않는 데이터**(메모리 위치안의 값)를 의미한다.