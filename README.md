# [Kaptan Ege](https://crashentertainment.github.io/)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Privacy Policy](https://crashentertainment.github.io/privacypolicy)

<div style="text-align: center;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/wUXnHaUFbms?si=tPriBBIb1_EoFNSA" 
    title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    referrerpolicy="strict-origin-when-cross-origin" allowfullscreen>
  </iframe>
</div>

<style>
  .image-container {
    display: flex;
    justify-content: center; /* Ortala */
    flex-wrap: wrap;         /* Taşarsa alt satıra geç */
    gap: 10px;               /* Resimler arası boşluk */
    margin-top: 20px;
  }

  .thumbnail {
    width: 150px;
    cursor: pointer;
    transition: 0.3s;
  }

  .thumbnail:hover {
    opacity: 0.8;
  }

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

  .modal-content {
    margin: auto;
    display: block;
    max-width: 90%;
    max-height: 80%;
  }

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

<!-- 📷 Resimlerin bulunduğu kapsayıcı -->
<div class="image-container">
 <img class="thumbnail" src="images/pc.png" alt="Resim 1">
 <img class="thumbnail" src="images/pc2.png" alt="Resim 2">
 <img class="thumbnail" src="images/pc3.png" alt="Resim 2">
 <img class="thumbnail" src="images/pc4.png" alt="Resim 2">
  <!-- İstersen daha fazla ekle -->
</div>

<!-- Modal -->
<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="imgBig">
</div>

<script>
  const modal = document.getElementById("myModal");
  const modalImg = document.getElementById("imgBig");
  const closeBtn = document.getElementsByClassName("close")[0];

  const thumbnails = document.querySelectorAll('.thumbnail');

  thumbnails.forEach(img => {
    img.onclick = function() {
      modal.style.display = "block";
      modalImg.src = this.src;
      modalImg.alt = this.alt;
    }
  });

  closeBtn.onclick = function() {
    modal.style.display = "none";
  }

  modal.onclick = function(event) {
    if(event.target === modal){
      modal.style.display = "none";
    }
  }
</script>



