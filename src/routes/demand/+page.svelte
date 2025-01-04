<script>
    let inp
    let out
    function calculate(){
        out = (-20*inp)/(5000-(20*inp))
    }
</script>

<style>
    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        min-height: 100vh;
        gap: 1rem;
    }

    h1 {
        color: #333;
        margin-bottom: 2rem;
    }

    input {
        padding: 0.5rem 1rem;
        border: 2px solid #333;
        border-radius: 4px;
        font-size: 1rem;
        width: 200px;
    }

    button {
        padding: 0.5rem 2rem;
        background-color: #333;
        color: white;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        font-size: 1rem;
        transition: background-color 0.3s ease;
    }

    button:hover {
        background-color: #555;
    }

    p {
        font-size: 1.2rem;
        color: #333;
    }
</style>

<div class="container">
    <h1>Calculate Elasticity of Demand</h1>
    <input type="number" bind:value={inp} placeholder="Enter value">
    <button on:click={calculate}>Calculate</button>
    <p>The elasticity of demand is: {out}</p>
</div>