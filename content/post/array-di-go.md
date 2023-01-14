---
title: "Array di Go"
date: 2023-01-14T00:00:00+00:00
# weight: 1
# aliases: ["/first"]
tags: ["go", "golang", "array"]
author: "Rendy"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Array adalah tipe data yang menyimpan sekumpulan elemen yang memiliki tipe yang sama. Dalam Go, Anda dapat membuat array dengan menentukan tipe elemen dan jumlah elemen dalam array."
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

# Pembuatan Array
Array adalah tipe data yang menyimpan sekumpulan elemen yang memiliki tipe yang sama. Dalam Go, Anda dapat membuat array dengan menentukan tipe elemen dan jumlah elemen dalam array.

## Membuat Array
Untuk membuat array dengan jumlah elemen tertentu, gunakan sintaks seperti ini:

```go
package main

func main() {
	var a [5]int
}
```
Ini akan membuat array dengan 5 elemen yang semuanya diinisialisasi dengan 0.

## Memberikan Nilai Awal pada Pembuatan Array
Anda juga dapat memberikan nilai awal pada saat pembuatan array dengan cara seperti ini:
```go
package main

func main() {
	b := [5]int{1, 2, 3, 4, 5}
}
```

## Penggunaan Tanda "..." dalam Pembuatan Array
Anda juga dapat menentukan jumlah elemen dalam array dengan menggunakan tanda "..." seperti ini:
```go
package main

func main() {
	c := [...]int{1, 2, 3, 4, 5}
}
```
Ini akan membuat sebuah array c dengan 5 elemen dan masing-masing elemen diisi dengan nilai 1, 2, 3, 4, 5. Anda tidak perlu menentukan jumlah elemen secara eksplisit seperti yang dilakukan dalam contoh sebelumnya, yaitu var a [5]int.

Penggunaan "..." pada saat pembuatan array sangat membantu ketika Anda tidak tahu jumlah elemen yang akan digunakan dalam array tersebut sehingga dapat membuat kode Anda lebih fleksibel. Namun, perlu diingat bahwa Anda hanya dapat menggunakan tanda "..." pada saat pembuatan array dan tidak dapat digunakan saat mengubah atau menambah elemen pada array yang sudah dibuat.

# Akses Elemen Array

Setelah Anda membuat array, Anda dapat mengakses elemen dalam array menggunakan indeks. Indeks dimulai dari 0, sehingga jika Anda ingin mengakses elemen pertama dalam array, Anda dapat menggunakan indeks 0.

## Mengakses Elemen Array
Untuk mengakses elemen dalam array, gunakan sintaks seperti ini:
```go
package main

import "fmt"

func main() {
	fmt.Println(b[1]) // will print 2
}
```

## Mengubah Nilai Elemen Array
Anda juga dapat mengubah nilai elemen dalam array dengan cara yang sama:
```go
package main

import "fmt"

func main() {
	b[1] = 10
	fmt.Println(b) // will print [1, 10, 3, 4, 5]
}
```

# Iterasi Array
Anda dapat melakukan iterasi pada array dengan menggunakan perulangan `for` atau dengan menggunakan `range`.

## Iterasi Menggunakan For
Untuk iterasi menggunakan for, gunakan sintaks seperti ini:
```go
package main

import "fmt"

func main() {
	for i := 0; i < len(b); i++ {
		fmt.Println(b[i])
	}
}
```
Ini akan mencetak setiap elemen dalam array `b`.

## Iterasi Menggunakan Range
Anda juga dapat menggunakan range untuk melakukan iterasi pada array seperti ini:
```go
package main

import "fmt"

func main() {
	for i, v := range b {
		fmt.Println("index:", i, "value:", v)
	}
}
```
Ini akan mencetak indeks dan nilai setiap elemen dalam array `b`.


