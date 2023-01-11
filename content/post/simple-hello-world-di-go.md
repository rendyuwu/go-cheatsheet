---
title: "Simple Hello World di Go"
date: 2023-01-09T00:00:00+00:00
# weight: 1
# aliases: ["/first"]
tags: ["go", "golang", "cheatsheet", "install go", "hello world"]
author: "Rendy"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Artikel ini akan mengajarkan Anda cara menginstall Go, membuat file program Go, dan menjalankan program Hello World"
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

# Simple Hello World di Go

Ingin belajar Go dengan mudah? Mulailah dengan membuat program sederhana "Hello World"! Artikel ini akan mengajarkan Anda cara menginstall Go, membuat file program Go, dan menjalankan program "Hello World" di Go. Ikuti langkah-langkah di artikel ini dan mulailah belajar Go sekarang juga!

## Instalasi Go

Sebelum memulai, pastikan Go sudah terinstall di sistem operasi Anda. Jika belum, ikuti langkah-langkah di bawah ini untuk menginstall Go:

1. Buka [halaman download Go](https://go.dev/dl/) dan pilih versi Go yang sesuai dengan sistem operasi Anda.
2. Ikuti instruksi yang diberikan untuk menginstall Go di sistem operasi Anda.
3. Pastikan Go telah terinstall dengan menjalankan perintah `go version` di terminal atau command prompt. Contoh: `$ go version`
   Jika Go telah terinstall dengan benar, maka akan muncul informasi versi Go yang terinstall.
```shell
$ go version
go version go1.19 linux/amd64
```

## Membuat File Program Go

1. Buka text editor pilihan Anda.
2. Buat file baru dengan ekstensi `.go`. Contoh: `hello.go`.
3. Ketik kode Go di dalam file tersebut.
4. Simpan file tersebut.

Perhatikan bahwa nama file harus sesuai dengan nama package yang terdapat di dalamnya. Jika Anda tidak menggunakan package, maka nama file boleh sesuka hati.

## Membuat Program "Hello World"

Untuk membuat program "Hello World" di Go, ikuti langkah-langkah di bawah ini:

1. Buka file program Go yang telah Anda buat di tahap sebelumnya.
2. Ketik kode di bawah ini di dalam file tersebut:
```go
package main

import "fmt"

func main() {
fmt.Println("Hello World")
}
```

3. Simpan file tersebut.

Program "Hello World" di Go telah selesai dibuat. Selanjutnya, Anda dapat menjalankan program tersebut dengan mengikuti langkah-langkah di tahap selanjutnya.

## Menjalankan Program "Hello World"

Untuk menjalankan program Go yang telah Anda buat di tahap sebelumnya, ikuti langkah-langkah di bawah ini:

1. Buka terminal atau command prompt.
2. Arahkan ke direktori tempat file program Go Anda disimpan.
3. Jalankan perintah `go run` seperti ini: `$ go run nama_file.go`. Contoh: `$ go run hello.go`
   Pastikan menggunakan nama file yang sesuai dengan yang telah Anda buat di tahap sebelumnya.
4. Program Go akan dijalankan dan hasilnya akan ditampilkan di console.
```shell
$ go run hello.go
Hello World
```

## Mem-build dan Menjalankan Hasil Binary Program Go

Untuk mem-build dan menjalankan hasil binary program Go, ikuti langkah-langkah di bawah ini:

1. Buka terminal atau command prompt.
2. Arahkan ke direktori tempat file program Go Anda disimpan.
3. Jalankan perintah `go build` seperti ini: `$ go build nama_file.go`. Contoh: `$ go build hello.go`
   Perintah ini akan mem-build file program Go Anda menjadi sebuah binary.
4. Setelah proses build selesai, Anda dapat menjalankan binary tersebut dengan perintah `./nama_binary`. Contoh: `$ ./hello`

Program Go akan dijalankan dan hasilnya akan ditampilkan di console.
```shell
$ ./hello
Hello World
```