# Rangkuman

## Git
<div style="text-align: justify"> 

**Git** merupakan layanan gratis dan open source version control system yang terdistribusi untuk mengatur segala sesuatu dari project kecil sampai project besar dengan mengandalkan kecepatan dan efisiensi.


Hampir setiap operasi berada di local: Git tidak perlu terhubung ke server untuk mendapatkan history dan menampilkannya cukup membaca langsung dari database lokal.


 

Salah satu cara untuk menggunakan Git adalah dengan menggunakan command line, penggunaan command line sangatlah simpel dan mudah.

### Instalasi

1. Instalasi git pada Linux Fedora bisa menggunakan $ yum install git

2. sedangkan pada Linux Ubuntu bisa menggunakan $ sudo apt-get install git.

3. Instalasi git pada MacOS bisa menggunakan $ brew install git (pastikan sudah terinstal homebrew).

4. Instalasi git pada Windows bisa dengan mendownload installer git pada laman installer.

Pastikan git sudah terinstal dengan menggunakan perintah $ git --version, maka akan menampilkan pesan versi dari git.

### Repository Git

Mendapatkan repository git di dalam project, bisa dengan menggunakan dua cara:

1. $ git init untuk menginisialisasi repository git pada project, kemudian akan membuat folder `.git` yang berisikan semua file repository yang akan dibutuhkan git.

2. $ git clone https://github.com/abdur-rohman2883/learn-git untuk menduplikasi repository yang sudah ada, pada perintah tersebut akan menduplikasi project sesuai dengan namanya dan di dalam project tersebut sudah terdapat folder `.git`.

  

### Perintah perintah dalam Git

1. $ git status untuk melihat adakah perubahan pada work directory dan file yang berada di untracked dan tracked.

2. $ git add <file> untuk mengubah status file / direktori menjadi staged.

3. Mengabaikan file atau direktori bilamana terdapat perubahan di dalamnya, buat file dengan nama `.gitignore` sebagai contoh tambahkan `*.log` dan `build/` untuk mengabaikan perubahan pada file dengan ekstensi log dan folder dengan nama build (termasuk didalamnya).

4. $ git commit -m “message” untuk memasukkan data snapshot ke dalam database git, ubah `message` dengan pesan sesuai kebutuhan, sebagai contoh `initial commit`.

5. $ git commit --amend -m “message” untuk melakukan perubahan commit dan nama pesan.

6. $ git reset HEAD `filename` untuk menyetel ulang file tersebut (kembali ke untracked).

7. $ git checkout -- `filename` untuk menyetel ulang file pada commit sebelumnya.

8. $ git remote add origin https://github.com/paulboone/ticgit untuk menambahkan remote.

9. $ git remote -v untuk melihat daftar remote.

10. $ git fetch origin untuk mengambil semua informasi pada remote origin.

11. $ git pull origin master untuk menarik informasi dari remote origin.

12. $ git push origin master untuk mengirimkan perubahan ke remote.

13. $ git remote rename origin github untuk mengubah nama remote.

14. $ git remote rm github untuk menghapus remote berdasarkan nama remote.

15. $ git branch dev untuk membuat branch dev dan $ git checkout dev untuk berpindah ke branch dev atau dipersingkat dengan $ git checkout -b dev.

16. $ git merge hotfix untuk menggabungkan branch sekarang dengan branch hotfix.

17. $ git branch -d dev untuk menghapus branch dev di lokal.

18. $ git push origin --all untuk berbagi semua branch yang ada di lokal ke remote (biasanya dipakai waktu initial push ke remote).

19. $ git branch untuk melihat semua branch yang ada dan $ git branch -v untuk melihat commit terakhir di setiap branch.

20. $ git branch --merged untuk melihat branch yang sudah merge ke branch sekarang.

21. $ git branch --no-merged untuk melihat branch yang belum merge ke branch sekarang.

22. $ git branch -D dev untuk menghapus branch dev secara paksa walaupun belum merge ke branch sekarang.

23. $ git fetch origin untuk mendapatkan informasi terbaru yang ada di remote dan kemudian $ git merge origin/master untuk menggabungkan informasi tersebut ke local work directory.

24. $ git push origin testing untuk mengirim local branch testing ke remote branch testing (local branch tidak sama dengan remote branch).

25. $ git checkout -b dev origin/dev untuk membuat branch baru dengan titik awal pada remote branch dev.

26. $ git push origin --delete hotfix-auth untuk menghapus remote branch hotfix-auth.
27. $ git rebase development untuk melakukan rebasing branch sekarang dengan local branch development.
28. $ git rebase origin/development untuk melakukan rebasing branch sekarang dengan remote branch development.
29. $  git rebase --continue untuk melanjutkan proses rebasing sampai selesai dan berhasil.
30. $  git rebase --abort untuk membatalkan rebasing.
31. $ git push origin development -f untuk mengirim perubahan ke remote branch  development secara paksa setelah melakukan rebasing. 

## SDLC dan Figma Introduction 
Software Development Life Cycle merupakan sebuah proses yang digunakan oleh industri software untuk mendesign, mengembangkan dan menguji aplikasi dengan kualitas yang tinggi.

### Waterfall Model
Waterfall model adalah sebuah model SDLC yang bersifat linier sequential, dengan arti bahwa setiap tahapan harus selesai terlebih dahulu baru melanjutkan tahapan berikutnya.

### Agile Model
Agile adalah model SDLC yang bersifat iterative and incremental process models, agile berfokus pada proses yang mampu beradaptasi dan kepuasan customer yang terdeliver secara langsung ke produk yang dikembangkan.

### Tracker
Tracker adalah sebuah metode manajemen proyek untuk melacak progress atau blocker pada semua kegiatan yang terlibat di dalam proyek.

**Manfaat**
- Peningkatan peluang keberhasilan proyek.
- Pembentukan tim yang solid.
- Mudah dalam menemukan blocker di dalam pengerjaan proyek.
- Tempat untuk melakukan diskusi terhadap tugas yang diberikan.
- Mudah dalam pembuatan report kepada customer.

<b>Tools</b>
- You Track
- Jira
- Asana
- Trello

### FIGMA IntroDUCTION
Figma adalah editor grafis vektor dan alat prototyping berbasis web dan bersifat free.

## Kotlin Basic
Nama sebuah package kotlin diletakkan di paling atas dari suatu file, kemudian baru melakukan import pada package yang berbeda.
```Kotlin
    package main
    import models.UserModel
    fun main() {
    println("Hello world!")
    println(UserModel("Hello", 12))
    }
```
Titik awal kotlin adalah pada main function, sehingga semua aplikasi kotlin berawal dari main function.
package main
```Kotlin
    import models.UserModel
    
    fun main() { // Entry point
    println("Hello world!")
    println(UserModel("Hello", 12))
    }
```
Function yang memiliki dua parameter Int dengan pengembalian Int,
```Kotlin
    fun sum(a: Int, b: Int): Int {
    return a + b
    }
    menggunakan shorthand,
    
    fun sum(a: Int, b: Int) = a + b
    tanpa pengembalian tipe data.
    fun printSum(a: Int, b: Int) {
    println("sum of $a and $b is ${a + b}")
    }
```
Kotlin menggunakan keyword val sebagai variabel yang bersifat read only (hanya bisa dibaca saja).
```Kotlin
    val a: Int = 1 // immediate assignment
    val b = 2 // `Int` type is inferred
    val c: Int // Type required when no initializer is provided
    c = 3 // deferred assignment
```
Variabel yang bersifat dapat diubah, kotlin menggunakan keyword var.
```Kotlin
    var x = 5 // `Int` type is inferred
    
    x += 1
```
Seperti halnya dengan bahasa pemrograman lainnya, kotlin mendukung single line comment dan multi line comments.
```Kotlin
    // This is an end-of-line comment

    /* This is a block comment
    
    on multiple lines. */
    /* The comment starts here
    
    /* contains a nested comment */
    
    and ends here. */
```
Membuat sebuah literal String pada koltin sama seperti dengan bahasa pemrograman lainnya, yaitu menggunakan single  quote ( ‘ ‘ ) atau double quotes ( “ “ ).
```Kotlin
    var a = 1
    
    // simple name in template:
    
    val s1 = "a is $a"
    a = 2
    
    // arbitrary expression in template:
    
    val s2 = "${s1.replace("is", "was")}, but now is $a"
```
Di dalam kotlin, conditional expression if hampir sama dengan bahasa pemrograman lainnya. Perbedaannya kotlin menggunakan if sebagai ternary operator juga.

```Kotlin
    fun maxOf(a: Int, b: Int): Int {
    if (a > b) {
    return a
    } else {
    return b
    }
    }

    fun minOf(a: Int, b: Int) = if (a < b) a else b
```
Semua value di dalam kotlin yang bisa mempunyai nilai null perlu diperjelas menggunakan tanda tanya ( ? ).

```Kotlin
    fun stringToInt(str: String): Int? {
    return try {
    parseInt(str)
    } catch (ex: Exception) {
    null}
    }
    fun randomString(int: Int?) {
    if (int != null) return print("Number $int")
    return print("")
    }
```
Kotlin menggunakan keyword for untuk melakukan perulangan pada jumlah yang sudah diketahui.

```Kotlin
    val items = listOf("apple", "banana", "kiwi")
    for (item in items) {
    println(item)
    }
    // Or
    for (index in items.indices) {
    println("item at $index is ${items[index]}")
    }
```
Kotlin menggunakan keyword while untuk melakukan perulangan pada jumlah yang belum tentu diketahui.

```Kotlin
    val items = listOf("apple", "banana", "kiwifruit")
    var index = 0
    while (index < items.size) {
    println("item at $index is ${items[index]}")
    index++
    }
```
Kotlin menggunakan keyword when sebagai pengganti switch case.
```Kotlin
    fun describe(obj: Any): String =
    when (obj) {
    1 -> "One"
    "Hello" -> "Greeting"
    is Long -> "Long"
    !is String -> "Not a string"
    else -> "Unknown"
    }
```
Kotlin mempunyai keyword in untuk mendeteksi sebuah angka di dalam sebuah deretan angka tertentu.

```Kotlin
    val x = 10
    val y = 9
    if (x in 1..y + 1) println("fits in range")
    val list = listOf("a", "b", "c")
    if (-1 !in 0..list.lastIndex) println("-1 is out of range")
    if (list.size !in list.indices) println("list size is out of valid list indices range, too")
    for (z in 1..10 step 2) print(z)
    for (z in 9 downTo 0 step 3) print(z)
```
Proses perulangan pada collection kotlin termasuk juga menambahkan built in method, seperti: map, filter, forEach dsb.


```Kotlin
    val items = listOf("banana", "avocado", "apple", "kiwi")
    for (item in items) {
    println(item)
    }
    items.filter { it.contains("a", true) }
    .sortedBy { it }
    .map { it.toUpperCase() }
    .forEach { println(it) }
```
Pembuatan instance class pada kotlin tidak memerlukan keyword new cukup langsung nama class dan diikuti dengan constructor class tersebut.
```Kotlin
    data class UserModel(var name: String, var age: Int)
    fun main() {
    println(UserModel("Angga", 12))
    }
```
</div>

 