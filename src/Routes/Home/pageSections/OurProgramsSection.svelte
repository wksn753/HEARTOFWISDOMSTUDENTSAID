<script>
    import OurWorkCard from "../componets/OurWorkCard.svelte";
import howsa4 from "/howsa4.jpeg";
    import ourwork1 from "/Ourwork1.jpeg";
    import ourwork2 from "/OurWork2.jpeg";
    import ourwork3 from "/OurWork3.jpeg";
</script>

<section class="padding16px">
    <h3 class="fw-bold fs-800">Our Programs</h3>
    <div class="even-coloumns wd-100">
        <OurWorkCard image={howsa4} title ="Community Sensitization" description ="Conducting outreaches to raise awareness about child development, protection, and care."/>
        <OurWorkCard image={ourwork1} title ="Educational Support" description ="Providing school fees and scholastic materials like pens, books, and uniforms."/>
        <OurWorkCard image={ourwork2} title ="Skill Development" description ="Skilling children during holidays in areas like tailoring, handcrafts, and baking."/>
        <OurWorkCard image={ourwork3} title ="Medical Care" description ="Offering medical care for children in need."/>
    </div>
    <div>
        <h3>Our Partners</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores voluptatem ipsam possimus aperiam facilis at fugit saepe suscipit neque, cum qui in nemo beatae ut voluptatibus delectus culpa dolore obcaecati.</p>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Unde libero iusto natus explicabo ad corporis, odit voluptatem impedit animi ducimus, expedita nam, labore nemo delectus! Sequi asperiores ad illum voluptate?</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus porro laudantium dignissimos accusantium quod cumque, error quae quo animi asperiores repellendus debitis itaque, modi placeat molestiae magni. Magni, architecto quis!</p>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sed consequatur velit itaque modi voluptate deleniti suscipit laborum vitae minus, culpa repellat reiciendis. Voluptates suscipit culpa, eveniet facilis animi harum hic.</p>
    </div>
</section>

<style>
</style>
