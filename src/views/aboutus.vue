<template>
  <div class="about-us-container">
    <div class="neumorphism-card main-card">
      <h2>Tentang Jamu Kita 🌿</h2>
      <p class="tagline">Warisan Nenek Moyang, Kebaikan untuk Generasi Sekarang.</p>
      

      <div class="content-section">
        <h3>Misi Kami</h3>
        <p>Di Toko Jamu Kita, kami percaya bahwa alam menyediakan solusi terbaik untuk kesehatan. Misi kami adalah melestarikan resep jamu tradisional Indonesia dan menyajikannya dalam bentuk yang praktis dan berkualitas tinggi untuk masyarakat modern. Kami berkomitmen menggunakan bahan-bahan alami terbaik, diproses secara higienis, untuk memastikan Anda mendapatkan khasiat jamu yang sesungguhnya.</p>
      </div>

      <div class="content-section">
        <h3>Cerita Kami</h3>
        <p>Berawal dari dapur kecil sang Nenek di sebuah desa di Jawa Tengah, kecintaan pada ramuan herbal tumbuh. Melihat bagaimana jamu membantu menjaga kesehatan keluarga secara turun-temurun, kami terinspirasi untuk berbagi kebaikan ini dengan lebih banyak orang. 'Jamu Kita' lahir dari semangat itu – semangat untuk menjaga tradisi, berbagi kesehatan, dan merayakan kekayaan alam Indonesia.</p>
      </div>

      <div class="team-section">
        <h3>Tim Kami</h3>
        <div class="team-members">
            <div class="team-member neumorphism-card-small">
                <img src="https://media.istockphoto.com/id/811146536/id/vektor/setengah-tubuh-kakek-avatar-vector.jpg?s=612x612&w=0&k=20&c=_vzvN3yji9f1tPBBAON3tF-X9UeiJymtL570dwupGSE=" alt="Pendiri">
                <h4>Mbah Zaini</h4>
                <span>Pendiri & Ahli Ramuan</span>
            </div>
             <div class="team-member neumorphism-card-small">
                <img src="../assets/ahmad.jpg" alt="Operasional">
                <h4>Ahmad Zaini</h4>
                <span>Manajer Operasional</span>
            </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutUs',
}
</script>

<style scoped>
.about-us-container {
  padding: 40px;
  background-color: #f0f2f5;
}

.neumorphism-card {
  background: #f0f2f5;
  border-radius: 30px;
  padding: 40px 50px;
  box-shadow: 15px 15px 30px #d1d3d6, -15px -15px 30px #ffffff;
  text-align: center;
}

.neumorphism-card-small {
  background: #f0f2f5;
  border-radius: 20px;
  padding: 20px;
  box-shadow: 8px 8px 16px #d1d3d6, -8px -8px 16px #ffffff;
  text-align: center;
  transition: transform 0.3s ease;
}
.neumorphism-card-small:hover {
    transform: translateY(-5px);
}

h2 {
  color: #333;
  font-size: 2.2em;
  margin-bottom: 5px;
}

.tagline {
    color: #e6b800; /* Aksen kuning */
    font-style: italic;
    font-size: 1.1em;
    margin-bottom: 30px;
}

.store-image {
    width: 100%;
    max-width: 600px;
    border-radius: 20px;
    margin-bottom: 40px;
    box-shadow: 8px 8px 16px #d1d3d6, -8px -8px 16px #ffffff;
}

.content-section {
    margin-bottom: 30px;
    text-align: left;
    background: #f0f2f5;
    padding: 25px;
    border-radius: 20px;
    box-shadow: inset 8px 8px 16px #d1d3d6, inset -8px -8px 16px #ffffff;
}

.content-section h3 {
    color: #333;
    margin-bottom: 15px;
    border-bottom: 2px solid #e6b800;
    padding-bottom: 5px;
    display: inline-block;
}

.content-section p {
    color: #555;
    line-height: 1.8;
    text-align: justify;
}

.team-section h3 {
    color: #333;
    margin-bottom: 25px;
    font-size: 1.5em;
}

.team-members {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    gap: 20px;
}

.team-member img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: 15px;
    box-shadow: 6px 6px 12px #d1d3d6, -6px -6px 12px #ffffff;
}
.team-member h4 {
    margin: 5px 0;
    color: #333;
}
.team-member span {
    font-size: 0.9em;
    color: #666;
}
</style>