마크다운(Markdown)
====
## 기초
마크다운(Markdown)언어는 마크업 언어로 HTML을 사용하지 않고 웹 문서를 만드는 것을 도와준다. 2004년 존그루버에 의해서 만들어졌으며 쉽게 쓰고 읽을 수 있다.

## 장, 단점
### 장점
>1. 간결하다
>2. 별도의 도구 없이 작성이 가능하다.
>3. 다양한 형태로 변환이 가능하다.
>4. 텍스트로 저장되어 용량이 적고 버전관리시스템을 사용할 수 있다.

### 단점
>1. 표준이 없다.
>2. 모든 HTML을 대체하지 못한다.

## 사용법(문법)
### 1. 줄바꿈  
더블스페이스 후 엔터를 넣어 사용한다. 단, 더블스페이스 이상도 인식한다.
> 안녕하세요.  
반갑습니다

### 2. 문단나누기
엔터를 두 번 친다.
>안녕하세요.
>
>반갑습니다.
### 3. 제목(Headers)
  * 큰 제목  
    Header  
    \======  
    이 때 '='는 한 개 이상이나 명확한 구분을 위해 여러 개를 붙이는 것을 권장한다.
    >Header
    > ==
    
  * 작은 제목(부제목)   
    Header  
    \-------  
    이 때, '-'는 한 개 이상이다.

    >Header
    >------
    
  * 글머리: 1-6까지 지원  
    \# H1  
    \## H2  
    \### H3  
    \#### H4  
    \##### H5  
    \###### H6  

    이 때, #와 내용은 띄어쓰지 않아도 되나, 보기 편하게 띄어쓴다. 또한 알아보기 쉽게 해시를 뒷부분에 넣기도 한다. 이때 뒤에 들어가는 해시는 한 개 이상이면 된다.
    ># H1
    >## H2
    >### H3
    >#### H4
    >##### H5
    >###### H6

### 4. BlockQuote
이메일에서 사용하는 \>를 사용한다.  
\>안녕하세요.  
\>>안녕하세요.  
\>>>안녕하세요.
>안녕하세요.
>>안녕하세요.
>>>안녕하세요.

### 5. 목록  
  #### - 순서있는 목록(Ordered List)  
  숫자와 점을 사용하고, 번호가 잘못 입력되더라도 내림차순으로 자동적으로 정의된다.  

  1\. 첫 번째  
  2\. 두 번째  
  3\. 세 번째
1. 첫 번째
2. 두 번째
3. 세 번째

만일, 숫자와 점을 이용하였으나 문법을 무시하고 싶으면 백슬래시(\\)를 숫자와 점 사이에 사용한다.  
또한 안쪽으로 들어가는 indent를 사용하고 싶으면 세 칸 이상(네 칸을 보통 사용한다.) 들여쓰기가 있으면 된다.  \
(백슬래시를 보여주기 위해 스페이스 대신 사용하였다.)  
1\.  
\\\\\\\1\.  
\\\\\\\\\\\\\\\1\.
1.
    1.
        1.

  #### - 순서없는 목록(Unordered List)
  별표나 빼기 더하기 기호로 사용한다.  
  \* 1단계  
  \\\\\\\\* 2단계  
  \\\\\\\\\\\\\\\\* 3단계

* 1단계
    * 2단계
         * 3단계

### 6. 코드
4개의 공백 또는 하나의 탭으로 된 들여쓰기를 만나면 변환되어 들여쓰지 않은 행을 만날때까지 코드로 인식된다.  
이 때 단락이 엔터로 단락이 나뉘어야 된다.

    import random
    random.randint(1,6)
    
### 7. 수평선
아래 줄은 모드 수평선을 만든다. 페이지 나누기 용도로 많이 쓴다.  
\* * *  
\***  
\*****  
\- - -  
\-----  
* * *


### 8. 강조
1. Bold  
\*\*Strong\*\* or \_\_Strong\_\_  
**Strong**
2. Italic  
\*Italic\* or \_Italic\_  
_Italic_
3. 취소선  
\~\~취소\~\~  
~~취소~~
### 9. 다른 단락 넣기
블록 인용구와 목록 단락에는 다른 단락을 넣을 수 있다. 이 때, 들여쓰기 4칸 이상을 해서 나눈다.  

블록 인용구 단락에 순서있는 목록 넣기  
\> 1.
>1.

블록 인용구 단락에 코드 넣기  
\>\\\\\\\\\import random
>     import random
(왠지 모르겠지만, 이 코드는 pycharm에서 5칸 띄어야 들어간다...)  

순서가 있는 목록에 블록 인용구 넣기  
1\. 첫 번째  
\\\\\\\\> 블록인용구  
1. 첫 번째
    > 블록인용구

순서가 있는 목록에 코드 넣기  
1\. 첫 번째  
\n  
\\\\\\\\\\\\\\code
1. 첫 번째

       code
(왠지 모르겠지만, 이 코드는 pycharm에서 7칸 띄어야 제대로 작동한다...)  

### 10. 특수문자 표현하기
문자 앞에 백슬래시(\\)를 사용한다.


### 11. 링크
* 인라인 링크  
글을 누르면 바로 넘어가는 링크  
\[Git hub](www.github.com)  
[Git hub](www.github.com)

* 참조링크  
참조를 통해서 링크를 거는 방식  
[link keyword][id]  
[id]: http주소

* 자동연결
주소를 보여주면서 연결하도록 만든다.
\<http://www.github.com>  
<http://www.github.com>

### 12. 이미지
Alt text: 설명, 주소: 사진주소, 사진 이름: 사진위에 커서를 올려놓을 때 나오는 이름  
\!\[Alt text](주소, "사진 이름")

## 파이참에서 사용
파이참에서는 마지막에 더블스페이스가 들어간 것을 자동으로 지운다. 따라서 줄바꿈을 놔두기 위해서는 plug-in을 설치해야 된다. md파일을 만든 후에 파이참을 재부팅하면 자동으로 plug-in을 설치할지 물어본다. 또는 Setting-Editor-plugin에서 설치할 수도 있다. 자동으로 설치할경우 Markdown Navigator와 Markdown support가 설치되며 원하는 것을 사용하면 된다. Navigator는 무겁지만 여러 편의성이 있고, support는 가볍다.

## Reference
쓰리래빗츠: <https://www.3rabbitz.com/markdown_guide>  

Github Guides: <https://guides.github.com/features/mastering-markdown/>  

Github Help: <https://help.github.com/articles/basic-writing-and-formatting-syntax/#paragraphs-and-line-breaks>  

Moodle, 마크다운의 고급활용: <https://docs.moodle.org/archive/ko/%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4%EC%9D%98_%EA%B3%A0%EA%B8%89_%ED%99%9C%EC%9A%A9#.ED.8A.B9.EC.88.98_.EB.AC.B8.EC.9E.90_.ED.91.9C.ED.98.84.ED.95.98.EA.B8.B0>  

나무위키, 마크다운: <https://namu.wiki/w/%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4>  

마크다운 작성법: <https://gist.github.com/ihoneymon/652be052a0727ad59601>  