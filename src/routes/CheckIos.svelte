<script>
    import { onMount } from "svelte";


    let mql;
    let mqlListener;
    let wasMounted = false;
    let matches = false;

    const ios = navigator.userAgent || navigator.vendor;
    
    matches = /iPad|iPhone|iPod/.test(ios);
</script>

<slot {matches} />
