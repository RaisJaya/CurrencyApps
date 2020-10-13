#Currency Apps
Aplikasi ini mencakup fungsi pergitungan nilai tukar rupiah dengan dolar
yang mana satu dolar dianggap senilai Rp.15.000,-

##Scop & Functionalities
- User dapat memasukkan angka
- user dapat menyentuh tombol hitung
- User mendapat info invalid jika memasukkan text

##How does it works?
Diawali dari method 'main window' pada class MainWindow.xaml.cs 
'''c#
 public MainWindow()
        {
            InitializeComponent();
            currency = new CurrencyController();
        }
'''

Logika perhitungan terdapat pada class 'CurrencyController.cs' sebagai berikut
'''c#
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }

        public Boolean isAllowed(string nominal)
        {
            Regex regex = new Regex("[^0-9.-]+");
            return !regex.IsMatch(nominal);
        }
'''
