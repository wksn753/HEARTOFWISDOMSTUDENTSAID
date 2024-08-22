<script>
    import OurWorkCard from "../componets/OurWorkCard.svelte";
    import howsa4 from "/howsa4.jpeg";
    import ourwork1 from "/Ourwork1.jpeg";
    import ourwork2 from "/OurWork2.jpeg";
    import ourwork3 from "/OurWork3.jpeg";
    import podAgency from "/podLogo.png";
    import dominionTakers from "/dominiontakers.jpeg"
</script>

<section class="padding16px">
    <h3 class="fw-bold fs-800">Our Programs</h3>
    <div class="even-coloumns wd-100">
        <OurWorkCard
            image={howsa4}
            title="Community Sensitization"
            description="Conducting outreaches to raise awareness about child development, protection, and care."
        />
        <OurWorkCard
            image={ourwork1}
            title="Educational Support"
            description="Providing school fees and scholastic materials like pens, books, and uniforms."
        />
        <OurWorkCard
            image={ourwork2}
            title="Skill Development"
            description="Skilling children during holidays in areas like tailoring, handcrafts, and baking."
        />
        <OurWorkCard
            image={ourwork3}
            title="Medical Care"
            description="Offering medical care for children in need."
        />
    </div>
    <div>
        <h3 class="fw-bold fs-800">Our Partners</h3>
        <p>Meet the organizations working with us to acheive our goals</p>
        <div class="even-coloumns">
            <div>
                <img src={podAgency} alt="" width="100" height="100" />
            </div>
            <div class="">
                <p class="fw-bold">The Pod Agency</p>
                <p>A design and digital marketing firm</p>
            </div>
        </div>
        <div class="even-coloumns">
            <div>
                <img src={dominionTakers} alt="" width="150" height="100" />
            </div>
            <div>
                <p class="fw-bold">Dominion takers</p>
                <p>A saving and credit group</p>
            </div>
        </div>
    </div>
</section>

<style>
</style>
