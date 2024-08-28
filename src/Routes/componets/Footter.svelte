<script>
    import linkedIn from "/linkedin2.svg";
    import x from "/x.svg";
    import yt from "/yout.svg";
    import { Link } from "svelte-routing";
</script>

<footer class="cta | footer d-f-c bg-primary-400 text-neutral-100">
    <div class="sb-footer section-padding d-f-c">
        <div class="sb-footer-links d-f-r">
            <div class="sb-footer-links-div d-f-c">
                <h4>HOWSA</h4>
                <Link to="/about"><p>About</p></Link>
                <Link to="/programs"><p>Services</p></Link>
                <Link to="/about"><p>Team</p></Link>
            </div>
            <div class="sb-footer-links-div d-f-c">
                <h4>Programs</h4>
                <a href="/programs#community"><p>Community Sensitization</p></a>
                <a href="/programs#education"><p>Educational Support</p></a>
                <Link to="/programs#skills"><p>Skill Development</p></Link>
                <Link to="/programs#medical"><p>Medical Care</p></Link>
            </div>
            <div class="sb-footer-links-div d-f-c">
                <h4>Social</h4>
                <div class="socialmedia d-f-r2">
                    <a
                        href="https://www.linkedin.com/company/heart-of-wisdom-students-aid-howsa-ug-limited/posts/?feedView=all&viewAsMember=true"
                        ><img src={linkedIn} alt="" width={45} height={45} /></a
                    >
                    <a href="https://x.com/HOWSA_Ugltd"
                        ><img src={x} alt="" width={45} height={45} /></a
                    >
                    <a
                        href="https://youtube.com/@heartofwisdomsa_ug?si=_pISMzHmdnD6fc3e"
                        ><img src={yt} alt="" width={45} height={45} /></a
                    >
                </div>
            </div>
        </div>
    </div>
    <hr />
    <div class="sb-footer-below">
        <div class="sb-footer-copyright d-f-r">
            <p class="white">
                Copyright &copy;{new Date().getFullYear()} HOWSA LTD. All rights
                reserved.
            </p>
        </div>
    </div>
</footer>

<style>
    .white{
        color: white;
    }
    .sb-footer-links {
        justify-content: space-between;
        align-items: flex-start;
        flex-wrap: wrap;
        width: 100%;
        text-align: left;
        margin-bottom: 2rem;
    }
    .sb-footer-links-div {
        width: 150px;
        margin: 1rem;
        justify-content: flex-start;
    }
    .sb-footer-links-div h4 {
        color: white;
    }

    .sb-footer-links-div > :global(a) {
        color: white;
        text-decoration: none;
    }
    .sb-footer-links-div h4 {
        font-size: 14px;
        line-height: 17px;
        margin-bottom: 0.9rem;
    }
    .sb-footer-links-div p {
        font-size: 12px;
        line-height: 15px;
        margin: 0.5rem 0;
        cursor: pointer;
    }
    .socialmedia a img {
        width: 80%;
    }
    .sb-footer-below-links {
        font-size: 13px;
        line-height: 15px;
        margin-left: 2rem;
        font-weight: 600;
        justify-content: space-between;
    }
    .sb-footer-below-links a {
        text-decoration: none;
        color: white;
        margin-right: 20px;
    }
    .footer hr {
        width: 100%;
        color: white !important;
    }
    .sb-footer-copyright {
        text-align: center;
        font-size: 13px;
        line-height: 15px;
        font-weight: 600;
        padding: 14px;
    }
    .d-f-r2{
        display: flex;
    }
</style>
