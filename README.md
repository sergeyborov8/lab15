## Laboratory work XV

Данная лабораторная работа посвещена изучению инструментов статического и динамического анализа кода
```ShellSession
$ open http://cppcheck.sourceforge.net
```

## Tasks

- [x] 1. Ознакомиться со ссылками учебного материала
- [x] 2. Используя **cpplint** провести анализ проекта на **C++**
- [x] 3. Используя **Cppcheck** провести анализ проекта на **C++**
- [x] 4. Используя **OCLint** провести анализ проекта на **C++**
- [x] 5. Используя **Valgrind** провести анализ проекта на **C++**
- [x] 6. Составить отчет и отправить ссылку личным сообщением в **Slack**

```ShellSession
$ cpplint main.cpp
Done processing main.cpp
```
```ShellSession
$ cppcheck main.cpp
Checking main.cpp...
```
```ShellSession
$ oclint main.cpp
OCLint Report

Summary: TotalFiles=1 FilesWithViolations=0 P1=0 P2=0 P3=0


[OCLint (http://oclint.org) v0.13]
```
```ShellSession
$ valgrind --tool=memcheck g++ main.cpp -o output -std=c++11
==14915== Memcheck, a memory error detector
==14915== Copyright (C) 2002-2015, and GNU GPL'd, by Julian Seward et al.
==14915== Using Valgrind-3.11.0 and LibVEX; rerun with -h for copyright info
==14915== Command: g++ main.cpp -o output -std=c++11
==14915==
==14915==
==14915== HEAP SUMMARY:
==14915==     in use at exit: 152,798 bytes in 207 blocks
==14915==   total heap usage: 362 allocs, 155 frees, 174,800 bytes allocated
==14915==
==14915== LEAK SUMMARY:
==14915==    definitely lost: 35,514 bytes in 136 blocks
==14915==    indirectly lost: 82 bytes in 5 blocks
==14915==      possibly lost: 0 bytes in 0 blocks
==14915==    still reachable: 117,202 bytes in 66 blocks
==14915==         suppressed: 0 bytes in 0 blocks
==14915== Rerun with --leak-check=full to see details of leaked memory
==14915==
==14915== For counts of detected and suppressed errors, rerun with: -v
==14915== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)
```
## Links

- [Google C++ Style Guide](https://github.com/cpplint/cpplint)
- [Cppcheck Manual](http://cppcheck.sourceforge.net/manual.pdf)
- [Valgrind Quick Start Guide](http://valgrind.org/docs/manual/index.html)
- [OCLint Tutorial](http://docs.oclint.org/en/stable/intro/tutorial.html)

```
Copyright (c) 2017 Братья Вершинины
```
