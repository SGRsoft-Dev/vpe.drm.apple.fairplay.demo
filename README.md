## NAVER CLOUD PLATFORM Video Player Enhancement DEMO

미디어플러스에서 제공하는 NAVERCLOUD VPE Player의 Apple FairPlay DRM 데모 코드

![](https://nnbkegvqsbcu5297614.cdn.ntruss.com/profile/202308/db85e25df98bf242d0ae25724a975dd7.png)



## 소스코드
[https://github.com/SGRsoft-Dev/vpe.drm.apple-fps.demo](https://github.com/SGRsoft-Dev/vpe.drm.apple-fps.demo)


*** 


## 필수
- 네이버클라우드 플랫폼 Video Player Enhancement SDK URL
- 네이버클라우드 VOD Station 재생소스
- PallyCon DRM 필수
***

## 제한사항

현재 데모코드에 사용된 필수 요소들은 개발자 로컬 테스트에서만 동작합니다. (http://localhost)

네이버클라우드 플랫폼 Video Player Enhancement 유료 라이선스가 필요합니다.

해당 데모는 PallyCon DRM을 지원합니다. (https://pallycon.com)

***


## 사용자 가이드
### NAVERCLOUD PLATFORM Video Player Enhancement
https://guide.ncloud-docs.com/docs/ko/vpe-overview


### VPE DRM 가이드
https://guide.ncloud-docs.com/docs/vpe-example-auth#multidrm

### PallyCon DRM 가이드
https://pallycon.com/ko/drm-platform/


***

## 실행방법

```bash
$ npm install
$ npm run dev
```

## DRM 세팅

```javascript
// src/demo.js

document.addEventListener('DOMContentLoaded',  async ()=> {

    window.drmPlayer = await ncplayerDRM('player',{
        playlist:[
            {
                drm:{
                    'com.apple.fps':{
                        src : '재생소스',
                        certificateUri: '인증서 url',
                        licenseUri : '라이선스 url',
                        licenseRequestHeader:{
                            'Content-type': 'application/x-www-form-urlencoded',
                            'pallycon-customdata-v2':'FPS 토큰키'
                        }
                    },
                },
            },
        ],
        autostart:true,
        muted:true,
        progressBarColor:"#ff0000",
    });

});


```

***


## 문의하기


SGRSOFT 개발팀  : dev@sgrsoft.com

채널톡 : https://sgrsoft.channel.io/home

영업 및 네이버클라우드 가입 문의 : biz@sgrsoft.com

SGRSOFT를 통하여 네이버클라우드 플랫폼 크래딧을 지원 받을 수 있습니다. (최대 300만원)


미디어플러스 웹사이트 :
[https://mediaplus.co.kr/](https://mediaplus.co.kr/)

![](https://nnbkegvqsbcu5297614.cdn.ntruss.com/profile/202308/851b6ea05f1fcc1cb827d841ca32346d.png)


