# java-calculator-precourse

## 구현할 기능 목록

### 1. 프로젝트의 요구사항인 Console API를 사용해 사용자에게 문자열을 입력받는다.

### 2. 입력받은 문자열에 대해 

  &nbsp;&nbsp;&nbsp;&nbsp;총합, 구분자를 기준으로 추출한 변수를 저장할 배열과 같이 필요한 변수들을 선언한다.

  ####  &nbsp;&nbsp;&nbsp;&nbsp;2-a. 특수 구분자를 사용하는 경우

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;만약 사용자가 입력한 문자열이 "//"로 시작하고 그 뒤에 나오는 문자 뒤에 "\n"로 끝나는 경우 커스텀 구분자로써 따로 변수에 저장을 한다.
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이 경우 StringBuilder와 append함수를 통해 index를 기준으로 커스텀 구분자를 구하게 된다.
  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;그 후 Split 함수를 사용하여 특수 구분자 및 기본 구분자에 대해 문자열을 나누고 그 결과값을 String 배열에 저장한다.

  ####  &nbsp;&nbsp;&nbsp;&nbsp;2-b. 기본 구분자만 사용하는 경우

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;split함수를 사용하여 기본 구분자("," 와 ":")에 대해 입력받은 문자열을 나누고 그 결과값을 String 배열에 저장한다.
      
  ####  &nbsp;&nbsp;&nbsp;&nbsp;2-c. ""와 같이 공백인 경우

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;공백인 경우 주어진 것처럼 총합을 나타내는 변수에 0을 대입한다.

  ####  &nbsp;&nbsp;&nbsp;&nbsp;2-d. 잘못된 형식을 입력한 경우

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;즉 특수 구분자 입력 관련 잘못된 경우나 기본 구문자만 사용하는 경우에 잘못된 형식인 경우(즉 숫자로 시작하지 않는 경우) 
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;IllegalArgumentException을 발생시킨 후 애플리케이션을 종료한다.

  #### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 문제에서 명시한 조건 중 양수로 구성된 경우이므로 0, 음수의 경우 잘못된 형식으로 처리가 필요하다.

### 3. String 배열에 저장되어 있는 숫자값을 반복문을 통해 읽은 후 int형으로 변환 후 총 합을 구하여 결과값을 출력한다.

  &nbsp;&nbsp;&nbsp;&nbsp;String 타입의 양수를 정수로 반환하기 위해 parseStringtoInt라는 함수를 만든다.
  
  &nbsp;&nbsp;&nbsp;&nbsp;해당 함수 내에서 NumberFormatException을 IllegalArgumentException으로 발생시키도록 변환한다.
  
  #### &nbsp;&nbsp;&nbsp;&nbsp;또한 변환 과정에서 0, 음수가 있는 경우 마찬가지로 IllegalArgumentException를 발생시키도록 작성한다.

  ####  &nbsp;&nbsp;&nbsp;&nbsp;3-a. int형으로 변환 중 문제가 생기는 경우 
  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;잘못된 형식이 입력된 경우로 위와 같이 IllegalArgumentException을 발생시킨 후 종료한다.  



  

  &nbsp;&nbsp;&nbsp;&nbsp;최종적으로 주어진 형식에 맞도록 결과값을 출력한다.

    
