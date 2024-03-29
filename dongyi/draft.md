# 동이튜브 인터뷰
## 1. 커리어 요약
### 1.1. 한성대 야간대 졸업


### 1.2. (1,000) 만 원 계약직
졸업 후 처음으로 시작한 프로젝트 **OraQ** 는, 4 개월 + 일주일이라는 기간 동안, 천 만원을 받고 일하는, 일종의 단기 계약직이었다. 그리고 흔히들 말하기를, 일정 수준 미만의 대학교에서, 교수가 소개해주어 소개해주어 취업하게 되는 직장의 가장 질이 나쁘다고들 한다. 본인의 대학 졸업 후 첫 직장은 바로 그러한 곳이었다. 

> 심지어 저 천만원이라는 금액조차, 처음에는 1년 기준 (1,800) 만원을 준다길래, 자리를 박차고 나오니 올려준 금액이었다. 게다가 프로젝트 중간 중간에 사장님 왈, "우리 와이프가, 고작 일개 대졸자에게 월급을 그리 많이 주냐면서 성화야" 와 같은 불만 아닌 불만을 토로하셨다. 이래저래 회사가 돈이 잘 안 벌리니, 사장님이 늘 초조해하시고 불안해하시던 기억이 난다.

게다가 프로젝트의 난이도는 상상을 초월하는 수준으로, 여지껏 본인이 맡아 개발한 모든 개인/상용 프로젝트를 통틀어, 난이도 Top 3 안에 들만큼 높았다. 사장님은 이 OraQ 프로젝트를 5 년 전부터 꼭 해 보고 싶어하셨으나, 도저히 이를 완성시켜주는 개발자가 없었으며, 최근 1 년 동안에도 개발자를 고용해 OraQ 프로젝트의 개발을 맡겼으나, 결국에는 실패하였다고 하시더라. 

> PACS 지원/관리 시스템 및 DICOM 이미지 뷰어를 개발하는 프로젝트였다. 
> 
> 단, OraQ 는 클라우드로 개발해야 했으며, 무려 웹에서 GPU 프로그래밍을 이용한 고속 연산이 필요했다. 의료 이미지들은 한 장에 수백 MB ~ 수 GB 를 우습게 넘어가는데, 그러한 이미지를 실시간 이펙트를 줌에도 속도 저하나 사용성에 지정이 없어야했기 때문이다. 모두가 알만한 용어로 표현하자면, 초당 프레임이 최소 20 fps 를 넘어가야 한달까?
>
> 그나마 다행인 것은, 프로젝트의 규모나 관리 시스템 그 자체는 방대하지 않았다는 것 정도?

당시의 본인 또한 OraQ 의 개요 및 목적을 들으며, 본인 또한 프로젝트 개발에 실패할 지도 모른다고 생각하였다. 아니, 당시의 통상적인 웹 개발 스킬로는 무조건 실패할 거라고 생각하였다. 당시 웹에서 주로 쓰이던 JSP 니 PHP 니 하는 것들을 사용해서는, 도저히 구현이 불가능하다고 여겼기 때문이다. 이에 본인은 설마 프로젝트를 실패한다고, 갓 대학교를 졸업한 사회 초년생인 본인에게까지 책임을 묻고 소송을 걸고 그럴까? 라는 생각으로 모험을 한 번 해 본다.

전통적인 웹 개발 스택을 과감히 버리고, 클라우드 서버를 C++ 로 직접 만들었으며, 이에 사용될 프레임워크를 직접 만들어 사용하였다. 프론트 어플리케이션과의 네트워크 통신에 사용될 프로토콜도 최적화를 위하여 직접 설계하였으며, 프론트 어플리케이션은 Flex (Flash) 를 사용하여, 웹에서 커스텀 소켓 프로그래밍 및 GPU 프로그래밍 요건을 충족하였다. 그리고 이처럼 족보에도 없는 새로운 방식으로 시도하는 개발이기에, 아키텍처 설계에 매우 많은 공을 들였다. 프로젝트의 성패는 설계에 달렸다는 생각 아래, 철저한 아키텍처 설계를 위하여 골몰하였으며 수없이 검토하였다.

>  - 철저한 아키텍처 설계
>    - 족보에도 없는 새로운 방식으로의 개발
>    - 첫째도 설계 둘째도 설계 셋째도 설계
>    - 설계에 매우 공을 들이고, 수없이 검토함
>  - 의료영상 관련 라이브러리들이 모두 C++/DLL 로 만들어지던 시절
>    - 클라우드 서버 전체를 C++ 로 개발
>    - 자체 C++ 프레임워크를 제작
>    - 네트워크 최적화 및 웹과의 실시간 연동을 위한 커스텀 프로토콜 설계
>  - 프론트 어플리케이션은 Flex (Flash) 로 개발
>    - 당시에는 지금처럼 HTML/JavaScript 가 발전하기 이전 시대
>    - 커스텀 소켓 프로그래밍이 가능하여 C++ 서버와 연동할 수 있고
>    - GPU 프로그래밍을 이용한 고속 병렬 연산이 가능함

이렇게 철저한 아키텍처 설계와 원칙을 지켜나가는 완고함, 그리고 기존의 개발 스택을 과감히 버리고 새로운 방식으로의 개발을 시도한 끝에, 이 프로젝트를 제 기간 내에 완성하여 상용 솔루션으로의 출시까지 마칠 수 있었다. 그리고 설계 단계에서 만들었던 다양한 문서들을 정리하여 개발 가이드 문서로 엮었는데, 이 점이 영업을 함에 있어서도 상당한 도움이 되었다고 한다.

다만, 회사에서는 본인의 공을 인정하더라도, 그만큼의 파격적인 대우를 해 주지는 않았다. 정규직으로 계약하는데 그 연봉이 본인의 바램만큼 크게 인상되는 수준은 아녔던지라, 이 프로젝트의 완성 및 계약 기간의 만료를 끝으로 본인은 회사를 떠났다. 하지만, 회사를 떠나더라도 본인이 거두었던 성과의 빛이 바래지는 것은 아니었다. 이 프로젝트 덕에, 대졸 신입사원이던 본인은 그 어느 회사를 들어가더라도, 코어 아키텍처를 설계하거나 핵심 알고리즘을 연구/개발하는 역할을 맡을 수 있었다. 심지어 "천재 신입 개발자" 라는 듣기 민망한 표어도 붙게 되더라. 덕분에 본인이 원하는 수준의 보상을 해당 회사로부터 직접 받지는 못했지만, 그 가치를 알아봐주는 다른 회사들이 있어, 오늘에 이르게 되었다. 

때문에 지금도 가끔 생각한다. 이 프로젝트가 더할나위 없는 기회가 되었다고 말이다.

### 1.3. 스타트업, 4 년차 연봉 1 억
위 OraQ 같은 프로젝트를, 몇 개 더 성공시켰다. 그러니까 오퍼 금액이 점점 높아지더라.

그리고 언제부터인가 블록체인 사업들이 유행하였고, 특히 신규 코인 발행에 관련되어 개발자들의 몸값이 높아지기 시작하였다. 특히 기존의 코인을 단순히 fork 하기보다, 무언가 특별한 목적이나 로직이 담기는 특수 코인을 발행하고자 하는 업체들이 생겨났는데, 그런 업체들에게 본인의 경력이 매우 매력적이었나보다.

아무튼 이러한 특수 코인을 발행하려는 업체들로부터 오퍼가 좀 있었는데, 그 오퍼 덕에 4 년차 때에 연봉이 1 억을 넘어가게 되었다. 본인은 당시 저러한 특수 코인을 발행하는 업체에 이직한 것은 아니고, 원래 다니던 회사에 "저에게 이만큼 연봉을 주겠다는 회사들이 있어요" 라고 얘기해서 연봉이 올라가게 된 케이스이다.





## 2. 개발을 시작하기까지
### 2.1. 개발을 언제, 그리고 왜 시작했는가
본인은 11 살 무렵에 프로그래밍을 시작했다. 당시 IT 붐이 일자, 정부에서는 각 학교의 교사들에게 IT 를 배워온 후 이를 학생들에게 가르치라 하였고, 그 덕에 학교 교사이시던 어머니의 서재에는 각종 IT 및 프로그래밍 입문 서적들이 많았다. 본인은 그 책들을 몇 권 빼 읽다가, 그대로 프로그래머가 된 케이스이다.

### 2.2. 취업 전에는 어떤 개발을 하였는가
초등학생 때 처음 만들어 본 것은 홈페이지다. 페인트 샵을 이용하여 홈페이지의 외관을 디자인하고, HTML 편집기를 이용하여 홈페이지를 제작하였다. 이후 플래시나 Php 등을 익혀, 보다 퀄리티가 높은 홈페이지를 제작하고, 게시판이나 회원관리 시스템 등을 스스로 만들어보거나 하였다.

그리고 중, 고등학생 때는 특히 낚시성 프로그램을 많이 만들었다. 프론트를 그럴싸하게 디자인하여, 게임 머니를 복사해주는 듯한 프로그램이되 실제로는 입력한 비밀번호가 탈취된다던가, 프리 서버를 관리해주는 듯한 프로그램인데 실제로는 FTP 트로이목마가 개설되어 서버 캐릭터를 변조할 수 있다던가 하는 프로그램들이었다. 때문에 중-고등학생 때에도 어지간한 웹 프로그래밍이나, DB SQL 쿼리 등, 각종 스킬을 능수능란하게 구사할 수는 있었다. 하지만 무언가 완성도있고, 상용 프로그램들과 견줄 수 있는 수준의 프로그램은, 대학생 때부터 만들 수 있었다. 

특히 대학생 때에는 규모 있는 프로그램을 많이 만들었기에, 아키텍처 설계나 클린 코드 작성에 관심이 많아, 이 부분으로 많은 공부를 하였다. 그리고 한 번 완성한 프로그램을 일부러 제로 베이스에서 두 번, 세 번 다시 만들어보면서, 프로그램을 어떻게 설계하고 어떠한 방식으로 만들어나가는 게 더 효율적일지도 참 많이 고민했었다.




## 3. 구직기
### 3.1. 대학교를 졸업하고 구직했을 때
본인이 대학교를 졸업하던 시기는 지금처럼 코딩 테스트가 있다던가, 개발자들에게 깃허브 계정이나 포트폴리오 등을 요구하여 개발 역량을 평가한다던가 하던 시절이 아니다. 그저 다른 학과들처럼 학력과 학점, 그리고 자격증과 인적성 및 토익 등이 평가 기준이 되던 시절이다. 심지어 인사담당자들은 공공연하게 아래와 같은 발언을 하고 다니던 시절이다.

> 개발은 3~6 개월 배우면 누구나 하는 것이다. 
> 
> 따라서 개발을 잘 못해도, 적당히 똘똘한 사람을 뽑아, 교육 기관에 6 달 정도 넣어두면 된다.

때문에 신입이 이력서를 쓸 때도 구구절절한 자기 성장스토리나 기업에 지원한 사유, 뭐 이런 자질구레한 얘기를 적어야했지, 지금처럼 "나의 github 의 id 는 무엇이며, 어떠한 개발을 해 왔고, 내 프로젝트로는 무엇이 있다" 등을 개발력을 어필할 수 있는 여건이 안 되었다.

덕분에 본인이 대학교를 졸업할 당시, 다른 구직자들에 비해 그다지 유리할만한 요소같은게 없었다. 그리고 중견기업 이상으로는 본인의 학력이 썩 좋지 않아서인지, 삼x 정도를 제외하고는 이력서 통과 자체가 잘 안 됐었다. 문제는 그러한 대기업들 또한, 그 금액과 상승률은 본인의 기대치에 비해 너무 낮았고, 그나마 서류 통과가 되는 중소기업들은 천편일률적으로 신입 연봉이 (2,400) 만원 수준이었다.

### 3.2. 차별을 받거나 고생한 적?
본인이 대학교를 졸업하고 스타트업 시작으로 직장 생활을 시작한 이래, 이렇다할 차별을 당해본 적은 없다. 개발해야 할 프로젝트의 난이도가 높아 고생은 했을 지언정, 그 외의 요소로 고생할 일도 없었다. 다만 제법 최근까지, 개발자는 매우 천대받는 직업이었던 듯 싶다.

본인이 중-고등학교에 다니던 시절, 학년이 바뀌면 늘 의례적인 담임 선생님과의 진로 상담이 있었고, 늘 직업란에 "프로그래머" 를 적어내던 본인에 대하여, 거의 대부분의 담임 선생님들께서 아래와 같은 충고를 해주셨기 때문이다.

> 개발자는 결코 할만한 직업이 못 된단다. 
> 
> 세상에 개발자만큼이나 박봉에 야근이 많은 직업이 또 어딨니? 심지어 수명도 짧아서 40 살도 되기 전에 다 은퇴한단다. 그런데 그러한 직업을 가지기 위하여, 굳이 어려서부터 미리 공부해가며 준비할 필요가 있을까? 정 정 개발이 재미있고 좋으면, 차라리 나중에 취미로나 해 보는게 어떻니?

이는 본인이 대학생이던 시절에도 달라지지 않았던 듯 싶다. 대학교를 다니던 중 동창회가 있어 나가보니, 그곳에 나온 같은 학과 02 학번의 대 선배님께서 술자리에서 울분을 토하시더라.

> 개발자는 결코 할만한 직업이 못 된다. 꼭 전공을 살릴 필요는 없으며, 아직 대학생이니 늦지 않았다. 가급 다른 직업을 알아봐라. 내가 개발자로 10 년 지내봤는데, 진짜 이 직업만큼이나 x 같은게 없다. 
>
> 배워야 할것은 산더미같은데, 개발하는 사람의 처우는 x 같다. 프로그램을 직접 개발하는 사람보다, 아무것도 모르면서 입만 놀리고 지시만 내리는 관리직들 나부랭이가 훨씬 많이 받고, 야근이나 주말 특근같은 것도 없다. 그에 비해 우리는 뭐냐? 허구헌날 주말에도 출근하고 야근은 일상화됏는데, 월급은 더 적다.

심지어 교수님들조차, 그분들의 말씀을 통하여, 그 사고의 편린을 엿볼 수 있었다.

> 개발은 6 달 정도 교육받고 실습하면 누구나 다 잘 할 수 있다. 결코 프로그래밍 실력 자체가 전문성이 될 수 없으니, 여러분도 사회에서 잘 나가고 싶다면, 이외의 스킬들을 다양하게 익힐 수 있도록 해라. 특히 자신의 업무 분야에서 도메인 지식에 대한 전문성을 키워야 한다.

### 3.3. 첫 회사를 골랐던 이유는?




## 4. 웹 개발자로써
### 4.1. 웹 개발을 하고 있는 이유는?
#### 4.1.1. TypeScript 를 선택한 이유와 전망
### 4.2. 앞으로의 커리어 목표
### 4.3. 평소 자기 개발을 어떻게 하는가
### 4.4. 회사를 선택하는 기준
### 4.5. 본인의 오픈소스 프로젝트 자랑




## 5. 연봉 협상과 인상
### 5.1. 연봉이 상당히 급격하게 올랐는데
#### 5.1.1. 이게 가능했던 이유는 무엇인지
#### 5.1.2. 회사에서 본인의 존재감은
#### 5.1.3. 협상 방법은 어떠했는지
### 5.2. 회사를 선택하는 기준
### 5.3. 흔히들 직전연봉, 학벌, 기업의 규모, 연차등이 발목을 잡는다고는 하는데
#### 5.3.1. 이에 대해 어떻게 생각하는지
대부분의 경우에 맞는 말이 아닐까 싶다. 

#### 5.3.2. 이걸 부순 방법은 무엇이라 생각하시는지


### 5.4. 사람들이 연봉 협상에 대해 흔히들 하는 오해
#### 5.4.1.. 연봉이 높으면 이직에 발목이 잡혀서 안 좋다






## 6. 최근 개발자 붐
### 6.1. 전공/비전공은 중요한가
본인은 자신이 작성한 코드를 되짚어보며, 성찰하고 반성한 후 이를 분석하여 개선해낼 수 있을 때, 그 실력이 가장 극적으로 상승한다고 생각한다. 그리고 이러한 성찰 및 개선의 범위가 점점 더 커져 작은 프로그램 코드 단위가 아닌 전체 아키텍처 수준의 개선이 가능해질 때, 비로소 그 실력이 정점에 달한다고 생각한다.

따라서 본인은 전공자가 비전공자보다, 자유로이 공부하고 실습할 수 있는 시간이 최소 4 년이나 더 있었다는 점에서, 훨씬 유리한 위치에 있다고 본다. 누군가 시켜서가 아닌 자발적으로 시작한 개발, 간단한 프로그램이라도 스스로 탐구하고 연구하여 무언가를 완성해 본 경험, 그리고 그 속에서 겪게되는 다양한 시행착오 및 각종 실수들과 이를 성찰하고 교정해나가는 일련의 과정. 이러한 경험들은 결코 누가 가르쳐주거나, 회사의 업무 지시 하달 등을 통하여 채득할 수 있는 성질의 것이 아니기 때문이다.

물론 예외는 있어, 간혹 좋은 회사의 경우에는 구성원 개발자들에게 끊임없이 코드 리뷰 및 리팩토링의 시간을 주기도 한다. 상호 간의 코드를 들여다보며 서로 반성하고 성찰하며, 개선점을 도출하여 이를 회사 코드나 아키텍처에 반영함으로써 품질을 올리는 등, 구성원 개발자들에게 끊임없는 성장의 기회를 주는 그런 회사들 말이다.

그리고 비전공자들 중에서도 그 시작은 박봉에 낮은 처우로 시작했더라도, 퇴근 후 자신이 주간에 작성했던 코드를 되돌아보며 "이러했으면 좋겠다~ 저러했으면 좋겠다~" 와 같은 자기 성찰과 반성을 하고, 이를 다음날 개선하여 반영할 수 있는 사람이라면, 이야기가 좀 다르지 않을까?

### 6.2. 면접관으로서 이력서를 볼 때, 학력과 학벌 및 전공을 어떻게 보는지
본인 또한 학벌이 좋은 편이 아니니, 내 스스로가 구직자들을 대함에 있어 학력과 학벌 및 전공에 제한을 두고 그러지는 않는다. 다만 학력과 학벌 및 전공에 무관하게, 이력서가 단순 프로젝트 개요와 기간 및 경력의 나열에 불과하면, 해당 구직자는 탈락시킨다.

### 6.3. 학원에서 많이들 유입되는데, 이런 분들에 대한 면접 경험
#### 6.3.1. 문제점
#### 6.3.2. 조언하자면
### 6.4. 웹개발자 구직자들에게 조언을 한다면
#### 6.4.1. 어떤 공부를 하면 좋은지