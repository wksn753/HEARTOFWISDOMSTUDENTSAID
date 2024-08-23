<script>
    export let svg;
    export let question;
    export let answer;
</script>

<div class="flow">
    <div class="coloumn"><img src={svg} alt="" width="48" height="48" class="padding-right8px"/><p class="fw-bold">{question}</p></div>
    <div><p>{answer}</p></div>
</div>

<style>
    .coloumn{
        display: flex;
        flex-direction: row;
    }
    .padding-right8px{
        margin-right: 0.5rem;
    }
</style>