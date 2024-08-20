<script>
    export let serviceImage;
    export let serviceTitle;
    export let serviceText;
    export let className = "";
    export let id ;
</script>
    <div id={id} class={"even-coloumns"}>
        <div class="heroImage">
                <img src={serviceImage} alt="services" />
        </div>
        <div class={"service-text flow "+className}>
                <h3 class="fs-800 fw-bold">{serviceTitle}</h3>
                <p class="fs-700">{serviceText}</p>
        </div>
    </div>

<style>
    @media (min-width:51em){
        .reversed {
        order: -1;
    }
    }
    .heroImage > img {
        border-radius: 0.5rem;
    }
    .blob1::before {
        content: "";
        position: absolute;
        top: 40%;
        left: 52%;
        width: 39%;
        aspect-ratio: 1/1.3;
        z-index: -1;
        background-image: url("/sideBlob.svg");
        background-repeat: no-repeat;
        background-position: top left;
    }
    .blob2::before {
        content: "";
        position: absolute;
        top: 85%;
        right: 62%;
        width: 39%;
        aspect-ratio: 1/1.3;
        z-index: -1;
        background-image: url("/blob2.svg");
        background-repeat: no-repeat;
        background-position: bottom left;
    }
    .blob3::before {
        content: "";
        position: absolute;
        top: 30%;
        left: 72%;
        width: 39%;
        aspect-ratio: 1/1.3;
        z-index: -1;
        background-image: url("/blob3.svg");
        background-repeat: no-repeat;
        background-position: bottom right;
    }
</style>
