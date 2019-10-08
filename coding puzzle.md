# NUS Computing Career Fair Coding Puzzle
This is the list of coding puzzles we are putting up for NUS Computing School career fair for interactivity

## String Reverse
<pre>
<code>
const reversal = str => {
  let temp = [];
  str = str.split("").map(x => x.codePointAt(0)).join(" ");
  str = str.split(/\s/g);
  str = str.map(x => parseInt(x));
  for (let x = str.length; x > 0; x--) {
  temp = temp.concat(str.pop());
  }
  str = temp;
  str = str.map(x => String.fromCharCode(x));
  str = str.join("");
  console.log(str);
};
reversal("noitavonnI gniripsnI eklhüZ");
</code>
</pre>
Javascript provided by Robert

---
## Merge Sort
<pre>
<code>
const mergeSort = (arr) => {
  if(arr.length <= 1) {
    return arr;
  }
  const half = parseInt(arr.length /2);
  const left = mergeSort(arr.slice(0,half));
  const right = mergeSort(arr.slice(half, arr.length));
  const merge = (left,right) => {
    const result = [];
    while(left.length > 0 && right.length > 0) {
      result.push(left[0] <= right[0]? left.shift() :right.shift());
    }
    return result.concat(left).concat(right);
  }
  return merge(left,right);
}

const a = [ 34, 7, 1, 3, 19, 5, 5];

console.log(mergeSort(a));
</code>
</pre>
Javascript provided by Ria

---
## Insertion Sort
<pre>
<code>
public static void insertionSort(int[] arr) {
  for(int i = 1; i < arr.length; i++) {
    int key = arr[i];
    int j = i-1;
    while(j > = 0 && arr[j] > key){
      arr[j+1] = arr[j];
      j--;
    }
    arr[j+1] = key;
  }
}
</code>
</pre>
Java provided by Jawen

---
## Palindrome
<pre>
<code>
public static void isPalindrome(String inputString) {
  int startIndex= 0;
  int endIndex = inputString.length() -1;
  while( start Index < endIndex) {
    if(inputString.charAt(startIndex != inputString.charAt(endIndex))) return false;
    startIndex++;
    endIndex--;
  }
  return true;
}
</code>
</pre>
Java provided by Florian M

---
## Prime Number Check
<pre>
<code>
public static boolean isPrime(int inputNumber, int currentDivisor) {
  if(inputNumber < 2) {
    return false;
  }

  if(inputNumber % 2 == 0) {
    return inputNumber == 2;
  }

  if(currentDivisor * currentDivisor > inputNumber) {
    return true;
  }

  if(inputNumber % currentDivisor == 0) {
    return false;
  }

  return is Prime(inputNumber, currentDivisor + 1);
}
</code>
</pre>
Java provided by Florian M

---
## Fibonacci Series Recursion
<pre>
<code>
int n1 = 0, n2 = 1, n3 = 0;
void printFibonacci(int count) {
  if(count > 0) {
    System.out.print(" " + n3);
    n1 = n2;
    n2 = n3;
    n3 = n1 + n2;
    printFibonacci(count - 1);
  }
}
</code>
</pre>
Java provided by JEDS