# TMDB API를 활용한 Request & Response

## Problem A

인기 영화 조회 인기 영화의 개수를 출력합니다. 

1. `requests`를 이용하여 인기 영화 정보(Get Popular)에 요청을 보냅니다. 

2. popular를 기준으로 받아온 데이터에서 영화 리스트의 개수를 계산합니다.  

3. 계산한 정보를 반환하는 함수 `popular_count`를 완성합니다. 

### 개선점

같이 프로젝트를 진행한 분은 api.key 파일을 따로 만들고, 키를 불러오는 방식으로 했는데,
나는 어째선지 api.key 파일을 만들어도 자꾸 키파일을 못찾는다 ㅜㅜ

분명히 동일한 위치에 놓았는데도 그렇다.

나중에 심심하면 다시 해보면서 원인 분석 해보는 것도 좋을 듯 하다.


## Problem B

Problem A에서 popular를 기준으로 가져온 영화 목록 중 평점이 8 이상인 영화들의 목록을 출력합니다. 

1. `requests`를 이용하여 인기 영화 정보(Get Popular)에 요청을 보냅니다.
2. 받아온 데이터에서 평점(key `vote_average`)를 기준으로 점수가 8 이상인 영화들의 목록을 리스트로 반환하는 함수 `vote_average_movies`를 완성합니다.

### 개선점

filter()를 잘 활용하자. 맨날 map()만 써서 filter()는 익숙하지 않은 듯 한데, filter()도 자주 써서 익숙해져야겠다.

## Problem C

특정 조건에 맞는 인기 영화 조회 II 영화목록을 평점순으로 출력하는 함수를 완성합니다. 

1. `requests`를 이용하여 인기 영화 정보(Get Popular)에 요청을 보냅니다.
2. 받아온 데이터 중 평점(key `vote_average`)이 높은 영화 다섯개의 정보를 리스트로 반환하는 함수 `ranking`을 완성합니다. 

### 개선점
제일 오래 걸렸다. 처음 받은 영화들의 정보 목록들이 딕셔너리 타입에 리스트 하나로 묶여 있어서 접근하는 데에 많이 헤맸다. 이것도 그냥 많이 연습해보는게 답인 듯 하다.


## Problem D

특정 영화 추천 영화 조회 제공된 영화 제목을 기준으로 추천영화 목록을 출력합니다.

1. `requests`를 이용하여 영화 검색(Search Movies) 요청을 보냅니다. (인자로 넘어온 `title` 사용)
2. 결과중 첫번째 영화가 검색한 영화가 맞다면 해당 영화의 id를 사용합니다.
3. id를 기반으로 추천영화 목록 조회 (Get Recommendations) URL을 생성합니다. 
4. `requests`를 이용하여 추천영화 목록 조회 URL에 요청을 보냅니다. 
5. 추천받은 영화 리스트에서 **제목만을** 리스트에 저장합니다. 
6. 저장된 리스트를 반환하는 함수 `recommendation`을 완성합니다. 
7. (2번) id값은 있지만 추천영화가 없는 경우 빈 리스트를 반환합니다. 
8. (3번) 올바르지 않은 영화 제목으로 검색할 수 없는 경우 `None`을 반환합니다. 

### 개선점
이것도 오래걸렸지만, C만큼 오래걸리지는 않았다. 아마 반복문을 쓸 일이 없어서 그런 듯 하다.


