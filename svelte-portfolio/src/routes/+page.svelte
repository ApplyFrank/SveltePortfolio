<script lang="ts">
    import type { Writable } from "svelte/store"

    import About from "../lib/index/About.svelte"
    import Experience from "../lib/index/Experience.svelte"
    import Projects from "../lib/index/Projects.svelte"
    import Contact from "../lib/index/Contact.svelte"
    import Navbar from "../lib/Navbar.svelte"
    import { browser } from "$app/environment"
	import { bind } from "svelte/internal"

    let mount = browser

    const sections = ["about", "experience", "projects", "contact"];

    let position: Writable<number>;
    let active: { [key: number]: boolean } = {}

</script>

<svelte:head>
    <title>FrankIsCool</title>
</svelte:head>

{#each sections as section}<div id={section} />{/each}


<div class="wrapper" class:mount>
    <!-- <Navbar bind:position={$position} /> -->
    <main class="h-screen">
        <About />
        <Experience />
        <Projects />
        <Contact />
    </main>
</div>