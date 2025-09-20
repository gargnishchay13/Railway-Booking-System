# Railway Booking System

This project is a Railway Booking System implemented in C++.  
The repository contains source files, header files, unit tests, and build instructions.  
This README provides details of the file structure, compiler information, and compilation instructions.

---

## Project Structure

```
.
├── ApplicationTestNegative.cpp
├── ApplicationTestPositive.cpp
├── Booking.cpp
├── Booking.h
├── BookingClass.cpp
├── BookingClass.h
├── BookingCategory.cpp
├── BookingCategory.h
├── Concession.cpp
├── Concession.h
├── Date.cpp
├── Date.h
├── Exceptions.cpp
├── Exceptions.h
├── Gender.cpp
├── Gender.h
├── Name.cpp
├── Name.h
├── Passenger.cpp
├── Passenger.h
├── Railways.cpp
├── Railways.h
├── Station.cpp
├── Station.h
├── UnitTestBooking.cpp
├── UnitTestBookingClass.cpp
├── UnitTestBookingCategory.cpp
├── UnitTestConcession.cpp
├── UnitTestDate.cpp
├── UnitTestGender.cpp
├── UnitTestName.cpp
├── UnitTestPassenger.cpp
├── UnitTestRailways.cpp
├── UnitTestStation.cpp
└── makefile
```

---

## Details of Various Header and Source Files

- **Station.h**: Header file for the `Station` class (data members, constructors, and functions).  
- **Station.cpp**: Implements constructors and functions of `Station`.  
- **UnitTestStation.cpp**: Unit tests for the `Station` class.  

- **Railways.h**: Header file for singleton `Railways` class.  
- **Railways.cpp**: Implements static constants and functions of `Railways`.  
- **UnitTestRailways.cpp**: Unit tests for the `Railways` class.  

- **Date.h**: Header file for the `Date` class.  
- **Date.cpp**: Implements constructors, functions, and static constants.  
- **UnitTestDate.cpp**: Unit tests for the `Date` class.  

- **Gender.h**: Header file for the `Gender` class (`Male`, `Female`).  
- **Gender.cpp**: Implements static constants for `Gender` hierarchy.  
- **UnitTestGender.cpp**: Unit tests for `Gender`.  

- **Name.h**: Header file for the `Name` class.  
- **Name.cpp**: Implements constructors and functions of `Name`.  
- **UnitTestName.cpp**: Unit tests for `Name`.  

- **Passenger.h**: Header file for the `Passenger` class.  
- **Passenger.cpp**: Implements functions of `Passenger`.  
- **UnitTestPassenger.cpp**: Unit tests for `Passenger`.  

- **BookingClass.h**: Header for hierarchy of booking classes.  
  - Root: abstract base `BookingClass`.  
  - Children (singleton classes): `ACFirstClass`, `ExecutiveChairCar`, `AC2Tier`, `FirstClass`, `AC3Tier`, `ACChairCar`, `Sleeper`, `SecondSitting`.  
- **BookingClass.cpp**: Implements hierarchy functions.  
- **UnitTestBookingClass.cpp**: Unit tests for booking classes.  

- **BookingCategory.h**: Header for `BookingCategory` and `Divyaang` hierarchy.  
- **BookingCategory.cpp**: Implements hierarchy functions.  
- **UnitTestBookingCategory.cpp**: Unit tests for `BookingCategory`.  

- **Concession.h**: Header for `Concession` hierarchy (applicable concessions).  
- **Concession.cpp**: Implements `Concession` functions.  
- **UnitTestConcession.cpp**: Unit tests for `Concession`.  

- **Exceptions.h**: Header for custom exception hierarchy.  
- **Exceptions.cpp**: Implements exception classes.  

- **Booking.h**: Header file for the `Booking` class.  
- **Booking.cpp**: Implements constructors, functions, and initializes static variables.  
- **UnitTestBooking.cpp**: Unit tests for `Booking`.  

- **ApplicationTestPositive.cpp**: Application-level positive test scenarios.  
- **ApplicationTestNegative.cpp**: Application-level negative test scenarios.  

- **makefile**: Simple makefile to compile and build the project.  

---

## Compiler Used

- **Compiler**: GNU GCC  
- **Language**: C++  
- **Standard**: C++11  
- **Libraries**: Standard C++ libraries  

---

## Compilation and Build Instructions

To build and run the project:

```sh
$ make
$ ./rbs
```

By default, `ApplicationTestPositive.cpp` is compiled.  
To run with another application file, e.g. `ApplicationTestNegative.cpp`:

```sh
$ make APPFILE=ApplicationTestNegative
$ ./rbs
```

---

## Unit Testing Instructions

Each class can be tested individually with the following commands:

- **Station**  
  ```sh
  g++ -std=c++11 Station.cpp Railways.cpp Exceptions.cpp UnitTestStation.cpp -o test
  ./test
  ```

- **Railways**  
  ```sh
  g++ -std=c++11 Station.cpp Railways.cpp Exceptions.cpp UnitTestRailways.cpp -o test
  ./test
  ```

- **Date**  
  ```sh
  g++ -std=c++11 Date.cpp Exceptions.cpp UnitTestDate.cpp -o test
  ./test
  ```

- **Gender**  
  ```sh
  g++ -std=c++11 Gender.cpp UnitTestGender.cpp -o test
  ./test
  ```

- **Name**  
  ```sh
  g++ -std=c++11 Name.cpp Exceptions.cpp UnitTestName.cpp -o test
  ./test
  ```

- **Passenger**  
  ```sh
  g++ -std=c++11 Station.cpp Railways.cpp Date.cpp Gender.cpp Name.cpp Passenger.cpp BookingClass.cpp BookingCategory.cpp Concession.cpp Booking.cpp Exceptions.cpp UnitTestPassenger.cpp -o test
  ./test
  ```

- **BookingClass**  
  ```sh
  g++ -std=c++11 BookingClass.cpp UnitTestBookingClass.cpp -o test
  ./test
  ```

- **BookingCategory / Divyaang**  
  ```sh
  g++ -std=c++11 Station.cpp Railways.cpp Date.cpp Gender.cpp Name.cpp Passenger.cpp BookingClass.cpp BookingCategory.cpp Concession.cpp Booking.cpp Exceptions.cpp UnitTestBookingCategory.cpp -o test
  ./test
  ```

- **Concession**  
  ```sh
  g++ -std=c++11 Concession.cpp Date.cpp Passenger.cpp BookingClass.cpp BookingCategory.cpp Gender.cpp Name.cpp Booking.cpp Station.cpp Railways.cpp Exceptions.cpp UnitTestConcession.cpp -o test
  ./test
  ```

- **Booking**  
  ```sh
  g++ -std=c++11 Station.cpp Railways.cpp Date.cpp Gender.cpp Name.cpp Passenger.cpp BookingClass.cpp BookingCategory.cpp Concession.cpp Booking.cpp Exceptions.cpp UnitTestBooking.cpp -o test
  ./test
  ```

---

## License

This project is open source. You are free to use, modify, and distribute with attribution.
