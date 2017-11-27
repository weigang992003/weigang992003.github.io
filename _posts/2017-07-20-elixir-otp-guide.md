---
layout: post
title:  "the little elixir otp guide"
date:   2017-07-22 11:10:00
categories: tech
---

Elixir describes itself as a functional, meta-programming-avare language
build on top of the Erlang virtual machine. Let's take this definition
apart piece by piece.

Elixir is a funciton programming language. This means it has all the
usual features you expect, such as immutalbe state, higher-order
functions, lazy evaluation, and pattern matching. You'll meet all of
these fatures and more in later chapters.

Elixir is also a meta-programmable language. Meta-programming involves
code that generates code (black magic, if you will). This is possible
because code can be represented as data, and data can be represented as
code. These facilities enable the programmer to add to the language new
constructs (among other things) that other languages find difficult or
even downright impossible.

This book is also about OTP, a framework to build fault-tolerant,
scalable, distributed applications. It's important to recognize that
Elixir essentially gains OTP for free because OTP comes as part of the
Erlang distribution. Unlike most frameworks, OTP comes packaged with a
lot of good stuff, including three kinds of databases, a set of
debugging tools, profilers, a test framework, and much more. Although we
only manage to play with a tiny subset, this book will give you a taste
of the pure awesomeness of OTP.

Why would you want to use Elixir instead of Erlang? There are at least
two reasons:the tooling and ecosystem.

What is Elixir/OTP good for?

Chat servers, Game Servers, web frameworks, distributed dataases,
real-time bidding servers, video-streamservers, long-running, 
