<template>
  <div class="article-page-container">
    <h2>Wawasan & Manfaat Jamu</h2>
    <p>Pelajari lebih dalam tentang khasiat ramuan tradisional Indonesia.</p>

    <div class="article-list">
      <div class="article-card neumorphism-card">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRCjBymlJ734euKjzJcodtX2HTzCnvnVc6F4g&s" alt="Kunyit Asam">
        <h3>Kunyit Asam: Emas Cair untuk Kesehatan Wanita</h3>
        <p>Jamu kunyit asam telah lama menjadi andalan wanita Indonesia. Kombinasi kunyit sebagai anti-inflamasi dan antioksidan dengan asam jawa yang kaya vitamin C tidak hanya baik untuk meredakan nyeri haid, tetapi juga membantu mencerahkan kulit, mengontrol berat badan, dan meningkatkan sistem kekebalan tubuh. Minuman segar ini adalah paket lengkap untuk vitalitas wanita.</p>
        <a href="#" class="btn-read">Baca Selengkapnya</a>
      </div>

      <div class="article-card neumorphism-card">
         <img src="https://static.promediateknologi.id/crop/0x0:0x0/0x0/webp/photo/p2/255/2024/11/16/IMG_5011-960681411.jpeg" alt="Beras Kencur">
        <h3>Beras Kencur: Hangatkan Tubuh, Redakan Batuk</h3>
        <p>Siapa yang tidak kenal beras kencur? Perpaduan beras yang menenangkan lambung dan kencur yang bersifat ekspektoran menjadikannya pilihan utama saat badan terasa pegal, masuk angin, atau batuk berdahak. Rasa manis dan hangatnya memberikan kenyamanan instan, serta membantu meningkatkan nafsu makan, terutama pada anak-anak.</p>
        <a href="#" class="btn-read">Baca Selengkapnya</a>
      </div>

      <div class="article-card neumorphism-card">
         <img src="https://awsimages.detik.net.id/community/media/visual/2020/02/19/7df804b8-3b00-4560-8eff-31ae511e74aa_169.jpeg?w=600&q=90" alt="Temulawak">
        <h3>Temulawak: Penjaga Hati dan Peningkat Imun</h3>
        <p>Temulawak, atau Curcuma zanthorrhiza, adalah kerabat kunyit yang tak kalah hebat. Dikenal sebagai 'hepatoprotektor', temulawak sangat baik untuk menjaga kesehatan fungsi hati. Selain itu, kandungan kurkuminoidnya berperan sebagai antioksidan kuat yang membantu melawan radikal bebas dan meningkatkan daya tahan tubuh secara keseluruhan.</p>
        <a href="#" class="btn-read">Baca Selengkapnya</a>
      </div>
       <div class="article-card neumorphism-card">
         <img src="https://asset.kompas.com/crops/kpLnWU5RoSZJascP_JgUwWnKBps=/32x22:1000x667/750x500/data/photo/2024/02/21/65d57119b06c1.jpg" alt="Pahitan">
        <h3>Jamu Pahitan: Pahit Membawa Sehat</h3>
        <p>Meskipun rasanya menantang, jamu pahitan yang biasanya terbuat dari sambiloto, brotowali, dan bahan pahit lainnya, memiliki khasiat luar biasa. Ia efektif membersihkan darah, mengatasi masalah kulit seperti jerawat dan gatal-gatal, mengontrol gula darah, dan meningkatkan kinerja ginjal. Sedikit pahit untuk kesehatan jangka panjang!</p>
        <a href="#" class="btn-read">Baca Selengkapnya</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Article',
}
</script>

<style scoped>
.article-page-container {
  padding: 20px 40px;
  background-color: #f0f2f5;
  text-align: center;
}

h2 {
    color: #333;
    margin-bottom: 5px;
}

p {
    color: #666;
    margin-bottom: 40px;
}

.article-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 40px;
}

.neumorphism-card {
  background: #f0f2f5;
  border-radius: 30px;
  padding: 30px;
  box-shadow: 15px 15px 30px #d1d3d6, -15px -15px 30px #ffffff;
  text-align: left;
  display: flex;
  flex-direction: column;
}
.neumorphism-card:hover {
    box-shadow: 18px 18px 36px #d1d3d6, -18px -18px 36px #ffffff;
}

.article-card img {
    width: 100%;
    height: 150px;
    object-fit: cover;
    border-radius: 20px;
    margin-bottom: 20px;
    box-shadow: 6px 6px 12px #d1d3d6, -6px -6px 12px #ffffff;
}

.article-card h3 {
    color: #333;
    margin-bottom: 10px;
    font-size: 1.3em;
}

.article-card p {
    color: #555;
    font-size: 0.95em;
    line-height: 1.7;
    text-align: justify;
    margin-bottom: 25px;
    flex-grow: 1; 
}

.btn-read {
  border: none;
  padding: 10px 20px;
  border-radius: 15px;
  cursor: pointer;
  font-weight: bold;
  transition: all 0.3s ease;
  background-color: #f0f2f5;
  box-shadow: 6px 6px 12px #d1d3d6, -6px -6px 12px #ffffff;
  color: #e6b800;
  text-decoration: none;
  text-align: center;
  align-self: flex-end; 
  margin-top: auto; 
}
.btn-read:hover {
    box-shadow: inset 3px 3px 6px #d1d3d6, inset -3px -3px 6px #ffffff;
    color: #cda500;
}
</style>