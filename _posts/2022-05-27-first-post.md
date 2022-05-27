---
title : "multi process"
date : 2022-05-27 17:31 +0900
category : study daily
---

# multi processing
여러개의 thread를 만들고 각각 fork해서 여러개의 process에서

ddmin을 진행하도록 만들어봤다.

**[github link](https://github.com/coolgogi/DeltaDebugging/blob/master/src/process/pcs_range.c)**

사용한 것은 mutex, semaphore, atomic instruction이다

위 3개 모두 race condition을 방지하기 위해 사용한다.

mutex는 최대 1개의 thread가 접근 가능하고 semaphore는 설정하기에 따라 여러 개의 thread가

접근할 수도 있다. atomic instruction도 mutex와 마찬가지로 최대 1개의 thread가 접근 가능하다.

semaphore를 활용해 producer-consumer pattern도 구현했는데, bounded buffer를 활용하여 queue의 크기를 제한했다.

main thread에서 할 일을 queue에 넣어두면 worker thread에서 이를 pop 하여 처리하고 다음 할 일을 기다리는 방식이다.

기존에는 thread별로 할 일을 다 지정하여 thread를 만들고 다 끝나면 다시 thread join을 통해 thread가 끝나길 기다렸다.

이렇게 하면 thread를 새로 만드는 작업이 시간이 많이 들어갈 것이라고 판단하여 thread를 한번 만들어놓고 전체 계산이 끝날때 까지

계속 사용할 수 있는 producer-consumer pattern, bounded buffer를 활용한 것인데, process 5개 부터 8개 까지 속도 저하가 일어났다.

이유는 아직 파악하지 못했다. 
