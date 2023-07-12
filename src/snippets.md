# Snippets

Random contents will temporarily reside here before goes to proper place.


## Install on Windows

Note: sesuaikan versi nya dalam contoh ini sesuai dengan
`https://download.clojure.org/install/linux-install-***` yang ada di
<https://clojure.org/guides/install_clojure>, untuk saat ini (12-Juli-2023)
versinya adalah `1.11.1.1347`.


Kita simpen dulu file powershell script instalan nya sbb:

```
Invoke-WebRequest `
 -UseBasicParsing https://download.clojure.org/install/win-install-1.11.1.1347.ps1 `
 -OutFile clj-win-install.ps1
```

Lalu jalankan file script tersebut:

```
Set-ExecutionPolicy -Scope Process Unrestricted

.\win-install-1.11.1.1347.ps1
```

Akan muncul prompt menanyakan dimana lokasi module ps clojure nya akan
diinstall, pilih 1.

Setelah selesai, cek dulu apakah sudah terinstall dengan benar:

```
Get-Command clojure
Get-Command clj
```

Selanjutnya, pada saat kita jalankan command `clojure` atau `clj` untuk pertama
kali, maka paket-paket dependensi yang dibutuhkan akan mulai didownload dan
disimpan.

```
clojure -M -e '(println :hello)'
```
