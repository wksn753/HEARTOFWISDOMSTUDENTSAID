<script>
    export let image;
    export let title;
    export let description;
</script>

<div class="even-coloumns">
    <div class="rounded">
        <img src={image} alt="">
    </div>
    <div>
        <h4 class="fw-bold">{title }</h4>
        <p>{ description }</p>
    </div>

</div>

<style>
    .rounded{
        border-radius: 10px;
        overflow: hidden;
    }
</style>