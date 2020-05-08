# Python 제외 정리

### 기본
* // 몫
* (**) 제곱


### 슬라이싱
* [2:5]하면 인덱스 2부터 5전까지만 출력된다. 

### 문자열 메소드
word = python
* word.startswith('Py') 결과 : False // 처음 시작이 Py로 시작하는가? 맞으면 True 틀리면 False
* word.endswith('s') 결과 : False
* '{0}에 사는 {1}입니다'.format("안양","대학생")
* lstrip() /rstrip() / strip() : 공백제거 strip() 함수를 사용하면 주어진 문자열에서 양쪽 끝에 있는 공백과 \n 기호를 삭제시켜 준다.
* strip는 양끝 공백 제거, lstrip는 왼쪽 공백 제거, rstrip는 오른쪽 공백 제거

### 리스트
sq = [1, 4, 9, 16, 25]
* sq[-3:] 결과 : 9, 16, 25
* sq[-2:] 하면 16, 25 나옴

### 리스트 메소드 - 일단 다적음
* append(a): 리스트 뒤쪽에 새로운 요소 추가
* extend(l): 기존 리스트에 l을 이어 붙임; + 연산자와 동일
* append, extend 의 차이 append는 리스트 그대로 삽입 [1,2,3 [4,5,6]] 이런식, extend는 [1,2,3,4,5,6] 리스트 자체를 삽입 안함 추가


<br>


* insert(idx, a): idx 위치에 a를 삽입
* remove(a): 리스트에서 a와 일치하는 첫번째 원소를 제거
* pop(): 리스트 맨 뒤쪽의 마지막 원소 제거
* pop(idx): idx 위치의 원소를 제거

<br>

* index(a): a와 일치하는 첫번째 원소의 인덱스
* index(?) 원하는 값의 인덱스를 출력함


<Br>


* sort(): (오름차순) 정렬 sort(reverse=True): 내림차순 정렬
* reverse(): 리스트 원소의 순서를 반대로


### 튜플과 리스트의 차이는 튜플은 변경이 불가능 리스트는 [] 튜플은 () 사용
* t = 123, 456, 'hello <- 튜플삽입
* x, y, z = t //언패킹
* x는 123 y는 456 z는'hello'로 분리

### 집합
* 집합은 같은 값 존재 불가
* a = set('abracabrl') 결과값 a = {a,b,r,c,l}
* -차집합, |합집합 , &교집합, ^ 대칭차집합 Xor

### dictionary
* {'key' : value}로 구성
* dic['guido'] = 4000 // dic 딕셔너리에 key-guido, value-40000을 추가
* list(dic) // 키 리스트 삽입 순서대로
* sorted(dic) // 키 리스트 (정렬된 순서)

### dictionary method
* keys(), values(), items() // 각각 key, 값, (키,값) 으로 이루어진 리스트

### 반복문
* for s in ['apple', 'banana', 'carrot'] // 3번 반복
* for s in 'threq qweq qweqwe' 글자 수만큼 반복
* for i range(2,5) : // 2에서 4까지 3번 반복
* for i range(0,10,2) : // 0에서 10까지 2씩 증가하면서 반복 0,2,4,6,8


### 내포
* squares = [x**2 for x in range(10)] 결과는 1,4,9,16 .......~ 81
* [(x, y) for x in [1,2,3] for y in [3,1,4] if x != y] // (x,y)를 생성하는데 리스트로 x와 y가 같지않은 경우만 튜플로 생성한다.
* {x: x**2 for x in (2, 4, 6)} // x:x의 제곱 식으로 2:4 4:16 6:36 으로 생성

### 함수
* def func1(x,y) : 이런식으로 작성

### 모듈과 패키지
* 최상위 수준으로 실행되는 모듈은 __name__ 변수가 '__main__'으로 지정됨
* C언어의 main 함수에 해당하는 내용을 다음과 같이 표현함
* 즉, __name__ == __main__은 인터프리터에서 직접 실행했을 경우에만 if문 내의 코드를 돌리라는 명령이 됩니다. 
* __name__은 interpreter가 실행 전에 만들어 둔 글로벌 변수입니다.


### 파일 입출력
* file = open('test.txt', 'w') // w는 쓰기모드
* file.write(), file.writelines() //write("?") 파일안에 저장함 file.close()반드시 해줘야함

<br>

* file = open('test.txt','r') //읽기모드
* str = file.read(), .readline(), .readlines() // 파일 읽음, 파일 한 줄 읽음, 파일 내용 줄바꿈 기준으로 리스트 반환

