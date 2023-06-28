<h2>Meet the Developers</h2>

<div class="carousel">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="src\Assets\person.jpg" alt="Developer 1">
        <h3>Eby Kurian</h3>
        <p>example@gmail.com</p>
      </div>
      <div class="carousel-item">
        <img src="src\Assets\person.jpg" alt="Developer 2">
        <h3>Gautham Suresh</h3>
        <p>example@gmail.com</p>
      </div>
      <div class="carousel-item">
        <img src="src\Assets\person.jpg" alt="Developer 3">
        <h3>Ebin J Alapatt</h3>
        <p>example@gmail.com</p>
      </div>
    </div>
</div>

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Geologica:wght@100;200;300;400;500;600;700;800;900&display=swap');

    h2{
        margin-left: 3%;
        font-size: 30px;
        font-family: 'Geologica', sans-serif;
    }
    .carousel {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 30px;
    }

    .carousel-inner {
        display: flex;
        transition: transform 0.5s ease-in-out;
        gap: 15rem;
    }

    .carousel-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    width: 100%;
    height: 100%;
    }

    .carousel-item img {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    margin-bottom: 10px;
    }

    .carousel h3 {
    font-size: 20px;
    margin-bottom: 5px;
    }

    .carousel p {
    font-size: 16px;
    color: #888;
    }
    @media(max-width: 927px ){
        .carousel-inner {
        gap: 100px;
        overflow-x: auto;
    }
    }
</style>