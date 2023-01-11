---
title: "Cara Menggunakan Variabel di Go"
date: 2023-01-09T00:00:00+00:00
# weight: 1
# aliases: ["/first"]
tags: ["go", "golang", "variable", "konstanta", "tipe data"]
author: "Rendy"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Ingin belajar tentang variabel di Go? Artikel ini akan membahas tentang pengertian variabel, tipe data yang tersedia, serta cara membuat dan menggunakan variabel di Go. Ikuti tutorial ini dan mulailah belajar tentang variabel di Go sekarang juga!"
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

## Pengertian Variabel

Variabel adalah tempat penyimpanan sementara data di dalam memori komputer. Variabel di Go dapat digunakan untuk menyimpan berbagai tipe data seperti string, integer, dan lain-lain.

## Tipe Data di Go

| No  | Tipe       | Deskripsi                                  | Contoh Value                              |
|-----|------------|--------------------------------------------|-------------------------------------------|
| 1   | bool       | Boolean (true/false)                       | `true`, `false`                           |
| 2   | int        | Integer (bilangan bulat)                   | `10`, `-5`, `0`                           |
| 3   | int8       | Integer 8 bit                              | `10`, `-5`, `0`                           |
| 4   | int16      | Integer 16 bit                             | `10`, `-5`, `0`                           |
| 5   | int32      | Integer 32 bit                             | `10`, `-5`, `0`                           |
| 6   | int64      | Integer 64 bit                             | `10`, `-5`, `0`                           |
| 7   | uint       | Unsigned integer (bilangan bulat positif)  | `10`, `0`                                 |
| 8   | uint8      | Unsigned integer 8 bit                     | `10`, `0`                                 |
| 9   | uint16     | Unsigned integer 16 bit                    | `10`, `0`                                 |
| 10  | uint32     | Unsigned integer 32 bit                    | `10`, `0`                                 |
| 11  | uint64     | Unsigned integer 64 bit                    | `10`, `0`                                 |
| 12  | float32    | Floating point 32 bit                      | `10.5`, `-2.5`, `0.0`                     |
| 13  | float64    | Floating point 64 bit                      | `10.5`, `-2.5`, `0.0`                     |
| 14  | complex64  | Complex number (bilangan kompleks) 64 bit  | `10.5+5.5i`, `-2.5-5.5i`, `0.0+0.0i`      |
| 15  | complex128 | Complex number (bilangan kompleks) 128 bit | `10.5+5.5i`, `-2.5-5.5i`, `0.0+0.0i`      |
| 16  | string     | String (teks)                              | `"Hello World"`, `"Go is Fun"`, `"12345"` |

## Cara mendeklarasikan variabel di Go
### Menggunakan keyword var
Cara pertama yang dapat digunakan untuk mendeklarasikan variabel di Go adalah dengan menggunakan keyword `var`. Penulisan syntaxnya adalah sebagai berikut:

```go
var namaVariable tipeData = nilai
```

Contoh:
```go
var name string
name = "Rendy"
fmt.Println(name)

name = "Wijaya"
fmt.Println(name)
```
Dalam contoh di atas, kita mendeklarasikan variabel bernama name dengan tipe data string. Kemudian, kita memberikan nilai "Rendy" pada variabel name dan mencetak nilainya dengan menggunakan perintah Println dari package fmt. Kemudian, kita mengubah nilai dari variabel name menjadi "Wijaya" dan mencetak nilainya kembali dengan menggunakan perintah Println dari package fmt.

Hasil output dari program di atas akan menjadi:
```markdown
Rendy
Wijaya
```

### Menggunakan syntax shorthand
Cara kedua yang dapat digunakan untuk mendeklarasikan variabel di Go adalah dengan menggunakan syntax shorthand. Penulisan syntaxnya adalah sebagai berikut:

```go
namaVariable := nilai
```

Contoh:
```go
name := "Rendy"
fmt.Println(name)

name = "Wijaya"
fmt.Println(name)
```
Dalam contoh di atas, kita mendeklarasikan variabel bernama name dengan tipe data string menggunakan syntax shorthand. Kemudian, kita memberikan nilai "Rendy" pada variabel name dan mencetak nilainya dengan menggunakan perintah Println dari package fmt. Kemudian, kita mengubah nilai dari variabel name menjadi "Wijaya" dan mencetak nilainya kembali dengan menggunakan perintah Println dari package fmt.

Hasil output dari program di atas akan menjadi:

```markdown
Rendy
Wijaya
```
Syntax shorthand ini hanya bisa digunakan pada saat proses mendeklarasikan variabel, tidak bisa digunakan pada saat proses pemberian nilai pada variabel yang sudah dideklarasikan sebelumnya.

## Pengertian konstanta dan cara mendeklarasikan konstanta di Go
Konstanta adalah variabel yang nilainya tidak bisa diubah setelah dideklarasikan. Penggunaan konstanta sangat berguna ketika kita membutuhkan nilai yang tidak akan berubah dalam sebuah program, seperti nilai PI atau nilai konversi satuan.

Cara mendeklarasikan konstanta di Go adalah dengan menggunakan keyword const seperti berikut:
```go
const namaKonstanta = nilai
```
Contoh:
```go
const Pi = 3.14
fmt.Println(Pi)

// Mencoba merubah nilai Pi
Pi = 3.1415 // akan menyebabkan error karena Pi adalah konstanta
```

Dalam contoh di atas, kita mendeklarasikan konstanta bernama Pi dengan nilai 3.14. Kemudian, kita mencetak nilai dari konstanta Pi dengan menggunakan perintah Println dari package fmt. Jika kita mencoba merubah nilai dari konstanta Pi, maka akan terjadi error karena konstanta tidak bisa diubah setelah dideklarasikan.