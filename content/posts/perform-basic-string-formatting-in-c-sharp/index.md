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

Learn how to use interpolated strings in C# to format output in a clean and readable way.

<!--more-->

## Question
> Which of the following lines of code correctly uses string interpolation assuming that the variable `value` is a string?

Try to answer this question first on [freeCodeCamp](https://www.freecodecamp.org/learn/foundational-c-sharp-with-microsoft/write-your-first-code-using-c-sharp/perform-basic-string-formatting-in-c-sharp).

## Option 1

```csharp
Console.WriteLine(@"My value: {value}");
```

The `@` symbol indicates a [verbatim string](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/verbatim), which means any content inside the string is treated literally.

**Output:**
```cmd
My value: {value}
```

{{< awesome fa-regular fa-circle-xmark >}} Incorrect - this does **not** perform string interpolation.
{.text-danger .mb-4 .fw-bold}

## Option 2

```csharp
Console.WriteLine($"My value: {value}");
```

The `$` symbol indicates this is an [interpolated string](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/interpolated).  Expressions inside `{}` are evaluated and inserted into the string.

Assuming `value = "The value"`, the output would be:

```cmd
My value: The value
```

{{< awesome fa-regular fa-circle-check >}} Correct - this is an example of string interpolation in C#.
{.text-success .fw-bold}

## Option 3

```csharp
Console.WriteLine(@"My value: [value]");
```

Again, this is a [verbatim string](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/verbatim) like in option 1.  The brackets `[]` are not used for interpolation in C#. Everything inside is printed exactly as written.

**Output:**
```cmd
My value: [value]
```

{{< awesome fa-regular fa-circle-xmark >}} Incorrect – this does not use interpolation.
{.text-danger .mb-4 .fw-bold}