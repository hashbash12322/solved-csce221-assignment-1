Download Link: https://assignmentchef.com/product/solved-csce221-assignment-1
<br>
Since a string is not included in the C++ language, this assignment was focused on the elementary design, implementation and test of the string class called my_string. The purpose of this class is to show how the STL string class is implemented and it provides the overview of the basic C++ concepts that were covered in CSCE 121.

<ol>

 <li>The description of data structures and algorithms used to solve the problem.

  <ul>

   <li>Provide definitions of data structures by using Abstract Data Types (ADTs)</li>

  </ul></li>

</ol>

The data structure that was used was a static array that terminated in the character ’ ’. No dynamic ADTs were used. The array was also included with the int values of sz and cap which held the number of elements of the array and the capacity of the array.

<ul>

 <li>Write about the ADTs implementation in C++.</li>

</ul>

The implementation of the Data Structure was called every time we initialized a my_string variable in the main.cpp file. Depending on the type of arguments, there were different constructors that initialized the data structure. For the basic, ’empty’ object, the default pointer was pointing to a new char array of size cap, which was set to a default capacity of 2 and a sz of 0. When sending in an int s in the argument, the constructor would first call a IncreaseCapacity() function that would check whether the capacity of the array was larger than the size, if no it would double the size of the capacity to allow the new elements to be written in the array. The third constructor was initialized by sending in a string. Again, the IncreaseCapacity() function was called if the number of elements were bigger than the capacity of the array. After the increase, the string would be assigned to a new array that was accessed though a pointer. We also have one more constructor that will copy the members from another data type to initialize it to its own.

<ul>

 <li>Describe algorithms used to solve the problem.</li>

</ul>

The algorithm that were used were various. One algorithm was to increase the size of the capacity by multiplying it by 2. This was done by reading in the the total size of the elements and determining if the capacity of the original array is large enough to hold all the elements. If not, then a temporary array was created to hold the array then the old array pointer was redirected to point at the temporary array. Another algorithm implemented was to count the number of elements in the incoming string. This was executed with a while statement that would count until the character ’ ’ was found. Other algorithms involved using for loops to assigned the elements from arrays to new arrays or to append strings to existing arrays.

<ul>

 <li>Analyze the algorithms according to assignment requirements.</li>

</ul>

The algorithm works very well when implemented in the main.cpp file. The constructors initialize the data objects for different input cases. The overloaded operators (+=,=) works very well by manipulating the character arrays that are available.

<ol start="2">

 <li>A C++ organization and implementation of the problem solution

  <ul>

   <li>Provide a list and description of classes or interfaces used by a program such as classes used to implementthe data structures or exceptions.</li>

  </ul></li>

</ol>

This imitates the string library that is not native to C++. We can implement these functions anywhere that requires a user to input string data in any program.

<ul>

 <li>Include in the report the class declarations from a header file (.h) and their implementation from a sourcefile (.cpp).</li>

</ul>

These files are included in the .tar file.

<ul>

 <li>Provide features of the C++ programming paradigms like Inheritance or Polymorphism in case of objectoriented programming, or Templates in the case of generic programming used in your implementation.</li>

</ul>

For this assignment, there was not an instance of Polymorphism except for the inclusion of iostream and stdexcept in the header file.

<ol start="3">

 <li>A user guide description how to navigate your program with the instructions how to:

  <ul>

   <li>compile the program: specify the directory and file names, etc.</li>

  </ul></li>

</ol>

To compile the program, it is important to run the make file which will make the header file and the .cpp files to output a single my_string.o file. To run the make file, simply type “make all”. To run the output file, simply type ./my_string in the terminal. This will execute the desired code.

<ul>

 <li>run the program: specify the name of an executable file.</li>

</ul>

The name of the output file to run is my_string. To run simply type ./my_string in the terminal.

<ol start="4">

 <li>Specifications and description of input and output formats and files

  <ul>

   <li>The type of files: keyboard, text files, etc (if applicable).</li>

  </ul></li>

</ol>

The user must use a keyboard to input text into a character array which uses the istream overloaded operator to read into the data structure.

<ul>

 <li>A file input format: when a program requires a sequence of input items, specify the number of items perline or a line termination. Provide a sample of a required input format.</li>

</ul>

The input that the user will type will read a string until white space, tab or new line character is found. The string before the character will be read into the data structure.

<ul>

 <li>Discuss possible cases when your program could crash because of incorrect input (a wrong file name,strings instead of a number, or such cases when the program expects 10 items to read and it finds only 9.)</li>

</ul>

The program could crash when the user inputs a string that is longer than 2^64 characters due to the IncreaseCapacity() function that depends on the doubling of an int. The input would be too many characters for the possible number of elements that the capacity int could hold.

<ol start="5">

 <li>Provide types of exceptions and their purpose in your program.

  <ul>

   <li>logical exceptions (such as deletion of an item from an empty container, etc.).</li>

  </ul></li>

</ol>

The exception used is an out_of_range Error when the at(int i) function is called. If the input i is negative or bigger than the size of the array, an exception will be thrown.

<ul>

 <li>runtime exception (such as division by 0, etc.)</li>

</ul>

If there is an error in the constructor and the capacity is set to 0, then the IncreaseCapcity() function will crash due to the capacity being multiplied by 2 and thus equaling 0 again. No string will be able to input into the function.

<ul>

 <li>Test your program for correctness using valid, invalid, and random inputs (e.g., insertion of an item at thebeginning, at the end, or at a random place into a sorted vector). Include evidence of your testing, such as an output file or screen shots with an input and the corresponding output</li>

</ul>

By testing the program with the included main.cpp, every input was successful. Here are some screenshots of the output.