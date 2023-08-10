<script>
    import Footer from '../Components/Footer.svelte';
    import CardsCat from '../Components/cardsCat.svelte';
</script>
<div class="cover">
    <div class="text">Empowering Communities,<br/>Promoting Sustainability: Your One-Stop Destination for Local,<br/>Organic, and Preloved Treasures!</div>
    <a href="/faq"><button class="lm">Learn More</button></a>
</div>
<div class="intro">
    <div class="content">
        <h3>Why are we the best?</h3>
        <p>We make everyone more easier to sell their products as well as buy them. No need of middle men .
         Not only fruits and veggies , sell any items that you produce . Support your local producers directly !!!</p>
         <br>
        <a href="/products">Try Now>></a>
    </div>
</div>
<CardsCat/>
<style>

@import url('https://fonts.googleapis.com/css2?family=Anton&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Geologica:wght@100;200;300;400;500;600;700;800;900&display=swap');
    *{
        padding: 0;
        margin: 0;
        box-sizing: border-box;
    }
    .cover{
        /* display: flex;
        flex-direction: column;
        align-items: center; */
        justify-content: center;
        width: 100vw;
        height: calc(100vh - 56px);
        background: url('src/Assets/asp.jpg');
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
    }
    .cover .text{
        /* transform: translate(10%,350%); */
        padding-top: 15%;
        padding-left: 5%;
        color: antiquewhite;
        font-size: 6vh;
        font-family: 'Anton', sans-serif;   
    }
    .cover .lm{
        width: 109px;
        height: 38px;
        background: antiquewhite;
        margin-top: 9%;
        margin-left: 45%;
       
        font-family: 'Inter', sans-serif;
        font-size: 17px;
        font-weight: 400;
        border-radius: 23.1193px;
        color: black;
        border: 0px;
    }
    .lm:hover{
        color: antiquewhite;
        background-color: transparent;
        border: 2px solid antiquewhite;
    }
    .intro{
        padding: 3.5%;
        /* height: 40vh; */
        display: flex;
        width:95%;
        margin: 2% auto;
        background-image: url("src/Assets/back.jpg");
        opacity: 0.9;
        border-radius: 13px;
    }
    
    .intro h3 {
        font-family: 'Geologica', sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 32px;
        line-height: 48px;
        color: whitesmoke;
    }
    
    .intro p{
        margin-top: 1%;
        font-family: 'Geologica', sans-serif;
        font-style: normal;
        font-weight: 500;
        font-size: 21px;
        line-height: 32px;
        color:antiquewhite;
    }
    .intro a{
        margin-top: 5%;
        padding: 2px;
        font-family: 'Geologica', sans-serif;
        font-style: normal;
        font-weight: 500;
        font-size: 21px;
        line-height: 32px;
        color:antiquewhite;
        border: 2px solid antiquewhite;
        border-radius: 5px;
    }
     /* @media (max-width:1280px){
        .intro img{
            height: 22vw;
            left:75%;
            top: -5%
        }
    }
    @media (max-width:1048px){
        .intro img{
            height: 24vw;
            left:75%;
            top: -5%
        }
    }
    @media (max-width:800px){
        .intro img{
            height: 24vw;
            left:50%;
            top: -5%
        }
    } */
    @media (max-width:1000px){
        .cover{
            height: 30rem;
        }
        .cover .text{
            font-size: 30px;
        }
    }
    @media (max-width:450px){
        .cover .lm{
            margin-left: 35%;            
        }
    }
</style>
<Footer/>