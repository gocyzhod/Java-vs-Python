변수 선언
--------

    python
    
없음
    
    Java
    
Boolean : false , true

char : 문자

String : 문자열

반복문 : for 문
------------

    python
    
for i in range(범위) :
    내용 ....
    
    Java
    
for ( int i = 0 ; i <= 범위 : i 늘어날 범위 ) { 
    내용....
}


조건문 : if 문
-------

    python 
        
if 조건문 :
    내용
    
    Java
    
if ( 조건문 ) {
    내용
}


num에 정수 입력받기
-----------

    python
    
import sys

input = sys.stdin.readline

num = int(input())

    Java ( buffereader 사용 // Scaaner 생략 )
    
import java.io.*;

....

......

    BufferedReader 명칭 = new BufferedReader(new InputStreamReader(System.in));
    
    int num = Integer.parseInt(br.readline());
    
    br.close();
    
    
tmp에 문자 입력받기
----------

    python
    
import sys

input = sys.stdin.readline

tmp = input().rstrip()

    java
    
import java.io.*;
....

......

    BufferedReader 명칭 = new BufferedReader(new InputStreamReader(System.in));
    
    String num = br.readline();
    
    br.close();
    
tmp에 문자열 입력받기
---------------

    python ( 문자와 동일 )
    
import sys

input = sys.stdin.readline

tmp = input().strip()

    java
    
import java.io.*;

....

......

    BufferedReader 명칭 = new BufferedReader(new InputStreamReader(System.in));
    
    StringTokenizer st = new StringTokenizer(br.readLine());

    // AB CDD EFFF GH 입력

    st.nextToken() // AB
    
    st.nextToken() // CDD
    
    st.nextToken() // EFFF
    
    st.nextToken() // GH

    // 아래와 같은 방법도 존재
    
    while(st.hasMoreTokens()) { 
    
        System.out.println(st.nextToken()); 
        
    }
    
자바 arraylist
---------

파이썬은 동적 리스트(배열) 이다. 단, 자바는 정적인데, 동적으로 바꾸어주는 역할을 하는 것이 arraylist 이다.

import java.util.ArrayList;     // 조건

ArrayList<Integer> integers1 = new ArrayList<Integer>(); // 타입 지정
    
ArrayList<Integer> integers2 = new ArrayList<>(); // 타입 생략 가능
    
ArrayList<Integer> integers3 = new ArrayList<>(10); // 초기 용량(Capacity) 설정
    
ArrayList<Integer> integers4 = new ArrayList<>(integers1); // 다른 Collection값으로 초기화
    
ArrayList<Integer> integers5 = new ArrayList<>(Arrays.asList(1, 2, 3, 4, 5)); // Arrays.asList()
    
보통 생성할 때는 new ArrayList<>()와 같이 타입을 생략해서 작성

    기능 1. add()
    
import java.util.ArrayList;

public class ArrayListTest {
    
    public static void main(String[] args) {
    
        ArrayList<String> colors = new ArrayList<>();
    
        // add() method
    
        colors.add("Black");
    
        colors.add("White");
    
        colors.add(0, "Green");
    
        colors.add("Red");

        // set() method
    
        colors.set(0, "Blue");

        System.out.println(colors);
    
    }
    
}
    
    기능 2. set()
    기존에 추가된 값을 변경
  
위의 예시에서 확인.
    
    기능 3. remove()
    추가했던 값을 삭제할 때 remove()
    
'''
import java.util.ArrayList;
    
import java.util.Arrays;

public class ArrayListTest {
    
   public static void main(String[] args) {
    
        ArrayList<String> colors = new ArrayList<>(Arrays.asList("Black", "White", "Green", "Red"));
    
        String removedColor = colors.remove(0);
    
        System.out.println("Removed color is " + removedColor);

        colors.remove("White");
    
        System.out.println(colors);

        colors.clear();
    
        System.out.println(colors);
    
    }
    
}
'''   
    
    기능 4. 값 존재 유무 확인
    contains()
