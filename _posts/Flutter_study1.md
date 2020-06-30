---
title: "2020-06-30 flutter study1"
date: 2020-07-01 01:20 +0900
categories: study
---

6월 30일 
목표
1. Flutter 관련 영상 전부시청 24개의 영상, 75분가량
2. Dart관련 영상 전부 시청 1개 영상, 41분 가량
3. icebreaking.txt를 이용해서 git 다루기


목표 1
24개 중 6개 영상 시청
일단 flutter 설치하고 개발 환경을 만드는데 시간이 오래걸렸습니다.. 조금 삽질을 많이 했네요.
그리고 zsh를 이쁘게 꾸미느라 시간을 썼습니다. 덕분에 zsh는 보기좋게 바꿨습니다.
학기 중에 항상 해야겠다고 생각만 했는데 방학들어서 후딱 해버렸습니다. 
oh-my-zsh랑 iterm2를 안쓰고 바꿔보려고 했는데 실패하고 사용했습니다.

fluttes는 Android와 iOS를 동시에 개발할 수 있는 프레임워크입니다. 
방학동안에 만들 어플리케이션에 사용할 프레임워크로 flutter를 사용하기로 결정했습니다.
그 이유는 여러가지가 있는데, 두 환경에서 모두 네이티브 성능을 낼 수 있다고 하고
또 다양한 위젯을 제공한다고 하여 선택했습니다.

Dart언어는 Java와 JavaScript를 섞어놓은 듯한 느낌이 들어서 크게 어려워보이진 않습니다.
조금만 사용하다보면 금방 익힐 수 있을 것 같습니다.

목표 2
Dart 관련 영상을 시청하는 것인데 이것은 전부다 시청했습니다.

우선 변수 타입을 따로 지정하지 않고 var로 사용하는 것이 별로 마음에 들지 않네요.
JavaScript에 있었던 게 기억이 납니다.
dynamic이라는 것도 있는데요, parameter로 아무거나 받을 수 있는거라고 하네요.

final은 한번 초기화되면 변경이 불가하다고 합니다.
const와의 차이점은 const는 정적 할당이고 final은 동적 할당이라고 합니다.

Option 을 지정한다고 했는데, parameter를 부분적으로 받을 수 있도록 해주는 기능입니다.
Java의 overloading과 유사합니다. @required로 꼭 받아야하는 parameter도 지정해줄 수 있습니다.

Dart에서 method는 1급 개체라고 합니다. parameter로 사용이 가능하다고 하네요.

비교문은 is, is!가 새롭게 있습니다.

type casting은 (from) as (to) 이렇게 합니다.

? 는 null을 처리하는데 사용한다고 합니다. 좀더 살펴봐야겠네요.

class에서 member를 private으로 만들고 싶으면 이름 앞에 _ 를 추가해주면 됩니다.

get name => " " (?)

다른 class를 참조하는 것은 세가지 방법이 있는데, extends, implements, with가 있습니다.
extends는 java에 있는 그대로 이고 implements는 (?),  with는 필요한 부분만 골라서 참조할 수 있습니다.

future는 아직 정확히 이해하진 못했습니다. 비동기 처리할때 편리하다고는 합니다.

stream은 그 부분만 다시 그리는 것이고 state는 전체를 다시 그린다고 합니다.

목표 3
팀원들과 icebreaking.txt을 이용하여 git 다루기는 어제 배웠던 기억을 되살려보며
어찌어찌 완성을 했습니다. 각자 branch를 파고 다시 master에 merge하는 방식으로 진행했습니다.

이걸 하면서 나중에 프로젝트를 진행할 때 pull request로 할지, 
아니면 다 같이 push, pull할 수 있도록 할지 고민했었는데요, 다 같이 push, pull하는 방향으로 결정했습니다.
master branch를 건드릴때만 조심한다면 충분히 다룰 수 있을 거라고 생각합니다.

