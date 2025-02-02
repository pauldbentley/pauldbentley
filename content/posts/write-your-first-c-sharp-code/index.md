---
title: 'Write Your First C# Code'
date: 2024-12-15T10:00:00-07:00
draft: false
categories:
    - Coding
tags:
    - csharp
    - freecodecamp-csharp
---

The console class has a Write() and WriteLine() method, this challengs helps to understand the differences between them.

<!--more-->

## Question

> What is the difference between `Console.Write` and `Console.WriteLine`?

Complete this challenge on [freeCodeCamp](https://www.freecodecamp.org/learn/foundational-c-sharp-with-microsoft/write-your-first-code-using-c-sharp/write-your-first-c-sharp-code).

## What do the docs say?
These methods sound like they are going to write a value to the console, potentially on a new line. Let's have a look at the documentation so see if we can find the differences.

The [documentation for the Write method](https://learn.microsoft.com/en-us/dotnet/api/system.console.write?view=net-9.0#system-console-write(system-string)) says:

> Writes the specified string value to the standard output stream.

The [documentation for the WriteLine method](https://learn.microsoft.com/en-us/dotnet/api/system.console.writeline?view=net-9.0#system-console-writeline(system-string)) says:

> Writes the specified string value, followed by the current line terminator, to the standard output stream.

So the difference looks to be if a new line is added after the value has been written to the console or not.

## Option 1

> `Console.Write` prints the output on a new line.

The documentation doesn't say anything about new lines for the this method.

{{< awesome fa-regular fa-circle-xmark >}} This is incorrect.
{.text-danger .mb-4 .fw-bold}

## Option 2

> `Console.WriteLine` prints the output on a new line.

While the documentation does mention a line terminator, it says the content is output first, then the line terminator.

{{< awesome fa-regular fa-circle-xmark >}} This is incorrect.
{.text-danger .mb-4 .fw-bold}

## Option 3

> `Console.WriteLine` appends a new line after the output.

This is what the documentation says.

{{< awesome fa-regular fa-circle-check >}} This is correct.
{.text-success .mb-4 .fw-bold}

## Thoughts

This method is an example of an important coding principal; "Make the Implicit, Explicit".

The C# team could have added an overload to the `Console.Write` method with a `bool` parameter to control if the new line is appended or not.
Then inside the method there would be a check on this value to add the new line or not.

From a maintenance point of view, this would increase the [Cyclomatic complexity](https://en.wikipedia.org/wiki/Cyclomatic_complexity).
There are also many overloads to the write method, so this would double the number required.
From the developers point of view, it's not initially obvious how to write value with a new line without looking at the documentation for all the parameters.