<template>
  <div class="row">
      <div id="home" class="col-sm-12 text-center">
          <div class="background">
              <h1>Welcome to The Rest of Your Life</h1>
              <h2>Let's pet a dog</h2>
              <button class="btn btn-success">Pet Pesto</button>
          </div>
      </div>
  </div>
</template>

<style>
    #home {
        background: url('../../src/assets/Pesto.jpg');
        background-size: cover;
        height: 800px;
        padding: 10%;
    }
    h1, h2 {
        margin: 6%;
    }
    .background {
        background: #eee;
        opacity: 0.8;
        max-width: 60%;
        margin: 0 auto;
        padding: 20px 0;
    }
    
</style>