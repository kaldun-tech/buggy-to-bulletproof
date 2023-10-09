## Chapter 5: Unit Testing <a id="ch05-unit-tests"></a>

### Tips to Make Your Unit Tests Great
Unit tests form the critical base of our testing pyramid. Creating a great foundation requires writing a lot of great unit tests! Here are some helpful tips to get you going:

**Keep tests simple and focused:** Each unit test should focus on testing a single, well-defined aspect of the code such as a single code path through a function or method. A complex test that tries to cover multiple scenarios at once should be split into smaller tests. Simplicity makes it easier to understand and maintain the tests.

**Use descriptive names:** This makes it much easier to maintain the test going forward. Inevitably requirements will change and someone will need to update the tests. A great name will provide the needed information about the purpose of the test without having to read the code.

**Use mocking and stubs:** This technique allows you to isolate the unit under test from its dependencies, like databases or services. Then you can focus on the particular unit’s behavior without relying on internal systems.

**Cover Edge Cases and Boundary Conditions:** Ensure that your unit tests cover edge cases and boundary conditions. This refers to scenarios that are at the extreme ends of the expected behavior. For example, if a function has an integer parameter, test it with both the minimum and maximum valid values as well as with invalid values.

**Test happy paths and error cases:** Build positive test cases for successful code paths and negative cases to handle unexpected or erroneous inputs. This helps ensure that your code behaves robustly and handles errors gracefully.

**Keep security in mind:** Consider common attack vectors like SQL and Command Injection, Cross-Site Scripting (XSS), and deserialization. Getting unit tests around these adds fantastic quality assurance value to your testing process.

#### Python Example

Here is a simple example of using unit tests in Python using the built-in unittest framework. We will revisit the calculator concept from chapter two, in this case focusing on the division function since that is a great example of where things can go wrong. Here is the method under test:

#### math_functions.py

```
def divide_numbers(a, b):
    """Divides inputs as integers"""
    if b == 0:
        raise ValueError("Division by zero is not allowed")
    return a / b
```

Now let's implement some unit tests.
1. Add a positive test case for the "happy path" that we expect to not throw an error.
2. Add a negative test case for the expected error with divide by zero.

#### test_math_functions.py

```
import unittest
from math_functions import divide_numbers

class TestMathFunctions(unittest.TestCase):

    def test_divide_numbers_normal:
        """Test normal integer division"""
        # Simple division
        result = divide_numbers(6, 2)
        self.assertEqual(result, 3)

        # Divide positive by negative
        result = divide_numbers(4, -2)
        self.assertEqual(result, -2)

    def test_divide_by_zero:
        """Check that division by zero raises a ValueError"""
        with self.assertRaises(ValueError):
            divide_numbers(5, 0)

if __name__ == '__main__':
    unittest.main()
```

This just scratches the surface of possible tests. Here's some more ideas:
- The divide_numbers method does not enforce typing of the input variables. Test for None input and different input types such as a str or list.
- Test case for if decimals are passed in.
- Test case for if the result of division would be fractional.

&copy; Kaldun Technologies 2023
