<style>
  body {
background-color: beige;
margin: 0;
}

main {
background-color: beige; 
color: gray;
text-align: center;
}

h1 {
text-align: center;
}

p {
text-align: center;
}

.lifts {
display: flex;
justify-content: center;
align-items: center;
margin-top: 20px;
}

button {
border-radius: 20%;
font-size: 20px;
background-color: white;
transition-duration: 0.4s;
}

button:hover {
background-color: white;
color: gray;
}

</style>
<body>
  <main>
    <h1>Powerlifting Warmup Calculator</h1>
    <p>Choose your lift below:</p>
    <div class="lifts">
      <a href="Squat"><button>Squat</button></a>
      <a href="Bench"><button>Bench</button></a>
      <a href="Deadlift"><button>Deadlift</button></a>
    </div>
  </main>
</body>
