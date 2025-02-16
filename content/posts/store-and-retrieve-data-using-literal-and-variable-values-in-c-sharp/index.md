---
title: "Store and Retrieve Data Using Literal and Variable Values in C#"
date: 2024-12-30T13:01:53Z
draft: false
categories:
    - Coding
tags:
    - csharp
    - freecodecamp-csharp
---

C# is a strongly typed language where each variable has a defined type which can be assigned to different values.

<!--more-->

## Question

> Which of the following lines of code creates a variable correctly?

Complete this challenge on [freeCodeCamp](https://www.freecodecamp.org/learnfoundational-c-sharp-with-microsoft/write-your-first-code-using-c-sharp/store-and-retrieve-data-using-literal-and-variable-values-in-c-sharp).

## Option 1

```csharp
int x = 12.3m;
```

Here we are declaring a variable called `x` with a type of [`int`](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types).  The key point to remember is that integers are whole numbers.

Next we assign `x` to the literal value `12.3m`.  The decimal point signifies that this is a [floating-point numeric type](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types) which can have decimal places. The `m` suffix is the literal for a `decimal` value.

[C# is a strongly typed language](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/) and makes sure that all operations in your code are type safe.  When you declare a variable you can't assign a value not compatible with its declared type.  For example, you can't declare an `int` and assign it a `decimal` value as this would cause data loss which could result in unexpected bugs.

If you tried to compile the code in this example, you would get a compiler error.

{{< awesome fa-regular fa-circle-xmark >}} This is incorrect.
{.text-danger .mb-4 .fw-bold}

## Option 2

```csharp
decimal x = 12.3m;
```

Here we are declaring a variable called `x` with a type of [`decimal`](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types).

Next we assign `x` to the literal value `12.3m`.  The `m` suffix is the literal for a `decimal` value.

{{< awesome fa-regular fa-circle-check >}} This is correct.
{.text-success .mb-4 .fw-bold}

## Option 3

```csharp
bool x = 'False';
```

Here we are declaring a variable called ```x``` with a type of [bool](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/bool).
A bool can be assigned the literal value ```true``` and ```false```.

Next we assign ```x``` to the value ```'False'```.
The single quote characters here indicate this is a [char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) type.
A char can be assigned to a single character.

If you tried to compile the code in this example, you would get a compiler error.

{{< awesome fa-regular fa-circle-xmark >}} This is incorrect.
{.text-danger .mb-4 .fw-bold}