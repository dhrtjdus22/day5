# day5
# 파일 읽기 쓰기
## open(파일이름,파일열기모드,인코딩)
> 파일을 연다   
```
파일이름이 같은 파일이 없으면 파일을 새로 생성한다   

파일열기모드   

r | 읽기모드 | 파일을 읽기만 할 때 사용   
w | 쓰기모드 | 파일에 내용을 쓸 때 사용   
a | 추가모드 | 파일의 마지막에 새로운 내용을 추가 시킬 때 사용   
```
## 파일쓰기 
```
file = open('sample.txt','w',encoding='utf8') #파일 열기

file.write('안녕하세요 반갑습니다.') #파일 쓰기

file.close() #파일 닫기
```
## 파일읽기
```
file = open('sample.txt', 'r', encoding='utf8')

lines = file.readlines()

for line in lines:
    print(f'{len(line)}: {line} ', end="")

file.close()
```
## 파일 이어쓰기
```
file = open('sample.txt', 'a', encoding='utf8')

file.write("오... 파이썬 공부는 재밌어\n")
file.write("즐겁게 하세요!!!!\n")

file.close()
``` 
## 라인단위로 읽기
```
file = open('Untitled.ipynb', 'r', encoding='utf8')

while True:
    line = file.readline()
    if not line:
        break
    line = line.strip()
    print(line, end='')
file.close()
```
## with ... as 구문 사용하기
> file.close()를 쓸 필요가 없음
```
with open('sample1.txt', 'r', encoding='utf8') as file:
    lines = file.readlines()
    for line in lines:
        print(f'{line} ', end="")
```
-----------------------------------------------------------
## Endian

### Big Endian   
<-높은주소 -----낮은주소->

### Little Endian
<-낮은주소 -----높은주소-> 

-----------------------------------------------------------
# except
> 에러문구
```
try :

 

except ? :
   #에러가 나면 실행할코드
```
## raise
> 예외를 발생시킴
```raise Exception()```
```raise Exception('정수가 아닙니다')```

-----------------------------------------------------------
# 모듈 - 메인

## __name__
> 모듈은 모듈이름,메인은 '__main__' 이 나온다
```
if __name__ == '__main__' :

	#코드
```
> 메인일 경우에만 코드기 실행된다
