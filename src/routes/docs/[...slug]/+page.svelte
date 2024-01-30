<script>
    import {page} from '$app/stores';
    console.log*($page.params.slug);

    const slugArr=$page.params.slug.split('/');
</script>

<h1>Docs Page</h1>

{#if slugArr.length===1}
<h1>Docs 페이지; 주제 {slugArr[0]}</h1>
{:else if slugArr.length ===2}
<h1>Docs 페이지; 주제 {slugArr[0]}; 소주제 : {slugArr[1]}</h1>
{/if}