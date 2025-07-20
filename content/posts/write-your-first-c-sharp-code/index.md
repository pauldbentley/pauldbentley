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

The Console class provides two similar sounding methods: Write() and WriteLine().  This challenge helps you to understand the differences between them.

<!--more-->

## Question

> What is the difference between `Console.Write` and `Console.WriteLine`?

Try to answer this question first on [freeCodeCamp](https://www.freecodecamp.org/learn/foundational-c-sharp-with-microsoft/write-your-first-code-using-c-sharp/write-your-first-c-sharp-code).

## What do the docs say?
At first glance, both methods sounds like they are going to write output to the console, with a new line or not.  So what's the actual difference? Let’s consult the documentation:

The [documentation for the Write method](https://learn.microsoft.com/en-us/dotnet/api/system.console.write?view=net-9.0#system-console-write(system-string)) says:

> Writes the specified string value to the standard output stream.

The [documentation for the WriteLine method](https://learn.microsoft.com/en-us/dotnet/api/system.console.writeline?view=net-9.0#system-console-writeline(system-string)) says:

> Writes the specified string value, followed by the current line terminator, to the standard output stream.

So the key difference is clear: `WriteLine()` appends a new line after printing, while `Write()` does not.

## Option 1

> `Console.Write` prints the output on a new line.

The documentation does not mention adding a new line for this method.

{{< awesome fa-regular fa-circle-xmark >}} This is incorrect.
{.text-danger .mb-4 .fw-bold}

## Option 2

> `Console.WriteLine` prints the output on a new line.

This is close, but it actually appends the line terminator _after_ the output.

{{< awesome fa-regular fa-circle-xmark >}} This is incorrect.
{.text-danger .mb-4 .fw-bold}

## Option 3

> `Console.WriteLine` appends a new line after the output.

This matches exactly what the documentation states.

{{< awesome fa-regular fa-circle-check >}} This is the correct answer.
{.text-success .mb-4 .fw-bold}

## Thoughts

This example demonstrates an important coding principal; "**Make the Implicit, Explicit**".

The C# team could have overloaded the `Console.Write()` with an optional `bool` parameter to control whether a newline should be added. Internally, the method could then decide whether to append a line terminator based on that value.

However, this approach would increase the [cyclomatic complexity](https://en.wikipedia.org/wiki/Cyclomatic_complexity), making it harder to maintain.  Since `Console.Write()` already has many overloads, introducing a flag would effectively double them.  It would also make it less clear to developers how to output text with or without a new line, forcing them to dig into overloads or documentation.

By having two distinct methods the intent remains obvious. This separation helps keep the language clean and the API intuitive.