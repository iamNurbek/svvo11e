<script>
// @ts-nocheck
    export let panelContent = ''
    export let isOpen
    export let panelID
    export let labeledBy;
</script>


<div 
    class='accordion-panel' 
    role="region" 
    class:open-panel={isOpen} 
    id="{panelID}"
    aria-labelledby={labeledBy}
>
{#if isOpen}
    <p>{panelContent}</p>
{/if}
</div>

<style>

    .accordion-panel {
        height: 0;
        width: 100%;
    }

    .open-panel {
        height: auto;
        border: solid 1px black;
    }

</style>