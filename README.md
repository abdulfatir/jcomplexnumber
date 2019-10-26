# jcomplexnumber
==============

A library which implements the complex number data type in Java. 

The features of this library include:  
1- Arithmetic Operations (addition, subtraction, multiplication, division)
2- Complex Specific Operations - Conjugate, Inverse, Absolute/Magnitude, Argument/Phase  
3- Trigonometric Operations - sin, cos, tan, cot, sec, cosec  
4- Mathematical Functions - exp, square, sqrt
5- **Complex Parsing** of type x+yi  


### Example Usage  

```java
import com.abdulfatir.jcomplexnumber.ComplexNumber;

public class TestComplexNumber
{
	public static void main(String args[])
	{
		// Default Complex Number 0+0i
		ComplexNumber c0 = new ComplexNumber();

		// 5+6i
		ComplexNumber c1 = new ComplexNumber(5,6);

		// 6-9i
		ComplexNumber c2 = new ComplexNumber(6,-9);

		ComplexNumber c1_plus_c2 = ComplexNumber.add(c1,c2);
		ComplexNumber c1_minus_c2 = ComplexNumber.subtract(c1,c2);
		ComplexNumber c1_into_c2 = ComplexNumber.multiply(c1,c2);
		ComplexNumber c1_by_c2 = ComplexNumber.divide(c1,c2);

		System.out.println(c1.toString()+" + "+c2.toString()+" = "+ c1_plus_c2.toString());
		System.out.println(c1.toString()+" - "+c2.toString()+" = "+ c1_minus_c2.toString());
		System.out.println(c1.toString()+" * "+c2.toString()+" = "+ c1_into_c2.toString());
		System.out.println(c1.toString()+" / "+c2.toString()+" = "+ c1_by_c2.toString());

		// Parsing Complex Numbers
		ComplexNumber c3 = ComplexNumber.parseComplex("-4+7i");
		System.out.println(c3.toString());

		// Formatting
		System.out.println(c3.format(ComplexNumber.RCIS));

		// Modulus
		System.out.println(c3.mod());

		// Conjugate
		System.out.println(c3.conjugate());

		// sin, cos
		System.out.println(ComplexNumber.sin(c3).toString());
		System.out.println(ComplexNumber.cos(c3).toString());
		
		// square and square root
		ComplexNumber c4 = new ComplexNumber(-5, 12);
		System.out.println(c4.square());
		System.out.println(c4.sqrt());
					
	}
}
```

