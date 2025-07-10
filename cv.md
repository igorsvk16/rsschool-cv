![photo](IMG_5117.jpg)

# Sivkov Igor

---

## Junior Frontend Developer

---

## Contacts:

- **Telegram:** @igorsvk
- **E-mail:** igorsvk16@gmail.com
- **Phone:** 89048665797
- **Discord:** sivkoff

---

## About me

19 years old, living in St. Petersburg.

I am currently actively studying frontend development.
I am also studying according to the plan presented on the website of The Odin Project, at RS School in the frontend direction and taking an intensive course in JS from T-Bank.
I participate in hackathons and develop my own projects.
I attend thematic meetups.

I learn quickly

I love learning new information and always complete any task, no matter how complex.

My goal is to become a sought-after developer

---

## Skills

- JS
- HTML5
- CSS
- Git
- Python

---

## Code example (Calculator logic):

```javascript
buttons.forEach((button) => {
  button.addEventListener("click", () => {
    if (button.textContent.includes("⇦")) {
      currentInput = currentInput.slice(0, -1);
      return updateDisplay(currentInput);
    }
    if (button.textContent.includes("C")) {
      clearAll();
      return updateDisplay();
    } else if (button.textContent.includes("=")) {
      if (
        num1 === null ||
        (num1 !== null && operator !== "" && currentInput === "")
      ) {
        return;
      } else if (currentInput !== "" && operator !== "") {
        num2 = Number(currentInput);
        currentInput = "";
        num1 = output.textContent = operate(num1, operator, num2);
        return clearAll();
      }
    } else if (button.textContent.includes(".")) {
      console.log(currentInput);
      console.log(!currentInput.includes("."));
      if (
        !currentInput.includes(".") &&
        currentInput !== "" &&
        endsWithNumber(currentInput)
      ) {
        console.log("1");
        currentInput += button.textContent;
        return updateDisplay(currentInput);
      } else {
        console.log("2");
        return;
      }
    } else if (["+", "-", "*", "/"].includes(button.textContent)) {
      if (num1 === null && currentInput !== "") {
        num1 = Number(currentInput);
        operator = button.textContent;
        waitForSecondOperand = true;
        currentInput = "";
        return;
      } else if (num1 === null && currentInput === "") {
        operator = button.textContent;
        return;
      } else if (num1 !== null && operator !== "" && currentInput === "") {
        return (operator = button.textContent);
      } else if (waitForSecondOperand && currentInput === "") {
        operator = button.textContent;
        return;
      } else {
        if (operator === "/" && Number(currentInput) === 0) {
          console.log("1");
          clearAll();
          updateDisplay();
          return alert('"Were you trying to divide by 0???');
        } else {
          console.log("2");
          num2 = Number(currentInput);
          let result = operate(num1, operator, num2);
          updateDisplay(result);
          num1 = result;
          operator = button.textContent;
          currentInput = "";
          waitForSecondOperand = true;
          return;
        }
      }
    } else {
      if (waitForSecondOperand) {
        currentInput = "";
        waitForSecondOperand = false;
      }
      if (currentInput.length < 13) {
        currentInput += button.textContent;
        updateDisplay(currentInput);
      }
    }
  });
});
```

---

## Experience

- The most difficult thing from a JS point of view is a [calculator](https://igorsvk16.github.io/Calculator) with all the exceptions worked out and the correct logic

### The other projects are also interesting from a visual effects point of view:

- [Landing-Page](https://igorsvk16.github.io/TOP-Project-Landing-Page/)

* [Etch-a-Sketch](https://igorsvk16.github.io/Project-Etch-a-Sketch-TOP/)

- [Rock-Paper-Scissors](https://igorsvk16.github.io/Project-Rock-Paper-Scissors/)

---

## Education

- 2028 Saint-Petersburg State University of Aerospace Instrumentation (SUAI) / Institute of Information Technology and Programming, Applied Computer Science

- The Odin Project (Foundations)

---

## Languages

- English - B1
- Russian - Native

---
