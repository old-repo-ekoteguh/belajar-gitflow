## Belajar Git Flow

### Installasi

* Windows `https://git-for-windows.github.io/`
* Mac `brew install git-flow-avh`
* Linux `https://github.com/petervanderdoes/gitflow-avh/wiki/Installing-on-Linux,-Unix,-etc`

### Inisiasi local repository

* Gunakan perintah `git flow init -d` secara otomatis akan membuat dua branch `master` dan `develop`,
* Branch master untuk production releases dan develop untuk next release development.
* Cek dengan perintah `git log` -> Initial commit langsung terbentuk
* Cek lagi dengan perintah `git branch` -> Branch yang di-checkout otomatis mengarah ke branch develop

### Tambah fitur baru

* Gunakan perintah `git flow feature start <nama-fitur>` secara otomatis akan membuat branch `feature/<nama-fitur>` dan otomatis di-checkout.
* Tambah file/folder di dalam branch <nama-fitur> tsb.
* Sebelum merge fitur tsb, alangkah baiknya ada proses code-review dan pull request
* Jangan jalankan perintah `git flow feature finish` -> Push ke origin dengan perintah `git flow feature publish`
