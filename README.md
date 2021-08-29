# 🖍 Kokuban
Kokuban makes it easy to style strings on the terminal for .NET applications. 

It is based on JavaScript library [Chalk](https://github.com/chalk/chalk) for many of its concepts and some of its code. Kokuban means blackboard in Japanese.

## Features
- Expressive API
- Auto detects color support
- Auto enables escape sequence support on Windows 10 20H1 or later
- 256 (8-bit) / TrueColor (24-bit) colors support

## Install

```
dotnet package add Kokuban
```

## Usage

```csharp
using Kokuban;

// Use `+` operator.
Console.WriteLine(Chalk.Red + "Hello");
Console.WriteLine(Chalk.Red + ("Hello " + (Chalk.Underline.BgBlue + "World")) + "!");

// Use indexer.
Console.WriteLine(Chalk.Red.Underline["Hello"]);

// Use `ToStyledString` extension method.
Console.WriteLine("Foo Bar Baz".ToStyledString(Chalk.White.Blue));

// Use `Render` method.
Console.WriteLine(Chalk.Rgb(255, 128, 128).Render("Hello Konnichiwa!"));
```

## License

```
MIT License

Copyright (c) Mayuki Sawatari <mayuki@misuzilla.org>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---- 
Part of the source code of this library is derived from the following libraries.
The original source codes are licensed under the MIT License.

chalk/supports-color
Copyright (c) Sindre Sorhus <sindresorhus@gmail.com> (https://sindresorhus.com)

chalk/ansi-styles
Copyright (c) Sindre Sorhus <sindresorhus@gmail.com> (https://sindresorhus.com)

Qix-/color-convert
Copyright © 2011-2016, Heather Arthur. Copyright © 2016-2021, Josh Junon.
```