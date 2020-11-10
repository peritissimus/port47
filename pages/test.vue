<template>
  <div class="container">
      <h1>Hello</h1>
  </div>
</template>

<script>
import p5 from "p5";

export default {
  head: {
    title: "Kushal | Test",
  },

  mounted() {
    console.log(window.innerWidth);
    const script = function (p5) {

        let c, r;
        let s = 15;
        let f = 0;

      p5.windowResized = (_) => {
        // console.log("resized")
        p5.resizeCanvas(p5.windowWidth, p5.windowHeight);
      };
      // NOTE: Set up is here
      p5.setup = (_) => {
        p5.createCanvas(p5.windowWidth, p5.windowHeight);

        c = p5.windowWidth / s;
        r = p5.windowHeight / s;
      };

      // NOTE: Draw is here
      p5.draw = (_) => {
        p5.background(0);
        p5.stroke(255);
        p5.noFill();

        f += 0.04;

        let yf = f;
        for ( let y= 0; y< r; y++){
            let xf = 0.0;
            for (let x = 0;x<c;x++){
                let ch = p5.map(p5.noise(xf,yf),0,1,-1,4);
                p5.fill(ch*10, ch*10, ch*10);
                p5.noStroke();
                xf +=0.6;
                p5.rect(x * s , y * s, s, s);
            }
            yf +=0.6;
        }


      };
    }; 
    
    // NOTE: Use p5 as an instance mode
    const P5 = require("p5");
    new P5(script);
  },
};
</script>

<style>
.test {
  background-color: #2e2e2e;
  background-size: cover;
  background-position: 50%;
  color: #f2f2f2;
}

h1 {
    color: #f2f2f2;
}

canvas{
    position: fixed;
    top: 0;
    left: 0;
    z-index: -1;
}
</style>