# Currency-Apps
Aplikasi ini mencakup fungsi untuk menentukan nilai tukar mata rupiah ke dolar. Yang mana 1 dollar dianggap bernilai Rp 15.000 

## Scope & Functionalities
- User dapat memasukkan angka yang akan dicek
- User dapat mengeklik tombol konversikan untuk melihat hasil
- User mendapat info invalid jika memasukkan berupa teks/huruf karena,memang tidak di peruntukan teks

## How does it works
Diawali dari method "MainWindow" pada class window.xaml.cs dideklarasikan dengan:

``` csharp
public MainWindow()
        {
            InitializeComponent();
            Currency = new CurrencyController();
        }
```
logika perhitungan terdapat pada CurrencyController.cs sebagai berikut:
``` csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```
