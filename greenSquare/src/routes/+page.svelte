<script>
	import Header from './../Components/Header.svelte';
</script>
<Header/>
<div class="cover">
    <div class="text">Empowering Communities,<br/>Promoting Sustainability: Your One-Stop Destination for Local,<br/>Organic, and Preloved Treasures!</div>
    <button class="lm">Learn More</button>
</div>

<style>

@import url('https://fonts.googleapis.com/css2?family=Anton&display=swap');
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