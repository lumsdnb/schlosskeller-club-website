<script>
    import { onMount } from "svelte";

    let matches;
    let ios;
    onMount(() => {
        ios = navigator.userAgent || navigator.vendor;
        matches = /iPad|iPhone|iPod/.test(ios);
    });
</script>

<slot {matches} />
