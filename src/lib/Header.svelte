<script>
    import {page} from '$app/stores'
    const itemMenu = [
        {label: 'Inicio', path: '/',  },
        {label: 'Sobre', path: '/sobre',  },
        {label: 'Portfólio', path: '/portfolio',  },
        {label: 'Contato', path: '/contato',  }
    ]
</script>

<nav class="bg-white shadow dark:bg-dark-800">
    <div class="container flex items-center justify-center p-6 mx-auto text-gray-600 capitalize dark:text-gray-800">
        <a class="link-logo" href="/"><img src="carro.png" alt="logo do carro" class="logo-carro"/></a>
        {#each itemMenu as {label, path} }
        {#if $page.url.pathname === path} 
        <a href={path} class="text-gray-800 transition-colors duration-300 transform dark:text-gray-800 border-b-2 border-blue-500 mx-1.5 sm:mx-6">{label}</a>
        {:else}
        <a href={path} class="text-gray-800 transition-colors duration-300 transform dark:text-gray-800  mx-1.5 sm:mx-6">{label}</a>
        {/if}
        {/each}
    </div>
</nav>

<style>
    .link-logo {
        display: inline-block;
        
    }

    .logo-carro {
        height: 4rem;
        margin-right: 3rem;
    }


</style>