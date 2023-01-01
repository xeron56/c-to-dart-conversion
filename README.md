# c-to-dart-conversion
Welcome to the C to Dart conversion repository! This project aims to provide tools and resources for converting C code to Dart, making it easier for developers to port their C code to the Dart ecosystem.Our goal is to make it as easy as possible for developers to convert their C code to Dart. We've created a suite of tools and resources to automate the process and handle the heavy lifting for you. These tools include scripts, libraries, and documentation that will guide you through the conversion process step by step.







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
