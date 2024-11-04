<script lang="ts">
	import type { Snippet } from "svelte";


    interface UserInputInterface {
        children: Snippet
        userName: string
    }

    let {userName, children}: UserInputInterface = $props()
    let name = $state(userName)
</script>


<h1>Digite</h1>
<input type="text" bind:value={name}>
<p>{name}</p>

{@render children()}
