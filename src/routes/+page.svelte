<script lang="ts">
    import Header from './Header.svelte';
    import Sidebar from './Sidebar.svelte';
    let isSidebarOpen = false;
    function toggleSidebar() {
        isSidebarOpen = !isSidebarOpen;
    }
</script>

<Header onToggleSidebar={toggleSidebar}/>

<Sidebar isOpen={isSidebarOpen} toggle={toggleSidebar} />

<svelte:head>
    <title>Cole's Website</title>
    <meta name="description" content="Cole's Website">
</svelte:head>

<section>
    <h1>Welcome to SvelteKit</h1>
    <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
</section>
<body>
    
</body>
<style>
    section {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        min-height: 100vh;
        text-align: center;
    }
    .icon {
        position: absolute;
        top: 0%;
        transform: translate(-50%, -38%);
        /* scale: .3; */
        left: 50%;
        height:auto;
        z-index: 2;
        /* border: 1px solid red; */
    }
/* .img-search {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    right: 20px;
    width: 25px;
    height: 25px;
    z-index: 2;
} */
img {
    position: relative;
    max-width: 100%;
    height: auto;
  }
</style>