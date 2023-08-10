<script>
	import { auth, db } from './../lib/firebase/firebase.js';
	import Footer from './../Components/Footer.svelte';
  import Header from './../Components/Header.svelte';
  import "../app.postcss";
  import "../app.css";
  import { onMount } from 'svelte'; 
  
  const nonAuthRoutes = ['/','/login']

  onMount(()=>{
    console.log('mounting');
    const unsubscirbe = auth.onAuthStateChanged(async user =>{
      const currentPath = window.location.pathname

      if(!user && !nonAuthRoutes.includes(currentPath)){
        window.location.href = '/';
        return;
      }
      if (user && currentPath === "/login") {
        window.location.href = '/';
        return;
      }
      if (!user){
        return;
      }
    })

  })
</script>
<Header/>
<slot />
