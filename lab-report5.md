# Lab Report 5 - Putting it All Together (Week 9)

## Part 1 - Debugging Scenario

### Original Post:
**Title:** Strange Behavior in String Reversal Method

**Description:** Hello, I'm working on a lab report and am having a weird issue with my string reversal method. I've attached the relevant code below: 

```
public class LabReport5 {

    // Intentional bug: Incorrect character swapping
    public static String reverseString(String input) {
        if (input == null || input.isEmpty()) {
            return "Input string is null or empty.";
        }

        char[] charArray = input.toCharArray();

        for (int i = 0; i < charArray.length; i++) {
            char temp = charArray[i];
            charArray[i] = charArray[charArray.length - 1];
            charArray[charArray.length - 1] = temp;
        }

        return new String(charArray);
    }
}
```

Here is a JUnit test case that fails:
```
public class TestLabReport5 {

    @Test
    public void testNormalString() {
        // test with a non-null and non-empty string
        String input = "Hello";
        String expected = "olleH";
        String actual = LabReport5.reverseString(input);
        assertEquals(expected, actual);
    }
}
```
![Image]() (ss of output when running test case

The problem is that when I use ```reverseString```, the output isn't what I expect. It seems like the characters aren't being swapped correctly because the output contains the same set of characters as the input but in a very weird order. I also noticed that the method works perfectly fine when the input string is null or empty, so I suspect there might be a bug in the character-swapping part of my code. 

Just to give you some background, I implemented the reversal by swapping each character in the string with the last character in the array. I thought this would be a straightforward way to reverse the string. Can anyone help me figure out what's going wrong here?

### Response from TA
Hey there! Thanks for providing the details. Your approach to swapping characters is interesting.

To narrow down the issue, you could try running your ```reverseString``` method with a simple test case (could be the same one you provided), and print the intermediate results within the loop. By doing so, you can observe the changes in the ```charArray``` at each iteration, which should help us see how the characters are being swapped at each step. For instance, you can add the following lines inside your loop: ``` System.out.println("Iteration " + i + ": " + new String(charArray)); ```.

### Student's Second Attempt

### The Setup

## Part 2 - Reflection
Throughout the second half of this quarter, I learned how versatile it is to work from the terminal. One part of the class that really stood out to me was how we could access, manipulate/edit, and even push files to GitHub directly from the command line. Previously, I hadn't known that it was possible to navigate GitHub without relying on a graphical interface. Also, working with Vim to edit files was  cool to learn about. Logging into the ieng6 computer remotely was definitely a highlight of the quarter since I had never done something like that before. I can see how the skills we learned in this lab will be very useful in any future software-related endeavors.

