<template>
  <div class="product-page-container">
    <h2>Semua Produk Jamu Kami</h2>
    <p>Temukan ramuan tradisional terbaik untuk Anda.</p>
    
    <div class="filter-bar neumorphism-card-flat">
        <span>Filter:</span>
        <button class="btn-filter active">Semua</button>
        <button class="btn-filter">Penyegar</button>
        <button class="btn-filter">Penghangat</button>
        <button class="btn-filter">Stamina</button>
    </div>

    <div class="product-grid">
      <div class="product-card neumorphism-card-small" >
        <img src="https://asset.kompas.com/crops/YdCxZWTFzecZK5U9uL-_uae7VgA=/24x0:867x562/1200x800/data/photo/2021/03/02/603e41b8eaf6b.jpg" alt="jamu kunyit" srcset="">
        <h3>Jamu Kunyit Asem {{ n }}</h3>
        <p>Deskripsi singkat jamu produk {{ n }}.</p>
        <span class="price">Rp 15.000</span>
        <button class="btn btn-add-cart">Lihat Detail</button>
      </div>
      <div class="product-card neumorphism-card-small" >
        <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxMTEhUTEhMWFhUSFxcXFhgVFRcXFhUVFRcXFxgYFRYYHSggGBolGxUVITEhJSotLi4uGB8zODMtNygtLisBCgoKDg0OGhAQGy0lICUtLS0tLS0rLS0tLS0tLS0tLS0rLS0tLS0tLS0tLS0rLS0tKy0tLS0tLS0tLS0tLS0tOP/AABEIALYBFQMBIgACEQEDEQH/xAAbAAEAAgMBAQAAAAAAAAAAAAAAAgQDBQYHAf/EAEIQAAIBAgMEBwUFBQYHAAAAAAABAgMRBCExBRJBUQZhcYGRobETIjJCUhRywdHwI2KS4fEHFTNTwtJDY3OCg6Ky/8QAGQEBAAMBAQAAAAAAAAAAAAAAAAIDBAEF/8QAJBEBAAIBBQACAgMBAAAAAAAAAAECAwQREiExE0EiURQyYUL/2gAMAwEAAhEDEQA/APcQAAAAAAAAAAAAAAAAAABgr4uEMm83pFZyfcszA8bJ6Qt955+Eb+pGbRDsRMrwNc6tR/Pb7sV+Nz43P/Ml4Q/2nOcO8ZbIGq36i0qvvjB+iROOJrL6Jdzg/wDUOcHCWyBRjtOK/wAROHW7OP8AErpd9i7GSaundPkSiYnxyY2fQAdcAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADT4rHyqScKLtGOU6nX9MOvr4GfbVdqKhF2lUdr8o/M14+ZXpU1FJRySK72+oTrX7So0VHRa6t5tvm282zKQPreRWmkj6mVZYqK1kvH8iL2hT+ryZzlDvGVonYpQx9N/Ou929S3Gomrpp9mZ2LRJMShMwRi4O9J7r4x+SXbHh2rzMrZFhxewOOVS6tuzj8UXr2p8V1ls56unlKOU4ZxfPmn1M3eExCqQUlxXg+KLaW3V2rszAAmiAAAAAAAAAAAAAAAAAAAAAAAAAAAAANFtqpbEUr8YSt23RP2iSu8kuZj6W02oQqxWdKWf3ZK0vRFKrU3kuWv5GPPk+OZmWnHXlGzLVxzeUF3v8EYXC+c5Nkb2MM655OTV2n7bK4YhY91cEfHUXJFOWIITqmec1v2sikLTcXwRFUVe8W4vqdil7RmSFUjGe8T67OOJbCGLqR199eEu56Mu4fFRmrxemqeTXajWU6pJwz3o5NenJ80b8GtnyzPfB+myky1sGX+JHgp5d6TNc6y3d7TmbHo5B+yc3/wASTkuzReh6mGd53hjyRtDagA0qQAAAAAAAAAAAAAAAAAAAAAAAAAAAaTbXSehh7xvvzXyRen3npH16jhdr9LMRVut5Qg/lg7eMtX5FGTUUp0ux4L3d/tvHUVB05VI78rJRvd3uuHA5hVJUtFvR5LWPO3NdRw/2qzvdXTv4d53CrXs+fnc8zU6ibT42UwcI9ZFXUleLuv1quBikyGIwcZO6bjLnF2ffwfeYfZVo8YVO39nLyvF+R5tscT3WWmJ/bLJkbkFN/NCUf4Zf/LZKLvz/AIX+RXxmE9wlFkbdUv4ZfkTUZfTL+FrzlZDhafIc3hlpstxqJK8mklq27Jd5UhSqPRRj953fhHLzMn92p51G5tZpPKKfVFF2PFO+9pV2vH0w05SxElCKapX10dR8EuUTvKVNRiorRJLwOShjadFxnUdoqSWS01tlyyOpwmLhVip05KUXxTv/AEZ72jmJq87URO7OADYzgAAAAAAAAAAAAAAAAAAAAAAfGwPlSoopyk0kldt5JJc2cF0k6ZuV6eGbjHR1Pml936V169hQ6X9JHiJujRbdKL+X/iNccvl5LvOZrUZpZwkuf8zBn1Ez+NG7Bgj+1kpVf1+mRdTIpTr9p8dbL+Ria92arPqTOy2HXU6cE9UlY8/qVb8vA6jo/iLU1+tGZ9T1WJSr26xxzI1IGGji08mWqb5Myc4k22VnEnFGdw6iO6jvjqKiTUCcYmSK6iSJTiKyvkidyni8RZZE+XGEdt2m6TVryjBaRTb7X/Q1+zsdVoS3qU3F8Vwl1ST1MeMrXm83/QjGXX5I00tMREwnxjbaXpHR/pJDEe7JblTlwl91/gb08gg2mmmrrR2tbvO+6Mbe9svZ1Le0Syf1pfiepp9Tz/G3rz8+n4/lXx0IANjIAAAAAAAAAAAAAAAAA+Skkrt2S5mhxvSinHKnFzfPSPi9SNr1r67FZnxvKtVRTlJ2S1bOT2/t1VIypQuoyupyXxNcUlwvz5Gtxu0alZ+/N2btZXil2bufmajbT9mru1ly4X6npqY8uomeqtWPDt3K1aFNNRUUnbK197Lnqzmds7Us1GKvvtKK+puySXB3MGCrTxU9yDSgmlO8rNRzTSs7t2T4rU7atg1KCUoxstFxVtGnwfYZdmjdoMPsKnuqdVtt/FFNJJ2V0mtbdpWxOz6bvCCaa0bbd/HIbXxdSE6VKEZSk3KyUZbqikkry5bt82z7ThWj70oWtnupxm7Xs7vTuGyW7ntpYSdJreWTeUlo+3kbro7W/Z2f1M01TaHt37HfUXOpLKV04KGSTbVnez0eufbZ2C3Fzg3nGXO6a5oz6qs8FlJ7ddTqlqjiWjVwqGanM8qelzd08aZPtZpo1DOpiLS5s20MTc+yxJq4VD66hLnLmy3WxTZTxlXhyR8vmUMbWybJV3mRrJVM87O/cZIzXLzINvl6H3d6vA9E2ZPaR6+9XJUMSoyUoy3WmmnmrNcSCiuvxDgdiXNnquwdpqvSUst5ZTS5811PU2R5t0Nx7pV0r+7VtGXDN/C/HLvPST2NPl+Sm/28nPj4W2AAXqQAAAAAAAAAAAABoemNVKgoXs5yjktWk7vuyRyNOulG2t9Hy6ju9sbIhiI2k5LheL/M4jE9G8VCTUae+tIuLST8XkYtRS823iGrDasRs0+2cdKL9x5q1lHNuTyz49yJQ2U61JvESaVr7sGt7t3s8+pItYrozicPH29Rxk21Ddi77kZfE23ZN7qay5mei6m45K27BWSSu5cVZ36zNas19aItEx00XRfAUMJVrRpb7cpQU5TlG8INTabbt7t1bndnXU3vqTi9L66ZZP0PNdqVn9rul/jRs1e6bpSvo19NW9/yOs2XUl9ntG9023dPJe7o/wBcTtv9IhDaWLkoynBKUqV291WU1G94q+d7XfaZFKNalGtSSftI3itU78Xy09CjjFUim0nkr+7q+dl2EcXiaeHpRlSlGNCVpZPL35JO19HeWcepkP8AEmg6TYZUJ068UvaU2r3TamnfXPNq9r8ivsnEOpGda6uqjjJLhGSi4vxUkZul2MozpR3au/Vk72iluxjmnmte3ianontNUKzjUSdOqt2Sej1yfK6bz5pEppzrMScpjuHZYWtdF6EjXVMPue9C8qMvhk/l/dm1kn18cnxLFKoeNlxzSdpaa2ifF5SLEJFBTMtOqVRCUrykSuV4zEq1jsQjunWqWXaa/Fy93qyJublKyzf648F1mHHVo5Qi72zb5y0yvwXDx4mjFj3/ACnxzftUlh/pdrnyMpLX8ycpJB52tx8/A1x2knSrp3yeXJFzCYadR2hG/XwXazYbJ6Oyl71W8VwivifbyOnw2HjBJRSSXBF1MW/cqL5f01ez9gqLUpybks8skn6s38qsnrJ+JidTkZaGFnU0yXN/hzNVK7dVZ72j2zPs2tJztdtcb52NsYMLhlBWWb4vizObaVmI7Y72iZ6AATQAAAAAAAAAAAAAFbaWFVWlOm1feT8eHmeS9JdsRpunQpOKjF++3e0XH5Gks23e+at1nsZ4p/aBs1QxlWLyjVtUj/3av+JSMmqjqLNOmneZq4jbe239qhUj+1hRbtKzjvX13brJcFdHXdGekH2iMt17soN5Ste3DeSvwy3uo5fEbKWlpX45Mr0NmVKct+lvRlmrq6yeqfNdTyMnyUmNpa/jtEvTa+PhuO9o7rbcmm1ZLtujy/pDiViKu/CPs4WXuq9nJXvK3PO19bJFussTUSjUba5Wgr9trEFhJcvNEYvFfEoxzPrXUsPpqyc8LfRGzp4OXH1X5mdYNdXj+RCcs7rIx9PmxNv1aD3W21pe/Dk08mtcmvA6Kjj6FRXX7KX7icoP/wAd7xf3W0aBYSHG3cn+JCeDivhcl1ZW8Dk3rbqYc+P7h1NJ3doTpz+7NKWXDdlZ3LDw1a1/ZSt1Wfozjt2dtE+Gv4SubbZ+xsbPOnQqLk7xprtTbVyr4MdvonlH22irTvb2dT+B2XaS372cnaL1u1Hwv73/AKin0Sx8vilBffrSflFMzU+gld/HWpq/07z9UiUaeseVc5fuWtxeNgsqacr8c7K2nW9X48CFDS/Pi+Z0+E6Dwj8daUvuxUfW5vcDsShS+Cmrri/efi9O4n8Vpl35K1jpxuB2FWrNNLdi/mle3ctWdhsvYlOik/il9Ute76Se1dsUcOr1JZvSKzk+xHL43pLWq5U0qcebtKT7Fou+5Z+GP1D8r+Otxm0adKO9OcYpcW0l4nPYvpcm7UKbn+9L3Y9yfvPwXaaB0N5707zlznm+6+i6kWIdhXbUTPiUYY+2eeLxFZpSqNJtLdh7sc34vvZ63RhuxUVwSXgjzLo7Rc8TSjwUt59kM/VI9QN2hiZrNpY9ZMbxEAANzGAAAAAAAAAAAAAAAAHDf2pbI36McRFZ0XaVtdyXHufqzuSFelGcXGSvGSaaejTyZC9IvWYSpbjaJeA4Zp+7K/U07J9RlqYXql4/yLPSXY8sHiJU5Z05Z05c48L9a0IUKieUvHPzPEyUms7PZpeLRurLArk/MfY1y/XezYeyj+n/ADIyprl6lXaxR+ypcPQ+Kgv0y17NcvMwVIK+i/XcBjkl1eLPlCi6k404pOU2klfiyNapYz9EcdbHUVJ/E5RV+coSUePOy7yVK8p2ctO0bvQth9HqWHinZSqcZtcf3F8q8zdXIRJnoRWIjpimd2OVzG5GWbKlSZGSFmlO5pekfSOND9lStKs1nd+7TT4y6+SKu3NvexTp0rOtJdqpp/NK3Hkn26a8zhcK03KT3pN3bd223q23xKcmXj1Hq6mPfuU9xzlvze9OWsmrvu5LqRbpxtz9D7Cn+syW51+VzJ6vL9vez63aN216k/dSuyrFSqzjCCzk7Rj1vmTrXeUZnZ139nuDcnUryX7kfV28jtynsjAqhRhTXyrN85PNvxLh7uKnCkQ8fLfnaZAAWKwAAAAAAAAAAAAAAAAAAavpDsSni6Tp1Mms4SWsJc11dR5FtPY9TDVHCorNaPhJc4s9xKW1dl08RDcqxuuD0lF84vgZ8+CMkder8Oecc9+PFqVdrrLDrJ/0v6I2/SDorVwzcre0pfXFZx++l66GihFdfqeTek1na0PUraLRvWU6s7Zbrfp4sxVZZfC/L8y1Slbj5GZyXG3d/Qjsk53ENtfDbtt+DNBi95SunZpppp5prNNPg7ne1aEZcbeP5FDEbKT+Zef4I7SdpcmN216N/wBo8JRUMbeE1Ze1jFuM+uSXwvy9DrqG3cNNXhiKLX/UivxPMJ9Hb8V46nyl0WzzsaPnU/D/AK9Ix3SLC01niKXZCW/L+GF2cvtLpVUqe7h4uEf8yaW+1+7FZR7Xd9hUwWwIx1a8TYww0F86S7Xf0Kr5pnxOuOIarBYO2bu23m3dtvi275myp0MtGZ96nH5m+xP1Y+1pfDHxzKFqEKL5Pw/FnyrVjHr9PEhVrt63/DwGGoyqSUKcN6T4LN/yRKO+ocnruWCpNy/pl3HfdC+jfsV7aqv2kl7qfyRf+pmbo50WjRtUrWlU1S+WHZzfWdMepptNx/K3rztRqOX418AAbWMAAAAAAAAAAAAAAAAAAAAAAAAZzW2+hlCteUP2U3xivdb64/lY6UEbUraNrQlW9qzvEvKsd0VxNLWO8vqhmvDVd5SjgJ8j2IrYjZ9KfxQi3ztZ+KMV9DE/1lrprJ/6h5OsBU+ln37BU4RZ6TPo/S+W68H6mKewHwn4x/mZ50eSF0aujz3+7qn0vzJLZ9T6ZeDO6lsasvh9m+9r8CK2NW/5fi/9pX/FyfpL+TRwywFT6X5n3+76n0vzO8jsSpxlDz/IlHo++M13R/mdjR5J+nP5VHAS2fU+l/ruIx2fUbsott8EnfwPSqWwaS+Lel2uy8EbCjh4QVoxUexJF1NBM/2lXbWx9Q4HZXQqrO0qz9nHkrOb/Bd/gdtsvZVLDx3aUbX1esn2sug3YsFMfkMmTNfJ7IAC5UAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAP/9k=" alt="" srcset="">
        <h3>Jamu Beras Kencur {{ n }}</h3>
        <p>Deskripsi singkat jamu produk {{ n }}.</p>
        <span class="price">Rp 12.000</span>
        <button class="btn btn-add-cart">Lihat Detail</button>
      </div>
      <div class="product-card neumorphism-card-small" >
        <img src="https://www.static-src.com/wcsstore/Indraprastha/images/catalog/full//106/MTA-53374687/jamu-bu-ratini_jamu-paitan-sambiloto-godog-jamu-paitan-sambiloto-rebus-500ml-1000ml_full01.jpg" alt="" srcset="">
        <h3>Jamu Paitan {{ n }}</h3>
        <p>Deskripsi singkat jamu produk {{ n }}.</p>
        <span class="price">Rp 11.000</span>
        <button class="btn btn-add-cart">Lihat Detail</button>
      </div>
      <div class="product-card neumorphism-card-small" >
        <img src="https://asset.kompas.com/crops/BHUd5qd_lpa9Ae-Zc1I-oAJ6g1k=/0x0:490x327/1200x800/data/photo/2023/05/01/644f83344bd06.png" alt="" srcset="">
        <h3>Jamu Temulawak {{ n }}</h3>
        <p>Deskripsi singkat jamu produk {{ n }}.</p>
        <span class="price">Rp 16.000</span>
        <button class="btn btn-add-cart">Lihat Detail</button>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: 'Product',
}
</script>

<style scoped>
.product-page-container {
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

.filter-bar {
    margin-bottom: 40px;
    padding: 15px 30px;
    text-align: center;
}

.neumorphism-card-flat {
  background: #f0f2f5;
  border-radius: 20px;
  box-shadow: 10px 10px 20px #d1d3d6, -10px -10px 20px #ffffff;
}

.btn-filter {
  border: none;
  padding: 8px 18px;
  border-radius: 12px;
  cursor: pointer;
  font-weight: 500;
  transition: all 0.3s ease;
  background-color: #f0f2f5;
  box-shadow: 5px 5px 10px #d1d3d6, -5px -5px 10px #ffffff;
  margin: 0 10px;
  color: #555;
}
.btn-filter:hover {
    color: #e6b800;
}
.btn-filter.active {
  color: #e6b800; /* Aksen kuning */
  box-shadow: inset 4px 4px 8px #d1d3d6, inset -4px -4px 8px #ffffff;
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 35px; /* Sedikit lebih besar */
}

.neumorphism-card-small {
  background: #f0f2f5;
  border-radius: 20px;
  padding: 25px;
  box-shadow: 9px 9px 18px #d1d3d6, -9px -9px 18px #ffffff;
  text-align: center;
  transition: transform 0.3s ease;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.neumorphism-card-small:hover {
    transform: scale(1.03);
    box-shadow: 12px 12px 24px #d1d3d6, -12px -12px 24px #ffffff;
}

.product-card img {
  max-width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 15px;
  margin-bottom: 15px;
  box-shadow: 6px 6px 12px #d1d3d6, -6px -6px 12px #ffffff;
}

.product-card h3 {
  margin: 10px 0 5px 0;
  color: #333;
  font-size: 1.1em;
}

.product-card p {
  color: #666;
  font-size: 0.85em;
  margin-bottom: 15px;
  line-height: 1.4;
  flex-grow: 1; /* Agar deskripsi mengisi ruang */
}

.price {
  color: #e6b800;
  font-weight: bold;
  font-size: 1.2em;
  display: block;
  margin-bottom: 20px;
}

.btn {
  border: none;
  padding: 10px 20px;
  border-radius: 15px;
  cursor: pointer;
  font-weight: bold;
  transition: all 0.3s ease;
  background-color: #f0f2f5;
  box-shadow: 6px 6px 12px #d1d3d6, -6px -6px 12px #ffffff;
  color: #555;
  width: 100%;
}
.btn:hover {
    box-shadow: inset 3px 3px 6px #d1d3d6, inset -3px -3px 6px #ffffff;
    color: #e6b800;
}
</style>