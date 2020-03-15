# web-pastel
  
![image](https://user-images.githubusercontent.com/35188271/76704054-aba85300-6719-11ea-8b4a-7e0306211b7d.png)

  
1. `홈페이지 제작` (AWS ec2 홈페이지 제작) / AWS DNS 등록 (새로운 홈페이지명)  `https://naver.com.홈페이지명.com`  
 ps) 로드벨런싱 제외, Throttle 제외, HW spec 제외  
 
2. `홈페이지 특징` : 이미지+텍스트 업로드 페이지 (ex: `http://fromtoday.co.kr/`   ,  `http://me2.do/5iyBceMF` )
         
# Flow

1.  `웹페이지` : 스마트 스토어 -> 링크 버튼 -> 네이버me(로그인 확인) -> 네이버 아이디, Oauth 토큰 유효성 확인후 -> 업로드 웹페이지 띄움.

2.  `웹-서버 데이터` : 이미지/버튼 (1~10) 매핑 -> 이미지 자르기(오픈소스 활용) ->  업로드(aws s3 덮어쓰기Mode) -> 폴더명:날짜+고객아이디(1.png ~ x.png)  
-> 구글시트에 데이터 넣음 (이메일 아이디, 이름1,이름2, 날짜, 결제여부, 이미지1, 문구1, 이미지2, 문구2 .... )  

-----------------  dataclay : 구글시트에 render 안한거 확인후 -> render 작업 실행 ----------------------

3.  `디자이너` : 구글 시트(현재 수동) -> After Effect -> 렌더링(300mb 예상) ->  AWS s3 데이터 저장. -> dataclay(구글시트 -> render컬럼 갱신) 
4.  `고객` : 결제 -> 구글시트 render 결과 완료 -> s3 링크 웹페이지 표시 -> s3에서 동영상 다운로드 -> s3-wodonggun주소/날짜/wodonggun@naver.com/output.mp4  

# After

1. `H/W 선택` - AWS 고성능 컴퓨터 or 회사 고성능 컴퓨터
2. `이미지 위치` - s3 or 로컬컴퓨터
3. `단가` - 
4. `유지보수` - 
