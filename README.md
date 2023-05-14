# SimpleLB

Simple LB is the simplest Load Balancer ever created.

It uses [RoundRobin algorithm](#RoundRobin-algorithm) to send requests into set of backends and support
retries too.

It also performs active cleaning and passive recovery for unhealthy backends.

Since its simple it assume if / is reachable for any host its available

# How to use
```bash
Usage:
  -backends string
        Load balanced backends, use commas to separate
  -port int
        Port to serve (default 3030)
```

In TERMINAL :

```
docker compose up
```
```
docker compose up -d
```
Example:

To add followings as load balanced backends
- http://localhost:3031
- http://localhost:3032
- http://localhost:3033
- http://localhost:3034
```bash
simple-lb.exe --backends=http://localhost:3031,http://localhost:3032,http://localhost:3033,http://localhost:3034
```



![image](https://github.com/islamicity24/simplelb/assets/126258837/8f6bfea6-f665-453f-87a0-bea13bf98969)

# RoundRobin-algorithm

jelaskan prinsip, kontex dan fungsi serta manfaat nya dari : RoundRobin algorithm

RoundRobin algorithm adalah salah satu algoritma scheduling atau penjadwalan dalam sistem komputer yang digunakan untuk membagi waktu pemrosesan CPU (Central Processing Unit) secara adil dan merata di antara beberapa proses yang berjalan secara bersamaan. Prinsip kerja algoritma ini adalah dengan membagi waktu CPU secara periodik atau berulang-ulang (round-robin) dengan durasi waktu yang sama untuk setiap proses yang berada dalam antrian.

Konteks dari RoundRobin algorithm adalah algoritma penjadwalan yang digunakan dalam sistem operasi untuk mengatur antrian proses yang membutuhkan pemrosesan CPU. Algoritma ini bekerja dengan mengalokasikan waktu pemrosesan yang sama untuk setiap proses dalam antrian, sehingga memastikan bahwa setiap proses memiliki kesempatan yang sama untuk mendapatkan sumber daya CPU.

Fungsi dari RoundRobin algorithm adalah untuk mengoptimalkan penggunaan CPU dengan cara membagi waktu pemrosesan secara adil dan merata di antara semua proses yang membutuhkan pemrosesan CPU. Dalam hal ini, algoritma ini membantu mengurangi waktu tunggu dan meningkatkan efisiensi dalam sistem komputer dengan mempercepat waktu respons dari sistem.

Manfaat dari RoundRobin algorithm adalah dapat meningkatkan efisiensi dan kinerja sistem dengan mengurangi waktu tunggu proses yang berada dalam antrian dan memastikan bahwa setiap proses mendapatkan kesempatan yang sama untuk diproses. Selain itu, algoritma ini juga dapat membantu meningkatkan pengalaman pengguna dalam menggunakan aplikasi atau sistem yang memerlukan pemrosesan CPU, karena setiap proses dapat diproses dengan cepat dan responsif.



