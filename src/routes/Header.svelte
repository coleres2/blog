<script lang="ts">
    import logo from '$lib/images/logo2.png';
    export let onToggleSidebar: any;
    function onKeyDown() {
        // ana  logous logic to onClick, but check if `Enter` (and no modifier) was pressed
    }
</script>
<header>
    <div class="bar"></div>
    <div class="corner">
        <button 
            class="hamburger" 
            tabindex="0" 
            on:click={onToggleSidebar}
        >
            <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 36 36" fill="currentColor">
                <path d="M0 0h30v4H0zM0 13h30v4H0zM0 26h30v4H0z"/>
            </svg>
        </button>
    </div>
    <div class="center">
        <img src={logo} alt="logo">
    </div>
</header>

<style>
    header {
        /* //display: flex; */
        width : 100%;
        position: fixed;
        text-align: center;
    }

    .corner {
            
            position: absolute;
            top: 0;
            left: 0;  
    }
    
    .bar {
        display: block;
        position: fixed;
        z-index: -1;
        top: 0;
        left: 0;
        width: 100%;
        height: 60px;
        background-color: rgb(111, 0, 255);
    }
    
    .center {
        text-align: center;
        display: inline-block;
        margin: auto;
        justify-content: center;
        object-fit: contain;
    }
    .center img {
        /* display: block; */
        /* //margin: 0 auto; */
        width: 140px; /* Set the width of the logo */
        height: auto; /* Set the height of the logo */
       
    }

    /* .hamburger {
        fill: white;
        stroke: white;
        stroke-width: 3;
        stroke-linecap: round;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        left: 20px;
        width: 25px;
        height: 25px;
        z-index: 2;
        border:red;
    } */
    .hamburger {
        display: inline-block;
        cursor: pointer;
        
        padding-right: 1rem;
        margin-left: 1rem;
        margin-top: 1rem;
    }
    
    svg {
        fill: white;
    }

</style>
   
   
   