<script>
    export let image;
    export let name;
    export let role;
</script>

<div>
    <div class="team-image">
        <img src={image} alt="">
    </div>
    <div>
        <p class="fw-bold fs-600">{name}</p>
        <p class="fs-500">{role}</p>
    </div>
</div>

<style>
    .team-image > img {
        border-radius: 0.5rem;
    }
</style>