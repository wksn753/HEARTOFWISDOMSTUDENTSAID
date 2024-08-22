<script>
    import TeamMember from "./componets/TeamMember.svelte";
    import heroImage from "/wholeteam.jpeg";
    import teamMember1 from "/team1.jpeg";
    import teamMember2 from "/team2.jpeg";
    import teamMember3 from "/team3.jpeg";
    import teamMember4 from "/team4.jpeg";
    import teamMember5 from "/team5.jpeg";
    import teamMember6 from "/team6.jpg";
    import teamMember7 from "/team7.jpeg";
    import teamMember8 from "/founder.jpg";
    import teamMember9 from "/admin.jpg";
    import teamMember10 from "/boardmember.jpg";
    import userPlaceHolder from "/placeholder.png";

    let showTeam = false;
    function onShowTeamClick() {
        showTeam = !showTeam;
    }
    let minimizedTeam = [
        {
            name: "Kiyingi Fredrick",
            role: "Executive director & Founder",
            image: teamMember8,
        },
        {
            name: "Mwebaze Becky Mary",
            role: "Administration, Ethics & Integrity",
            image: teamMember9,
        },
        {
            name: "Council Serwanga Alex",
            role: "Governance,HR,Legal,Policy Expert",
            image: teamMember3,
        },
    ];

    let maximizedTeam = [
        {
            name: "Kiyingi Fredrick",
            role: "Executive director & Founder",
            image: teamMember8,
        },
        {
            name: "Mwebaze Becky Mary",
            role: "Administration, Ethics & Integrity",
            image: teamMember9,
        },
        {
            name: "Council Serwanga Alex",
            role: "Governance,HR,Legal,Policy Expert",
            image: teamMember3,
        },
        {
            name: "Counsel Solomon Opolot",
            role: "Legal Advisor",
            image: teamMember1,
        },
        {
            name: "Ssebuyira Isaac kitiibwa",
            role: "Board Of Trustees",
            image: teamMember2,
        },
        {
            name: "Namugerwa Bridget",
            role: "Board Of Trustees",
            image: teamMember10,
        },
        { name: "Mubiru Derrick", role: "Secretary", image: teamMember4 },
        {
            name: "Nwadde Jeoffrey",
            role: "Donor's relations, communication and data management specialist",
            image: teamMember5,
        },
        {
            name: "Nabbanja Racheal",
            role: "Child development, rights and well fare expert",
            image: teamMember6,
        },
        {
            name: "Namutu Martha",
            role: "Education & Child Development Expert",
            image: teamMember7,
        },
        { name: "Kusiima Darlison", role: "Finance", image: userPlaceHolder },
    ];
    $: team = showTeam ? maximizedTeam : minimizedTeam;
</script>

<section class="padding16px">
    <div class="even-coloumns">
        <div>
            <div><h2 class="fs-secondary-heading fw-bold">About</h2></div>
            <p class="image-with-blob-bg">
                HEART OF WISDOM STUDENTS AID (HOWSA) UG LIMITED is a dedicated
                non-profit Christian-based charity located in Kampala, Uganda.
                We are committed to providing essential support to
                underprivileged school-going children, including orphans, street
                children, those with disabilities, and financially struggling
                students. Our goal is to ensure these children have access to
                quality education and the necessary resources to thrive. The
                company is as a result of the burden that God place on the heart
                of Mr. Kiyingi Fredrick while he was still pursuing his
                bachelor’s degree at Makerere University seeing many students
                struggling with tuition while he was still at the university and
                throughout his academic journey because he had also gone through
                the same struggles of poverty, hopelessness, tuition challenges
                during his primary and secondary school level studying on the
                mercies and assistance of good-hearted people. In January 2024
                HOWSA-UG became operational with beneficiaries from kasese
                district which is found in western part of Uganda after the
                C.E.O being driven with compassion seeing many children dropping
                out of school, others with no hope of attending school after the
                loss of their beloved ones in ADF war attacks in the land,
                landslides, natural death, early pregnancies and others lacking
                support to pursue education while he was practicing his forestry
                profession activities with the local communities in Kasese
                district in 2023. Usually, the district of kasese faces a lot of
                challenges ranging from landslides, hunger, early marriages,
                producing a lot of children, unemployment to ADF caused civil
                wars and most children in different villages end up with no
                assistance after the loss of their beloved ones, drop out of
                school and the poverty circle. After seeing the need and the
                suffering of many orphaned children and families, HOWSA UG
                intervened to revive the future of these children through
                academic sponsorship, mentorship, skilling, spiritual growth,
                develop their gifts and talents, advocating for their rights and
                promote community development as the objectives of the company.
                The company went on to other parts of the country like
                Butambala, islands of Ggolo and other parts of central Uganda to
                offer similar support to less advantaged children, hope to
                families and support to marginalized communities. At the moment
                we have a total of 50 beneficiaries that we are support at
                primary and secondary level in the different parts of the
                country in the identified vulnerable communities. For the first
                time we have seen, a smile on their faces and a hope for their
                better future. Our beneficiaries include; Orphaned children from
                poor back ground who lack financial means to pursue education,
                School dropouts, Street children who are deprived of access to
                education due to their circumstances, Children with
                disabilities, financially struggling children, Schools and
                higher learning institutions, Organized community gender-based
                groups, Refugees and Project affected communities. We are happy
                to be a life and community transforming company that extends the
                love of God to many less advantaged children through our
                inclusive education sponsorship and society development programs
                to make everyone in different communities in each generation to
                profit.
            </p>
        </div>
        <div class="rounded">
            <img src={heroImage} alt="" />
        </div>
    </div>
    <div>
        <h3 class="fw-bold fs-secondary-heading">Team</h3>
        <div class="team-grid">
            {#each team as member}
                <TeamMember
                    image={member.image}
                    name={member.name}
                    role={member.role}
                />
            {/each}
        </div>
        <div>
            {#if !showTeam}
                <button class="button" on:click={onShowTeamClick}
                    >Show Team</button
                >
            {:else}
                <button class="button" on:click={onShowTeamClick}>Hide</button>
            {/if}
        </div>
    </div>
    <div class="spacer"></div>
    <div>
        <h3 class="fs-secondary-heading fw-bold">Frequently Asked Questions</h3>
    </div>
</section>

<style>
    @media (min-width: 51em) {
        .team-grid {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 1rem;
        }
    }
    .rounded > img {
        border-radius: 0.5rem;
    }
    .image-with-blob-bg::before {
        content: "";
        position: absolute;
        top: 30%;
        right: 72%;
        width: 39%;
        aspect-ratio: 1/1.3;
        z-index: -1;
        background-image: url("/blob2.svg");
        background-repeat: no-repeat;
        background-position: top left;
    }
    .spacer{
        margin-top: 1rem;
    }
</style>
