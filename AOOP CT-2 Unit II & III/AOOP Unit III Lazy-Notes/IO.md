**Java I/O (Input and Output)**

- Java I/O is used for processing input and producing output based on that input.

- It involves the concept of streams for efficient I/O operations.

- The `java.io` package contains classes and interfaces required for I/O operations.

**Stream**

- A stream is a sequence of objects that supports various methods and can be pipelined to produce desired results.

- Streams can be used for reading and writing data from/to various sources like collections, arrays, or I/O channels.

- Streams do not modify the original data structure; they provide results based on pipelined methods.

- Each intermediate operation on a stream is lazily executed, and it returns a stream, allowing various operations to be pipelined together.

**Standard Streams**

- Java provides three standard streams:
  1. Standard Input (`System.in`): Used for reading input data, typically from the keyboard.
  2. Standard Output (`System.out`): Used for writing output data, usually displayed on the screen.
  3. Standard Error (`System.err`): Used for outputting error messages, also typically displayed on the screen.

- Example:
  ```java
  System.out.println("Simple message");
  System.err.println("Error message");
  int i = System.in.read();
  System.out.println((char) i);
  ```

**Stream Types**

- Two primary types of streams:
  1. **OutputStream**: Used for writing data to a destination, which can be a file, array, peripheral device, or socket.
  2. **InputStream**: Used for reading data from a source, which can be a file, array, peripheral device, or socket.

**Java FileOutputStream**

- `FileOutputStream` is used for writing data to a file.

- It can write byte-oriented and character-oriented data.

- It is recommended to use `FileWriter` for character-oriented data.

**Java FileInputStream**

- `FileInputStream` is used for reading data from a file.

- It reads byte-oriented data, such as image or binary data.

- For character-oriented data, use `FileReader`.

**Java BufferedOutputStream**

- `BufferedOutputStream` is used to buffer an output stream, improving performance.

- It writes data to an internal buffer before sending it to the destination stream.

- Use `BufferedOutputStream` to efficiently write data.

**Java BufferedInputStream**

- `BufferedInputStream` is used to read data from a stream efficiently.

- It reads data into an internal buffer, which can be read from efficiently.

**Java SequenceInputStream**

- `SequenceInputStream` reads data from multiple streams sequentially, one after another.

- It is used when data needs to be read from multiple sources in a sequence.

**Java ByteArrayOutputStream**

- `ByteArrayOutputStream` writes data into a byte array.

- It can be used to write common data into multiple files or streams.

- The internal buffer automatically grows as needed.

**Java ByteArrayInputStream**

- `ByteArrayInputStream` reads data from a byte array.

- It is useful for reading data stored in memory.

- The internal buffer grows as needed.

In summary, Java I/O provides a wide range of classes and streams for reading and writing data efficiently from various sources. Understanding the appropriate stream types and classes is essential for effective I/O operations in Java.