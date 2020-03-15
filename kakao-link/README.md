  # 초대장 샘플
  
  ![image](https://user-images.githubusercontent.com/35188271/66035808-c9f10c80-e546-11e9-84fb-6ef3db40ee87.png)

  ```c
  <a id="kakao-link-btn" href="javascript:;">
    <img src="//developers.kakao.com/assets/img/about/logos/kakaolink/kakaolink_btn_medium.png"/>
    </a>
    
    <script type='text/javascript'>
      
          // 고유키값 - 건들지 마세요
        Kakao.init('고유키값');
          
        Kakao.Link.createDefaultButton({
          container: '#kakao-link-btn',
          objectType: 'location',
          
          // 지도 표시할 주소
          address: '경기 수원시 장안구 경수대로 930',
          
          // 지도 제목
          addressTitle: '드마리스 수원점 - 파스텔무비지점',
          content: {
            title: '우동근 첫번째 생일, 함께 축하해주세요♥',
            description: '일시 : 2019-09-24   PM 6:30\n장소 : 김포공항 마이어스(김포한강점)',
            
            // 메인 애기 사진 주소 (이미지 파일 주소 지정)
            imageUrl: 'https://cdn.imweb.me/thumbnail/20190923/e1dd649722e14.png',
            
            link: {
              mobileWebUrl: 'https://pastelmovie.com',
              webUrl: https://pastelmovie.com'
            }
          },
           buttons: [
            {
              title: '초대장 보기',
              link: {
                //초대장 링크 weburl=데스크탑,  mobile=스마트폰 
                mobileWebUrl: 'https://pastelmovie.com/89',
                webUrl: 'https://pastelmovie.com/89'
              }
            }
          ]
        });
    
    </script>
    ```
