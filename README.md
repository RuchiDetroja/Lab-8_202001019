# Lab-8_202001019

**SOFTWARE ENGINEERING</br></br>
NAME: Ruchi Detroja     
ID: 202001019     
LAB 8**

➔**Below is the provided code for the ‘Boa’ class created for testing.**</br></br>
// represents a boa constrictor</br></br>

public class Boa {</br>
&emsp;private String name;</br>
&emsp;private int length; // the length of the boa, in feet</br>
&emsp;private String favoriteFood;</br></br>
&emsp;public Boa (String name, int length, String favoriteFood){</br>
&emsp;&emsp;this.name = name;</br>
&emsp;&emsp;this.length = length;</br>
&emsp;&emsp;this.favoriteFood = favoriteFood;</br>
&emsp;}</br>

// returns true if this boa constrictor is healthy</br>

&emsp;public boolean isHealthy(){</br>
&emsp;&emsp;return this.favoriteFood.equals("granola bars");</br>
&emsp;}</br>

// returns true if the length of this boa constrictor is</br>
// less than the given cage length</br>

&emsp;public boolean fitsInCage(int cageLength){</br>
&emsp;&emsp;return this.length < cageLength;</br>
&emsp;}</br>
}</br></br>

➔ Now we create a Junit Test case for testing the above ‘Boa’ class and named it ‘Boa_test’.</br>
➔ Below is the Test code for running the initial test cases.</br></br>

package test_lab8;</br>
import static org.junit.jupiter.api.Assertions.*;</br>
import org.junit.Before;</br>
import org.junit.jupiter.api.Test;</br></br>

class Boa_test {</br>
&emsp;@Test</br>
&emsp;public void testIsHealthyWithFavoriteFoodGranolaBars() {</br>
&emsp;&emsp;Boa boa = new Boa("Benny", 5, "granola bars");</br>
&emsp;&emsp;assertTrue(boa.isHealthy());</br>
&emsp;}</br>

&emsp;@Test</br>
&emsp;public void testIsHealthyWithFavoriteFoodNotGranolaBars() {</br>
&emsp;&emsp;Boa boa = new Boa("Benny", 5, "mice");</br>
&emsp;&emsp;assertFalse(boa.isHealthy());</br>
&emsp;}</br>

&emsp;@Test</br>
&emsp;public void testFitsInCageWhenLengthLessThanCageLength() {</br>
&emsp;&emsp;Boa boa = new Boa("Benny", 5, "granola bars");</br>
&emsp;&emsp;assertTrue(boa.fitsInCage(10));</br>
&emsp;}</br>

&emsp;@Test</br>
&emsp;public void testFitsInCageWhenLengthGreaterThanCageLength() {</br>
&emsp;&emsp;Boa boa = new Boa("Benny", 20, "granola bars");</br>
&emsp;&emsp;assertFalse(boa.fitsInCage(10));</br>
&emsp;}</br>
}</br>
➔ Now we ran the above test cases successfully.</br>
➔ Now we use the @Before tag to run another test case.</br>
➔ The @Before tag runs before every test case(@Test).</br>
➔ The code snippet below show how to execute it.</br>

&emsp;private Boa jen;</br>
&emsp;private Boa ken;</br></br>
&emsp;@Before</br>
&emsp;public void setUp() throws Exception {</br>
&emsp;&emsp;jen = new Boa("Jennifer", 2, "grapes");</br>
&emsp;&emsp;ken = new Boa("Kenneth", 3, "granola bars");</br>
&emsp;}</br>

➔**Now performing Q5**</br>
➔ Below is the test code for the question.</br>
&emsp;@Test</br>
&emsp;public void testIsHealthy() {</br>
&emsp;&emsp;Boa jen = new Boa("Jen", 5, "granola bars");</br>
&emsp;&emsp;Boa ken = new Boa("Ken", 6, "mice");</br>
&emsp;&emsp;assertTrue(jen.isHealthy());</br>
&emsp;&emsp;assertFalse(ken.isHealthy());</br>
&emsp;}</br>
&emsp;@Test</br>
&emsp;public void testFitsInCage() {</br>
&emsp;&emsp;Boa jen = new Boa("Jen", 5, "granola bars");</br>
&emsp;&emsp;Boa ken = new Boa("Ken", 6, "mice");</br>
&emsp;&emsp;assertFalse(jen.fitsInCage(2));</br>
&emsp;&emsp;assertTrue(jen.fitsInCage(10));</br>
&emsp;&emsp;assertTrue(jen.fitsInCage(15));</br>
&emsp;&emsp;assertFalse(ken.fitsInCage(4));</br>
&emsp;&emsp;assertTrue(ken.fitsInCage(15));</br>
&emsp;&emsp;assertTrue(ken.fitsInCage(20));</br>
&emsp;}</br>

➔ **Now creating another method in the ‘Boa’ class for Q7.</br>**

&emsp;Method Code:</br>

&emsp;&emsp;public int lengthInInches() {</br>
&emsp;&emsp;&emsp;return this.length * 12;</br>
&emsp;&emsp;}</br>

&emsp;Testing code:</br>

&emsp;@Test</br>
&emsp;public void testLengthInInches() {</br>
&emsp;&emsp;Boa boa = new Boa("John", 5, "grapes");</br>
&emsp;&emsp;int expectedLengthInInches = 60;</br>
&emsp;&emsp;int actualLengthInInches = boa.lengthInInches();</br>
&emsp;&emsp;assertEquals(expectedLengthInInches, actualLengthInInches);</br>
&emsp;}

Boa class file: 

![class-file](https://user-images.githubusercontent.com/123498746/233034210-b456f973-e55e-44ab-ba94-4f02d7e859e3.png)

BoaTest.java file:

Created 10 test cases: 2 for checking isHealthy() function, 6 for fitsInCage() function and 2 for lengthInInches() function.

![testcase-file1](https://user-images.githubusercontent.com/123498746/233034269-44bc05d3-e667-4323-923a-1052a753a2f9.png)
![testcase-file2](https://user-images.githubusercontent.com/123498746/233034317-9928381c-42e4-431e-8857-112d0b86aaf7.png)
![testcase-file3](https://user-images.githubusercontent.com/123498746/233034351-d017bd7f-5017-40d1-9be3-6b6532293daf.png)
