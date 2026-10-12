# _java_8_coding
java 8 is introduce many functionality mainly functional programming and collection processing 


Java 8 — Short Notes
Java 8 introduced many important features, especially functional programming and easier collection processing.
1. Lambda Expression ⭐
Used to write short implementations of functional interfaces.
(a, b) -> a + b

Example:
List<Integer> list = Arrays.asList(1, 2, 3);

list.forEach(n -> System.out.println(n));

2. Functional Interface ⭐
An interface containing exactly one abstract method.
@FunctionalInterface
interface Calculator {
    int add(int a, int b);
}

Common examples:
- Runnable
- Comparator
- Predicate
- Function
- Consumer
- Supplier
3. Stream API ⭐
Used to process collections in a clean and declarative way.
List<Integer> nums = Arrays.asList(10, 20, 30, 40);

nums.stream()
    .filter(n -> n > 20)
    .forEach(System.out::println);

Common methods:
- filter() → filtering
- map() → transformation
- sorted() → sorting
- distinct() → remove duplicates
- collect() → convert result
- reduce() → combine values
- forEach() → iterate
4. Method Reference
Short form of a lambda expression.
list.forEach(System.out::println);

Instead of:
list.forEach(x -> System.out.println(x));

Types:
- Class::staticMethod
- object::instanceMethod
- Class::instanceMethod
- Class::new
5. Optional ⭐
Used to reduce NullPointerException problems.
Optional<String> name = Optional.of("Saurabh");

name.ifPresent(System.out::println);

Important methods:
- of()
- ofNullable()
- isPresent()
- orElse()
- orElseGet()
6. Default Method
Interfaces can have method implementations.
interface Vehicle {
    default void start() {
        System.out.println("Vehicle started");
    }
}

7. Static Method in Interface
interface Test {
    static void show() {
        System.out.println("Hello");
    }
}

Called using:
Test.show();

8. Date and Time API ⭐
Java 8 introduced java.time.
Important classes:
LocalDate
LocalTime
LocalDateTime
ZonedDateTime
Period
Duration

Example:
LocalDate date = LocalDate.now();
System.out.println(date);

9. Predicate
Returns true/false.
Predicate<Integer> p = n -> n > 10;

10. Function
Takes input and returns output.
Function<Integer, Integer> square = n -> n * n;

11. Consumer
Takes input but does not return anything.
Consumer<String> c = s -> System.out.println(s);

12. Supplier
Takes no input and returns a value.
Supplier<String> s = () -> "Hello";

Java 8 Interview Must-Know
Feature	Main Purpose
Lambda	Short function implementation
Functional Interface	One abstract method
Stream API	Process collections
Method Reference	Shorter lambda
Optional	Handle null safely
Default Method	Method implementation in interface
Static Interface Method	Static behavior in interface
Date/Time API	Modern date/time handling
Predicate	Returns boolean
Function	Input → Output
Consumer	Input → No output
Supplier	No input → Output
