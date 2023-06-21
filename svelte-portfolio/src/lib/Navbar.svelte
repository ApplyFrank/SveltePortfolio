<script lang="ts">
    import { browser } from "$app/environment";

    export let position = 0

    let menu = false;

    const links: [string, string][] = [
        ["/#about", "About"], //why is there a # infront?
        ["/#experience", "Experience"],
        ["/#projects", "Projects"],
        ["/#contact", "Contact"]
    ]

    let scroll: boolean
    // $: if (browser) scroll = document.body.classList.contains("scroll") || position != 0;

</script>
<h1>Navbar</h1>