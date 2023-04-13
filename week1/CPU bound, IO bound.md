- 버스트: 어떤 현상이 짧은 시간안에 집중적으로 일어나는 일
- CPU버스트: 프로세스가 CPU에서 한번에 연속적으로 실행되는 시간
- I/O버스트: 프로세스가 IO작업을 요청하고 결과를 기다리는 시간

⇒ 프로세스는 CPU버스트와 I/O버스트의 연속

- CPU bound 프로세스: I/O버스트는 적고, CPU버스트 많은 프로세스
    
    ex)동영상 편집프로그램, 머신러닝 프로그램(연산 多)
    
- IO프로세스: I/O버스트가 많음
    
    ex)일반적인 백엔드 API 서버
    
- CPU bound 프로그램에서 적절한 스레드 수=CPU개수+1
    *그 이유: 스레드 수가 많으면, 컨텍스트 스위칭이 생겨서 CPU를 낭비하기 떄문에 코어개수만큼만 스레드 수가 있다면 컨텍스트 스위칭이 없기 때문이다.
    