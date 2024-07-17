# ANALISIS KERENTANAN DI WEBSITE ONLINE SHOP

## Pentest
### Perencanaan 
Menentukan pelaksanaan pengujian penetrasi. Tujuan dari perencanaan ini adalah untuk memastikan bahwa pengujian penetrasi berhasil mencapai tujuan dan sasaran yang diharapkan. 

### Pengumpulan Informasi 
Pengumpulan informasi target dilakukan dengan cara Observasi maupun menggunakan tools yang terdapat di kali linux. Saya menemukan sebuah Website E-Commerce yang menjual Produk Kosmetik untuk Simulasi yaitu Ganpati Cosmetics. Setelah melakukan observasi Saya menemukan kerentanan pada website   
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj1ubNtOYK8PjCVkqA1o1j5rpDjCg3yDYe6buhitbUCc3H6P9PQWBKScftd7mgZqgjfwfdacSFQSf06mph6AeJtlgX2aWIZT84tZ-aYYrV5-GMNbT-8tbl1BGQS-_D8vhaVjob-mqe41EaJdapBt4d7eqt2maoBo28L8l-sv1QpJGKN0_rkSK_BzkJXfI4/s1254/1.png" alt="Profile Picture">
</figure>


### Eksploitasi 
1. Masuk kedalam login page dan menemukan 2 form yaitu email dan password. Saya mencoba menginputkan username “admin” dan password “admin” untuk melakukan pengecekan apakah website tersebut mempunyai akun admin dengan password default. Setelah mencoba ternyata Saya tidak mendapatkan hasil apa – apa 
2. Eksplorasi berlanjut pada page register dan mencoba membuat akun baru dengan isi berikut
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhKK7VoQeo5SX2MVb3fknOVpb8BbEf92zIwFGPhb_tPOpUQuz_BqZbqNOfPecnv9gq7hUBWhxD68GRNWq1KRR9iKHtTZAQbRRleOwprKU2iQrPYi0jz83u6JOdFFpb7O_28MnXNuRJ-DDA75VytDOskUQKTYo3AFs7HWNFqnqwfBK7McIAp905svTdHlXI/s556/2.png" alt="Gambar 2">
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj7GXhRS80Yvvf_NDaGXnwNs7d4L4BHpiETk-WdNR7be7dMcL5b9fY60ITKR8XpUH19RNgZPBgRfzLq71fkzNMdknIgYkbiEdfv5E87uLEo9R1Q0HpzwXrmjOGpyMypH23A2lOBVlF0Q91kl015EGA0nI1cUR_l2_UXshp1UUqXBz1GVB3oQ8GpLdGpP-k/s552/3.png" alt="Gambar 3">
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgQ-SIoUfFcNJHgrzCgeY6_A5Hn2HJ6Uh9VK3Ci-n10f91z46ERmYl323kJ_sG49wB918P8zG40HQOkk2SZ_3Q5n0PinDC7_tCgcPXABKIHCOb1JFR-Pzz5nilxlrra6aQlkj1aiGcvn-FcWDKS5afPVlA5CpvOr4ImTN3wqyk0FCi1DHWzOi5mUKl1E8E/s1258/4.png" alt="Gambar 4">
</figure>
3. Setelah berhasil melakukan register Saya melanjutkan eksplorasi untuk mencari kerentanan dari fitur – fitur yang ada di website tersebut. Namun Saya belum menemukan sesuatu yang bisa Saya eksploitasi lebih lanjut. Setelah menghabiskan beberapa waktu, Saya memutuskan untuk logout dari akun dan  mencoba mencari kerentanan pada login page website tersebut 
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjvZLW4NobxQl8jhyphenhyphenk3rH7V6rDfI9BkuJDGj7i9hP1D9CMVzstYT6SHAQUSJyL8s_8svPC61eg1lOtS8IDwIwHVJAoyhaDmPNYdc0BXc3r-rnXr00sDlkVtcMHELg31ALyQ9HkI6UsO_17U7YdJ9xU1IITg0rx19Ef7lHMZgZoYg3l0u0g-EVqQ8FTWIm8/s1288/5.png" alt="Profile Picture">
</figure>
4. Pada halaman login Saya mencoba untuk membypass autentikasi pada website tersebut menggunakan teknik sql injection. Saya langsung saja menggunakan payload yang umum digunakan pada login sql injection yaitu ' OR '1'='1. Dan ternyata pada pecobaan pertama Saya berhasil masuk kedalam website tersebut dengan mudah tanpa menggunakan username dan password yang valid 
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjI_pcIhMVdU8CvNCjfc42B6-BOFASHd2-gfgv9fkdDAT0SusIKELzW7VoGr48aZBKGqMEZW2_f_CntotYWxDMw4woiYU1bCA99JOjmQIagnskpJnlEHSpe_yKoZpJLbRiKhsHghDS64tdRIXVIfqW2w-rPZSX3Cz8G_C8pxxd3uktx11H9lIwc7Tt1sIU/s601/6.png" alt="Gambar 6">
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhVk1OH67fJo_KFhqoWkSsZPEQoy2H-MaX5BpXPFcJlb9e5kmodQbmT6YGE0Po_nUcR9I9Wa1sTtWeLHm-t2jsu2S0FbFKIquwJqASojX1cF2rj_9EbyLx3-ou4LjbMd72B3RpbdZ7IIOdWotRC9XT-j1lVVe4sNS-zD3rONCnt8wOraZFSVIyLjli8XkU/s601/7.png" alt="Gambar 7">
</figure>
5. Dari percobaan Saya diatas, Saya dapat menyimpulkan bahwa query yang terdapat pada form login tersebut adalah “ Select * From tb_name Where username= ‘ ’ And password ‘ ’ ” dan setelah diberikan payload sql injection maka query nya berubah menjadi ' OR '1'='1 menyebabkan kondisi dimana apapun yang di inputkan oleh user menghasilkan logika yang selalu benar. Jadi setelah user mencoba menginputkan username yang tidak valid maka user tetap dapat masuk kedalam website tersebut dengan cara memanipulasi query menjadi seperti gambar dibawah.  
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhfybJoKtj_rLX3cq_LmExWkTbyxbMVS-0xmLJeSkdOe7TfUdlXQD-GP0humH5H9iT7Cgm9qcQjBoSKiUDsxiP30tEFsILJWVzg6nV88XeDiWKCWUAMlcnaxbvcodHHwf0VX1Z7ylmMh1m7ziDlwDksWZ4lx8QIjSyCwVa-bfnSrVJzuwYYJSsEy1dooTs/s601/8.png" alt="Profile Picture">
</figure>
6. Kemudian Saya juga menemukan kerentanan lain pada Website ini yaitu Saya menemukan sebuah URL http://localhost/e_com/trimer.php?cat_id=7  yang memiliki Kerentanan pada SQL injection
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhMGKOvsSwmGUJkr6Dtfs9LP8oSIA53-1QbapVlTQNdiwZlSmU8DngxYg1MlzppPFvcPkF9XRDaubPc1NH11z2wJepfhDVWIjQhLTQs5VA_tJ5ZPtisTEmA6RYWckBq2urJaBo0ekRLio4xLNaEsKkd9b0ZtPyToYVdgTfUG10h-IPVAK01LGtLv4odqPU/s1293/9.png" alt="Profile Picture">
</figure>
Tanda petik tunggal pada parameter cat_id menyebabkan error yang menunjukkan bahwa input user tidak divalidasi dengan baik, sehingga rentan terhadap SQL injection.  
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhcgFj8e0jSw6N9hR9tlb1_cH8r8sjfLxHkcM3agESjFqeEtEoX0Y6q8TBlQl_UALOVWjvw024S_Gda0jwjCSqfUoSZ9Y4UX4b-vjkUPtOAzDlIZwvSHkriAvdHxdeW-pXttST8nCWYmTye3U0GjMyaQ3eHBCe_EiZDb2FliiWJLuP06hlFaI6NGsAHnRo/s1309/10.png" alt="Image">
</figure>
7. Kemudian Saya mencoba untuk menggunakan tool bernama SQLMAP untuk melakukan pengujian pada URL http://localhost/e_com/trimer.php?cat_id=7 dengan perintah sqlmap -u localhost/e_com/trimer.php?cat_id=7 --dbs perintah tersebut memiliki fungsi untuk menampilkan semua database pada seluruh server tersebut 
<figure>
    <img src="https://blogger.googleusercontent.com/img/a/AVvXsEgWKpF5HI4vABQsik3LNVfeYSkwg8-v1cRlJlAQM8TsLAZSWkfsFJs9HD2XPfDRCLOxzElpDqRRYQPlq3HwMpyUDRhZsPa9GKGep29-SEETS0K96Ft4srzX4W2EXNVfy9TcEwXc7XTcSbVFgvRrlDyN8O5ACa5yLJEqrmq5aHABBpVb4yruH1jj6KUV7rg" alt="Profile Picture">
</figure>
8. Kemudian Saya melanjutkan penyerangan menggunkan command : sqlmap -u localhost/e_com/trimer.php?cat_id=7 e_com –tables untuk melihat tabel pada database 
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgBRQCqKBYz1rYQrDoegjaSsu1n5zOcSIB7j5LACoO3b1Aob_jZ3MiyqrnqCNcq5IgKEkHPM5WE_moEmoN3mUy5Ty7lKOGN1m2qiV0U4N__gtK09OwEvGp7hz92fPI-IylYMUSwPC4pseDipprRsqNOiQczjyIAUtG4I9Z9FiEEZcpcLqnboUR_TSmM7-8/s553/12.png" alt="Profile Picture">
</figure>
9. Kemudian menambahkan perintah sqlmap -u localhost/e_com/trimer.php?cat_id=7 e_com --tables e_com –dump. Untuk mengekstrak atau menyimpan tabel  
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgHWjsYX-c0iOPzwJj6jkxmz7NLuHGBvnG7YeJvjADRsbIZJvSP1fYPS727hq7klvmJRAaWeEN0uyqdVMcmlfEN7vi95cO5VtFwBdKVzdh7pg8fgtwHe9i3uw8QUno54Nisno1sviI24fyM483tAo3oqbDSM3tR0a7zxfkNtdS2NVTeUsK0rEDlZzL3oSs/s542/13.png" alt="Profile Picture">
</figure>
10. Hasil dari File dump
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgWf38q2aVX4VgaaSpzc1tL9oin8HtMRWZOvy_icEZlBW-r4jqDshvxjZYO_v1AUewAwEUq9bsYNNSOXIPSxXWTbpjXvEcEo48P4D8kFvkzuvcaHAbOL5GgykKA69jJ69UzTDln3kWZvOAeVf3A3CFq5sJjszIZB1KoeY7btbSF35mq2I4O5FqpWModHp4/s552/14.png" alt="Profile Picture">
</figure>
11. Dari file dump, terlihat bahwa tabel customers berisi informasi krusial seperti email dan password. Saya mencoba login ke website menggunakan email raku08@gmail.com dan password 12345, dan berhasil masuk ke akun tersebut. dan Berhasil Login ke akun Tersebut 
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiHmPZNFVG3ohN6fgqB_yr_vSfFCHwHuwbj4MjPsRoWay6Y3oBh0P2oE14-IcalVtE-dShI9Xg4bIj4pRmAObHIIuhKLFpulK2pjplA9vwIbjug-ogt71DlcXTzSQGrVDpOhjZBGb6Ax9gLQxOE_CHkHpbty12kJVgX58qCjVDnGW8Rbv0Fjoz733LKcTQ/s560/15.png" alt="Profile Picture">
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj0BdGwkYT-Vyqmnw71y3KKix1EfsQSZ_y70tLjkkZzXQsuW3RoZVFGvboKXeLjZAP8x0fPQ3oe8BeLMt2NOqVGcUOzEkyBBEVk1ykbqHRqzjDQnB1pCYvg1uYdPjrrkOTdQRVTZFxRUBvrNyvsscHxKzBT9xWY1lnYSu6SXQwaYXN1DXZFrf9VCywJyuU/s497/16.png" alt="Profile Picture">
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjqDDXpsdzttsYPHtTcYJ7Je9X1852rtzPCDMoUKN7spCrC5fft2Ab9ymHn6bgOdcNXjFXxJu3BqyNG2S-04waQ5GM5siZMyjcOv-BHvVl9ebzQ34Yf3fPfkQTU2nxM8hpRhlpgCAM7VZ3rvSkJOKOG8FtboG770wynSv802PUd8A1dwuHHSleGLbEAGaE/s464/17.png" alt="Profile Picture">
</figure>
12. Saya juga menemukan informasi penting dalam tabel admin, yaitu email dan password untuk login ke akun admin. Saya mencoba login ke halaman admin dengan email rakeshalakh@gmail.com dan password 12345, dan berhasil masuk ke halaman admin. 
<figure>
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg_31oz1rGMZ0p2tMABlDpfoxgEEsSIhlPBwH-JOseNcgSO0gAdejs5PEIJSx167WWMSuv5LJrZxkevbyLCJJl_kmPJO5zVsT2n91uoCndG4m5kGijcMykmyldojxWwcSXIS4zKxP3Eoz-Hybrd8JvW0-x8HZxuHijWQjgfb7KnzckgkstdNBzRZadweFM/s601/18.png" alt="Profile Picture 1">
    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgcYv_6HMNgfdB66E5-KH6-U9hThE-KyFLhQfcEA2vF1vxHyNem_otj4lah5kx7PImSwtiHabmcD6hNOmHmBTBt3kok-o_zhyphenhyphenkLk_d89ieNiUUiNhwYCSMaEStyqiTu6YildfRyWALtP_JWsw-xHD7F2dSTzNz9nz-YvmIzMmTNyPXs006gKRNCLmPbfhA/s592/19.png" alt="Profile Picture 2">
</figure>
13. Berhasil login pada halaman Admin
<figure>
        <img src="https://blogger.googleusercontent.com/img/a/AVvXsEgWKpF5HI4vABQsik3LNVfeYSkwg8-v1cRlJlAQM8TsLAZSWkfsFJs9HD2XPfDRCLOxzElpDqRRYQPlq3HwMpyUDRhZsPa9GKGep29-SEETS0K96Ft4srzX4W2EXNVfy9TcEwXc7XTcSbVFgvRrlDyN8O5ACa5yLJEqrmq5aHABBpVb4yruH1jj6KUV7rg" alt="Profile Picture">
</figure>
