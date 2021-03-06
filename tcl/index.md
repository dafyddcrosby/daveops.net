---
title: Tcl
---

Syntax cheatsheet
-----------------

```tcl

 if {blah == 0} {
 # blah
 } elseif {blah == 1} {
 # blah!
 } else {
 # blah?
 }
 
 switch xyz {
 a
-  #drop into next block
 b {
 format 1
 }
 default {
 format 3
 }
 }   # returns 3
 
 set false 0
 set true 1
```

Namespaces
----------

```tcl
 
 namespace eval blah {}
```

Profiling statements
--------------------

```tcl

 puts "unbraced: [time { expr 15 * 20 } 1000]"
 puts "braced:   [time { expr {15 * 20} } 1000]"

```

Disassemble statement
---------------------

This is fun, because it shows just how much of a difference there is in optimizing statements

```tcl

 ::tcl::unsupported::disassemble script {expr $a eq $b}
 ::tcl::unsupported::disassemble script {expr {$a eq $b}}
```

Creating tests
--------------

```tcl

 package require tcltest
 namespace import ::tcltest::*
 
 # Software under test
 source sum.tcl
 
 test sum_addTwoZerosExpectZero {
 Test: [sum 0 0] == 0
 } -body {
 sum 0 0
 } -result 0
 
 test sum_addTwoPositiveNumbers {} -body {
 sum 4 9
 } -result 13
 
 test sum_addPositiveToNegative {} -body {
 sum -95 72
 } -result -23
 
 cleanupTests
```
