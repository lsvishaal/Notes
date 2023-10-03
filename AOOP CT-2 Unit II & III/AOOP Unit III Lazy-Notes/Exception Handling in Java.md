**Exception Handling in Java**

Exception handling is a aspect of Java programming, allowing you to  manage errors and unexpected situations. This unit covers exception hierarchy, throwing and catching exceptions, built-in exceptions, and creating custom exceptions.

**Difference Between Error and Exception**

- **Errors:** Errors indicate serious problems and abnormal conditions that most applications should not try to handle. They are typically caused by factors outside the application's control, such as memory errors, hardware errors, or JVM errors.

- **Exceptions:** Exceptions are conditions within the code that a developer can handle and take necessary corrective actions. Examples include DivideByZero exception, NullPointerException, ArithmeticException, and ArrayIndexOutOfBoundsException.

**Exception Hierarchy**

- All exception classes are subtypes of the `java.lang.Exception` class, which itself is a subclass of `Throwable`.

**Categories of Exceptions**

1. **Checked Exceptions:** These occur at compile time and must be handled by the programmer. Examples include IOException, ClassNotFoundException.

2. **Unchecked Exceptions:** These occur at runtime and are ignored at compile time. They include programming bugs and logic errors, like NullPointerException and ArrayIndexOutOfBoundsException.

**Throwing & Catching Exceptions**

- Keywords used in exception handling: `try`, `catch`, `finally`, `throw`, and `throws`.

- **try-catch** block is used to guard against and handle runtime errors. It includes code that might generate an exception and a catch clause specifying the exception type to catch.

**Examples of Built-in Exceptions**

1. **ArithmeticException:** Occurs during mathematical operations like division by zero.

```java
try {
    int result = 42 / 0;
} catch (ArithmeticException e) {
    // Handle exception
}
```

2. **ArrayIndexOutOfBoundsException:** Occurs when accessing an array element at an invalid index.

```java
try {
    int[] arr = new int[5];
    int value = arr[10];
} catch (ArrayIndexOutOfBoundsException e) {
    // Handle exception
}
```

3. **NullPointerException:** Occurs when performing operations on a null object reference.

```java
try {
    String str = null;
    int length = str.length();
} catch (NullPointerException e) {
    // Handle exception
}
```

4. **NumberFormatException:** Occurs when converting a string to a numeric value fails.

```java
try {
    String str = "XYZ";
    int num = Integer.parseInt(str);
} catch (NumberFormatException e) {
    // Handle exception
}
```

**Nested Try Statements**

- You can nest try statements to handle multiple exceptions in different parts of your code.

```java
try {
    // Outer try block
    try {
        // Inner try block
    } catch (ExceptionType1 e1) {
        // Inner catch block 1
    }
} catch (ExceptionType2 e2) {
    // Outer catch block
}
```

**Multi-Catch Block**

- You can catch multiple exceptions in a single catch block using the multi-catch feature introduced in Java 7.

```java
try {
    // Code that may throw exceptions
} catch (ExceptionType1 | ExceptionType2 e) {
    // Handle multiple exceptions
}
```

**Finally Block**

- The `finally` block contains code that always executes, whether an exception occurs or not. It's used for cleanup tasks like closing files or connections.

```java
try {
    // Code that may throw exceptions
} catch (Exception e) {
    // Handle exception
} finally {
    // Cleanup code (always executed)
}
```

**Throwing Exceptions**

- You can explicitly throw exceptions using the `throw` keyword.

```java
if (condition) {
    throw new ExceptionType("Error message");
}
```

**Throws Keyword**

- The `throws` keyword is used in method declarations to declare exceptions that a method may throw. It informs the caller that the method can potentially throw these exceptions.

```java
void myMethod() throws ExceptionType1, ExceptionType2 {
    // Method code
}
```

**Advantages of Exception Handling**

- Control the program's flow and maintain normal execution.
- Provide information to callers about potential exceptions.
- Organize and differentiate between different error types.

**Java StackTraceElement**

- `StackTraceElement` class in Java represents a single stack frame, typically corresponding to a method invocation.

- All stack frames, except the top one, represent method invocations. The top stack frame represents the execution point where the stack trace was generated.

**Class Declaration**
```java
public final class StackTraceElement extends Object implements Serializable
```

**Constructors**
1. `StackTraceElement(String declaringClass, String methodName, String fileName, int lineNumber)`: Creates a stack trace element representing a specific execution point.
   - `declaringClass`: Fully qualified name of the class containing the execution point.
   - `methodName`: Name of the method containing the execution point.
   - `fileName`: Name of the file containing the execution point or null if not available.
   - `lineNumber`: Line number in the source file containing the execution point or a negative number if not available.

**Understanding Stack Trace**
- A stack trace is a list of method calls from the start of the application to the point where an exception was thrown.

- It is a valuable debugging tool that shows the sequence of method calls leading to an exception.

- Stack traces help pinpoint where an error occurred and how the program reached that point in the code.

**Example:**
```java
public class StackTraceExample {
    public static void main(String[] args) {
        try {
            throw new RuntimeException("Something went wrong"); // Throwing a runtime exception
        } catch (Exception e) {
            System.out.println("Printing stack trace:");
            StackTraceElement[] stackTrace = e.getStackTrace();
            for (StackTraceElement s : stackTrace) {
                System.out.println("\tat " + s.getClassName() + "." + s.getMethodName()
                                   + "(" + s.getFileName() + ":" + s.getLineNumber() + ")");
            }
        }
    }
}
```

**Output:**
```
Printing stack trace:
    at StackTraceExample.main(StackTraceExample.java:4)
```

In summary:
- `StackTraceElement` represents a single method invocation in a stack trace.
- Stack traces are invaluable for debugging, showing the method call sequence leading to an exception.
- The class provides information about the class, method, file, and line number where an exception occurred.
- Stack traces help developers locate and fix errors efficiently.
