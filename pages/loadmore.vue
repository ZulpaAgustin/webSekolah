<script setup>
import { ref } from "vue";

useHead({
  title: "Guru - Website Sekolah"
})

const db_teachers = ref([
  {
    id: 1,
    nama: "Zul Hilmi",
    foto: "https://avatars.githubusercontent.com/u/6418851?v=4",
  },
  {
    id: 2,
    nama: "Taufik Hidayat",
    foto: "https://avatars.githubusercontent.com/u/6418851?v=4",
  },
  {
    id: 3,
    nama: "Lisye Ingriani",
    foto: "https://avatars.githubusercontent.com/u/6418851?v=4",
  },
  {
    id: 4,
    nama: "Arip",
    foto: "https://avatars.githubusercontent.com/u/6418851?v=4",
  },
  {
    id: 5,
    nama: "Deni Maulana",
    foto: "https://avatars.githubusercontent.com/u/6418851?v=4",
  },
  {
    id: 6,
    nama: "Adi Iasan",
    foto: "https://avatars.githubusercontent.com/u/6418851?v=4",
  },
  {
    id: 7,
    nama: "Suminar",
    foto: "https://avatars.githubusercontent.com/u/6418851?v=4",
  },
  {
    id: 8,
    nama: "Tini Gartini",
    foto: "https://avatars.githubusercontent.com/u/6418851?v=4",
  },
]);

const teachers = ref([...db_teachers.value.slice(0, 3)]);
const start = ref(teachers.value.length);
const end = ref(start.value + 3);

const loadmore = () => {
  // Gabungkan data lama dengan data baru dari db_teachers
  teachers.value = [
    ...teachers.value,
    ...db_teachers.value.slice(start.value, end.value),
  ];
  // Perbarui nilai start dan end
  start.value = end.value;
  end.value = end.value + 3;
};
</script>

<template>
  <div class="utama">
    <div class="page-title">
      <h1 class="judul">Guru/Pendidik</h1>
      <p class="text-muted text-center">Guru-Guru SMKN 4 Tasikmalaya</p>
    </div>
    
   <!-- Baris untuk kartu -->
   <div class="row justify-content-center g-2">
      <div v-for="teacher in teachers" :key="teacher.id" class="col-md-4 d-flex justify-content-center align-items-stretch">
        <div class="card" style="width: 16rem;">
          <img :src="teacher.foto" alt="Foto Guru" class="card-img-top" />
          <div class="card-body text-center">
            <h5 class="card-title">{{ teacher.nama }}</h5>
          </div>
        </div>
      </div>
    </div>
    <!-- Tombol Load More -->
    <div class="text-center mt-3">
      <button class="btn btn-dark" @click="loadmore" v-if="start < db_teachers.length">Load More</button>
    </div>
  </div>
</template>

<style scoped>
.utama {
  margin-top: 90px;
}

.judul {
  font-size: 2.5rem;
  color: #004080;
}

.page-title {
  text-align: center;
  margin-bottom: 2rem;
}

.page-title h1 {
  font-size: 2.5rem;
  color: #004080;
}

.card {
  margin-bottom: 10px;

}
</style>

<!-- <script setup>
import { ref, onMounted } from "vue";
import { createClient } from "@supabase/supabase-js";

// Konfigurasi Supabase
const supabaseUrl = "https://your-supabase-url.supabase.co"; // Ganti dengan URL Supabase Anda
const supabaseKey = "your-supabase-anon-key"; // Ganti dengan kunci anon Anda
const supabase = createClient(supabaseUrl, supabaseKey);

// State
const teachers = ref([]);
const start = ref(0);
const limit = ref(3);
const loading = ref(false);

// Fungsi untuk mengambil data dari Supabase
const fetchTeachers = async () => {
  loading.value = true;
  const { data, error } = await supabase
    .from("teachers") // Nama tabel Supabase
    .select("*")
    .order("id", { ascending: true }) // Mengurutkan berdasarkan id
    .range(start.value, start.value + limit.value - 1);

  if (error) {
    console.error("Error fetching teachers:", error);
    return;
  }

  // Gabungkan data lama dengan data baru
  teachers.value = [...teachers.value, ...data];
  start.value += limit.value;
  loading.value = false;
};

// Panggil saat komponen dimuat
onMounted(() => {
  fetchTeachers();
});
</script>

<template>
  <div class="utama">
    <div class="page-title">
      <h1 class="judul">Guru/Pendidik</h1>
      <p class="text-muted text-center">Guru-Guru SMKN 4 Tasikmalaya</p>
    </div>

   
    <div class="row justify-content-center g-2">
      <div
        v-for="teacher in teachers"
        :key="teacher.id"
        class="col-md-4 d-flex justify-content-center align-items-stretch"
      >
        <div class="card" style="width: 16rem;">
          <img :src="teacher.foto" alt="Foto Guru" class="card-img-top" />
          <div class="card-body text-center">
            <h5 class="card-title">{{ teacher.nama }}</h5>
          </div>
        </div>
      </div>
    </div>

    
    <div class="text-center mt-3">
      <button
        class="btn btn-dark"
        @click="fetchTeachers"
        :disabled="loading"
        v-if="teachers.length < start"
      >
        {{ loading ? "Loading..." : "Load More" }}
      </button>
    </div>
  </div>
</template>

<style scoped>
.utama {
  margin-top: 90px;
}

.judul {
  font-size: 2.5rem;
  color: #004080;
}

.page-title {
  text-align: center;
  margin-bottom: 2rem;
}

.page-title h1 {
  font-size: 2.5rem;
  color: #004080;
}

.card {
  margin-bottom: 10px;
}
</style> -->
