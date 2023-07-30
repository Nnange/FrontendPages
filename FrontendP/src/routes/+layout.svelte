<script>
    import "../app.css"
	import Header from "../components/Header.svelte";
    
</script>
<div class="container mx-auto">
    <Header />
    <div>
        <slot />    
    </div>

</div>