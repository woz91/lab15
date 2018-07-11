# Лабораторная работа №15. Отчет.

## Задание на лабораторную работу:

- [x] 1. Ознакомиться со ссылками учебного материала
- [x] 2. Используя **cpplint** провести анализ проекта на **C++**
- [x] 3. Используя **Cppcheck** провести анализ проекта на **C++**
- [x] 4. Используя **OCLint** провести анализ проекта на **C++**
- [x] 5. Используя **Valgrind** провести анализ проекта на **C++**
- [x] 6. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Выполнение работы.
	
В соответствии с последовательностью, определенной заданием на лабораторную работу, были выполнены следующие действия:
- [X] Для успешного выполнения задания создан новый пустой репозиторий lab15 с лицензией MIT. Осуществлено копирование наполнение репозитория:

```ShellSession
$ export GITHUB_USERNAME=woz91
```

```ShellSession
$ git clone https://github.com/${GITHUB_USERNAME}/lab14 lab15
$ cd lab15
$ git remote remove origin
$ git remote add origin git@github.com:${GITHUB_USERNAME}/lab15
```

- [X] 1. Проведено ознакомление по приведенным ссылкам со следующими материалами по [Google C++ Style Guide](https://github.com/cpplint/cpplint), [Cppcheck Manual](http://cppcheck.sourceforge.net/manual.pdf), [Valgrind Quick Start Guide](http://valgrind.org/docs/manual/index.html), [OCLint Tutorial](http://docs.oclint.org/en/stable/intro/tutorial.html).
- [X] 2. С помощью инструмента **Cpplint** проведен анализ проекта:

```ShellSession
$ cpplint sources/demo.cpp
sources/demo.cpp:0:  No copyright message found.  You should have a line: "Copyright [year] <Copyright Owner>"  [legal/copyright] [5]
sources/demo.cpp:2:  Found C++ system header after other header. Should be: demo.h, c system, c++ system, other.  [build/include_order] [4]
sources/demo.cpp:6:  Tab found; better to use spaces  [whitespace/tab] [1]
sources/demo.cpp:7:  Tab found; better to use spaces  [whitespace/tab] [1]
sources/demo.cpp:8:  Missing space before ( in while(  [whitespace/parens] [5]
Done processing sources/demo.cpp
Total errors found: 5
```

- [X] 3. С помощью инструмента **Cppcheck** проведен анализ проекта:
```ShellSession
$ cppcheck --enable=all sources/demo.cppChecking sources/demo.cpp...
(information) Cppcheck cannot find all the include files (use --check-config for details)
```

- [ ] 4. С помощью инструмента **OCLint** проведен анализ проекта:
```ShellSession
```

- [X] 5. С помощью инструмента **Valgrind** проведен анализ проекта:
```ShellSession
$ valgrind --tool=memcheck ls -l
==5276== Memcheck, a memory error detector
==5276== Copyright (C) 2002-2015, and GNU GPL'd, by Julian Seward et al.
==5276== Using Valgrind-3.11.0 and LibVEX; rerun with -h for copyright info
==5276== Command: ls -l
==5276== 
итого 4
-rw-rw-r-- 1 vaulex vaulex 314 фев 13 19:25 demo.cpp
==5276== 
==5276== HEAP SUMMARY:
==5276==     in use at exit: 13,011 bytes in 8 blocks
==5276==   total heap usage: 236 allocs, 228 frees, 92,225 bytes allocated
==5276== 
==5276== LEAK SUMMARY:
==5276==    definitely lost: 0 bytes in 0 blocks
==5276==    indirectly lost: 0 bytes in 0 blocks
==5276==      possibly lost: 0 bytes in 0 blocks
==5276==    still reachable: 13,011 bytes in 8 blocks
==5276==         suppressed: 0 bytes in 0 blocks
==5276== Rerun with --leak-check=full to see details of leaked memory
==5276== 
==5276== For counts of detected and suppressed errors, rerun with: -v
==5276== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)

```

- [X] 6. Составлен отчет о работе в формате MD, ссылка отправлена в **slack**.

	
>## Выводы:

>В ходе проделанной работы проведено ознакомление с инструментами анализа кода проекта **Cpplint**, **Cppcheck**, **OCLint**, **Valgrind** на примере **demo.cpp**.
