# Array, Slice, Map

- [Array, Slice, Map](#array-slice-map)
- [Array](#array)
  - [Membuat Array](#membuat-array)
  - [Mengisi Array Melebihi Kapasitas](#mengisi-array-melebihi-kapasitas)
  - [Inisialisasi Nilai Awal Array](#inisialisasi-nilai-awal-array)
    - [Gaya Horizontal](#gaya-horizontal)
    - [Gaya Vertikal](#gaya-vertikal)
  - [Inisialisasi Nilai Awal Array Tanpa Jumlah Element](#inisialisasi-nilai-awal-array-tanpa-jumlah-element)
  - [Array Multidimensi](#array-multidimensi)
  - [Perulangan Array Menggunakan for](#perulangan-array-menggunakan-for)
  - [Perulangan Array Menggunakan for range](#perulangan-array-menggunakan-for-range)
- [Slice](#slice)
- [Map](#map)


## Array
**Array** adalah sekumpulan data dengan jenis / tipe data yang sama yang disimpan dalam sebuah variable. Array memiliki kapasitas yang nilainya telah ditentukan saat pembuatan. setiap element array memiliki nilai awal yang berbeda tergantung dari tipe datanya, jika `bool` maka nilai awalnya `false` jika `int` makan nilai awalnya `0.

### Membuat Array
```go
var animal [4]string
```

### Mengisi Array Melebihi Kapasitas
```go
animal[0] = "kucing"
animal[1] = "ayam"
animal[2] = "kuda"
animal[3] = "katak"
animal[4] = "burung" // ini akan menyebabkan error
```

### Inisialisasi Nilai Awal Array

#### Gaya Horizontal
cara ini mengisi array berderet kesamping
```go
var names = [4]string {"jhon", "chena", "rey", "mysterio"}
```

#### Gaya Vertikal
cara ini mengisi array berderet kebawah
```go
var fruits = [4]string {
	"apple",
	"mango",
	"grape",
	"watermelon",
}
```

### Inisialisasi Nilai Awal Array Tanpa Jumlah Element
jika menggunakan cara ini kita tidak perlu memberikan kapasitas array diawal, jumlah kapasitas array dapat diganti dengan `...`
```go
var numbers = [...]int{1,2,3,4,5,6,6,7,8,9,10,11,}
```

### Array Multidimensi
array multidimensi adalah array yang setiap elemennya juga merupakan array, untuk array yang merupakan element boleh tidak dituliskan jumlah elemennya.

#### Cara 1
```go
var numbers = [2][3]int{{1,2,3},{3,2,1},}
```

#### Cara 2 
```go
var numbers = [2][3]int{[3]int{1,2,3}, [3]int{3,2,1},}
```

### Perulangan Array Menggunakan for
jika melakukan perulangan array menggunakan for maka kita harus mendefinisikan panjang dari array yang akan ditampilkan
```go
var animal = [4]string{"ayam","kuda","kelinci","burung",}
for i := 0; i < len(animal); i++ {
    fmt.Println(animal[i])	
}
```

### Perulangan Array Menggunakan for range
```go
var animal = [4]string{"ayam","kuda","kelinci","burung",}
for key, value := range animal {
	fmt.Println(key, animal)
}
```

## Slice
slice merupakan reference / referensi. slice dapat terbentuk dari array yang sudah ada atau dapat membuat slice baru dari awal.