## NFT_training

파이썬으로 NFT 만들어보기

## 참고 사이트
https://betterprogramming.pub/create-your-own-nft-collection-with-python-82af40abf99f

## 1. NFT 이미지 생성

파일: nft_create_images.py

특징들: 얼굴, 머리, 귀, 눈, 입, 코, 악세서리, 수염

이미지: 8가지의 특징들을 가중치에 따라 랜덤하게 조합하여 생성


## 2. NFT 메타데이터 생성  

### NFT 메타데이터란 ? 

NFT 이름, 설명, 이미지 링크, 특징 들을 담고 있는 json 문서이다.

(이더리움)NFT smart contract에 필요하다.

<img src="https://miro.medium.com/max/1400/0*blUV7iNHWCgmRJDT.png" alt="Example" title="Example"/>

### 클라우드에 NFT 이미지 업로드

대용량의 이미지 파일을 블록체인에 업로드 하는 것은 매우 비싸다.

따라서 [Pinata](InterPlanetary File System)를 통해 IPFS에 이미지를 올리고 그 링크를 블록체인에 업로드 한다.

만들어진 프로젝트의 링크는 _BASE URL_ 이다. https://gateway.pinata.cloud/ipfs/QmbrxDifGTVS9kDJscNjBJvU6a1Kb9REkhuMqBV9oE7k3H?preview=1




## 3. Smart Contract 에 올리기  
## 4. NFT 만들기
