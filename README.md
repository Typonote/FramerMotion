# FramerMotion 🎨

framer-motion는 리액트에서 애니메이션과 제스쳐를 쉽게 다룰 수 있도록 해주는 라이브러리이다. <br/>
- 링크 1: https://www.framer.com/motion/ <br/>
- 링크 2: https://github.com/framer/motion


## 1. Installation

```
npm install framer-motion  OR  yarn add framer-motion
```
```
import { motion } from "framer-motion"
...
...
<motion.div></motion.div>
```

- non EcmaScript module Error 발생 시, CRACO 설정을 진행해야 한다.
```
npm install @craco/craco --save
```
```
craco.config.js 생성 후, 적용

module.exports = {
  webpack: {
    configure: {
      module: {
        rules: [
          {
            type: "javascript/auto",
            test: /\.mjs$/,
            include: /node_modules/,
          },
        ],
      },
    },
  },
};
```
```
Package.json의 "scripts" 부분 수정

"scripts": {
    "start": "craco start",
    "build": "craco build",
    "test": "craco test",
    "eject": "react-scripts eject"
  },
```



## 2. Animation


## 3. Variants

![Hnet com-image](https://user-images.githubusercontent.com/81430564/147209835-b4b5f2db-ea26-44f0-bbbe-92e88e1754bb.gif)

```
const boxVariants = {
  start: {
    opacity: 0,
    scale: 0.5,
  },
  end: {
    scale: 1,
    opacity: 1,
    transition: {
      type: "spring",
      duration: 0.5,
      bounce: 0.5,
      delayChildren: 0.3,             // 하위 컴포넌트의 애니메이션이 시작 타이밍을 지정
      staggerChildren: 0.2,           // 하위 컴포넌트의 애니메이션을 설정한 시간 만큼 시차를 둘 수 있습니다.
    },
  },
};

const circleVariants = {
  start: {
    opacity: 0,
    y: 10,
  },
  end: {
    opacity: 1,
    y: 0,
  },
};


    <Wrapper>
      <Box variants={boxVariants} initial="start" animate="end">
        <Circle variants={circleVariants} />
        <Circle variants={circleVariants} />
        <Circle variants={circleVariants} />
        <Circle variants={circleVariants} />
      </Box>
    </Wrapper>
 
```






