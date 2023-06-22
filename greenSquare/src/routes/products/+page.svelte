<script>
	import { authUser } from '$lib/authStore';
  import { redirect } from '@sveltejs/kit';
 
  export const load = async () => {
  const unsubscribe = authUser.subscribe((user) => {
    if (!user) {
      throw redirect(302, '/login');
    }
  });
 
  unsubscribe();
 
  return {};
};
</script>

<section class="thumbnails">
    <img
      src="./images/vegetable list.jpg"
      alt="product"
      class="main-thumbnail invisible-mob"
    />
    <div class="mobile-thumb hidden">
      <img
        src="./images/vegetable list.jpg"
        class="thumb-mob"
        alt="product"
      />
      <button id="next">
        <img src="./images/icon-next.svg" alt="next" />
      </button>
      <button id="previous">
        <img src="./images/icon-previous.svg" alt="previos" />
      </button>
    </div>
    <div>
      <div class="preview">
        <img
          class="selected"
          src="./images/cabbage.jpg"
          alt=""
        />
        <img src="./images/organic tomatoes.jpg" alt="" />
        <img src="./images/ginger.jpg" alt="" />
        <img src="./images/carrot.jpg" alt="" />
      </div>
    </div>
  </section>
  <!-- content -->
  <section class="content">
    <p class="company">Chandran kumar</p>
    <h1 class="title">Homemade produce</h1>
    <p class="info">
      this years produce includes 20kg tomatoes,5kg ginger,20kg carrots and 20kg cabbage &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
      &nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 
      &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
      &nbsp; &nbsp; 
    </p>
    <div class="price">
      <div class="new-price">
        <p class="now">&#8377;125.00</p>
        
      </div>
     
    </div>
    <div class="buttons">
      
      <button class="add_btn">
        
        Add to cart
      </button>

      <button class="add_btn">
        
          Buy Now
        </button>


    </div>
  </section>

<!-- Lightbox -->
<div class="lightbox invisible">
<div class="lightbox-container">
  <button class="close-lightbox"><img src="./images/icon-close.svg" alt="close"></button>
  <img
    src="src/Assets/tomato.jpg"
    alt="product"
    class="main-thumbnail invisible-mob"
  />
  <div class="preview">
    <img
      class="selected"
      src="./images/image-product-1-thumbnail.jpg"
      alt=""
    />
    <img src="./images/image-product-2-thumbnail.jpg" alt="" />
    <img src="./images/image-product-3-thumbnail.jpg" alt="" />
    <img src="./images/image-product-4-thumbnail.jpg" alt="" />
  </div>
</div>
</div>
<style>
    @import url("https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@400;700&display=swap");
:root {
  --Orange: hsl(26, 100%, 55%);
  --Pale-orange: hsl(25, 100%, 94%);
  --Very-dark-blue: hsl(220, 13%, 13%);
  --Dark-grayish-blue: hsl(219, 9%, 45%);
  --Grayish-blue: hsl(220, 14%, 75%);
  --Light-grayish-blue: hsl(223, 64%, 98%);
  --White: hsl(0, 0%, 100%);
  /* (with 75% opacity for lightbox background) */
  --Black: hsl(0, 0%, 0%);
}
/* Default styles */
img {
  max-width: 100%;
}
/* visibility actions */
.hidden {
  display: none;
}
.invisible {
  display: none !important;
}
/* Navbar styles */

.thumbnails {
  display: flex;
  flex-direction: column;
  margin-top: 105px;

}
.main-thumbnail {
  border-radius: 10px;
  width: 1100px;
  cursor: pointer;
}
.preview {
  display: flex;
  gap: 1rem;
  margin-top: 2rem;
}
.preview img {
  width: 90px;
  border-radius: 10px;
  cursor: pointer;
}
.preview img:hover {
  opacity: 60%;
}

.selected {
  border: 2px solid var(--Orange);
  /*opacity: 50%;*/
}
.content {
  margin-left: 3rem;
}
.company {
  color: var(--Dark-grayish-blue);
  text-transform: uppercase;
  font-weight: 700;
  margin-bottom: 1rem;
}
.title {
  font-size: 2.5rem;
  margin-bottom: 2rem;
}
.info {
  color: var(--Dark-grayish-blue);
  line-height: 1.5;
  margin-bottom: 1rem;
}
.price {
  display: flex;
  flex-direction: column;
  gap: 0.6rem;
  margin-bottom: 1rem;
}
.new-price {
  display: flex;
  align-items: center;
}
.new-price p {
  font-size: 1.5rem;
  font-weight: 700;
}

.add_btn {
  cursor: pointer;
  width: 65%;
  margin-left: 1rem;
  background-color: var(--Orange);
  color: white;
  font-weight: 700;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.7rem;
  font-family: inherit;
  border: none;
  border-radius: 7px;
  padding: 1rem;
}
.add_btn:hover {
  opacity: 70%;
}

/* Lightbox styles */
.lightbox {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.75);
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
.lightbox-container {
  position: relative;
}
.close-lightbox {
  position: absolute;
  top: -40px;
  right: 10px;
  color: orange;
  background-color: transparent;
  border: none;
  cursor: pointer;
}
.close-lightbox:hover img {
  filter: sepia(100%) hue-rotate(-50deg) saturate(600%) contrast(1);
}
.close-lightbox img {
  width: 20px;
  height: 20px;
}
.lightbox .main-thumbnail {
  width: 400px;
}

@media screen and (max-width: 700px) {
  /* visibility actions */
  .hidden {
    display: flex;
  }
  .invisible-mob {
    display: none;
  }
  /* default styles */

  /* Navbar styles */

  .thumbnails {
    height: 40%;
  }
  .content {
    margin: 2rem;
    height: 50%;
  }
  .preview {
    display: none;
  }
  .mobile-thumb {
    position: relative;
    display: flex;
    overflow-x: hidden;
    min-width: 95vw;
    margin-top: -0.5rem;
    z-index: 1;
  }
  .mobile-thumb img {
    object-fit: cover;
    width: 100%;
    z-index: 1;
  }
  .title {
    font-size: 2.2rem;
  }
  .price {
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
  .buttons {
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }
  .add_btn {
    width: 100%;
    margin-left: 0;
  }
  #next {
    position: absolute;
    right: 10%;
    top: 50%;
    border: none;
    background-color: var(--White);
    width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    text-align: center;
    cursor: pointer;
    z-index: 10;
  }
  #previous {
    position: absolute;
    left: 10%;
    top: 50%;
    border: none;
    background-color: var(--White);
    width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    text-align: center;
    cursor: pointer;
    z-index: 10;
  }
  #previous img,
  #next img {
    width: 15px;
  }
}

</style>