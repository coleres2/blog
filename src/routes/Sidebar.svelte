<script lang="ts">
    import { createEventDispatcher } from 'svelte';
    import '../app.postcss';
    import { page } from '$app/stores';
    import { onMount } from 'svelte';
    import {
        Navbar,
        NavBrand,
        NavLi,
        NavUl,
        NavHamburger,
        Sidebar,
        SidebarGroup,
        SidebarItem,
        SidebarWrapper,
        Drawer,
        CloseButton,
        SidebarDropdownWrapper
    } from 'flowbite-svelte';
    //import { Cog } from 'svelte-heros-v2';
    import { sineIn } from 'svelte/easing';
    export let isOpen:boolean;
    export let toggle: () => void;
    let sidebarWidth = 300;
    let m = { x: 0, y: 0 };
    function closeSidebar(event:MouseEvent) {
		m.x = event.clientX;
        if(m.x > sidebarWidth) {
            toggle();
        }
	}
    
    console.log(m.x);
    //let breakPoint = sidebar.width;
    // function toggle() {
    //   isOpen = !isOpen;
    // }
    
  </script>
<wrapper>
<div class="sidebar" class:open={isOpen} class:close={!isOpen}>
    <ul>
        <li><button on:click={toggle}>Click me</button></li>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Projects</a></li>
        <li><a href="#">Blog</a></li>
        
    </ul>
    </div>
    <button
    class = "not-sidebar"
    class:open={isOpen}
    > </button>
</wrapper>
  
  
  
  <style>
    .sidebar {
        position: fixed;
        top: 0;
        left: -300px;
        width: 300px;
        height: 100vh;
        background-color: rgb(255, 255, 255);
        transition: transform 0.3s ease-in-out;
        z-index: 9999;
    }

    .not-sidebar {
        position: fixed;
        top: 0;
        left: -300px;
        width: 100%;
        height: 100%;
        display:none;
        z-index: 9998;
    }
  
    .open {
      transform: translateX(300px);
    }
    .close {
      transform: translateX(-300px);
    }
    
  </style>
  