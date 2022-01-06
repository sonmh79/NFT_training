## NFT_training

파이썬으로 NFT 만들어보기

## 참고 사이트
https://betterprogramming.pub/create-your-own-nft-collection-with-python-82af40abf99f

## 1. NFT 이미지 생성

* 파일: `nft_create.py`

* 특징들: 얼굴, 머리, 귀, 눈, 입, 코, 악세서리, 수염

* 방법: 8가지의 특징들을 가중치에 따라 랜덤하게 조합하여 생성

NFT 클래스는 다음과 같다.

* `NFT`
  * `face`,`eyes`,`nose` ... 등 # 클래스 변수들
  * `__init__()` # 클래스 선언 시 자동으로 특징들을 조합하여 유니크한 이미지 정보 생성 (변수명 `all_images`)
  * `trait_counts()` # 특징들 갯수 카운트
  * `create_images()` # 만들어진 이미지 정보를 바탕으로 실제 특징별 이미지를 조합하여 실제 이미지를 생성한다. 상위 폴더 밑에 `images` 폴더가 생긴다.


* 코드 사용 순서: 
    ```python
  nft = NFT()
  nft.create_images()
  # pinata에 생성된 images 폴더를 등록 후 링크와 프로젝트 이름을 IMAGE_BASE_URl과 PROJECT_NAME에 적어준다.
  # nft.create_metadata()

## 2. NFT 메타데이터 생성  

### NFT 메타데이터란 ? 

NFT 이름, 설명, 이미지 링크, 특징 들을 담고 있는 json 문서이다.

(이더리움)NFT `smart contract`에 필요하다.

<img src="https://miro.medium.com/max/1400/0*blUV7iNHWCgmRJDT.png" alt="Example" title="Example"/>

### 클라우드에 NFT 이미지 업로드

대용량의 이미지 파일을 블록체인에 업로드 하는 것은 매우 비싸다.

따라서 [Pinata](https://www.pinata.cloud)를 통해 IPFS에 이미지를 올리고 그 `링크`를 블록체인에 업로드 한다.

회원가입 후 1단계에서 만들어진 `images`폴더를 업로드 한다.

업로드 후, 만들어진 프로젝트의 링크는 `IMAGE_BASE_URL` 변수에 할당해준다. 

예시) IMAGE_BASE_URL = https://gateway.pinata.cloud/ipfs/QmbrxDifGTVS9kDJscNjBJvU6a1Kb9REkhuMqBV9oE7k3H/
(맨 뒤에 / 넣기)


### 메타데이터 생성

`nft.create_metadata()`

1단계에서 만들어진 리스트 `all_images` 안의 이미지 정보들을 각각  json 파일로 변환한다.

예를 들어, 100개의 이미지 정보가 있다면 100개의 json파일로 만든다.

각 json 파일은 `이미지 링크 주소`, `id`, `이름`, `속성` 등을 담고 있다.

만들어진 이미지 별 Json 파일을 또 다 [Pinata](https://www.pinata.cloud)에 업로드한다.

<img src="https://miro.medium.com/max/1400/1*8no0xmIMH4ZxN5A_CehE0A.png" />
(이미지 json파일 예시)


코드 사용 순서
  ```python
  #nft = NFT()
  # nft.create_images()
  ``` pinata에 생성된 images 폴더를 등록 후 링크와 프로젝트 이름을 IMAGE_BASE_URl과 PROJECT_NAME에 적어준다. ```
  nft.create_metadata()
  ```

## 3. Smart Contract 에 올리기  
## 4. NFT 만들기
