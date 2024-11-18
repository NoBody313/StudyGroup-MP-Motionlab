
# Week 1 - Git

## Panduan Perintah Git

Berikut ini adalah penjelasan tentang perintah-perintah Git yang sering digunakan:

### 1. `git init`
Perintah ini digunakan untuk menginisialisasi sebuah repositori Git baru di direktori lokal. Saat menjalankan `git init`, Git akan membuat folder tersembunyi bernama `.git` yang menyimpan semua data konfigurasi dan versi kontrol yang diperlukan untuk mengelola perubahan di repositori. Setelah itu, kamu bisa mulai menggunakan Git untuk melacak perubahan, menambahkan file, dan melakukan commit.

### 2. `git clone <URL repository (HTTP / SSH)>`
Perintah `git clone` digunakan untuk menyalin (clone) sebuah repositori dari URL tertentu, entah itu repositori lokal atau remote. Biasanya digunakan untuk men-download repositori yang ada di GitHub, GitLab, atau Bitbucket ke dalam komputer atau laptop mu. Setelah melakukan clone, kamu akan memiliki salinan penuh kecuali file atau folder yang termasuk dalam `.gitignore` dari repositori tersebut di perangkat kamu.

### 3. `git add <nama file>`
Perintah ini digunakan untuk menambahkan file tertentu ke dalam *staging area*, yaitu area di mana file yang akan di-commit disiapkan. Setelah menambahkan file dengan `git add`, file tersebut siap untuk dimasukkan dalam commit berikutnya. Kamu bisa menambahkan file tertentu atau menambahkan semua file dengan `git add .`.

- `git add .`: Menambahkan semua perubahan (termasuk file baru, perubahan, dan penghapusan) ke dalam staging area.

### 4. `git status`
Perintah ini digunakan untuk menampilkan status dari repositori. `git status` akan menunjukkan file mana yang telah diubah, file yang belum di-commit, file yang sudah di-stage, dan file yang belum ditambahkan ke dalam repositori Git. Ini sangat berguna untuk melihat apa yang telah dilakukan sejak commit terakhir.

### 5. `git branch`
Perintah `git branch` digunakan untuk menampilkan daftar branch yang ada di repositori. Branch adalah cabang dari sejarah commit, yang memungkinkan kamu untuk melakukan perubahan secara terpisah dari branch utama (biasanya `master` atau `main`).

- `git branch` : Melihat list yang ada di repositori, Ini sinonim dari `git branch --list`.
- `git branch <nama branch>` : Membuat branch baru <nama branch>. 
- `git branch -d <nama branch>` : Menghapus spesifik branch. Ini termasuk tindakan yang "aman" pada git yang mencegah kamu dari menghapus branch jika ada perubahan yang belum digabungkan.
- `git branch -D <nama branch>` : Menghapus paksa branch spesifik, walaupun branch tersebut memiliki perubahan yang belum digabungkan. Perintah ini digunakan jika kamu ingin menghapus paksa semua commit dengan perubahan tertentu. 
- `git branch -m <nama branch>`: Mengganti nama branch yang sedang aktif.
- `git branch -a` : Menampilkan keseluruhan branch yang ada di lokal dan remote repositori.

### 6. `git checkout <nama branch>`
Perintah ini digunakan untuk berpindah dari satu branch ke branch lainnya. Dengan `git checkout`, kamu bisa memilih branch yang ingin kamu kerjakan. Jika kamu ingin membuat branch baru sekaligus berpindah ke branch tersebut, kamu bisa menggunakan `git checkout -b <nama branch>`.

### 7. `git commit -m "<pesan>"`
Perintah `git commit` digunakan untuk menambahkan pesan perubahan yang telah dilakukan di repositori ke dalam history commit Git. Setelah melakukan perubahan pada file, kamu bisa menambahkan file tersebut ke dalam staging area menggunakan `git add` dan kemudian membuat commit dengan pesan yang menjelaskan perubahan yang telah dilakukan. Pesan commit harus singkat namun informatif mengenai apa yang telah diubah.

### 8. `git log`
Perintah ini digunakan untuk menampilkan riwayat commit pada repositori. `git log` akan menampilkan informasi tentang setiap commit, termasuk ID commit (hash), nama pembuat commit, tanggal commit, dan pesan commit. Ini berguna untuk melacak perubahan dan melihat riwayat proyek.

### 9. `git reset --hard <commit hash>`
Perintah `git reset --hard` digunakan untuk mengembalikan repositori ke kondisi commit tertentu, dengan menggunakan `commit hash`. Perintah ini akan menghapus semua perubahan yang belum di-commit dan mengembalikan file ke keadaan seperti pada commit yang dituju. Gunakan dengan hati-hati, karena perubahan yang belum di-commit akan hilang.

### 10. `git revert <commit hash>`
Berbeda dengan `git reset`, perintah `git revert` digunakan untuk membalikkan perubahan yang telah dilakukan oleh commit tertentu, namun dengan cara membuat commit baru yang membatalkan perubahan tersebut. Ini berguna jika kamu ingin membatalkan perubahan tanpa menghapus riwayat commit.

### 11. `git push`
Perintah `git push` digunakan untuk mengirim perubahan dari repositori lokal ke repositori remote (misalnya GitHub). Dengan `git push`, perubahan yang telah di-commit di repositori lokal akan diperbarui di repositori remote pada branch yang aktif.

- `git push -f`: Menyebabkan perubahan di repositori remote terupdate dengan mengabaikan peringatan yang ada. Perintah ini berisiko karena bisa menimpa perubahan yang ada di remote.
- `git push -u origin <nama branch>`: Perintah ini digunakan untuk mengaitkan branch lokal dengan branch remote tertentu (misalnya, `origin`). Setelah itu, kamu bisa menggunakan `git push` tanpa harus menyebutkan remote dan branch lagi.

### 12. `git pull`
Perintah `git pull` digunakan untuk mengambil (download) perubahan terbaru dari repositori remote dan menggabungkannya dengan branch lokal yang sedang aktif. Ini adalah cara untuk memastikan bahwa repositori lokal kamu selalu terupdate dengan perubahan yang ada di repositori remote.

---

Dengan kombinasi perintah-perintah ini, kamu dapat dengan mudah mengelola proyek menggunakan Git, melacak perubahan, dan berkolaborasi dengan tim dalam pengembangan.
