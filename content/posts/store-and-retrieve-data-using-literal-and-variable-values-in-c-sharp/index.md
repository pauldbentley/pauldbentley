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

C# is a strongly typed language, meaning that every variable must be declared with a specific type, and values assigned to it must be compatible with that type.

<!--more-->

## Question

> Which of the following lines of code creates a variable correctly?

Try it yourself on [freeCodeCamp](https://www.freecodecamp.org/learnfoundational-c-sharp-with-microsoft/write-your-first-code-using-c-sharp/store-and-retrieve-data-using-literal-and-variable-values-in-c-sharp).

## Option 1

```csharp
int x = 12.3m;
```

Here, we're declaring a variable `x` of type [`int`](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types).  The key point to remember is that `int` is used for **whole numbers** not decimals.

We're then trying to assign it to the value `12.3m`.  The presence of a decimal point makes this a [floating-point](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types) value, and the `m` suffix is the literal for a `decimal`.

[C# is a strongly typed language](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/) and enforces type safety.  Assigning a `decimal` value to an `int` variable is not allowed as it would lead to data loss. This kind of mismatch causes a **compiler error**.

{{< awesome fa-regular fa-circle-xmark >}} This is incorrect.
{.text-danger .mb-4 .fw-bold}

## Option 2

```csharp
decimal x = 12.3m;
```

Here, we're declaring a variable `x` of type [`decimal`](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types) and assign the literal `12.3m`.  The `m` suffix is the literal for a `decimal`.  This tells the compiler this is a decimal, not a double (which would be the default for floating-point literals without a suffix).

{{< awesome fa-regular fa-circle-check >}} This is the correct answer.
{.text-success .mb-4 .fw-bold}

## Option 3

```csharp
bool x = 'False';
```

Here, we're declaring a variable `x` of type [bool](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/bool).
A bool can can either be `true` or `false`.

Next we assign `x` to the value `'False'` enclosed in **single quotes** which in C# denotes a [char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) (a single character).

Since `'False'` is actually multiple characters, this won't compile either.

If you wanted to assign a `bool` with the value false, you would write:

```csharp
bool x = false;
```

{{< awesome fa-regular fa-circle-xmark >}} This is incorrect.
{.text-danger .mb-4 .fw-bold}