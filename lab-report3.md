# Lab Report 3 - Bugs and Commands (Week 5)
## Part 1 - Bugs
One of the bugs from week 4's lab was the implementation of ```reverseInPlace```:
```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

### A failure-inducing input for the buggy program:
```
  @Test
  public void testReverseInPlace() {
    int[] input = {1, 2, 3};
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(new int[]{3, 2, 1}, input);
  }
```

### An input that doesn't induce a failure:
```
  @Test
  public void testReverseInPlace1() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
  }
```

### The symptom:
![Image](report3-symptom.png)

### The bug:

code before:
```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

code after:
```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < (arr.length/2); i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
```
The fixed code correctly reverses the contents of the array by swapping elements in the first half with their counterparts in the second half, ensuring the entire array is reversed. In contrast, the original code incorrectly overwrote each element with the last element. The fix involves iterating through the first half of the array (which is why the loop iterates over ```length/2```), using a temporary variable 'temp' for swapping, resulting in the correct reversal.

