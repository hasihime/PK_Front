<script>
    import {page} from '$app/stores';
    console.log*($page.params.slug);

    const slugArr=$page.params.slug.split('/');
    console.log($page.params);
    const {lang = 'kr'}=$page.params;

</script>

{#if lang === 'kr'}
    <h1>안녕</h1>
{:else if lang ==='en'}
    <h1>hello</h1>
{:else if lang ==='jp'}
    <h1>こんにちは。</h1>
{/if}




{#if slugArr.length===1}
<h1>Docs 페이지; 주제 {slugArr[0]}</h1>
{:else if slugArr.length ===2}
<h1>Docs 페이지; 주제 {slugArr[0]}; 소주제 : {slugArr[1]}</h1>
{/if} 