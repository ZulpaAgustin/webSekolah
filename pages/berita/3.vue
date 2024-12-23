<template>
  <div class="utama">
    <div class="row">
      <!-- Konten Utama Berita -->
      <div class="col-lg-8">
        <div class="main-news">
          <img
            src="/assets/img/septi.jpg"
            alt="Berita Utama"
            class="main-news-image"
          />
          <h2 class="main-news-title">Pelaksanaan Kegiatan Zona Integritas</h2>
          <p class="main-news-content">
            <i style="color: blue;">#Cari_aman</i> 
            Skill Competition 2024 
            <br>di selenggarakan oleh Safety Riding Center PT Daya Adicipta Motora Bandung
          </p>
        </div>
      </div>

      <!-- Berita Lainnya -->
      <div class="col-lg-4">
        <div class="other-news">
          <h3 class="other-news-title">Berita Lainnya</h3>
          <div class="other-news-item">
            <img
              src="/assets/img/utama.png"
              alt="Berita 1"
              class="other-news-image"
            />
            <h5 class="other-news-heading">Judul Berita 1</h5>
            <a href="#" class="other-news-link">Baca Selengkapnya</a>
          </div>
          <div class="other-news-item">
            <img
              src="/assets/img/utama.png"
              alt="Berita 2"
              class="other-news-image"
            />
            <h5 class="other-news-heading">Judul Berita 2</h5>
            <a href="#" class="other-news-link">Baca Selengkapnya</a>
          </div>
          <div class="other-news-item">
            <img
              src="/assets/img/utama.png"
              alt="Berita 3"
              class="other-news-image"
            />
            <h5 class="other-news-heading">Judul Berita 3</h5>
            <a href="#" class="other-news-link">Baca Selengkapnya</a>
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

/* Konten Utama Berita */
.main-news {
  padding: 20px;
}
.main-news-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
  margin-bottom: 15px;
}
.main-news-title {
  font-size: 2rem;
  color: #004080;
  margin-bottom: 10px;
}
.main-news-content {
  font-size: 1.1rem;
  color: #333;
  line-height: 1.6;
}

/* Berita Lainnya */
.other-news {
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
}
.other-news-title {
  font-size: 1.5rem;
  color: #004080;
  margin-bottom: 20px;
}
.other-news-item {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
}
.other-news-image {
  width: 80px;
  height: 80px;
  object-fit: cover;
  border-radius: 8px;
  margin-right: 10px;
}
.other-news-heading {
  font-size: 1rem;
  color: #333;
  margin: 0;
}
.other-news-link {
  display: block;
  font-size: 0.9rem;
  color: #004080;
  text-decoration: none;
  margin-top: 5px;
}
.other-news-link:hover {
  text-decoration: underline;
}
</style>
