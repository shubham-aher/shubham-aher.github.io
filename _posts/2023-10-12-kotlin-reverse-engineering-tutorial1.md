---
published: false
---
---
layout: post
title: Kotlin Reverse Engineering Tutorial#1: Study of Boolean Datatype Size
published: false
---

### Intro

In this blogpost we will see the basic disassembly of code generated for JVM bytecode from a compiled Kotlin class to understand how boolean data type is treated internally.   

Kotlin source code file (BooleanSize.kt) : 
```
package com.shubhamaher.hellokotlin

fun main() {
    var booleanTrue : Boolean = true
}
```

Generated bytecode disassembly in Intellij : 
```
// ================com/shubhamaher/hellokotlin/BooleanSizeKt.class =================
// class version 50.0 (50)
// access flags 0x31
public final class com/shubhamaher/hellokotlin/BooleanSizeKt {


  // access flags 0x19
  public final static main()V
   L0
    LINENUMBER 4 L0
    ICONST_1
    ISTORE 0
   L1
    LINENUMBER 5 L1
    RETURN
   L2
    LOCALVARIABLE booleanTrue Z L1 L2 0
    MAXSTACK = 1
    MAXLOCALS = 1

  // access flags 0x1009
  public static synthetic main([Ljava/lang/String;)V
    INVOKESTATIC com/shubhamaher/hellokotlin/BooleanSizeKt.main ()V
    RETURN
    MAXSTACK = 0
    MAXLOCALS = 1

  @Lkotlin/Metadata;(mv={1, 1, 15}, bv={1, 0, 3}, k=2, d1={"\u0000\u0008\n\u0000\n\u0002\u0010\u0002\n\u0000\u001a\u0006\u0010\u0000\u001a\u00020\u0001\u00a8\u0006\u0002"}, d2={"main", "", "hellokotlin"})
  // compiled from: BooleanSize.kt
}


// ================META-INF/hellokotlin.kotlin_module =================
,
com.shubhamaher.hellokotlin
BooleanSizeKt
```