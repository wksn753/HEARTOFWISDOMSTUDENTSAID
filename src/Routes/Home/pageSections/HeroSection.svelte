<script>
    import hero_image from "/howsa3.jpeg";
</script>

<section class="padding16px even-coloumns ">
    <div>
        <h2 class="fs-primary-heading fw-bold">
            Transforming Lives Through Education.
        </h2>
        <p class="txt-alin-justified  herotext1 image-with-blob-bg">
            Empowering Uganda's Future HOWSA UG LTD is a Christian non-profit
            dedicated to uplifting underprivileged children in Uganda. We
            support orphaned, disabled, and financially struggling children by
            funding education, providing school supplies, nurturing talents, and
            instilling Godly values. Join us in creating brighter futures
            through education and holistic development.
        </p>
        <p class="fw-bold">Support Our Mission Today!</p>
        <div class="herotext1"></div>
        <button class="button">Donate</button>
    </div>
    <div class="heroImage">
        <img src={hero_image} alt="" class="" />
    </div>
</section>

<style>
    .heroImage > img {
        border-radius: 1rem;
    }
    .herotext1 {
        padding-block: 5% 2%;
    }
    .image-with-blob-bg::before {
        content: "";
        position: absolute;
        top: 30%;
        right: 72%;
        width: 39%;
        aspect-ratio: 1/1.3;
        z-index: -1;
        background-image: url("/sideBlob.svg");
        background-repeat: no-repeat;
        background-position: top left;
    }
</style>
