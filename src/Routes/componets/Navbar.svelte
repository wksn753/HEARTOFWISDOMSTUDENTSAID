<script>
    import { Link } from "svelte-routing";
    import logo from "/logo.jpeg";

    let showMobbileMenu = false;
    let pages = ['Home', 'About', 'Programs', 'Contact'];
    let currentPage = pages[0];

    function setCurrentPage(page) {
        currentPage = page;
    }
    function handleMenuClick() {
        showMobbileMenu = !showMobbileMenu;
        const menu = document.querySelector("nav");
        menu.style.display = showMobbileMenu ? "block" : "none";
    }
</script>

<header class="primary-header">
    <div class="wd-100 padding16px">
        <div class="nav-wrapper">
            <Link to="/" class="nav-header nav-title"
                ><img  class="logo" src={logo} alt="" width={35} height={35} />
                <h1 class="fs-secondary-heading fw-bold">HEART OF WISDOM</h1></Link
            >
            <button
                class="mobile-nav-toggle"
                aria-controls="primary-navigation"
                aria-expanded="false"
                on:click={() => {
                    handleMenuClick();
                }}
            >
                <span class="material-symbols-outlined icon-hamburger">
                    {#if showMobbileMenu}
                        close
                    {:else}
                        menu
                    {/if}
                </span>
                <span class="material-symbols-outlined icon-close"> close </span>
                <span class="visually-hidden">Menu</span>
            </button>
            <nav
                id="primary-navigation"
                class={showMobbileMenu ? "opened" : "primary-navigation"}
            >
                <ul role="list" aria-label="Primary" class="nav-list">
                    <li class={currentPage==='Home'?"active nav-li":'nav-li'}>
                        <Link  to="/" on:click={()=>{currentPage='Home'}}>Home</Link>
                    </li>
                    <li class={currentPage==='About'?"active nav-li":'nav-li'}>
                        <Link  to="/about" on:click={()=>{currentPage='About'}}>About</Link>
                    </li>
                    <li class={currentPage==='Programs'?"active nav-li":'nav-li'}>
                        <Link  to="/programs" on:click={()=>{currentPage='Programs'}}>Programs</Link>
                    </li>
                    <li class={currentPage==='Donate'?"active nav-li":'nav-li'}>
                        <Link  to="/" on:click={()=>{currentPage='Donate'}}>Donate</Link>
                    </li>
                    <li class={currentPage==='Contact'?"active nav-li":'nav-li'}>
                        <Link  to="/contact" on:click={()=>{currentPage='Contact'}}>Contact</Link>
                    </li>
                </ul>
            </nav>
            <button class="button hide-on-mobile">Donate</button>
        </div>
    </div>
</header>

<style>
    nav ul {
        display: flex;
        justify-content: flex-end;
        align-items: center;
    }
    .nav-li > :global(a):hover {
        color: var(--clr-accent-400);
    }
    .nav-li > :global(a){
        text-decoration: none;
        transition: color 0.3s ease;
        color: #1a1a1a;

        display: flex;
        align-items: center;
        height: 100%;
        padding: 0 1.875rem;
    }
    
    .active > :global(a){
        color: var(--clr-accent-500) !important;
    }
    .logo{
        border-radius: 50%;
    }
    @media (max-width:50em) {
  .cardImage{
    order: -1;
  }
  .hide-on-mobile{
    display: none;
  }
  .primary-navigation{
    display: none;
  }
  .hide{
    display: none;
  }
  .primary-header[data-overlay]::before{
    content: "";
    position: fixed;
    inset: 0;
    background-image: linear-gradient(rgb(0 0 0 / 0),rgb(0 0 0 / 0.8));
  }
  .mobile-nav-toggle{
    display: block;
    cursor: pointer;
    background: transparent;
    border: 0;
    padding: 0.5em;
  }
  .mobile-nav-toggle .icon-close{
    display: none;
  }
  .opened{
    display: grid;
    position: fixed;
    inset: 7rem var(--size-400) auto;
    border-radius: var(--size-100);
    padding: var(--size-700);
    background: var(--clr-accent-100);
    box-shadow: 0 0 0.75em rgba(0, 0, 0, 0.15), 0 0 0 1000vmax rgba(0, 0, 0, 0.15);
  }
  .nav-list{
    display: grid;
    gap: var(--size-600);
    font-weight: var(--fw-bold);
    text-align: center;
    justify-content: center;
  }
  .nav-list li{
    width: 100%;
  }
  
}
    
</style>
