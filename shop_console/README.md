#  Dart Console - Sorin's Shopping Mall
This is a simple console-based shopping mall program written in Dart.
It allows users to view products, add items to a cart, check the total price and quantity, and reset or exit the program.

## Features

### 1. 상품 목록 보기 (Show product list)
- [1]을 입력하면 미리 정의된 5개의 상품이 출력됩니다.
- 각 상품은 Product class로 구성되어 있으며, 상품명과 가격 정보를 가집니다.

/*
    예시:
    셔츠 / 45000 원
    원피스 / 30000 원
    반팔티 / 35000 원
    반바지 / 38000 원
    양말 / 5000 원
*/

### 2. 장바구니에 담기 (Add to cart)
- [2]를 입력한 뒤 상품명과 수량을 입력하면 해당 상품이 장바구니에 담깁니다.
- 예외 처리(try-catch)를 통해 잘못된 인풋(문자, 없는 상품, 음수 입력 등) 시 오류를 방지합니다.

/*
    상품명을 입력하세요: 원피스
    수량을 입력하세요: 2
    장바구니에 상품이 담겼어요!
*/


### 3. 장바구니 보기 (View cart)
- [3]을 누르면 장바구니에 담긴 총 금액과 상세 리스트가 출력됩니다.
- List<String> totalList와 List<String> totalAmount를 사용하여 상품명과 수량을 각각 저장합니다.

/*
    장바구니에 96000 원 어치를 담으셨네요!

    <쇼핑 리스트>
    - 원피스 * 2 개
    - 셔츠 * 1 개
*/

### 4. 프로그램 종료 (Exit program)
- [4]를 입력하면 "정말 종료하시겠습니가?"라는 확인 메시지가 나오며, [5]를 눌러야 종료됩니다.
- try-catch문을 이용하여 오류를 방지합니다. 
    - 숫자 이외의 형식이 입력되면 '입력값이 올바르지 않아요!' 메시지가 출력됩니다.
    - 5 이외의 숫자가 입력되면 종료되지 않습니다.

/*
    정말 종료하시겠습니까? 종료하시려면 [5]를 눌러주세요.
*/

### 5. 장바구니 초기화 (Reset cart)
- [6]을 입력하면 totalPrice, totalList, totalAmount 모두 초기화되어 장바구니가 비워집니다.
- 장바구니가 이미 비어있을 경우, 안내 메시지를 출력합니다.



## Key Logics
### class structure
- product : 상품명(name), 가격(price)을 가지며, .info()로 출력됨
- ShoppingMall : 상품 전체 목록과 장바구니의 총합, 상품별 리스트와 수량을 관리

### 데이터 입력 처리
- 모든 인풋은 stdin.readLineSync()로 받아 int.parse() 또는 toString()으로 처리
- try-catch문을 통해 입력 오류 발생 시 에러 메시지를 출력하여 프로그램 종료 없이 처리


## How to Run
1. dart가 설치되어 있어야 합니다.
2. terminal에서 해당 파일이 있는 디렉토리로 이동 후 실행:
    dart run shop_console.dart


## 추가하고 싶은 기능 아이디어 (To-Do)
- 장바구니에서 상품 개별 삭제 기능
- 장바구니 저장 및 불러오기
- 할인 쿠폰 시스템
