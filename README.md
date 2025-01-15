# Frontend-Development
<!DOCTYPE html>
<html>
  <head></head>
  <body>
    <!-- Code changes are at the bottom. -->
    <p>
      <button onclick="
        updateCalculation('1');
      ">1</button>

      <button onclick="
        updateCalculation('2');
      ">2</button>

      <button onclick="
        updateCalculation('3');
      ">3</button>

      <button onclick="
        updateCalculation(' + ');
      ">+</button>
    </p>

    <p>
      <button onclick="
        updateCalculation('4');
      ">4</button>

      <button onclick="
        updateCalculation('5');
      ">5</button>

      <button onclick="
        updateCalculation('6');
      ">6</button>

      <button onclick="
        updateCalculation(' - ');
      ">-</button>
    </p>

    <p>
      <button onclick="
        updateCalculation('7');
      ">7</button>

      <button onclick="
        updateCalculation('8');
      ">8</button>

      <button onclick="
        updateCalculation('9');
      ">9</button>

      <button onclick="
        updateCalculation(' * ');
      ">*</button>
    </p>

    <p>
      <button onclick="
        updateCalculation('0');
      ">0</button>

      <button onclick="
        updateCalculation('.');
      ">.</button>

      <button onclick="
        // Note: eval() takes a string and runs it as code.
        // Avoid using eval() in real world projects since
        // it can potentially be given harmful code to run.
        // Only use eval() for learning purposes.
        calculation = eval(calculation);
        console.log(calculation);

        // Remember to save the calculation here.
        localStorage.setItem('calculation', calculation);
      ">=</button>

      <button onclick="
        updateCalculation(' / ');
      ">/</button>
    </p>

    <p>
      <button onclick="
        calculation = '';
        console.log(calculation);

        // Remember to save the calculation here.
        localStorage.setItem('calculation', calculation);
      ">Clear</button>
    </p>

    <script>
      let calculation = localStorage.getItem('calculation') || '';

      function updateCalculation(value) {
        calculation += value;
        console.log(calculation);
        localStorage.setItem('calculation', calculation);
      }

      // Optional: you can also create a function in order
      // to reuse this code.
      function saveCalculation() {
        localStorage.setItem('calculation', calculation);
      }
    </script>
  </body>
</html>
