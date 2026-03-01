# PBW-MINI-PROJECT-2
## Fauzia Inanta Aurelia/ 2409116044/ Sistem Informasi (B)

# Tampilan Section/Fitur
## 1. Navbar
Menampilkan navigasi utama untuk berpindah ke setiap section: Home, About Me, Experience, dan     Contact.

<img width="1887" height="65" alt="image" src="https://github.com/user-attachments/assets/271eef58-8505-4f64-828a-a5f6254d53dd" />


## 2. Home (Hero Section)
Menampilkan perkenalan singkat berisi: 

・Judul: “Hi, I'm Fauzia”

・Role / profesi

・Deskripsi singkat

・Tombol navigasi ke About Me

・Foto profil

<img width="1893" height="815" alt="image" src="https://github.com/user-attachments/assets/f32567ed-f679-4732-8073-6d5b589526af" />


## 3. About Me
Berisi:

・Deskripsi diri

・Riwayat pendidikan

・Skills dengan progress bar

<img width="1888" height="670" alt="image" src="https://github.com/user-attachments/assets/f39837cc-9464-4123-a376-ac55c3e5ac16" />

## 4. Experiences Page
Menampilkan pengalaman dalam bentuk card grid:

<img width="1894" height="638" alt="image" src="https://github.com/user-attachments/assets/6a8a280f-89d9-4482-9996-2b95f42a152f" />

## 5. Contact Section

  ・ Menampilkan sosial media dan email:

<img width="1898" height="440" alt="image" src="https://github.com/user-attachments/assets/4373da0b-ffaa-4d3f-b0b7-ef87185eeecf" />

# Penjelasan Kode
## 1. Navbar
Menggunakan Bootstrap Navbar untuk navigasi responsif.

    • <nav class="navbar navbar-expand-lg navbar-light custom-navbar fixed-top shadow-sm">

Nama pada navbar diambil dari Vue.

    • <a class="navbar-brand fw-bold" href="#home">{{ navbarName }}</a>
## 2. Homepage 
Section ini menampilkan judul, role, deskripsi, tombol, dan foto profil.

    • <section id="home" class="hero-section d-flex align-items-center">
Deskripsi dinamis dari Vue:

    • <p class="hero-desc">{{ heroDescription }}</p>
Tombol navigasi:

    • <a href="#about" class="btn btn-light custom-btn mt-3">More about me!</a>

## 3. About Me Section 
Berisi deskripsi diri dan riwayat pendidikan:

    • <p>{{ about }}</p>
      <ul>
        <li v-for="exp in education" :key="exp">{{ exp }}</li>
      </ul>
Skills menggunakan progress bar:

    • <div v-for="skill in skills" :key="skill.name">
        <span>{{ skill.name }}</span>
        <div class="skill-bar-container">
          <div class="skill-bar" :style="{ width: skill.level + '%' }"></div>
      </div>
    </div>
    
## 4. Experiences Section
Menampilkan pengalaman dalam bentuk card grid:

    • <div class="col-md-4" v-for="exp in experiences" :key="exp.title">
        <div class="card experience-card h-100 shadow-sm">
          <img :src="exp.image" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title">{{ exp.title }}</h5>
          <p class="card-text">{{ exp.desc }}</p>
        </div>
      </div>
    </div>
Data pengalaman diatur di Vue:

     • experiences: [
        { title: "Makeup Artist Assistant", desc: "...", image: "images/mua.jpg" }
        ]

## 5. Contact Section
Menampilkan sosial media dan email:

    • <p class="contact-info">{{ email }}</p>

## 6. Vue JS (Data Dinamis)
Vue digunakan untuk menampilkan data secara dinamis menggunakan interpolation `{{ }}` dan directive `v-for`.

## 7 Penjelasan Styling (CSS)
Hero Title Font

    • .hero-title {
        font-family: 'Charmonman', cursive !important;
        font-size: 4.5rem;
      }

Menggunakan Google Fonts agar tampilan judul lebih estetis.

Custom Button

    • .custom-btn {
        border-radius: 30px;
        background-color: #C8A1B1;
        color: #fff;
      }
Experience Card Image

    • .experience-card img {
        height: 200px;
        object-fit: cover;
        }
Agar ukuran gambar pada semua card sama dan rapi.

# Teknologi yang Digunakan

1. `HTML5`
2. `CSS3`
3. `Bootstrap 5`
4. `Vue JS (CDN)`
5. `Google Fonts`

# Fitur Utama

1. `Responsive Design (Bootstrap Grid System)`
2. `Dynamic Data Rendering (Vue JS)`
3. `Progress Bar Skills`
4. `Experience Card Layout`
5. `Custom Font dari Google Fonts`
6. `Smooth Scroll Navigation`
