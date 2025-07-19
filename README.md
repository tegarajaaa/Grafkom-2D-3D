# Grafkom-2D-3D

# 🎮 Aplikasi Grafika Komputer 2D & 3D Interaktif dengan PyOpenGL

Proyek ini merupakan implementasi aplikasi grafika komputer 2D dan 3D interaktif untuk memenuhi Tugas Besar UAS mata kuliah **Grafika Komputer** di **Universitas Muhammadiyah Malang**. Aplikasi ini dibangun menggunakan **Python**, **PyOpenGL**, **Pygame**, dan **GLUT**, serta mendemonstrasikan berbagai teknik grafika seperti penggambaran objek, transformasi geometri, clipping, pemodelan 3D, dan interaksi pengguna secara real-time.

---

## 📁 Struktur Direktori

```
grafika-komputer-umm/
│
├── modul_a_2d/           # Modul A - Aplikasi Grafika 2D
│   ├── main_2d.py
│   ├── shape.py
│   ├── transform.py
│   └── clipping.py
│
├── modul_b_3d/           # Modul B - Aplikasi Grafika 3D
│   ├── main_3d.py
│   ├── camera.py
│   ├── lighting.py
│   └── utils.py
│
├── assets/               # (Opsional) untuk tekstur, skybox, .obj
│
├── README.md             # Dokumentasi proyek
└── requirements.txt      # Daftar pustaka Python
```

---

## 🧩 Modul A - Aplikasi Grafika 2D Interaktif

### 📌 Deskripsi

Modul ini menggunakan kombinasi **Pygame** dan **PyOpenGL** untuk membangun antarmuka interaktif di mana pengguna dapat menggambar dan memanipulasi objek-objek 2D secara visual.

### 🎯 Fitur-Fitur

* ✅ Penggambaran objek dasar:

  * Titik (`GL_POINTS`)
  * Garis (`GL_LINES`)
  * Persegi / kotak (`GL_LINE_LOOP`)
  * Elips (menggunakan perhitungan titik keliling)
* ✅ Transformasi objek 2D:

  * Translasi (geser)
  * Rotasi
  * Skala (perbesaran/perkecilan)
* ✅ Seleksi objek menggunakan mouse
* ✅ Pewarnaan dan pengaturan ketebalan objek
* ✅ Window clipping dengan algoritma **Cohen-Sutherland**
* ✅ GUI Pygame + event handler mouse/keyboard
* ✅ Ukuran window default: **800x600**

---

## 📦 Modul B - Aplikasi Grafika 3D Interaktif

### 📌 Deskripsi

Modul ini menggunakan **PyOpenGL** dan **GLUT** untuk membangun visualisasi kubus 3D yang dapat dirotasi, diterangi secara dinamis, dan dikendalikan menggunakan input pengguna.

### 🎯 Fitur-Fitur

* ✅ Pemodelan kubus 3D secara manual (8 titik, 6 sisi)
* ✅ Pemberian warna berbeda pada tiap sisi kubus
* ✅ Pencahayaan realistis:

  * Komponen ambient, diffuse, dan specular
* ✅ Material shading & efek refleksi cahaya
* ✅ Warna background dinamis (animasi RGB sinusoidal)
* ✅ Kontrol kamera:

  * Keyboard:

    * `W`, `S` = maju / mundur (Z axis)
    * `A`, `D` = kiri / kanan (X axis)
    * `Z`, `X` = atas / bawah (Y axis)
  * Mouse drag = rotasi objek pada sumbu X dan Y
  * Tombol `R` untuk reset posisi kamera
* ✅ Depth testing (`glEnable(GL_DEPTH_TEST)`)
* ✅ Render loop menggunakan `glutIdleFunc()`

---

## 🛠️ Teknologi yang Digunakan

| Teknologi        | Deskripsi                                |
| ---------------- | ---------------------------------------- |
| Python 3.x       | Bahasa utama untuk scripting dan logika  |
| PyOpenGL         | Binding Python untuk pustaka OpenGL      |
| Pygame           | Digunakan untuk membuat window dan event |
| GLUT             | Toolkit event handler dan rendering loop |
| NumPy            | Perhitungan matematis dan transformasi   |
| Anaconda/Jupyter | Rekomendasi environment interaktif       |

---

## ⚙️ Cara Menjalankan (Rekomendasi via Anaconda/Jupyter)

### 1. Install Environment (sekali saja)

```bash
conda create -n grafkom-env python=3.10
conda activate grafkom-env
pip install PyOpenGL PyOpenGL_accelerate pygame numpy
```

### 2. Jalankan Aplikasi 2D

```bash
cd modul_a_2d
python main_2d.py
```

### 3. Jalankan Aplikasi 3D

```bash
cd modul_b_3d
python main_3d.py
```

> **Catatan**: Untuk menjalankan dalam Jupyter Notebook, cukup gunakan `!python main_2d.py` di dalam sel notebook.

---

## 📚 Referensi dan Sumber Belajar

* [PyOpenGL Documentation](http://pyopengl.sourceforge.net/)
* [Pygame Documentation](https://www.pygame.org/docs/)
* Buku *Computer Graphics with OpenGL* – Donald Hearn & M. Pauline Baker
* Tutorial Cohen-Sutherland:

  * [https://www.geeksforgeeks.org/line-clipping-set-1-cohen-sutherland-algorithm/](https://www.geeksforgeeks.org/line-clipping-set-1-cohen-sutherland-algorithm/)
* Panduan OpenGL Lighting:

  * [https://learnopengl.com/Lighting/Basic-Lighting](https://learnopengl.com/Lighting/Basic-Lighting)
* StackOverflow & forum komunitas PyOpenGL

---

## 👨‍🎓 Identitas Mahasiswa

| Data               | Keterangan                            |
| ------------------ | ------------------------------------- |
| **Nama**           | Tegar Reski Pratama                   |
| **NIM**            | 202310370311215                       |
| **Universitas**    | Universitas Muhammadiyah Malang (UMM) |
| **Fakultas**       | Teknik Informatika                    |
| **Mata Kuliah**    | Grafika Komputer                      |
| **Dosen Pengampu** | Muhammad Ilham Perdana, S.Tr.T., M.T               |

---

## 📌 Lisensi

Proyek ini dibuat untuk kepentingan akademik dan bersifat open-source untuk pembelajaran. Diperbolehkan menggunakan dan memodifikasi dengan menyertakan kredit pembuat asli.
