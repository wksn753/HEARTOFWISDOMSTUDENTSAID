<script>
    import TeamMember from "./componets/TeamMember.svelte";
import heroImage from "/howsa3.jpeg";
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
    function onShowTeamClick(){
        showTeam = !showTeam;
    }
    let minimizedTeam = [{"name": "Kiyingi Fredrick","role":"Executive director & Founder","image":teamMember8},{"name": "Mwebaze Becky Mary","role":"Administration, Ethics & Integrity","image":teamMember9},{"name": "Council Serwanga Alex","role":"Governance,HR,Legal,Policy Expert","image":teamMember3}]

    let maximizedTeam = [{"name": "Kiyingi Fredrick","role":"Executive director & Founder","image":teamMember8},{"name": "Mwebaze Becky Mary","role":"Administration, Ethics & Integrity","image":teamMember9},{"name": "Council Serwanga Alex","role":"Governance,HR,Legal,Policy Expert","image":teamMember3},{"name": "Counsel Solomon Opolot","role":"Legal Advisor","image":teamMember1},{"name": "Ssebuyira Isaac kitiibwa","role":"Board Of Trustees","image":teamMember2},{"name": "Namugerwa Bridget","role":"Board Of Trustees","image":teamMember10},{"name": "Mubiru Derrick","role":"Secretary","image":teamMember4},{"name": "Nwadde Jeoffrey","role":"Donor's relations, communication and data management specialist","image":teamMember5},{"name": "Nabbanja Racheal","role":"Child development, rights and well fare expert","image":teamMember6},{"name": "Namutu Martha","role":"Education & Child Development Expert","image":teamMember7},{"name": "Kusiima Darlison","role":"Finance","image":userPlaceHolder}]
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
                quality education and the necessary resources to thrive.
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
                <TeamMember image= {member.image} name = {member.name} role = {member.role}/>
            {/each}
        </div>
        <div>
            {#if !showTeam}
               <button class="button" on:click={onShowTeamClick}>Show Team</button>
               {:else} 
               <button class="button" on:click={onShowTeamClick}>Hide</button>
            {/if}
        </div>
    </div>
</section>

<style>
    @media (min-width:51em) {
        .team-grid{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 1rem;
    }
    }
    .rounded > img{
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
</style>
