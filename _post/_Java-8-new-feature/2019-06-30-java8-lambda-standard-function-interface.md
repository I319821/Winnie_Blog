
# Java 函数式接口

在JDK8中 *java.util.function* 包提供了43个函数式接口，其中有6个基础接口。必要时可以通过这6个接口推断出其余接口。

1. UnaryOperator接口代表有一个参数并且返回值与参数类型一致的函数。
2. BinaryOperator接口代表有两个参数，并且返回值与参数类型一致的函数。
1. Predicate接口代表有一个参数并返回boolean类型的函数。
1. Fuction接口代表其参数与返回值类型不一样的函数。
1. Supplier接口代表没有参数并返回一个值的函数。
1. Consumer代表的是带有一个函数但不返回任何值的函数。

这6个基础函数接口的概述如下：

接口 | 函数签名 | 范例
---|---|---
UnaryOperator<T>| T apply( T t )|String::toLowerCase
BinaryOperator<T>|T apply( T t1, T t2 )|BigInteger::add
Predicate<T>|boolean test( T t )|Collection::isEmpty
Function<T,R>|R apply( T t )|Arrays::asList
Supplier<T>|T get( )|Instant::now
Consumer<T>|void accept(T)|System.out::println


---



## 1. UnaryOperator

接口 | 函数签名
---|---
IntUnaryOperator | int applyAsInt( int operand )
LongUnaryOperator| long applyAsLong( long operand )
DoubleUnaryOperator| double applyAsDouble( double operand )


## 2. BinaryOperator

接口 | 函数签名
---|---
IntBinaryOperator | int applyAsInt( int left, int right )
LongBinaryOperator| long applyAsLong( long left, long right )
DoubleBinaryOperator| double applyAsDouble( double left, double right )


## 3.Predicate

接口 | 函数签名
---|---
IntPredicate | boolean test( int value )
LongPredicate | boolean test( long value )
DoublePredicate| boolean test( double value )
BiPredicate| boolean test( T t, U u )


## 4.Function

接口 | 函数签名
---|---
IntFunction | R apply( int value )
LongFunction | R apply( long value )
DoubleFunction | R apply( double value )
BiFunction | R apply( T t, U u )
ToIntFunction| int applyAsInt( T value )
LongToIntFunction | int applyAsInt( long value )
DoubleToIntFunction | int applyAsInt( double value )
ToLongFunction | long applyAsLong( T value )
IntToLongFunction | long applyAsLong( int value )
DoulbeToLongFunction| long applyAsLong( double value )
ToDoubleFunction | double applyAsDouble( T value )
IntToDoubleFunction| double applyAsDouble( int value )
LongToDoubleFunction| double applyAsDouble( long value )


## 5.Supplier

接口 | 函数签名
---|---
BooleanSupplier | boolean getAsBoolean( )
IntSupplier | int getAsInt( )
LongSupplier| long getAsLong( )
DoubleSupplier| double getAsDouble( )

## 6. Consumer

header 1 | header 2
---|---
IntConsumer | void accept( int value )
LongConsumer | void accept( long value )
DoubleConsumer| void accept( double value)
BiConsumer| void accept( T t, U u )
ObjIntConsumer | void accept( T t, int value )
ObjLongConsumer| void accept( T t, long value )
ObjDoubleConsumer| void accept( T t, double value )




























