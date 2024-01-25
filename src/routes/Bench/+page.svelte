<script>
    let max = ''
    let set1 = ''
    let set2 = ''
    let set3 = ''
    let set4 = ''
    let set5 = ''
    let set6 = ''
    let set7 = ''
    let set8 = ''
    let set9= ''
    let final = ''
    let warmup = ''
    let temp = ''
    let temp2 = ''

    function roundLess(input){
        var result = Math.floor(input * .82/5)
        if (result % 5 !== 0) {
         result = Math.ceil(result/5)*5
        }
        return result * 5;
    }

    function roundNearest25(input){
        var result = Math.floor(input * .84/5)
        if (result % 5 !== 0) {
         result = Math.ceil(result/5)*5
        }
        return result * 5;
    }
    function buttonPress(){
        if(max<95){
            warmup = ''
            final = "Please enter a value greater than or equal to 95"
            set1 = ''
            set2 = ''
            set3 = ''
            set4 = ''
            set5 = ''
            set6 = ''
            set7 = ''
            set8 = ''
            set9= ''
            return
        }
        if(max==95){
            warmup = "Your warmup is: "
            set1 = "45lbs (empty bar) x 2-5 reps | "
            temp = Math.round((max*.8)/5)*5
            set2 = temp + "lbs x 1 rep | "
            set3= ''
            set4 = ''
            set5 = ''
            set6 = ''
            set7 = ''
            set8 = ''
            set9= ''
            final = max + "lbs x 1 rep | "
            return
        }
        if(max<=135){
            warmup = "Your warmup is: "
            set1 = "45lbs (empty bar) x 5 reps | "
            set3 = " "
            temp = Math.ceil((max*.85)/5)*5
            set2 = temp + "lbs x 2 reps | "
            set4 = ''
            set5 = ''
            set6 = ''
            set7 = ''
            set8 = ''
            set9= ''
            final = max + "lbs x 1 rep | "
            return
        }
        if(max<= 185){
            warmup = "Your warmup is: "
            set1 = "45lbs (empty bar) x 5 reps | "
            set2 = "95lbs x 3 reps | "
            set3 = roundLess(max) + "lbs x 1 rep | "
            final = max + "lbs x 1 rep | "
            set4 = ''
            set5 = ''
            set6 = ''
            set7 = ''
            set8 = ''
            set9= ''
            return
        }
        if(max<=225){
            warmup = "Your warmup is: "
            set1 = "45lbs (empty bar) x 5 reps | "
            set2 = "95lbs x 3-5 reps | "
            set3 = "135 x 2 reps |  "
            temp = roundLess(max);
            set4 = temp + "lbs x 1 rep | "
            final = max + "lbs x 1 rep | "
            set5 = ''
            set6 = ''
            set7 = ''
            set8 = ''
            set9= ''
            return
        }
        if(max<=275){
            warmup = "Your warmup is: ";
            set1 = "45lbs (empty bar) x 8 reps | ";
            set2 = "135lbs x 5 reps | "
            temp = roundLess(max);
            set3 = temp + " x 1-3 reps | "
            final = max + "lbs x 1 rep | "
            set5 = ''
            set6 = ''
            set7 = ''
            set8 = ''
            set9= ''
            return
        }
        if(max<=315){
            warmup = "Your warmup is: ";
            set1 = "45lbs (empty bar) x 8 reps | ";
            set2 = "135lbs x 5 reps | "
            set3 = "225 x 2-3 reps |"
            temp = roundLess(max);
            set4 = temp + " x 1-3 reps | "
            final = max + "lbs x 1 rep | "
            set5 = ''
            set6 = ''
            set7 = ''
            set8 = ''
            set9= ''
            return
        }
        if(max>315){
            warmup = ''
            final = "Bro you're too strong figure it out on your own"
            set1 = ''
            set2 = ''
            set3 = ''
            set4 = ''
            set5 = ''
            set6 = ''
            set7 = ''
            set8 = ''
            set9= ''
            return
        }
    }
</script>
<body>
<main>
    <h1>Calculate your Bench Warmup</h1>
    <p>Enter your 1 Rep Max Attempt.</p>
    <input type="text" bind:value={max}>
    <div class= "calculate">
        <button on:click={buttonPress}>Calculate Warmup</button>
    </div>
    <p>
        {warmup}
        {set1}
        {set2}
        {set3}
        {set4}
        {set5}
        {set6}
        {set7}
        {set8}
        {set9}
        {final}
    </p>
    <p>
        Choose your lift:
    </p>
    <div class="lifts">
        <a href="Squat"><button>Squat</button></a>
        <a href="Bench"><button>Bench</button></a>
        <a href="Deadlift"><button>Deadlift</button></a>
        </div>
</main>
</body>

<style>
    h1{
        text-align: center;
    }
    input{
        margin: 5px auto;
        display: block;
    }
    p{
        text-align: center;
    }
    div.calculate {
        text-align: center;
    }
    button{
        border-radius: 20%;
        font-size: 20px;
        background-color: white;
        transition-duration: 0.4;
    }
    button:hover {
        background-color: white;
        color: gray;
    }
    .lifts{
        text-align: center;
    }
     body {
      background-color: beige;
      margin: 0;
    }
    main {
      background-color: beige; 
      color: gray;
    }
</style>
