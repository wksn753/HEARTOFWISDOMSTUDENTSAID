<script>
  import { Router, Route } from "svelte-routing";
  import Home from "./Routes/Home/Home.svelte";
  import About from "./Routes/About/About.svelte";
  import OurWork from "./Routes/OurWork/OurWork.svelte";
  import Contact from "./Routes/Contact/Contact.svelte";
  import Navbar from "./Routes/componets/Navbar.svelte";
  import Footter from "./Routes/componets/Footter.svelte";


  export let url = "";
</script>

<Router>
  <Navbar/>
  <main class="ht-100vh">
    <Route path="/" component={Home} />
    <Route path="/about" component={About} />
    <Route path="/programs" component={OurWork} />
    <Route path="/contact" component={Contact} />
  </main>
  <Footter/>
</Router>

<style>
</style>
