# TUGAS_SBD_BACKUP_RECOVERY
# Nama    : Wilianto
# Keas    : TI.19.B2
# Nim     : 311910184

# -------------TUGAS 10 SISTEM BASIS DATA------------------
# TUGAS Backup dan Restore Menggunakan Perintah SQL
# 1. BUKA CMD MASUK MYSQL USE DATABASE YANG MAU DI BACKUP 
![image](https://user-images.githubusercontent.com/81583408/122800358-07826400-d2ed-11eb-8944-2b34533f9b47.png)
# 2. LIAT TABEL DAN Lakukan proses penguncian table.
![image](https://user-images.githubusercontent.com/81583408/122800440-1ff27e80-d2ed-11eb-91d2-1892255dc696.png)
![image](https://user-images.githubusercontent.com/81583408/122800538-40223d80-d2ed-11eb-97da-d863bc5ffd65.png)
# 3. Lakukan proses backup table dengan perintah : SELECT * INTO OUTFILE 'b_pelanggan' from pelanggan;
![image](https://user-images.githubusercontent.com/81583408/122800662-66e07400-d2ed-11eb-9340-d8309deab336.png)
# 4. Jika proses backup berhasil maka akan muncul file backup pada direktori
#  C: xampp/mysql/data/wilianto_311910184
![image](https://user-images.githubusercontent.com/81583408/122800722-7bbd0780-d2ed-11eb-9e9f-ba1406a9f403.png)
# 5 . delete tabel pelanggan;
![image](https://user-images.githubusercontent.com/81583408/122801054-dd7d7180-d2ed-11eb-8af9-a467d26bb311.png)
# 6. Data yang telah di backup dapat dikembalikan kapan saja bila diperlukan. Sintaks SQL yang digunakan
# adalah LOAD DATA INFILE. Perintah yang dijalankan adalah load data infile 'b_pelanggan' into table pelanggan;
![image](https://user-images.githubusercontent.com/81583408/122801236-0f8ed380-d2ee-11eb-8ccc-ee1de84034bb.png)

------------------------------------------------------------------------------------------------------------------------------------------------
# TUGAS Backup dan Restore Menggunakan MySQLDump
# 1.Menuju ke folder aplikasi mysqldump di xamp/mysql/bin
#  Jalankan shell atau commad prompt dan ketikkan perintah berikut untuk memulai dump database : mysqldump -u root -p wilianto_311910184 > backup2.sql
![image](https://user-images.githubusercontent.com/81583408/122802431-8d9faa00-d2ef-11eb-8281-474aca40ae74.png)
# 2. Jika proses backup berhasil maka akan muncul file backup pada direktori
#   C:\xampp\mysql\bin
![image](https://user-images.githubusercontent.com/81583408/122802709-deaf9e00-d2ef-11eb-9c48-589f1955c4f2.png)
# 3. Data yang telah dibackup dapat di restrore kembali ke dalam database dengan perintah : mysqldump -u root -p wilianto_311910184 < C:\xampp\mysql\bin\backup2.sql
![image](https://user-images.githubusercontent.com/81583408/122803340-ac527080-d2f0-11eb-92e5-29d0de7f4a91.png)

-----------------------------------------------------------------------------------------------------------------------------------
# Tulisakan script cron job untuk melakukan backupotomatis setiap hari minggu jam 12 malam !
#  1. Script Untuk menjalankan backup database setiap hari minggu jam 12 malam : script dibawah :
## 0 0 * * 7 mysqldump -u root -p wilianto_311910184 > backup2.sql 

------------------------------------------------------------------------------------------------------- 




