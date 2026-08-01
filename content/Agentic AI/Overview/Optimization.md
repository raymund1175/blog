
Agentic AI 시대의 성능 기준
- as is: 모델의 답변 정확성
	- 단위: Token
- to be: 여러 에이전트 간 협력 구조의 완성도
	- 단위: Task (작업단위)
	- 상태 관리
		- KV Cache(단기 기억)
		- Vector DB(장기 기억)
		- 로그 및 추적 기록 (audit, reproducibility)
	- cost - depth 간 tradeoff
		- 에이전트와의 통신 및 대화가 많아지면 latency, cost 상승
		- 대화 횟수, 단계별 토큰 수, 근거 첨부 등 운영 규칙 필요
	- 신뢰 및 권한 관리
		- 각 에이전트가 접근 가능한 도구와 데이터 정의
	- 관측 및 실험
		- prompt, cache hit ratio, 도구 실패율, consistency 등의 지표 모니터링
		- 새로운 설정은 A/B test로 검증
첨언
- 미래에는 GPU, NPU뿐 아니라 CXL(Compute Express Link) 같은 새로운 메모리 공유 기술이 중요한 역할을 할 것. 여러 에이전트와 모델이 동시에 데이터를 다루는 상황에서, 메모리를 유연하게 나누고 연결할 수 있어야 한다. 

용어
- Cache: 캐시는 주기억장치와 CPU 사이에 위치. 캐시 메모리는 메모리 계층 구조에서 가장 접근이 빠른 위치에 존재한다. 이러한 특성 덕분에 캐시를 사용하면 주기억장치에 접근하는 횟수가 줄어들면서 처리 속도가 빨라진다. 
	- Cache hit ratio: 에이전트에게 새로운 작업이 주어졌을 때, 처음부터 끝까지 새로 생각해서(비용과 시간 소모) 답을 내는 것이 아니라 **"이거 아까 했던 작업이랑 똑같네?" 하고 기억(캐시)에서 바로 정답을 꺼내오는 비율**
- A/B test: 기존 버전(A)과 수정된 버전(B)을 유사한 집단에게 동시에 노출하여 결과를 비교하는 테스트 방법

[참고 링크](https://www.linkedin.com/posts/dongsoo-lee-45028017_agentic-ai-%EC%B5%9C%EC%A0%81%ED%99%94-%EC%9D%B4%EC%8A%88%EC%97%90-%EB%8C%80%ED%95%9C-%EA%B0%84%EB%8B%A8%ED%95%9C-%EC%86%8C%EA%B0%9C-kv-cache-activity-7368596764829937665-c4J3/?originalSubdomain=kr)
