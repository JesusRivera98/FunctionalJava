# FunctionalJava
This repository is from Platzi's course ["Programación Funcional con Java SE"](https://platzi.com/clases/java-funcional/)

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)

## General info

In this course we learn concepts related to functional programming using Java SE and as a final product we generate a console application that allows job searches at job.github.com

### Concepts

| Java | Description |
|-|-|
|Consumer <T>| Receives data of type T and does not generate any results|
|Function <T, R>| Takes a data of type T and generates a result of type R|
|Predicate <T>| Takes a data of type T and evaluates if the data meets a condition|
|Supplier <T>| Does not receive any data, but generates a data of type T each time it is invoked|
|UnaryOperator <T>| Receives a data of type T and generates a result of type T|

#### There are two types of operations: intermediate and final.

|||
|-|-|
|Terminal operations| Are those operations that do not generate a new Stream as a result.|
|Intermediate operation| Is said to any operation within a Stream that returns a new Stream as a result. That is, after invoking an intermediate operation with a certain type of data, we will obtain as a result a new Stream containing the already modified data.|


#### The operations intermediate that are already defined are:

|Operation|Description|
|-|-|
|filter (…)|-|
|map (…)|-|
|flatMap (…)|-|
|distinct (…)| Compare each element of the Stream against the rest using the equals method. In this way, it prevents the Stream from containing duplicate elements.|
|limit (…)| Receives a long that determines how many elements of the original Stream will be preserved.|
|peek (…)| It works like a magnifying glass, like a moment of observation of what is happening in the Stream. What this operation does is take a Consumer, pass the data as they are present in the Stream and generate a new identical Stream in order to continue operating.|
|skip (…)| This operation is contrary to limit (). While limit () reduces the elements present in the Stream to a specific number, skip discards the first n elements and generates a Stream with the remaining elements in the Stream.|
|sorted (…)| Requires that the elements present in the Stream implement the Comparable interface to be able to do a natural sorting within the Stream. The resulting Stream contains all the elements but already ordered|

#### The most common terminal operations found in Stream are:

|||
|-|-|
|Coincidence| The anyMatch, allMatch and noneMatch operations are used to determine if there are elements in a Stream that meet a certain Predicate|
||anyMatch ()|
||allMatch ()|
||noneMatch ()|
|Search| These operations return an Optional as a result of searching for an element within the Stream.|
||findAny ()|
||findFirst ()|
|Reduction|They are two operations whose purpose is to obtain the smallest element (min) or the largest element (max) of a Stream using a Comparator|
||min ()|
||max ()|
|reduce ()||
|reduce (InitialValue, BinaryOperator)| Returns a value of the same type as the Stream after applying BinaryOperator on each element of the Stream.|
|reduce (BinaryAccumulator)| Returns an Optional of the same type as the Stream, with a single value resulting from applying the BinaryAccumulator on each element|
|reduce (InitialValue, BinaryFunction, BinaryOperator)| Generates a value of type V after applying BinaryFunction on each element of type T in the Stream and obtaining a V result.|
|count ()| used to obtain how many elements are in the Stream.|
|toArray ()| Adds all the elements of the Stream to an array and returns that array.|
|collect ()| Collector is an interface that will take data of type T from the Stream, a mutable data type A, where the elements will be added (mutable implies that we can change their content, such as a LinkedList) and will generate a result of type R .|
|Iteration|
|forEach ()| As simple and as cute as a classic for|
## Technologies

This project was created using:
* Java
* IntelliJ IDEA
* OpenJDK 8
* ####  MVNrepository
- JCommander
- feign-core
- feign-gson

## Setup

To work in this project, install it locally:
* [IntelliJ IDEA](https://www.jetbrains.com/es-es/idea/download)
* [OpenJDK 8](https://adoptopenjdk.net/?variant=openjdk8&jvmVariant=hotspot)
* [Java](https://www.java.com/es/download/manual.jsp) 8 or higher

