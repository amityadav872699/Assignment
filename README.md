# Assignment
This is assignment
<!DOCTYPE html>
<html lang="eng">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="/Assignment2/style.css" />
    <title>Assignment_2</title>
  </head>
  <body>
    <div class="container">
      <div class="text">String Occurence</div>
      <br /><br />
      <form>
        <div class="sentence">Enter a Sentence:</div>
        <input type="text" id="sentence" />
        <div class="sentence letter">Enter a Letter:</div>
        <input type="text" id="letter" />
        <button type="button" onclick="validate()">Submit</button>
      </form>
    </div>
    <script>
      function validate(sentence, letter, count) {
        var occur = 0;
        count = 1;
        sentence = document.getElementById("sentence").value;
        letter = document.getElementById("letter").value;

        if (count == 0) {
          document.write(sentence);
          return;
        }
        for (i = 0; i < sentence.length; i++) {
          if (sentence.charAt(i) == letter) {
            occur++;
          }
          if (occur == count) {
            break;
          }
        }
        if (i < sentence.length - 1) {
          alert("The Result: " + sentence.substring(i + 1));
        } else {
          alert("The letter doesn't exist in the sentence");
        }
      }
    </script>
  </body>
</html>
