
<script>
    // const productContainers = [...document.querySelectorAll('.product-container')];
//     const nxtBtn = [...document.querySelectorAll('.nxt-btn')];
//     const preBtn = [...document.querySelectorAll('.pre-btn')];

//     productContainers.forEach((item, i) => {
//     let containerDimensions = item.getBoundingClientRect();
//     let containerWidth = containerDimensions.width;

//     nxtBtn[i].addEventListener('click', () => {
//         item.scrollLeft += containerWidth;
//     })

//     preBtn[i].addEventListener('click', () => {
//         item.scrollLeft -= containerWidth;
//     })
// })
</script>

<section class="product"> 
    <h2 class="product-category">Products Near you</h2>
    <!-- <button class="pre-btn"><img src="src\Assets\right.png" alt="PREV"></button>
    <button class="nxt-btn"><img src="src\Assets\right.png" alt="NEXT"></button> -->
    <div class="product-container">
        <div class="product-card">
            <div class="product-image">
                <img src="src\Assets\tomato.jpg" class="product-thumb" alt="">
                <button class="card-btn">add to wishlist</button>
            </div>
            <div class="product-info">
                <h2 class="product-brand">brand</h2>
                <span class="price">$20</span>
            </div>
        </div>
        <div class="product-card">
            <div class="product-image">
                <img src="src\Assets\tomato.jpg" class="product-thumb" alt="">
                <button class="card-btn">add to wishlist</button>
            </div>
            <div class="product-info">
                <h2 class="product-brand">brand</h2>
                <span class="price">$20</span>
            </div>
        </div>
        <div class="product-card">
            <div class="product-image">
                <img src="src\Assets\tomato.jpg" class="product-thumb" alt="">
                <button class="card-btn">add to wishlist</button>
            </div>
            <div class="product-info">
                <h2 class="product-brand">brand</h2>
                <span class="price">$20</span>
            </div>
        </div>
        <div class="product-card">
            <div class="product-image">
                <img src="src\Assets\tomato.jpg" class="product-thumb" alt="">
                <button class="card-btn">add to wishlist</button>
            </div>
            <div class="product-info">
                <h2 class="product-brand">brand</h2>
                <span class="price">$20</span>
            </div>
        </div>
        <div class="product-card">
            <div class="product-image">
                <img src="src\Assets\tomato.jpg" class="product-thumb" alt="">
                <button class="card-btn">add to wishlist</button>
            </div>
            <div class="product-info">
                <h2 class="product-brand">brand</h2>
                <span class="price">$20</span>
            </div>
        </div>
        <div class="product-card">
            <div class="product-image">
                <img src="src\Assets\tomato.jpg" class="product-thumb" alt="">
                <button class="card-btn">add to wishlist</button>
            </div>
            <div class="product-info">
                <h2 class="product-brand">brand</h2>
                <span class="price">$20</span>
            </div>
        </div>
        <div class="product-card">
            <div class="product-image">
                <img src="src\Assets\tomato.jpg" class="product-thumb" alt="">
                <button class="card-btn">add to wishlist</button>
            </div>
            <div class="product-info">
                <h2 class="product-brand">brand</h2>
                <span class="price">$20</span>
            </div>
        </div>
        <div class="product-card">
            <div class="product-image">
                <img src="src\Assets\tomato.jpg" class="product-thumb" alt="">
                <button class="card-btn">add to wishlist</button>
            </div>
            <div class="product-info">
                <h2 class="product-brand">brand</h2>
                <span class="price">$20</span>
            </div>
        </div>
        <div class="product-card">
            <div class="product-image">
                <img src="src\Assets\tomato.jpg" class="product-thumb" alt="">
                <button class="card-btn">add to wishlist</button>
            </div>
            <div class="product-info">
                <h2 class="product-brand">brand</h2>
                <span class="price">$20</span>
            </div>
        </div>
        <div class="product-card">
            <div class="product-image">
                <img src="src\Assets\tomato.jpg" class="product-thumb" alt="">
                <button class="card-btn">add to wishlist</button>
            </div>
            <div class="product-info">
                <h2 class="product-brand">brand</h2>
                <span class="price">$20</span>
            </div>
        </div>
    </div>
</section>

<style>
    
.product {
  position: relative;
  overflow: hidden;
  padding: 20px;
}

.product-category {
  font-size: 30px;
  font-weight: 500;
  margin-bottom: 40px;
  text-transform: capitalize;
}

.product-container {
  display: flex;    
  overflow-x: auto;
  scroll-behavior: smooth;
}

.product-container::-webkit-scrollbar {
  display: none;
}

.product-card {
  flex: 0 0 auto;
  width: 250px;
  height: 450px;
  margin-right: 40px;
}

.product-image {
  position: relative;
  width: 100%;
  height: 350px;
  overflow: hidden;
}

.product-thumb {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card-btn {
  position: absolute;
  bottom: 10px;
  left: 50%;
  transform: translateX(-50%);
  padding: 10px;
  width: 90%;
  text-transform: capitalize;
  border: none;
  outline: none;
  background: #fff;
  border-radius: 5px;
  transition: 0.5s;
  cursor: pointer;
  opacity: 0;
}

.product-card:hover .card-btn {
  opacity: 1;
}

.card-btn:hover {
  background: #ff7d7d;
  color: #fff;
}

.product-info {
  width: 100%;
  height: 100px;
  padding-top: 10px;
}

.product-brand {
  text-transform: uppercase;
}

.price {
  font-weight: 900;
  font-size: 20px;
}


/* .pre-btn,
.nxt-btn {
  border: none;
  width: 10vw;
  height: 100%;
  position: absolute;
  top: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(90deg, rgba(255, 255, 255, 0) 0%, #fff 100%);
  cursor: pointer;
  z-index: 8;
} */

</style>
