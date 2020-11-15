# Shift 1 JARKOM 2020 - T19
Penyelesaian Soal Shift 1 Komunikasi Data, dan Jaringan Data 2020\
Kelompok T19
  * Made Krisnanda Utama (05311840000033)
  * Muhammad Irsyad Ali (05311840000041)


---
## Table of Contents
* [Persiapan](#persiapan-1)
* [Soal 1](#soal-2)
* [Soal 2](#soal-3)
* [Soal 3](#soal-4)
* [Soal 4](#soal-5)
* [Soal 5](#soal-6)
* [Soal 6](#soal-7)
* [Soal 7](#soal-8)
* [Soal 8](#soal-9)
* [Soal 9](#soal-10)
* [Soal 10](#soal-11)
* [Soal 11](#soal-12)
* [Soal 12](#soal-13)
* [Soal 13](#soal-14)
* [Soal 14](#soal-15)
* [Soal 15](#soal-16)
* [Soal 16](#soal-17)
* [Soal 17](#soal-18)
---

## Persiapan
   Sebelum mengerjakan soal. Kami melakukan konfigurasi dulu pada file ```topologi.sh``` untuk menginput server PROBOLINGGO. Sama halnya
dengan file ```bye.sh``` juga kami inputkan server PROBOLINGGO. Kemudian sesuai modul pengenalan UML, pada router SURABAYA, mengaktifkan
IP Forwardingnya pada ```/etc/sysctl.conf``` dan menggunakan command ```sysctl -p``` untuk mengaktifkan perubahannya. Kemudian mengsetting
IP tiap UML lokasinya di file ```/etc/network/interfaces```. Kemudian tiap UML disetting agar IPnya aktif, command yang digunakan yaitu
```service networking restart```. Supaya bisa terkoneksi dengan internet pada router SURABAYA kami jalankan command
```iptables it nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.168.0.0/16```. Untuk mempermudah export proxy tiap kali menjalankan UML,
pada tiap UML kami buatkan file ```proxy.sh``` menjalankannya file tersebut menggunakan perintah ```source proxy.sh```. Kemudian install
bind9 di server MALANG,dan MOJOKERTO dengan perintah ```apt-get install bind9 -y```, sedangkan apache2 diiinstall di server PROBOLINGGO
dengan perintah ```apt-get install apache2 -y```. 

## Soal 1
Pertama-tama kami mengkonfigurasikan DNS server MALANG agar domain ```http://semerut03.pw``` mengarah ke server IP PROBOLINGGO. 
![1_1](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/1_1install%20bind_1.png)
## Soal 2
![2_1](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/2_1CNAME_alias_1.png)

![2_2](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/2_2CNAME_alias_1(berhasil%20ping%20di%20client).png)
## Soal 3
![3_1](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/3_1.png)

![3_2](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/3_2.png)
## Soal 4
![4_1](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/4_1reverse%20DNS_1.png)

![4_2](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/4_2reverse%20DNS_2(update%20di%20gresik).png)

![4_3](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/4_3reverse%20DNS_3%20(error%20saat%20install%20DNS_UTILS).png)

![4_4](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/4_4reverse%20DNS_4(complit).png)

## Soal 5
![5_1](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/5_1DNS%20MASTER-SLAVE_1(master).png)

![5_2](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/5_2.png)

![5_3](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/5_3DNS%20MASTER-SLAVE_4(testing%20slave%20di%20gresik).png)

## Soal 6
![6_1](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/6_1Delegasi%20subdomain_%20konfigurasi%20di%20etc%20bind%20jarkom%20semerut19%20pada%20malang%20.png)

![6_2](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/6_2Delegasi%20subdomain_%20konfigurasi%20di%20named%20conf%20options_semerut19pw%20pada%20malang.png)

![6_3](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/6_3Delegasi%20subdomain_%20konfigurasi%20di%20named%20conf%20local_semerut19pw_pada%20malang_setelah%20diedit.png)

![6_4]()

![6_5](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/6_5Delegasi%20subdomain_%20konfigurasi%20di%20named%20conf%20local__%20pada%20mojokerto.png)

![6_6](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/6_6Delegasi%20subdomain_%20konfigurasi%20di%20etc%20bind%20delegasi%20GUNUNG%20semerut19%20pw_pada%20mojokerto.png)

![6_7](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/6_7Delegasi%20subdomain_%20pengetesan%20ping%20ke%20sub%20domain%20baru(gunung).png)

## Soal 7
![7_1](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/6_6Delegasi%20subdomain_%20konfigurasi%20di%20etc%20bind%20delegasi%20GUNUNG%20semerut19%20pw_pada%20mojokerto.png)

![7_2](https://github.com/krisnanda59/Sif-Jarkom1/blob/main/dokum_no1%20-no7fixed/7_2Delegasi%20subdomain_%20berhasil%20ping%20dari%20gresik%20kepada%20gunung%20semerut19%20%26%20naik%20gunung%20semeru%20t19.png)

## Soal 8

## Soal 9

## Soal 10

## Soal 11

## Soal 12

## Soal 13

## Soal 14

## Soal 15

## Soal 16

## Soal 17
