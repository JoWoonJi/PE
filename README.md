# PE 파일 복구

---

GitHub repository 

[https://github.com/JoWoonJi/PE](https://github.com/JoWoonJi/PE)

링크 [JoWoonJi/PE (github.com)](https://github.com/JoWoonJi/PE)

---

과제 정리

- [x]  인프런 윈도우 악성코드 분석 강의 듣기
- [x]  실습해보기
- [ ]  다른 문제도 풀어보기

---

# #1. 불필요하게 삽입된 헤더

- 1-1.  원본 메모장이 변조되어 실행이 되지 않는 메모장이 있다. 문제점을 찾아 수정하고 복구해보자. 1번 변조된 메모장이 실행되지 않음을 확인.

![1-1](https://github.com/JoWoonJi/PE/blob/main/img/1-1.not%20work.jpg)

---

- 1-2. PEview 프로그램으로 확인해보고 Hex Editor로 수정한다.  원본파일과 변조파일 크기를 비교해보면 딱 16바이트 차이가 난다. 16바이트는 딱 1줄만큼의 차이다. 불필요하게 삽입된 첫 줄을 삭제해준다.

![2-2](https://github.com/JoWoonJi/PE/blob/main/img/1-2.edit.jpg)

---

- 1-3. 수정 후 정상적으로 실행이 됨을 확인.

![2-3](https://github.com/JoWoonJi/PE/blob/main/img/1-3.solved%20working.jpg)

---

---

---

---

---

# #2. 곳곳에 값이 변조 된 경우

- 2-1. hxd로 compare 기능을 활용해 원본 파일과 변조 파일을 비교한다

![2-1](https://github.com/JoWoonJi/PE/blob/main/img/2-1.use%20hxd%20compare.jpg)

---

- 2-2. difference 기능을 활용하여 값이 다른 부분을 수정해준다.

![2-2](https://github.com/JoWoonJi/PE/blob/main/img/2-2.edit.jpg)

---

- 2-3. 해결하여 정상적으로 실행이 됨.

![2-3](https://github.com/JoWoonJi/PE/blob/main/img/2-3.working.jpg)

---

<aside>
💡 특정 위치의 값을 바꾸면 왜 실행이 안되는지, 변조 되었지만 프로그램은 실행이 잘 되는 것은 무슨 이유인지 심화 학습이 필요

</aside>
