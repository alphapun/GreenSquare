<script>
	import { authHandlers } from './../store/store.js';
	import { fly } from 'svelte/transition';
    import Search from "./Search.svelte";
    let screenSize;
    let showNav = false;
    const handleClick = ()=>{
        // console.log("clicked");
        showNav = !showNav
    }
</script>
<svelte:window bind:innerWidth={screenSize} />
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<header>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <i class="fa fa-bars" id="fa-bars" style="font-size:24px" on:click={handleClick}></i>
    {#if showNav}
        {#if screenSize<1000}
            <div class="sidebar" transition:fly="{{ x:-100, duration: 1000 }}">
                <div class="item 1">Sign In</div>
                <a href="/products"><div class="item 2">Shop</div></a>
            </div>
        {/if}
    {/if}
    
    <div class="logo">
       <a href="/"><img src="src\Assets\logo.png" alt="logo"></a>
        <div class="name">Green<br/>Square</div>
    </div>
    <Search/>
    <div class="user">
        <a href="/login"><img src="src/Assets/user.png" alt="user"></a>
        <button on:click={authHandlers.logout}><img src="src\Assets\cart.png" alt="cart"></button>
    </div>  
</header>

<!--
    max width 1690px
    logo width 148px
    logo height 40px
    header will be 127 px
    on resizing after 796px
    - only logo should be there in the middle.
    - side menu bar almost 75% of the screen.
    - header will be 84 px
 -->
 <style>
    @import url('https://fonts.googleapis.com/css2?family=Amatic+SC:wght@700&display=swap');
    header{
        max-width: 90%;
        margin: auto;
        display: flex;
        align-items: center;
        justify-content: space-between;

    }
    #fa-bars{
        display: none;
    }
    .logo{
        max-height: 53px;
        max-width: 170px;
        display: flex;
        align-items: center;
    }
    .logo img{
        height: 50px;
    }
    .logo .name{
        font-family: 'Amatic SC', cursive;
        font-size: 20px;
    }
    .user{
        display: flex;
    }
    .user img{
        height: 30px;
        cursor: pointer;
    }
    .sidebar{
        background-color: rgb(106, 156, 106);
        left: 0;
        top: 50px;
        display: flex;
        flex-direction: column;
        align-items: center;
        align-content: space-between;
        gap: 30px;
        position: fixed;
        width: 100vw;
        /* height: calc(100vh - 60px); */
        height: 100vh;
        align-items: center;
        z-index: 100;
    }
    .sidebar .item{
        /* border: 2px solid blue; */
        font-size:2em;
    }
    @media (max-width:690px){
        .user{
            display: none;
        }
        .logo{
            margin: auto;
        }
        #fa-bars{
        display: block;
        }
    }
 </style>