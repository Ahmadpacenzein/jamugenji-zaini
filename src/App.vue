<template>
  <div id="app"> <div class="navbar1" v-if="showNavAndFooter">
      <div class="nav-logo">
        <img src="https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcT1S-JWoq3hikl6i8AUrLOVoFXCsDnIifRbiorl0F0SKUnm3wmx" alt="Logo Jamu Kita"> 
        <span>JamuGenji</span>
      </div>

      <div class="nav-links">
        <router-link to="/">Home</router-link>
        <router-link to="/product">Product</router-link>
        <router-link to="/aboutus">About Us</router-link>
        <router-link to="/artikel">Artikel</router-link>
      </div>

      <div class="nav-auth">
        <router-link to="/login" class="btn btn-login">Login</router-link>
        <router-link to="/signup" class="btn btn-signup">Signup</router-link>
      </div>
    </div>

    <router-view class="main-content"></router-view>

    <footer1 v-if="showNavAndFooter"></footer1>
  </div>
</template>

<script>
import footer1 from './views/footer.vue'; 
import login from './views/login.vue'; 
import signup from './views/signup.vue';

export default {
  components: {
    footer1,
    login,
    signup 
  },


  computed: {
    showNavAndFooter() {
      const hiddenPaths = ['/login', '/signup'];   
      return !hiddenPaths.includes(this.$route.path);
    }
  }
}
</script>

<style>
/* Style Global (tidak scoped) atau bisa juga Anda buat scoped 
  jika hanya ingin berlaku di App.vue, tapi #app dan body 
  biasanya global.
*/

/* Reset dasar & warna latar */
body {
  margin: 0;
  background-color: #f0f2f5; /* Warna dasar neumorphism */
}

#app {
  font-family: 'Poppins', Avenir, Helvetica, Arial, sans-serif; /* Ganti font jika mau */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #333;
  background-color: #f0f2f5;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.main-content {
  flex-grow: 1; /* Membuat konten utama mengisi ruang kosong */
}

/* === Gaya Navbar1 === */
.navbar1 {
  display: flex;
  justify-content: space-between; /* Menyebar elemen: logo kiri, link tengah, auth kanan */
  align-items: center;
  padding: 15px 40px;
  background-color: #f0f2f5;
  box-shadow: 8px 8px 16px #d1d3d6, -8px -8px 16px #ffffff;
  border-radius: 0 0 25px 25px;
  margin-bottom: 40px;
  position: sticky; /* Membuat navbar menempel saat scroll */
  top: 0;
  z-index: 1000;
  transition: top 0.3s; /* Efek transisi jika ada perubahan posisi */
}

.nav-logo {
  display: flex;
  align-items: center;
  font-weight: bold;
  font-size: 1.5em;
  color: #333;
  flex-shrink: 0; /* Mencegah logo mengecil */
}

.nav-logo img {
  height: 40px;
  width: 40px; /* Pastikan persegi jika logo bulat */
  margin-right: 15px;
  border-radius: 50%;
  object-fit: cover;
  box-shadow: 4px 4px 8px #d1d3d6, -4px -4px 8px #ffffff;
}

.nav-links {
  flex-grow: 1; /* Memungkinkan area ini tumbuh */
  display: flex;
  justify-content: center; /* Menengahkan tautan */
  gap: 35px; /* Jarak antar tautan */
}

/* Gaya dasar untuk semua router-link di navbar */
.nav-links a, 
.nav-auth .btn { 
  text-decoration: none;
  color: #555;
  font-weight: 500;
  padding: 10px 18px;
  border-radius: 15px;
  transition: all 0.3s ease;
  white-space: nowrap; /* Mencegah teks turun baris */
}

/* Gaya hover & aktif untuk tautan utama */
.nav-links a:hover,
.nav-links a.router-link-exact-active { /* Kelas ini otomatis ditambahkan Vue Router */
  color: #e6b800; /* Warna kuning */
  background-color: #f0f2f5;
  box-shadow: inset 5px 5px 10px #d1d3d6, inset -5px -5px 10px #ffffff;
}

.nav-auth {
  display: flex;
  align-items: center;
  gap: 15px; /* Jarak antara Login dan Signup */
  flex-shrink: 0; /* Mencegah area ini mengecil */
}

/* Gaya Neumorphism untuk tombol */
.nav-auth .btn {
  border: none;
  cursor: pointer;
  font-weight: bold;
  background-color: #f0f2f5;
  box-shadow: 6px 6px 12px #d1d3d6, -6px -6px 12px #ffffff;
  display: inline-block;
}

.nav-auth .btn:hover {
    box-shadow: inset 3px 3px 6px #d1d3d6, inset -3px -3px 6px #ffffff;
}

.btn-login {
    color: #333;
}
.btn-login:hover {
    color: #555;
}

.btn-signup {
  background-color: #f0f2f5;
  color: #e6b800; /* Warna kuning */
  /* Anda bisa beri shadow berbeda jika mau */
  box-shadow: 6px 6px 12px #d1d3d6, -6px -6px 12px #ffffff;
}
.btn-signup:hover {
    color: #cda500;
}
</style>