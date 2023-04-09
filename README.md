# Django1
hello world

> Django 스터디
------

## Member
> 조현호 고우석 김재윤 이정현

## Datae
> 매주 월요일 오후 9시

## 챕터 7 - 자료구조
------
### 목차: 리스트,튜플,딕셔너리
------
## 리스트
*선언

 list=[]
숫자,문자형 상관없음 (자료형 신경 쓸 필요가 없음)


``` python
lst=[]
```

*추가 ,
리스트 맨 뒤에 추가
``` python
lst.append(value)
```


*추가 2,원하는 위치에 삽입	

``` python
lst.insert(index,value)
```

*제거(데이터 삭제)
``` python
del lst[index]
```

*제거 2(데이터 삭제 ~> 반환)


index를 넣는 경우도 있지만 잘 사용 x
``` python
lst.pop(index)
```


*제거 3(리스트에서 직접 값을 찾아서 삭제)
``` python
lst.remove(value)
```

*정렬 (c++ 정렬과 동일)(원본이 정렬됨)
``` python
lst.sort()
```

*정렬2(원본은 유지한 채 정렬된 새로운 리스트 만들고 싶을 때) 
``` python
new=sorted(lst)
```

*역순정렬 
``` python
lst.sort(reverse=True)
```

*슬라이싱(리스트 함수 중 제일 중요하다고 생각함)
(start<= <end,jump는 몇 칸씩 이동할지)

``` python
lst[start:end:jump]
```

(0<= <4)
``` python
lst[:4]
```

(1<= <=end)
``` python
lst[1:]
```

(리스트 제일 뒤에서 하나 출력도 가능)
``` python
lst[-1]
```

(역순으로도 필요한 만큼 출력도 가능)

3번 인덱스 부터 0번 인덱스까지 역순으로(3,2,1,0) 
``` python
lst[3::-1]
```
* [deep copy,shallow copy] (https://wikidocs.net/16038)

* 반복문 
``` python
for i in lst:
     print(i) #기본이 출력후 줄바꿈
```
* 최대,최소,합
``` python
max(lst)  
min(lst)
sum(lst)
```



------
## 튜플
* 선언
``` python
tup=()
```
* 리스트로 변환법
``` python
list(tup)
```

* 함수
``` python
tuple(lst).index(5)#튜플 안에 5 값을 찾아서 그 인덱스를 반환
tuple(lst).count(2)#lst안에 값이 몇 개 있는 지 출력
```
------
## 딕셔너리(key:values)
* 선언
``` python
student={'student num':'12345','major':'CS'}
```
``` python
student['major']#'CS' 출력
```
* 추가
 ``` python
student['성적']=4.0 # {'student num': '12345', 'major': 'CS', '성적': 4.0}
```
* 수정
``` python
student[value]=new value
```

* 삭제
``` python
del student[value]#키값을 찾아서 key:values 모두 삭제
```

* 함수 
``` python
student.get('student num')#key 를 넣으면 value'12345' 출력
```
``` python
a = {'name': 'pey', 'phone': '010-9999-1234', 'birth': '1118'}
a.keys()#출력 dict_keys(['name', 'phone', 'birth'])
```
``` python
a.values()#dict_values(['pey', '010-9999-1234', '1118'])

```

``` python
a.items()#dict_items([('name', 'pey'), ('phone', '010-9999-1234'), ('birth', '1118')])
```

``` python
 a.clear()# 딕셔너리 안에 있는 모든 값 삭제
```
## 보통 그대로 사용하기 보다는 list(a.함수()) 이런 방식으로 리스트로 바꿔서 사용

``` python
 for key,value in student.items():#key값과 value 모두 출력됨
       print(key,value)
for i in student:#key 값만 출력됨
    print(i)
```
