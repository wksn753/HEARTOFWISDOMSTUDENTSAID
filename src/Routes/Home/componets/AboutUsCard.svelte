<script>
    export let title;
    export let text;
    export let image;
</script>

<div class="about-card">
    <div><img src={image} alt=""><h3 class="fs-600 fw-bold">{title}</h3></div>
    <p class="fs-500">{text}</p>
</div>

<style>
    .about-card{
        padding: 20px;
        border-radius: 10px;
        margin-bottom: 20px;
        width: 300px;
        padding: 0.5rem;
        transition: all 0.3s ease-in-out;
    }

</style>