---
title: "Konversi Tipe Data di Go"
date: 2023-01-10T00:00:00+00:00
# weight: 1
# aliases: ["/first"]
tags: ["go", "golang", "konversi tipe data", "casting", "strconv"]
author: "Rendy"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Ingin tahu cara mengubah tipe data di Go? Artikel ini akan membahas cara konversi tipe data di Go, mulai dari cara casting hingga menggunakan library strconv. Juga akan dijelaskan perhatian yang perlu diperhatikan saat melakukan konversi tipe data. Cek artikel ini untuk mempelajari lebih lanjut!"
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

# Konversi Tipe Data di Go
Go merupakan bahasa pemrograman yang type-safe, sehingga kita harus memastikan tipe data dari suatu variabel sesuai dengan tipe data yang diinginkan sebelum melakukan operasi terhadap variabel tersebut. Kadangkala, kita perlu mengubah tipe data suatu variabel agar sesuai dengan kebutuhan kita. Cara untuk mengubah tipe data suatu variabel disebut dengan _konversi tipe data_.

## Cara mengubah tipe data
Untuk mengubah tipe data suatu variabel, kita bisa menggunakan syntax `TipeBaru(variabel)`. Contohnya:
```go
package main

import "fmt"

func main() {
	var x int = 10
	var y float64 = float64(x) // mengubah tipe data int ke float64

	fmt.Println(y) // Output: 10.0
}
```
Di dalam contoh di atas, kita mengubah tipe data `x` yang semula bertipe `int` menjadi `float64`. Syntax `float64(x)` akan mengubah tipe data `x` menjadi `float64`.

## Casting
Casting adalah proses mengubah tipe data suatu variabel secara _eksplisit_. Ada dua jenis casting yang dapat dilakukan di Go, yaitu casting dari tipe data yang lebih kecil ke tipe data yang lebih besar, dan casting dari tipe data yang lebih besar ke tipe data yang lebih kecil.

### Casting dari tipe data yang lebih kecil ke tipe data yang lebih besar
Untuk casting dari tipe data yang lebih kecil ke tipe data yang lebih besar, kita bisa menggunakan syntax `TipeBaru(variabel)`. Contohnya:
```go
package main

import "fmt"

func main() {
	var x int8 = 10
	var y int32 = int32(x) // mengubah tipe data int8 ke int32

	fmt.Println(y) // Output: 10
}
```
Di dalam contoh di atas, kita mengubah tipe data `x` yang semula bertipe `int8` menjadi `int32`. Syntax `int32(x)` akan mengubah tipe data x menjadi int32.

### Casting dari tipe data yang lebih besar ke tipe data yang lebih kecil
Dalam Go, Anda dapat melakukan casting tipe data yang lebih besar ke tipe data yang lebih kecil dengan menggunakan syntax seperti di bawah ini:

```go
package main

import "fmt"

func main() {
	var x float64 = 10.5
	var y int8 = int8(x)

	fmt.Println(y) // Output: 10
}
```
Pada contoh di atas, kita mengkonversi tipe data `float64` (angka pecahan) ke tipe data `int8` (angka bulat kecil) dengan menggunakan casting. Nilai `10.5` akan dikonversi menjadi `10` karena `int8` hanya dapat menyimpan nilai bulat.

## Menggunakan library `strconv`
Library `strconv` merupakan library bawaan di golang yang berguna untuk melakukan konversi tipe data dari `string` ke tipe data lainnya, seperti `int`, `float`, dan lain-lain. Berikut adalah contoh penggunaannya:
```go
package main

import (
	"fmt"
	"strconv"
)

func main() {
	// convert string to int
	i, err := strconv.Atoi("42")
	if err != nil {
		fmt.Println(err)
	}
	fmt.Println(i)

	// convert string to float
	f, err := strconv.ParseFloat("3.14", 64)
	if err != nil {
		fmt.Println(err)
	}
	fmt.Println(f)
}
```
Output:
```markdown
42
3.14
```
Selain Atoi dan ParseFloat, ada juga beberapa fungsi lain yang bisa digunakan di library strconv, seperti ParseInt, ParseUint, dan lain-lain. Silakan cek dokumentasi resmi di https://golang.org/pkg/strconv/ untuk informasi lebih lengkap.
