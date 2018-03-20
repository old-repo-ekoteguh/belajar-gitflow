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

### Release
* Gunakan perintah `git flow release start <nama rilis/versi>`, secara otomatis akan membuat branch baru bernama `release/<nama rilis/versi>`
* Untuk rilis, pastikan tahapan sebelum rilis sudah dikerjakan Minify (CSS, JS, Image Optimization), Config file (config, .env), dkk
* Jika sudah selesai semua, baru jalankan perintah `git flow release finish <nama rilis/versi>`

Contoh:
`git flow release start 'v1.0'`
`git flow release finish 'v1.0'`

* Jangan lupa untuk update dulu origin/master dengan perintah `git push origin master --tags`
