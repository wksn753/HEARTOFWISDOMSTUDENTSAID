<script>
    import OurProgramCard from "./componets/OurProgramCard.svelte";
    import howsa1 from "/educationImage.jpeg";
    import howsa2 from "/howsa2.jpeg";
    import howsa3 from "/howsa3.jpeg";

    function isEven(number) {
        if (number == 0) {
            return false;
        }
        if (number % 2 != 0) {
            return false;
        } else {
            return true;
        }
    }
    let services = [
        {
            title: "Educational Support",
            description:
                "Education is the cornerstone of our mission. We provide financial assistance for school fees, uniforms, and scholastic materials such as books, pens, and backpacks. This support ensures that children from vulnerable communities can attend school without financial barriers.",
            image: howsa1,
            id:"education"
        },
        {
            title: "Child Well-being",
            description:
                "We are committed to safeguarding the mental, physical, and spiritual health of children. Our programs include medical care, counseling, and spiritual mentorship to ensure children grow up healthy and resilient.",
            image: howsa2,
            id:"medical"
        },
        {
            title: "Community Sensitization and Outreach",
            description:
                "We conduct community sensitization and outreach programs to raise awareness about child development, protection, and care. These programs engage local leaders, parents, and guardians to create a supportive environment for children.",
            image: howsa3,
            id:"community"
        },
    ];
</script>

<section class="padding16px">
    <div class="">
        <h2 class="fw-bold fs-800">Programs</h2>
        <p class="programsIntro">
            At HEART OF WISDOM STUDENTS AID (HOWSA) UG LIMITED, we believe that
            every child deserves the opportunity to succeed. Our programs are
            designed to provide comprehensive support to underprivileged
            children, ensuring they have access to education, healthcare, and
            the tools necessary to develop their talents and skills. Explore our
            key programs and see how we are making a difference.
        </p>
    </div>
    <div>
        {#each services as service, index}
            {#if isEven(index + 1)}
                <OurProgramCard
                    serviceImage={service.image}
                    serviceTitle={service.title}
                    serviceText={service.description}
                    className="reversed {"blob"+(index+1)}"
                    id={service.id}
                />
            {:else}
                <OurProgramCard
                    serviceImage={service.image}
                    serviceTitle={service.title}
                    serviceText={service.description}
                    className={"blob"+(index+1)}
                    id={service.id}
                />
            {/if}
        {/each}
    </div>
</section>

<style>
    .programsIntro{
        padding: 1rem 0;
    }
</style>
