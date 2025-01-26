---
title: "Perform Basic String Formatting in C#"
date: 2025-01-15T10:00:00-07:00
draft: false
categories:
    - Coding
tags:
    - csharp
    - freecodecamp-csharp
---

This question looks at how to format a string using string interpolation.

<!--more-->

## Question
> Which of the following lines of code correctly uses string interpolation assuming that the variable value is a string?

## Option 1

```csharp
Console.WriteLine(@"My value: {value}");
```

The ```@``` character at the start of the string indicates this is a [verbatim string](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/verbatim).  This means anything inside the string is interpreted literally.

So the command above would write ```My value: {value}``` to the console. 

{{< awesome fa-regular fa-circle-xmark >}} This is incorrect.
{.text-danger .mb-4 .fw-bold}

## Option 2

```csharp
Console.WriteLine($"My value: {value}");
```

The ```$``` character at the start of the string indicates this is an [interpolated string](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/interpolated).  When an interpolated string is processed into the final string, the compiler will replace anything inside ```{}``` with the result of the expression.

Let's say we have set the value of ```value``` to ```"The value"```.  The command above would write ```My value: The value``` to the console. 

{{< awesome fa-regular fa-circle-xmark >}} This is correct.
{.text-success .fw-bold}

## Option 3

```csharp
Console.WriteLine(@"My value: [value]");
```

The ```@``` character at the start of the string indicates this is a [verbatim string](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/verbatim).  This means anything inside the string is interpreted literally.

So the command above would write ```My value: [value]``` to the console. 

{{< awesome fa-regular fa-circle-xmark >}} This is incorrect.
{.text-danger .mb-4 .fw-bold}