# 2018 Winter-Hellcamp 



안녕하세요 ~



이번 헬캠에서는 실제 윈도우 상용 프로그램중 하나의 1-day에 대한 익스플로잇을 작성하여 계산기를 띄우는 것을 목표로 하고자 합니다. 그를 위해서 선행하여야 할 지식들이 있고 이를 과제로 부여합니다!



### 선행 과제

1. docs 

   ```
   https://pwnwiz.tistory.com/52?category=708324
   ```

   해당 주소의 buffer overflow foundation pub.pdf와 All About RTL.pdf 공부하기



2. 환경 설정

   윈도우 프로그램이다 보니 윈도우에 관한 환경을 구축해오셔야 됩니다.

   - 윈도우 7 or 8 ( 저는 8 사용할 겁니다. )
   - github 아이디 ( 제가 초대할 수 있는 계정 정보를 이메일로 보내주시면 됩니다. )
   - windbg : 윈도우용 디버거 ( 리눅스는 pwndbg가 짱짱 )
   - 010editor : 파일 수정할 때 편리한 편집기
   - mona : windbg의 extension ( 필수 !! )



3. 보호기법 공부

   ```
   https://bpsecblog.wordpress.com/memory_protect_linux/
   ```

   익스플로잇 작성을 할 때 보호기법을 알아야 제대로 이해가 가능



4. 구구단 만들기

   저번 기수에서도 했지만 제출률이 안좋았습니다..

   구구단을 만들기를 통하여 assembly 코드를 보는 능력과 작성하는 능력, 쉘 코드를 만드는 능력을 향상 시킬 수 있습니다. 원래는 쉘 코드를 만들어보는게 제일 좋으나 익스플로잇도 해야하니 해당 부분은 개인 자습으로!

   구구단 코드 구현 조건:

    - 메뉴 :
       - 1단~19단 출력
       - 원하는 단 입력받은 뒤 출력
       - 프로그램 종료 (  exit 0으로 정상 종료되게 끔 )
   - 조건 : 
     - 1단 ~19단 구현시 mul 또는 add를 활용하여 하나씩 직접 더하거나 곱해지도록 구현한다.
     - 한 단을 출력할 경우 13단일 경우에 13 x 1 = 13, 13 x 9 = ** 까지 구현하면 된다.
     - 코드는 Ubuntu 16.04 LTS 기준으로 돌아가도록 해야한다. ( 기본 GCC 사용 )
     - 사용자로부터 입력 받는 부분에서 write 또는 scanf 둘다 가능 ( C 라이브러리 가져다 써도 됨 )



5. CTF 문제 풀기

   깃허브에 회원 가입을 한 뒤, 아래의 2문제를 푸시고 라이트업과 익스플로잇 코드를 작성하신 뒤 깃 레포를 만드시면 됩니다.

   - ropasaurusrex
     - 32bit Linux Stack Overflow

   - SSG Academy 
     - 64bit Linux Stack Overflow 
     - nc 203.250.148.108 40005 -> flag 따기

   동아리 워게임 사이트가 내부 수리 중이라 깃허브를 통해서 바이너리를 배포합니다.

   같이 푸셔도 좋으나 꼭꼭 다 이해를 하고 라이트업과 익스플로잇을 작성하셔야 됩니다!



6. Windows Tutorial 

```
https://www.corelan.be/index.php/2009/07/19/exploit-writing-tutorial-part-1-stack-based-overflows/

https://www.corelan.be/index.php/2009/07/23/writing-buffer-overflow-exploits-a-quick-and-basic-tutorial-part-2/
```

윈도우 실습을 위한 기초 지식을 위해 필요 



### 주제 설명



이번 주제는 windows의 한 프로그램에서 발생한 크래시를 가지고 root cause를 분석하고 수정하여 쉘 코드로 공격을 하는 과정을 같이 해볼 겁니다. 저도 윈도우는 별로 안해봐서 쉬운 주제를 가지고 왔으니 재미있게 해봅시다.



### 제출 관련

- e-mail : pwnwiz@gmail.com
- due date : 2019.1.14.
