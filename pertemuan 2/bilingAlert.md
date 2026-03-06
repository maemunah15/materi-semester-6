# Membuat Billling Alert di AWS untuk menghindari kelebihan alokasi dana 

1. Menu Dashboard AWS kita pilih Billing Preference untuk mengaktifkan Alert
-Masuk Menu Billing and Cost Manajemen
![alt text](image-6.png)

-Pada Menu Cost Manajemen Scroll Ke bawah pilih Billing Preferences
-Pilih Menu Alert Preferences klik Edit
![alt text](image-1.png)

-Isi Email ceklis Receive
-Klik Update 
![alt text](image-2.png)

2. Masuk Menu Cloudwatch
-Pilih All Service lalu cari Cloudwatch
![alt text](image-7.png)

3. Pilih Menu Create Alarm
-Pastikan Region ada di US N Virginia
![alt text](image-9.png)
-Klik Menu  Create Alert
-Klik Metric
-Klik Menu Billing
-Pilih Menu Total Estimated Charge
-Pilih / Ceklis Mata Uang USD
-Klik Select Metric
-beri nama Alert = NIM_Billing Alert
![alt text](image-10.png)

-Conditions  Static->Greathertha-> 1 USD
![alt text](image-11.png)

-Create new Topic = > NIM_BillingAlert -? KLik Create
-Select an existing SNS topic - > NIM_BillingAlert
-Klik Next
-Alarm Name -> NIM_BillingAlert 
-Create Alarm
-Buka 
![alt text](image-12.png)