<template>
  <footer class="footer">
    <div class="footer-overlay"></div>
    <div class="footer-content">
      <div class="footer-section about">
        <h3>Toko Jamu Kita</h3>
        <p>Menyediakan jamu tradisional berkualitas untuk kesehatan dan vitalitas Anda. Dibuat dengan resep warisan dan bahan alami pilihan.</p>
      </div>

      <div class="footer-section contact">
        <h3>Hubungi Kami</h3>
        <p><i class="icon-map"></i> Jl. Panca Karya, Indragiri Hulu, Riau</p>
        <p><i class="icon-phone"></i> (+62) 123-456-789</p>
        <p><i class="icon-mail"></i> info@jamuGenji</p>
      </div>
      <div class="footer-section social">
        <h3>Ikuti Kami</h3>
        <div class="social-icons">
            
          <a href="https://www.facebook.com/zeinbangjenzeropitu" class="social-icon"><i class="icon-facebook"><img src="../assets/facebook-brands.svg" alt="" srcset=""></i></a>
          <a href="https://www.instagram.com/invites/contact/?i=1vvdraqae9b34&utm_content=3ie48ek" class="social-icon"><i class="icon-instagram"><img src="../assets/instagram-brands.svg" alt="" srcset=""></i></a>
          <a href="#" class="social-icon"><i class="icon-whatsapp"><img src="../assets/whatsapp-brands.svg" alt="" srcset=""></i></a>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      &copy; 2025 Toko JamuGenji | Dibuat dengan ❤️ dan Ramuan Tradisional
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style scoped>
.footer {
  background-color: #d1d3d6;
  color: #333;
  padding: 40px 20px 10px 20px;
  position: relative;
  margin-top: 60px;
  border-radius: 25px 25px 0 0;
  box-shadow: 0 -8px 16px rgba(0, 0, 0, 0.1);
  overflow: hidden; 
}

.footer-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
 
  background-image: url('https://upload.wikimedia.org/wikipedia/commons/thumb/0/05/Ragam_Hias_Sunda_-_Mega_Mendung.svg/768px-Ragam_Hias_Sunda_-_Mega_Mendung.svg.png'); 
  background-repeat: repeat;
  background-size: 300px;
  opacity: 0.1; 
  z-index: 0;
  filter: grayscale(100%) brightness(0.8); 
}

.footer-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  margin-bottom: 20px;
  position: relative;
  z-index: 1;
  padding: 20px;
  background: rgba(240, 242, 245, 0.6); 
  backdrop-filter: blur(5px); 
  border-radius: 20px;
  box-shadow: 8px 8px 16px #bebebe, -8px -8px 16px #ffffff;
}

.footer-section {
  flex: 1;
  min-width: 220px;
  margin: 15px;
}

.footer-section h3 {
  color: #e6b800; /* Aksen kuning */
  margin-bottom: 15px;
  font-weight: 600;
}

.footer-section p, .footer-section ul li a {
  color: #444;
  text-decoration: none;
  line-height: 1.6;
  font-size: 0.9em;
}

.footer-section ul {
  list-style: none;
  padding: 0;
}

.footer-section ul li {
  margin-bottom: 8px;
}

.footer-section ul li a:hover {
  color: #e6b800;
  text-decoration: underline;
}

.social-icons a {
  display: inline-block;
  width: 40px;
  height: 40px;
  line-height: 40px;
  text-align: center;
  margin-right: 10px;
  border-radius: 50%;
  background-color: #f0f2f5;
  color: #555;
  text-decoration: none;
  box-shadow: 4px 4px 8px #bebebe, -4px -4px 8px #ffffff;
  transition: all 0.3s ease;
  font-weight: bold; /* Ganti dengan ikon asli */
}

.social-icons a:hover {
  color: #e6b800;
  box-shadow: inset 3px 3px 6px #bebebe, inset -3px -3px 6px #ffffff;
  transform: translateY(-2px);
}

.footer-bottom {
  text-align: center;
  padding-top: 20px;
  border-top: 1px solid rgba(0, 0, 0, 0.05);
  font-size: 0.8em;
  color: #555;
  position: relative;
  z-index: 1;
}

/* Ganti .icon-* dengan kelas library ikon Anda */
.icon-map, .icon-phone, .icon-mail, 
.icon-facebook, .icon-instagram, .icon-twitter, .icon-whatsapp {
  margin-right: 8px;
}
</style>