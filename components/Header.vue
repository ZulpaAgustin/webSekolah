<template>
  <div>
    <nav class="navbar">
      <div class="logo">
        <img src="/assets/img/logopo.png" alt="Logo" />
        <h5>SMKN 4 Tasikmalaya</h5>
      </div>
      <ul class="nav-links">
        <li><nuxt-link to="/">Beranda</nuxt-link></li>
        <li><nuxt-link to="/profile/">Profile</nuxt-link></li>
        <li><nuxt-link to="/berita/">Berita</nuxt-link></li>
        <li><nuxt-link to="/prestasi/">Prestasi</nuxt-link></li>
        <li><nuxt-link to="/ekstra/">Ekstrakurikuler</nuxt-link></li>
        <li class="contact"><nuxt-link to="/kontak/">
          <button class="primary-btn">KONTAK KAMI</button></nuxt-link></li>
      </ul>
    </nav>
  </div>
</template>

<style scoped>
/* Navbar Tetap */
button {
  border: none;
  background: none;
  outline: none;
  transition: 0.5s;
  cursor: pointer;
}

.primary-btn {
  padding: 10px 20px; /* Ukuran padding tombol */
  font-size: 1rem; /* Ukuran teks tombol */
  line-height: 1; /* Pastikan tinggi tombol tetap normal */
  background: #121a6a;
  color: white;
  border-radius: 5px; /* Membuat sudut tombol melengkung */
}

.contact {
  display: flex;
  align-items: center; /* Menjaga tombol tetap sejajar */
  height: 100%; /* Pastikan mengikuti tinggi navbar */
}

.primary-btn:hover {
  background-color: #03031e; 
}

.navbar {
  position: fixed; /* Navbar tetap di atas layar */
  top: 0;
  left: 0;
  z-index: 1000; /* Tetap di atas elemen lain */
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #004080;
  color: white;
  width: 100%; /* Lebar penuh */
  height: 70px; /* Tinggi navbar */
  padding: 0;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* Bayangan lembut */
}

/* Logo dan teks */
.logo {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding-left: 1rem; /* Padding kiri */
}
.logo img {
  height: 50px;
  width: 50px;
  object-fit: contain;
}
.logo h5 {
  margin: 0;
  font-size: 1.5rem;
}

/* Tautan navigasi */
.nav-links {
  display: flex;
  list-style: none;
  gap: 1.5rem;
  margin: 0;
  padding-right: 1rem; /* Padding kanan */
}
.nav-links a {
  color: white;
  text-decoration: none;
  font-size: 1rem;
  transition: color 0.3s ease;
}
.nav-links a:hover {
  color: #0077ff;
}

.nav-links li {
  display: flex;
  align-items: center; /* Pastikan semua elemen dalam barisan tetap sejajar */
  height: 70px; /* Sama dengan tinggi navbar */
}

/* Reset margin body */
:global(body) {
  margin: 0;
}
</style>
