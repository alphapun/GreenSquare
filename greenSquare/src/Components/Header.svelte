<script>
    import Search from "./Search.svelte";
</script>
<header>
    <div class="logo">
        <img src="src\Assets\logo.png" alt="logo">
        <div class="name">Green<br/>Square</div>
    </div>
    <Search/>
    <div class="user">
        <img src="src/Assets/user.png" alt="user">
        <img src="src\Assets\cart.png" alt="cart">
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
    .user img{
        height: 30px;
    }
 </style>