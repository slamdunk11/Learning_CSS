# 클래스 이름 세부적으로 작성하는 이유
- button1.jsx, button2.jsx, button1.css와 button2.css 처럼 css 파일을 따로 작성해도, 그 안에 클래스명을 똑같이 쓰면
  `오버라이딩 문제`가 발생한다...!(나중에 나오는 button2.css 걸로 다 처리됨)
  
  ```javascript
  // button1.css
  .button{
    background-color: blue;
  }
  .text{
    color: white
  }
  ```
  ```javascript
  //button2.css
  .button{
    background-color: red;
  }
  text{
    color: green;
  }
  ```
- 그래서 button1__button(button1 안에 있는 button), button2__button, button1__text 이런 식으로 클래스명을 세부적으로 작성하는데
- 그냥 CSS 사용 시 BEM(Block Element Modifier)와 같이 CSS 클래스명 정하는 규칙 등이 있다

# PostCSS 사용 이유
- 위의 복잡한 CSS 클래스명 같은 걸 걱정하지 않고도 모듈화가 가능!
- 클래스명 동일하게 button으로 써도 됨!

### 사용방법
- css파일 이름을 button1.module.css로
- import할 때 `import styles from "./button1.module.css";`
- 사용할 때 `<div className={styles.button}>`
- 실제로 개발자도구에서 Elements 확인하면 button1_button__~라고 모듈화가 되어서 나타난다
