#Convert HTML Elements

####Basically there are limited elements that need to be converted for this exercise. 

* I decided to take advantage of that by adding into a switch statement, iterated through by a "for" loop. 
* Take advantage as you like. I have the solution below. Remember, copy only if you understand it. 

```function convertHTML(str) {

  var temp = str.split('');

//The symbols are limited in the test cases. You should take advatage of that with a switch
  for (var i = 0; i < temp.length; i++) {
    switch (temp[i]) {
      case '<':
        temp[i] = '&lt;';
        break;
      case '&':
        temp[i] = '&amp;';
        break;
      case '>':
        temp[i] = '&gt;';
        break;
      case '"':
        temp[i] = '&quot;';
        break;
      case "'":
        temp[i] = '&apos;';
        break;
    }
  }

  temp = temp.join('');
  return temp;
}


convertHTML("Dolce & Gabbana");
```