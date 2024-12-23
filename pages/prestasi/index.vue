<template>
  <div class="utama">
    <!-- Header -->
    <div class="container mt-5 text-center">
      <h1 class="mb-4">Prestasi Sekolah</h1>
      <p class="text-muted">Berikut adalah daftar prestasi yang telah diraih oleh siswa-siswi dan sekolah kami</p>
    </div>

    <!-- Daftar Prestasi -->
    <div class="container mt-4">
      <div class="row">
        <!-- Card 1 -->
        <div class="col-md-6 mb-4">
          <div class="card">
            <div class="image-wrapper">
              <img src="/assets/img/p11.jpg" class="card-img-top" alt="Prestasi 1">
            </div>
            <div class="card-body">
              <h5 class="card-title">Juara 1 Lomba Debat Bahasa Inggris</h5>
              <p class="card-text">
                Prestasi luar biasa diraih oleh siswa kami pada tingkat nasional dalam lomba debat Bahasa Inggris.
              </p>
            </div>
          </div>
        </div>
        <!-- Card 2 -->
        <div class="col-md-6 mb-4">
          <div class="card">
            <div class="image-wrapper">
              <img src="/assets/img/p22.jpg" class="card-img-top" alt="Prestasi 2">
            </div>
            <div class="card-body">
              <h5 class="card-title">Juara Umum Olimpiade Sains</h5>
              <p class="card-text">
                Sekolah kami berhasil meraih juara umum pada olimpiade sains tingkat provinsi.
              </p>
            </div>
          </div>
        </div>
        <!-- Card 3 -->
        <div class="col-md-6 mb-4">
          <div class="card">
            <div class="image-wrapper">
              <img src="/assets/img/p33.jpg" class="card-img-top" alt="Prestasi 3">
            </div>
            <div class="card-body">
              <h5 class="card-title">Juara 2 Kejuaraan Sepak Bola</h5>
              <p class="card-text">
                Tim sepak bola sekolah kami berhasil menjadi juara 2 pada kejuaraan antar sekolah.
              </p>
            </div>
          </div>
        </div>
        <!-- Card 4 -->
        <div class="col-md-6 mb-4">
          <div class="card">
            <div class="image-wrapper">
              <img src="/assets/img/p1.jpg" class="card-img-top" alt="Prestasi 4">
            </div>
            <div class="card-body">
              <h5 class="card-title">Juara 3 Lomba Seni Lukis</h5>
              <p class="card-text">
                Dalam ajang seni lukis tingkat nasional, siswa kami berhasil meraih juara 3.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.utama {
  margin-top: 90px;
}

h1 {
  color: #004080;
}

.image-wrapper {
  width: 100%;
  height: 200px; 
  overflow: hidden; 
  display: flex;
  justify-content: center;
  align-items: center;
}

.card-img-top {
  width: 100%;
  height: 100%;
  object-fit: cover; 
}
</style>
