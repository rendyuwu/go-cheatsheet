---
title: "Slice di Go"
date: 2023-01-01T00:00:00+00:00
# weight: 1
# aliases: ["/first"]
tags: ["go", "golang", "slice"]
author: "Rendy"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Slice adalah tipe data yang mirip dengan array, namun lebih fleksibel dalam hal ukuran. Slice menyimpan referensi ke elemen-elemen dalam array, sehingga Anda dapat mengubah elemen dalam array melalui slice dan sebaliknya."
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

# Apa itu Slice?
Slice adalah tipe data yang mirip dengan `array`, namun lebih fleksibel dalam hal ukuran. `Slice` menyimpan referensi ke elemen-elemen dalam `array`, sehingga Anda dapat mengubah elemen dalam array melalui `slice` dan sebaliknya.

## Pembuatan Slice

### Membuat Slice dari Array

Anda dapat membuat `slice` dari `array` dengan menentukan indeks awal dan akhir dari `slice` yang ingin Anda buat. Contohnya:
```go
a := [5]int{1, 2, 3, 4, 5}
b := a[1:3]
```
Ini akan membuat sebuah `slice b` yang berisi elemen a[1] dan a[2] dari `array a`.

Cara lainnya seperti table berikut

| **Membuat slice** | **Keterangan**                                                                    |
|-------------------|-----------------------------------------------------------------------------------|
| array[low:high]   | Membuat slice dari array dimulai dari index low sampai index sebelum high         |
| array[low:]       | 	Membuat slice dari array dimulai dari index low sampai index terakhir pada array |
| array[:high]	     | Membuat slice dari array dimulai dari index 0 sampai index sebelum high           |
| array[:]	         | Membuat slice dari array dimulai dari index 0 sampai index terakhir pada array    |

### Membuat Slice Menggunakan Make
Anda juga dapat membuat `slice` menggunakan built-in function `make()`. Contohnya:
```go
c := make([]int, 5)
```

Ini akan membuat sebuah `slice c` yang berisi 5 elemen yang diinisialisasi dengan 0. Anda juga dapat memberikan kapasitas awal pada saat pembuatan `slice` dengan cara seperti ini:
```go
d := make([]int, 5, 10)
```
Ini akan membuat sebuah `slice d` yang berisi 5 elemen yang diinisialisasi dengan 0 dan memiliki kapasitas 10.

### Memberikan Nilai Awal pada Pembuatan Slice
Anda juga dapat memberikan nilai awal pada saat pembuatan `slice` dengan cara seperti ini:
```go
e := []int{1, 2, 3, 4, 5}
```
Ini akan membuat sebuah `slice e` yang berisi 5 elemen dan masing-masing elemen diisi dengan nilai 1, 2, 3, 4, 5.

## Akses Elemen Slice
Setelah Anda membuat `slice`, Anda dapat mengakses elemen dalam `slice` menggunakan indeks. Indeks dimulai dari 0, sehingga jika Anda ingin mengakses elemen pertama dalam `slice`, Anda dapat menggunakan indeks 0.

### Mengakses Elemen Slice
Untuk mengakses elemen dalam `slice`, gunakan sintaks seperti ini:
```go
fmt.Println(b[1]) // will print 2
```

### Mengubah Nilai Elemen Slice
Anda juga dapat mengubah nilai elemen dalam `slice` dengan cara yang sama:
```go
b[1] = 10
fmt.Println(b) // will print [1, 10, 3, 4, 5]
```
Perlu diingat bahwa jika Anda mengubah elemen dalam `slice`, itu juga akan berpengaruh pada array yang digunakan untuk membuat `slice` tersebut. Karena `slice` merupakan referensi dari array, jika Anda mengubah elemen dalam `slice`, maka elemen yang sama dalam array juga akan berubah.

## Iterasi Slice
Anda dapat melakukan iterasi pada `slice` dengan menggunakan perulangan `for` atau dengan menggunakan `range`.

### Iterasi Menggunakan For
Untuk iterasi menggunakan `for`, gunakan sintaks seperti ini:
```go
for i := 0; i < len(b); i++ {
    fmt.Println(b[i])
}
```
Ini akan mencetak setiap elemen dalam `slice b`.

### Iterasi Menggunakan Range
Anda juga dapat menggunakan `range` untuk melakukan iterasi pada `slice` seperti ini:
```go
for i, v := range b {
    fmt.Println("index:", i, "value:", v)
}
```

Ini akan mencetak indeks dan nilai setiap elemen dalam `slice b`.

## Fitur Tambahan Slice
Slice memiliki beberapa fitur tambahan yang sangat berguna dalam pengembangan aplikasi Go, diantaranya:

| **Operasi**                      | **Keterangan**                                                                                                       |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------|
| len(slice)	                      | Untuk mendapatkan panjang slice                                                                                      |
| cap(skice)	                      | Untuk mendapatkan kapasitas slice                                                                                    |
| append(slice, data)              | Membuat slice baru dengan menambahkan data pada posisi terakhir slice, jika array penuh maka akan membuat array baru |
| make([]string, length, capacity) | Membuat slice baru                                                                                                   |
| copy(destination, source)        | Menyalin slice dari source ke destination                                                                            |





