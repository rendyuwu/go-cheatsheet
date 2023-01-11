---
title: "Type Declaration di Go"
date: 2023-01-10T00:00:00+00:00
# weight: 1
# aliases: ["/first"]
tags: ["first"]
author: "Rendy"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Desc Text."
#canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
image: "<image path/url>" # image path/url
alt: "<alt text>" # alt text
caption: "<text>" # display caption under cover
relative: false # when using page bundles set this to true
hidden: true # only hide on current single page
editPost:
#URL: "https://github.com/<gitlab user>/<repo name>/tree/<branch name>/<path to content>/"
Text: "Suggest Changes" # edit text
appendFilePath: true # to append file path to Edit link
---

# Type Declaration di Go
Type declaration adalah sebuah cara untuk mendeklarasikan tipe data baru di dalam bahasa pemrograman Go. Type declaration ini bisa digunakan untuk memberikan nama baru pada tipe data yang sudah ada di Go, atau juga bisa digunakan untuk membuat tipe data baru yang terdiri dari tipe data yang sudah ada di Go.

Type declaration ini sangat berguna ketika kita ingin menggunakan tipe data yang spesifik dan mudah dipahami oleh developer lain di dalam proyek yang sedang kita kerjakan. Selain itu, type declaration juga dapat membantu kita untuk mengelompokkan tipe data yang sama ke dalam satu kelompok tipe data yang lebih besar, sehingga kita bisa membuat kode yang lebih terstruktur dan mudah dipahami.

## Cara mendeklarasikan tipe data baru di Go
Untuk mendeklarasikan tipe data baru di Go, kita dapat menggunakan syntax `type`. Contohnya:
```go
type NamaTipeDataBaru TipeDataAsli
```
Contoh implementasinya:
```go
type Celcius float64
type Fahrenheit float64
```
Di sini, kita mendeklarasikan tipe data baru `Celcius` dan `Fahrenheit` dengan tipe data asli `float64`. Setelah ini, kita dapat menggunakan tipe data baru ini seperti tipe data aslinya. Misalnya, kita dapat menggunakan operator `+`, `-`, ataupun tipe data baru ini sebagai parameter atau return value dari suatu fungsi.

Perhatikan bahwa tipe data baru ini tidak merupakan tipe data asli yang ada di Go, tetapi hanya merupakan alias dari tipe data asli tersebut. Ini berguna jika kita ingin memberi label yang lebih semantik pada tipe data asli tersebut, sehingga lebih mudah dipahami oleh orang lain atau oleh kita sendiri.

## Perbedaan type declaration dengan type conversion di Go

Type declaration dan type conversion adalah dua cara yang digunakan untuk mengubah tipe data di Go. Namun, terdapat beberapa perbedaan antara kedua cara tersebut.

Type declaration digunakan untuk mendeklarasikan tipe data baru yang merupakan kombinasi dari tipe data yang sudah ada. Contohnya adalah mendeklarasikan tipe data baru bernama `Person` yang merupakan alias dari tipe data `string`.

Type conversion, di sisi lain, digunakan untuk mengubah tipe data suatu variabel menjadi tipe data lain. Contohnya adalah mengubah tipe data `int` menjadi tipe data `float64`.

Perbedaan lain antara type declaration dan type conversion adalah penggunaannya. Type declaration hanya dapat digunakan pada saat mendeklarasikan variabel, sedangkan type conversion dapat digunakan kapan saja.

Contoh penggunaan type declaration:
```go
package main

type Person string

var p Person
```
Contoh penggunaan type conversion:
```go
package main

var x int = 10
var y float64 = float64(x)
```


