<script>
    import hero_image from "/howsa3.jpeg";
</script>

<section class="padding16px even-coloumns herobackground">
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
        <button class="button margin-1rem">Donate</button>
    </div>
</section>

<style>
    @media(max-width:50em){
        .margin-1rem{
        margin-bottom: 1rem;
    }
    }
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
    .herobackground{
        padding-top: 12.5rem;
        padding-bottom: 12.5rem;
        background-color: #5a7c80;
        color: white;
        background-image: url("/howsa3.jpeg");
        background-blend-mode: multiply ;
        background-size: cover;
    }
</style>
