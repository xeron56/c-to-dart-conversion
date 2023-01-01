# Programming Language Conversion to Dart
Welcome to the Programming Language Conversion to Dart repository! This project is dedicated to helping developers bring their code to the Dart ecosystem, no matter what language it was originally written in.

Whether you have code written in C, Java, Python, or any other language, we've got you covered. Our repository contains a variety of tools and resources for automating the conversion process and making it as seamless as possible.

Our conversion tools are designed to be user-friendly and easy to use, with detailed documentation to guide you through the process step by step. And if you run into any issues or have ideas for improving the repository, we have a welcoming community of contributors who are happy to help.

So if you're interested in bringing your code to the Dart ecosystem, check out the Programming Language Conversion to Dart repository. We think you'll find it to be a valuable resource for making the transition smoothly and efficiently


# c-to-dart-conversion
Welcome to the C to Dart conversion repository! This project aims to provide tools and resources for converting C code to Dart, making it easier for developers to port their C code to the Dart ecosystem.Our goal is to make it as easy as possible for developers to convert their C code to Dart. We've created a suite of tools and resources to automate the process and handle the heavy lifting for you. These tools include scripts, libraries, and documentation that will guide you through the conversion process step by step.

There are a few potential advantages to converting C code to Dart:

*Dart is a modern, object-oriented programming language that is designed to be scalable and easy to use. By converting your C code to Dart, you can take advantage of these features and potentially improve the maintainability and readability of your code.

*Dart is widely used in the development of mobile, desktop, and web applications. If you're looking to port your C code to one of these platforms, Dart may be a good choice.

*Dart has a large and active developer community, with many libraries and frameworks available to help you build powerful applications quickly. By converting your C code to Dart, you can tap into this community and potentially benefit from the contributions of others.

*Dart is natively supported by the Flutter framework, which is used for building cross-platform mobile applications. If you're interested in using your C code in a Flutter app, converting to Dart may be a good option.







| C | Dart | Example |
| --- | --- | --- |
| `int` | `int` | `int x = 10;` |
| `double` | `double` | `double x = 10.5;` |
| `char *` | `String` | `char *s = "Hello";` becomes `String s = "Hello";` |
| `char[]` | `List<int>` | `char s[] = "Hello";` becomes `List<int> s = [72, 101, 108, 108, 111];` |
| `struct` | `class` | `struct Point { int x, y; };` becomes `class Point { int x; int y; }` |
| `typedef` | `typedef` | `typedef int (*Func)(int);` becomes `typedef Func = int Function(int);` |
| `#define` | `const` or `final` | `#define PI 3.14` becomes `const double PI = 3.14;` |
| `if (cond) { ... } else { ... }` | `if (cond) { ... } else { ... }` | `if (x < 10) { ... } else { ... }` |
| `for (int i = 0; i < 10; i++) { ... }` | `for (int i = 0; i < 10; i++) { ... }` | `for (int i = 0; i < 10; i++) { ... }` |
| `while (cond) { ... }` | `while (cond) { ... }` | `while (x < 10) { ... }` |
| `do { ... } while (cond);` | `do { ... } while (cond);` | `do { ... } while (x < 10);` |
| `switch (x) { case 0: ... break; case 1: ... break; default: ... break; }` | `switch (x) { case 0: ... break; case 1: ... break; default: ... break; }` | `switch (x) { case 0: ... break; case 1: ... break; default: ... break; }` |
| `goto label;` | `continue` or `break` | `goto end;` becomes `break;` |





| C | Dart | Example |
| --- | --- | --- |
| `void function(int arg)` | `void function(int arg)` | `void foo(int x) { ... }` becomes `void foo(int x) { ... }` |
| `int function(void)` | `int function()` | `int foo() { return 10; }` becomes `int foo() { return 10; }` |
| `return value;` | `return value;` | `return 10;` |
| `int *ptr` | `Pointer<Int>` | `int *ptr;` becomes `Pointer<Int> ptr;` |
| `*ptr` | `ptr.value` | `*ptr = 10;` becomes `ptr.value = 10;` |
| `ptr->field` | `ptr.ref.field` | `ptr->x = 10;` becomes `ptr.ref.x = 10;` |
| `&var` | `Pointer.fromAddress(var.address)` | `&x` becomes `Pointer.fromAddress(x.address)` |
| `sizeof(type)` | `sizeOf<Type>()` | `sizeof(int)` becomes `sizeOf<Int>()` |




| C | Dart | Example |
| --- | --- | --- |
| `typedef struct { ... } Type;` | `class Type { ... }` | `typedef struct { int x, y; } Point;` becomes `class Point { int x; int y; }` |
| `enum { ... }` | `enum` | `enum { RED, GREEN, BLUE };` becomes `enum Color { RED, GREEN, BLUE }` |
| `#include <stdio.h>` | `import 'dart:ffi';` | `#include <stdio.h>` becomes `import 'dart:ffi';` |
| `printf("Hello, world!\n");` | `print("Hello, world!");` | `printf("Hello, world!\n");` becomes `print("Hello, world!");` |
| `malloc(size)` | `allocate<Type>(count)` | `malloc(sizeof(int))` becomes `allocate<Int>(1)` |
| `free(ptr)` | `free(ptr)` | `free(ptr)` |



| C | Dart | Example |
| --- | --- | --- |
| `FILE *fp = fopen("file.txt", "r");` | `RandomAccessFile fp = await RandomAccessFile.open("file.txt");` | `FILE *fp = fopen("file.txt", "r");` becomes `RandomAccessFile fp = await RandomAccessFile.open("file.txt");` |
| `fclose(fp);` | `fp.close();` | `fclose(fp);` becomes `fp.close();` |
| `fgets(str, n, fp);` | `fp.read(str.ptr, n);` | `fgets(str, n, fp);` becomes `fp.read(str.ptr, n);` |
| `fputs(str, fp);` | `fp.write(str.ptr);` | `fputs(str, fp);` becomes `fp.write(str.ptr);` |



| C | Dart | Example |
| --- | --- | --- |
| `#define MACRO(x) (x*x)` | `const macro = (x) => (x*x);` | `#define MACRO(x) (x*x)` becomes `const macro = (x) => (x*x);` |
| `#ifdef MACRO` | `#ifdef MACRO` | `#ifdef MACRO` |
| `#ifndef MACRO` | `#ifndef MACRO` | `#ifndef MACRO` |
| `#else` | `#else` | `#else` |
| `#endif` | `#endif` | `#endif` |
| `#error` | `#error` | `#error` |
| `#pragma` | `#pragma` | `#pragma` |



| C | Dart | Example |
| --- | --- | --- |
| `__FILE__` | `Platform.script.path` | `__FILE__` becomes `Platform.script.path` |
| `__LINE__` | `StackTrace.current.lineNumber` | `__LINE__` becomes `StackTrace.current.lineNumber` |
| `__func__` | `StackTrace.current.member` | `__func__` becomes `StackTrace.current.member` |
| `__DATE__` | `DateTime.now().toIso8601String()` | `__DATE__` becomes `DateTime.now().toIso8601String()` |
| `__TIME__` | `DateTime.now().toIso8601String()` | `__TIME__` becomes `DateTime.now().toIso8601String()` |



| C | Dart | Example |
| --- | --- | --- |
| `#include <stdlib.h>` | `import 'dart:math';` | `#include <stdlib.h>` becomes `import 'dart:math';` |
| `srand(time(NULL));` | `Random().seed = DateTime.now().microsecondsSinceEpoch;` | `srand(time(NULL));` becomes `Random().seed = DateTime.now().microsecondsSinceEpoch;` |
| `rand()` | `Random().nextInt(max);` | `rand()` becomes `Random().nextInt(max);` |
| `RAND_MAX` | `Random.secure().nextInt(max);` | `RAND_MAX` becomes `Random.secure().nextInt(max);` |



| C | Dart | Example |
| --- | --- | --- |
| `#include <setjmp.h>` | `import 'dart:io';` | `#include <setjmp.h>` becomes `import 'dart:io';` |
| `jmp_buf buf;` | `int buf;` | `jmp_buf buf;` becomes `int buf;` |
| `setjmp(buf);` | `buf = throw 'error';` | `setjmp(buf);` becomes `buf = throw 'error';` |
| `longjmp(buf, 1);` | `rethrow;` | `longjmp(buf, 1);` becomes `rethrow;` |
| `#include <assert.h>` | `import 'package:test/test.dart';` | `#include <assert.h>` becomes `import 'package:test/test.dart';` |
| `assert(cond);` | `expect(cond, isTrue);` | `assert(x > 0);` becomes `expect(x > 0, isTrue);` |
| `#include <math.h>` | `import 'dart:math';` | `#include <math.h>` becomes `import 'dart:math';` |
| `cos(x)` | `cos(x)` | `cos(x)` |
| `sin(x)` | `sin(x)` | `sin(x)` |
| `tan(x)` | `tan(x)` | `tan(x)` |
| `acos(x)` | `acos(x)` | `acos(x)` |



| C | Dart | Example |
| --- | --- | --- |
| `#include <ctype.h>` | `import 'dart:math';` | `#include <ctype.h>` becomes `import 'dart:math';` |
| `isalpha(c)` | `isAlpha(c)` | `isalpha(c)` becomes `isAlpha(c)` |
| `isdigit(c)` | `isDigit(c)` | `isdigit(c)` becomes `isDigit(c)` |
| `isspace(c)` | `isWhitespace(c)` | `isspace(c)` becomes `isWhitespace(c)` |
| `isupper(c)` | `isUpperCase(c)` | `isupper(c)` becomes `isUpperCase(c)` |
| `islower(c)` | `isLowerCase(c)` | `islower(c)` becomes `isLowerCase(c)` |
| `toupper(c)` | `toUpperCase(c)` | `toupper(c)` becomes `toUpperCase(c)` |
| `tolower(c)` | `toLowerCase(c)` | `tolower(c)` becomes `toLowerCase(c)` |
| `#include <string.h>` | `import 'dart:ffi';` | `#include <string.h>` becomes `import 'dart:ffi';` |
| `strlen(s)` | `s.length` | `strlen(s)` becomes `s.length` |



| C | Dart | Example |
| --- | --- | --- |
| `#include <stdarg.h>` | `import 'dart:ffi';` | `#include <stdarg.h>` becomes `import 'dart:ffi';` |
| `va_list args;` | `Pointer<NativeType> args;` | `va_list args;` becomes `Pointer<NativeType> args;` |
| `va_start(args, last);` | `args = va_start(args, last);` | `va_start(args, last);` becomes `args = va_start(args, last);` |
| `va_arg(args, type);` | `va_arg(args, type);` | `va_arg(args, type);` |
| `va_end(args);` | `va_end(args);` | `va_end(args);` |
| `#include <time.h>` | `import 'dart:ffi';` | `#include <time.h>` becomes `import 'dart:ffi';` |
| `time(NULL)` | `DateTime.now().millisecondsSinceEpoch` | `time(NULL)` becomes `DateTime.now().millisecondsSinceEpoch` |

# c++-to-dart-conversion

| C++ | Dart | Example |
| --- | --- | --- |
| `#include <iostream>` | `import 'dart:io';` | `#include <iostream>` becomes `import 'dart:io';` |
| `std::cout << "Hello, world!" << std::endl;` | `stdout.writeln("Hello, world!");` | `std::cout << "Hello, world!" << std::endl;` becomes `stdout.writeln("Hello, world!");` |
| `std::cin >> x;` | `stdin.readLineSync()` | `std::cin >> x;` becomes `stdin.readLineSync()` |
| `#include <string>` | `import 'dart:ffi';` | `#include <string>` becomes `import 'dart:ffi';` |
| `std::string s;` | `String s;` | `std::string s;` becomes `String s;` |
| `s.length()` | `s.length` | `s.length()` becomes `s.length` |
| `s.substr(pos, len)` | `s.substring(pos, len)` | `s.substr(pos, len)` becomes `s.substring(pos, len)` |
| `#include <vector>` | `import 'package:collection/collection.dart';` | `#include <vector>` becomes `import 'package:collection/collection.dart';` |
| `std::vector<int> v;` | `List<int> v;` | `std::vector<int> v;` becomes `List<int> v;` |
| `v.push_back(x);` | `v.add(x);` | `v.push_back(x);` becomes `v.add(x);` |



| C++ | Dart | Example |
| --- | --- | --- |
| `#include <algorithm>` | `import 'package:collection/collection.dart';` | `#include <algorithm>` becomes `import 'package:collection/collection.dart';` |
| `std::sort(v.begin(), v.end());` | `v.sort();` | `std::sort(v.begin(), v.end());` becomes `v.sort();` |
| `std::reverse(v.begin(), v.end());` | `v = v.reversed.toList();` | `std::reverse(v.begin(), v.end());` becomes `v = v.reversed.toList();` |
| `std::max_element(v.begin(), v.end());` | `v.reduce(max);` | `std::max_element(v.begin(), v.end());` becomes `v.reduce(max);` |
| `std::min_element(v.begin(), v.end());` | `v.reduce(min);` | `std::min_element(v.begin(), v.end());` becomes `v.reduce(min);` |
| `std::unique(v.begin(), v.end());` | `v.toSet().toList();` | `std::unique(v.begin(), v.end());` becomes `v.toSet().toList();` |
| `std::swap(a, b);` | `a = a + b; b = a - b; a = a - b;` | `std::swap(a, b);` becomes \` |



| C++ | Dart | Example |
| --- | --- | --- |
| `#include <array>` | `import 'package:collection/collection.dart';` | `#include <array>` becomes `import 'package:collection/collection.dart';` |
| `std::array<int, 3> a = {1, 2, 3};` | `List<int> a = [1, 2, 3];` | `std::array<int, 3> a = {1, 2, 3};` becomes `List<int> a = [1, 2, 3];` |
| `a.front()` | `a.first` | `a.front()` becomes `a.first` |
| `a.back()` | `a.last` | `a.back()` becomes `a.last` |
| `a.fill(x);` | `a.fillRange(0, a.length, x);` | `a.fill(x);` becomes `a.fillRange(0, a.length, x);` |
| `#include <deque>` | `import 'package:collection/collection.dart';`



| C++ | Dart | Example |
| --- | --- | --- |
| `#include <deque>` | `import 'package:collection/collection.dart';` | `#include <deque>` becomes `import 'package:collection/collection.dart';` |
| `std::deque<int> d;` | `ListQueue<int> d;` | `std::deque<int> d;` becomes `ListQueue<int> d;` |
| `d.push_back(x);` | `d.add(x);` | `d.push_back(x);` becomes `d.add(x);` |
| `d.push_front(x);` | `d.addFirst(x);` | `d.push_front(x);` becomes `d.addFirst(x);` |
| `d.pop_back();` | `d.removeLast();` | `d.pop_back();` becomes `d.removeLast();` |
| `d.pop_front();` | `d.removeFirst();` | `d.pop_front();` becomes `d.removeFirst();` |
| `d.front()` | `d.first` | `d.front()` becomes `d.first` |
| `d.back()` | `d.last` | `d.back()` becomes `d.last` |
| `#include <forward_list>` | `import 'package:collection/collection.dart';` | `#include <forward_list>` becomes `import 'package:collection/collection.dart';` |
| `std::forward_list<int> fl;` | `SplayTreeSet<int> fl;` | `std::forward_list<int> fl;` becomes `SplayTreeSet<int> fl;` |
| `fl.push_front(x);` | `fl.add(x);` | `fl.push_front(x);` becomes `fl.add(x);` |
| `fl.pop_front();` | \`fl.remove(fl.first); |  | 




| C++ | Dart | Example |
| --- | --- | --- |
| `#include <map>` | `import 'package:collection/collection.dart';` | `#include <map>` becomes `import 'package:collection/collection.dart';` |
| `std::map<std::string, int> m;` | `Map<String, int> m;` | `std::map<std::string, int> m;` becomes `Map<String, int> m;` |
| `m["key"] = value;` | `m["key"] = value;` | `m["key"] = value;` |
| `m.at("key")` | `m["key"]` | `m.at("key")` becomes `m["key"]` |
| `m.count("key")` | `m.containsKey("key")` | `m.count("key")` becomes `m.containsKey("key")` |
| `m.erase("key");` | `m.remove("key");` | `m.erase("key");` becomes `m.remove("key");` |
| `#include <unordered_map>` | `import 'package:collection/collection.dart';` | `#include <unordered_map>` becomes `import 'package:collection/collection.dart';` |
| `std::unordered_map<std::string, int> um;` | `Map<String, int> um;` | `std::unordered_map<std::string, int> um;` becomes `Map<String, int> um;` |
| `um["key"] = value;` | `um["key"] = value;` | `um["key"] = value;` |
| `um.at("key")` | `um["key"]` |  |
