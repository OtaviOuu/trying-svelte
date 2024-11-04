<script lang="ts">
	import type { Snippet } from "svelte";

    interface slot {
        children: Snippet
    }

    import "../app.css";



    let {children}:slot = $props()
</script>

{@render children()}