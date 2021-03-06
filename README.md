# FramerMotion π¨

framer-motionλ λ¦¬μ‘νΈμμ μ λλ©μ΄μκ³Ό μ μ€μ³λ₯Ό μ½κ² λ€λ£° μ μλλ‘ ν΄μ£Όλ λΌμ΄λΈλ¬λ¦¬μ΄λ€. <br/>
- λ§ν¬ 1: https://www.framer.com/motion/ <br/>
- λ§ν¬ 2: https://github.com/framer/motion


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

- non EcmaScript module Error λ°μ μ, CRACO μ€μ μ μ§νν΄μΌ νλ€.
```
npm install @craco/craco --save
```
```
craco.config.js μμ± ν, μ μ©

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
Package.jsonμ "scripts" λΆλΆ μμ 

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
      delayChildren: 0.3,             // νμ μ»΄ν¬λνΈμ μ λλ©μ΄μμ΄ μμ νμ΄λ°μ μ§μ 
      staggerChildren: 0.2,           // νμ μ»΄ν¬λνΈμ μ λλ©μ΄μμ μ€μ ν μκ° λ§νΌ μμ°¨λ₯Ό λ μ μμ΅λλ€.
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

## 4. Drag

![Hnet com-image](https://user-images.githubusercontent.com/81430564/147386278-ec9cc76f-efa7-4999-8d7b-aa0e6982a6ec.gif)


## 5. Path

![Hnet com-image](https://user-images.githubusercontent.com/81430564/147386338-c14d8923-58af-446c-9baf-a457989e8fb9.gif)

## 6. Slider

![Hnet com-image](https://user-images.githubusercontent.com/81430564/147386366-6df1643c-61d1-431f-a384-f5ab3015182e.gif)

## 7. Layout Id

![Hnet com-image](https://user-images.githubusercontent.com/81430564/147386431-a32573b0-b637-4ebb-9b26-314234fda7ed.gif)


## 8. Modal

![Hnet com-image](https://user-images.githubusercontent.com/81430564/147386394-16f0632c-ca71-4f8b-a6cb-e9426070ad1b.gif)







