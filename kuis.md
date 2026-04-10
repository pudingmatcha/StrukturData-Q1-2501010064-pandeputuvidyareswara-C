# kuis 1
## 1. Karakteristik Memori dan Akses Data
Jelaskan mengapa operasi akses elemen pada Array dapat dilakukan dalam waktu konstan
O(1), sedangkan pada Singly Linked List membutuhkan waktu linear O(n). Hubungkan
jawaban Anda dengan konsep alamat memori (kontinu vs non-kontinu).
jawaban:
Kalau array, data itu disimpen berurutan di memori (kontinu). Jadi tiap elemen posisinya udah jelas. Misalnya kita mau ambil data ke-5, komputer tinggal langsung hitung alamatnya dari awal, terus langsung loncat ke sana. Nggak perlu ngecek satu-satu. Makanya cepet banget, waktunya tetap → O(1).
Nah kalau singly linked list, datanya itu nggak berurutan di memori (acak / non-kontinu). Tiap node cuma nyimpen data sama alamat ke node berikutnya. Jadi kalau mau ambil data ke-5, kita harus mulai dari awal dulu, terus jalan node per node sampai ketemu. Nggak bisa langsung loncat.

## 2. Analisis Efisiensi Operasi Manipulasi
Dalam kondisi apa sebuah Linked List lebih diunggulkan dibandingkan Array untuk operasi penyisipan (insertion) dan penghapusan (deletion) data? Berikan alasan teoritisnya
jawaban:
Linked List lebih unggul dibandingkan array saat sering melakukan penyisipan dan penghapusan data, terutama di bagian tengah atau awal. Hal ini karena pada Linked List tidak perlu menggeser elemen lain seperti pada array, melainkan cukup mengubah pointer untuk menyambungkan node sebelum dan sesudahnya.
Sebaliknya, pada array, setiap kali ada penyisipan atau penghapusan di tengah, elemen-elemen setelahnya harus digeser, sehingga membutuhkan waktu lebih lama, yaitu O(n). Selain itu, Linked List juga lebih fleksibel karena ukurannya bisa bertambah atau berkurang secara dinamis tanpa perlu mengatur ulang kapasitas memori.
Namun, keunggulan ini berlaku jika posisi node yang ingin diubah sudah diketahui, karena jika belum, tetap perlu pencarian terlebih dahulu yang memakan waktu O(n).

## 3. Konsep Doubly Linked List
Jelaskan struktur anatomi dari sebuah node pada Doubly Linked List. Apa dampak keberadaan pointer tambahan tersebut terhadap penggunaan memori serta fleksibilitas penelusuran dibandingkan dengan Singly Linked List?
jawaban:
Pada Doubly Linked List, satu node terdiri dari data, pointer ke node berikutnya (next), dan pointer ke node sebelumnya (prev). Jadi, setiap node bisa terhubung ke dua arah, yaitu maju dan mundur.
Karena ada pointer tambahan, penggunaan memori jadi lebih besar dibandingkan Singly Linked List yang hanya punya satu pointer. Namun, kelebihannya adalah kita bisa menelusuri data dengan lebih fleksibel, karena bisa bergerak ke depan maupun ke belakang tanpa harus mulai dari awal.
Jadi, Doubly Linked List lebih boros memori, tapi lebih mudah digunakan untuk navigasi dua arah.
