<script>
    import AboutUsCard from "../componets/AboutUsCard.svelte";
    import ObjectivesCard from "../componets/ObjectivesCard.svelte";
    import missionImage from "/mission.svg";
    import visionImage from "/vision.svg";
    import valuesImage from "/values.svg";

</script>

<section class="padding16px about-section">
    <div>
        <h2 class="fs-primary-heading fw-bold">About HOWSA</h2>
        <p class="herotext1">HEART OF WISDOM STUDENTS AID (HOWSA) UG LIMITED is a non-for-profit Christian-based charity in Uganda dedicated to supporting underprivileged school-going children. Our mission is to bridge the education gap and empower these children through financial assistance, educational resources, skill development, and moral guidance.</p>
    </div>
    <div class="even-coloumns wd-100">
        <AboutUsCard image={missionImage} title="Mission Statement" text="To bridge the education gap and empower school going underprivileged children through financial assistance educational resources, skill development and moral guidance to enable them become responsible citizens that will better their communities with the principles of God."/>
        <AboutUsCard image={visionImage} title="Vision" text="To bridge the education gap and empower underprivileged children acquire education through academic sponsorship, Advocacy, skilling, talent development, moral and spiritual guidance which will enable them become responsible citizens and to better their communities with the principles of God. o transform lives and societies through education and holistic development of underprivileged children and communities worldwide."/>
        <ObjectivesCard image={valuesImage}/>
    </div>
    <div>
        <h3 class="fs-800 fw-bold">Our Objectives</h3>
        <ul class="flow2 numbered-items" >
            <li>Provide support for less privileged students, covering school fees, scholastic materials, and other academic expenses.</li>
            <li>Safeguard students against threats to their mental, physiological, and spiritual wellbeing.</li>
            <li>Mentor and equip children with moral and spiritual values through the word of God.</li>
            <li>Identify, nurture, and develop children's innate skills, talents, and abilities.</li>
            <li>Work with institutions to improve education affairs.</li>
            <li>Transform vulnerable families and communities.</li>
        </ul>
    </div>
</section>

<style>
    .herotext1 {
        padding-block: 5px 2px;
    }
    .row-grid{
        display: grid;
    }
    .about-section{
        background-color: #10e7dc;
        color: white;
    }
</style>