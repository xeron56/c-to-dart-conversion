
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

