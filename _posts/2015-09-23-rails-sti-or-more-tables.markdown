---
layout: post
title:  "Rails STI vs additional DB tables"
date:   2015-09-23 17:48:45
categories: ruby-on-rails sti
---
According to wikipedia **STI** is _"a way to emulate object-oriented inheritance in a relational database"_. In my project (SaaS shop platform) I have the entity named "widgets", which stands for simple and isolated piece of shop. Pretty abstract, huh? Anything can be a widget, really. So, I need a way to implement _n_ widgets (n > 5), what path should I go?

## STI road

### STI principle

The first thought that I had was STI. STI works pretty simple in Rails: suppose you have a model `Animal`, which has two children: `Animal::Cat` and `Animal::Dog`. You create table `animals` and include `type` column. Then, after you call `Cat.create(name: 'Kitty')` you will get new record in the database:

`animals` table:

| type        | name  |
| ----------- | ----- |
| Animal::Cat | Kitty |

<br/>
Quite simple.

### Back to widgets

## New tables highway
