# [Kaptan Ege](https://crashentertainment.github.io/) [Privacy Policy](https://crashentertainment.github.io/privacypolicy)

<div style="text-align: center;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/wUXnHaUFbms?si=tPriBBIb1_EoFNSA" 
    title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    referrerpolicy="strict-origin-when-cross-origin" allowfullscreen>
  </iframe>
</div>

<style>
  /* Küçük resim stili */
  .thumbnail {
    width: 150px;  /* Küçük boyut */
    cursor: pointer;
    transition: 0.3s;
  }
  .thumbnail:hover {
    opacity: 0.8;
  }

  /* Modal arka planı */
  .modal {
    display: none; 
    position: fixed; 
    z-index: 1000; 
    padding-top: 60px; 
    left: 0; top: 0;
    width: 100%; height: 100%;
    overflow: auto; 
    background-color: rgba(0,0,0,0.8);
  }

  /* Modal içindeki büyük resim */
  .modal-content {
    margin: auto;
    display: block;
    max-width: 90%;
    max-height: 80%;
  }

  /* Kapatma butonu */
  .close {
    position: absolute;
    top: 30px;
    right: 35px;
    color: white;
    font-size: 40px;
    font-weight: bold;
    cursor: pointer;
  }
</style>

<!-- Küçük resim -->
<img id="myImg" class="thumbnail" src="images/pc.png" alt="Resim Açıklaması"> <img id="myImg" class="thumbnail" src="images/pc2.png" alt="Resim Açıklaması">

<!-- Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="imgBig">
</div>

<script>
  // Elemanları seç
  const modal = document.getElementById("myModal");
  const img = document.getElementById("myImg");
  const modalImg = document.getElementById("imgBig");
  const closeBtn = document.getElementsByClassName("close")[0];

  // Küçük resme tıklandığında modal açılır, büyük resim modalda gösterilir
  img.onclick = function(){
    modal.style.display = "block";
    modalImg.src = this.src;
  }

  // Kapatma butonuna tıklayınca modal kapanır
  closeBtn.onclick = function() {
    modal.style.display = "none";
  }

  // Modal dışına tıklayınca da kapatılabilir
  modal.onclick = function(event) {
    if(event.target === modal){
      modal.style.display = "none";
    }
  }
</script>

