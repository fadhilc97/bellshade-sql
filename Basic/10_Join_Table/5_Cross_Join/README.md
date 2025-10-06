# CROSS JOIN

![CROSS JOIN](https://www.w3schools.com/mysql/img_cross_join.png)

`CROSS JOIN` sintaks yang digunakan untuk menampilkan suatu data atau _record_
dengan menghubungkan dua tabel dalam satu kali perintah. Data yang ditampilkan
pada `CROSS JOIN` adalah setiap data pada tabel (_table_) sebelah kiri
dipetakan ke seluruh data pada tabel (_table_) sebelah kanan tanpa mempedulikan
kecocokan relasinya. Begitu pula sebaliknya.

## Sintaks

```sql
SELECT column_name(s)
FROM table1
CROSS JOIN table2;
```

## Contoh

### Demo Database

Table:
Products

| ProductID | ProductName |
| :-------: | :---------: |
|     1     |    Shirt    |
|     2     |    Pants    |

Table:
Colors

| ColorID | ColorName |
| :-----: | :-------: |
|    1    |    Red    |
|    2    |   Green   |
|    3    |   Blue    |

### Contoh Syntax

```sql
SELECT Products.ProductName, Colors.ColorName
FROM Products
CROSS JOIN Colors;
```

Karena diberikan syntax `CROSS JOIN` untuk menggabungkan kedua tabel, maka data
yang ditampilkan adalah setiap data yang ada di tabel _Products_ terhubung ke
seluruh data yang ada di tabel _Colors_ tanpa memperhatikan kesesuaian relasi
antara kedua tabel tersebut.

Berikut hasil dari Query SQL di atas:

### Hasil

| ProductName | ColorName |
| :---------: | :-------: |
|    Shirt    |    Red    |
|    Shirt    |   Green   |
|    Shirt    |   Blue    |
|    Pants    |    Red    |
|    Pants    |   Green   |
|    Pants    |   Blue    |

Hasil di atas menunjukkan bahwa setiap data products yang bernama _Shirt_ dan
_Pants_ terhubung ke seluruh data colors. Kedua tabel tersebut tidak harus
berelasi satu sama lain.

### Catatan

- Jika kedua tabel berelasi, menambahkan klausa `WHERE` dengan mencocokkan
  kolom yang berelasi akan memberikan hasil yang sama dengan klausa `INNER JOIN`.

## Referensi

<https://www.w3schools.com/mysql/mysql_join_cross.asp>
