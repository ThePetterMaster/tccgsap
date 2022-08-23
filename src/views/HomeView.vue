<template>
<div>
  <div class="container">
    <div class="boxcontainer"> 
      <div v-bind:id=" `box${index}`" class="box" v-for="(elemento, index) in elementos" :key="index">
        {{elemento}}
      </div>
      
      <div id="i"><div id="borda"></div>i</div>
      <div id="j"><div id="borda"></div>j</div>
      
      
    </div>
    <div class="imagemContainer">
      <img src="./sort.png" alt="Selection Sort" width="500" height="500" />
      <div id="bordacodigo"></div>
    </div>
    
  </div>

  <button @click="selectionSort">Ordenar</button>
  
  
</div>



</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import gsap from 'gsap'
import Vue from 'vue'

var tl = gsap.timeline()


const map1 = new Map();

// var prevWidth = window.innerWidth;
// var observer = new ResizeObserver(function(entries) {
//     const width = entries[0].borderBoxSize?.[0].inlineSize;
//     if (typeof width === 'number' && width !== prevWidth ) {
//         prevWidth = width;
//         console.log(width);
//     }
// })
// observer.observe(window.document.body);







export default {
  name: 'HomeView',
  components: {
    HelloWorld
  },
  data() {
    return {
      larguraDaTela: window.innerWidth,
  
      elementos:[4,3,2,1],
      oredenados:[1,2,3,4],
      
    };
  },
  mounted() {


    gsap.set("#bordacodigo",{scale: 0}) 
    gsap.set("#i",{scale: 0})
    gsap.set("#j",{scale: 0})   
 


    // console.log(window.innerWidth)
    // console.log(window.innerWidth )
    // gsap.to(".box", { x: 200 })
    // timeline = gsap.timeline({ repeat: -1, repeatDelay: 1, yoyo: true });
    // timeline.to(this.$el, { rotation: -90, duration: 2, ease: "back" });
    // timeline.to(this.$el, { duration: 0.5, backgroundColor: "yellow" }, "-=1");
    // gsap.to(".box", {
    //   keyframes: {
    //     x: [0, 0, 509, 509],
    //     y: [0,-150,-150, 0],
    //     ease: "power1.inOut"
    //   },
    //   duration: 4
    // });
    // gsap.to(".box2", {
    //   keyframes: {
    //     x: [0, 0, -509, -509],
    //     y: [0,-150,-150, 0],
    //     ease: "power1.inOut"
    //   },
    //   duration: 4
    // });
  //   let tl = gsap.timeline()
  //   tl.to("#box0", { 
  //    duration: 2,ease: "sine.out",
  //    y: -150,
  //  });
  //   tl.to("#box3", { 
  //    duration: 2,ease: "sine.out",
  //    y: -150,

  //  });
  //   tl.from("#box0", { 
  //    duration: 2,ease: "sine.out",
  //    x: 3*window.innerWidth/4,

  //  });
  //    tl.from("#box3", { 
  //   duration: 2,ease: "sine.out",
  //   x: -3*window.innerWidth/4,


  // },"<");
  //   tl.to("#box0", { 
  //    duration: 2,ease: "sine.out",
  //    y: 0,
  //  });
  //   tl.to("#box3", { 
  //    duration: 2,ease: "sine.out",
  //    y: 0,

  //  });
   
   





  // tl.to("#box4", { 
  //    duration: 2,ease: "sine.out",
  //    y: -150,
  //  });
  //   tl.to("#box3", { 
  //    duration: 2,ease: "sine.out",
  //    y: -150,

  //  });
  //   tl.to("#box4", { 
  //    duration: 2,ease: "sine.out",
  //    x: window.innerWidth/4,

  //  });
  //    tl.to("#box3", { 
  //   duration: 2,ease: "sine.out",
  //   x: - window.innerWidth/4,


  // },"<");
  //   tl.to("#box4", { 
  //    duration: 2,ease: "sine.out",
  //    y: 0,
  //  });
  //   tl.to("#box3", { 
  //    duration: 2,ease: "sine.out",
  //    y: 0,

  //  });
  // tl.to(box, 2, {xPercent:-100, left:"100%", yPercent:-100, top:"100%", force3D:true})
 

    var element = document.querySelector(".box2");
    // var rect = element.getBoundingClientRect();
    // console.log(rect.top, rect.right, rect.bottom, rect.left);
  },
  methods: {

    selectionSort() { 
      tl.set("#bordacodigo",{scale: 1})
      tl.to( "#bordacodigo", { y:-27*8.5  });
      
      


  




      // console.log(document.querySelector(".box").offsetWidth)
       var largura = document.querySelector(".boxcontainer").getBoundingClientRect().right;
      for (var i = 0; i < this.elementos.length; i++) {
         gsap.set(`#box${this.oredenados.indexOf(this.elementos[i])}` ,{ x: (i-this.oredenados.indexOf(this.elementos[i]))*100});
         console.log(`#box${i}`)
         console.log(i-this.oredenados.indexOf(this.elementos[i]))
      }
      // map1.set("#box0", "#box1");
  
      let n = this.elementos.length;
      // console.log(this.elementos)
      //2314  
      var i=0
      var j=i+1  
      for( i = 0; i < n; i++) {  
        tl.set("#i",{scale: 1})
        tl.to( "#bordacodigo", { y:-27*7.5  });
    
   
        // tl.to(`#borda`, { 
        // duration: 0,ease: "sine.out",
        // x: -window.innerWidth/this.elementos.length -window.innerWidth/(this.elementos.length*2),

        //  });
        // tl.to(`#borda`, { 
        // duration: 2,ease: "sine.out",
        // x: -window.innerWidth/(this.elementos.length*2),

        //  });
        // tl.fromTo( "#i",{ x:( -(largura/(this.elementos.length*2)+largura/(this.elementos.length))+(largura*i-1)/(this.elementos.length)) }, {x: ( -(largura/(this.elementos.length*2)+largura/(this.elementos.length))+(largura*i)/(this.elementos.length)) });
       tl.set("#i",{scale: 1})
       tl.fromTo( "#i",{ x:( -0.5*(this.elementos.length-1)*document.querySelector(".box").offsetWidth+document.querySelector(".box").offsetWidth*(i-1)) }, { x:( -0.5*(this.elementos.length-1)*document.querySelector(".box").offsetWidth+document.querySelector(".box").offsetWidth*(i))  });
        var min = i;
        tl.to( "#bordacodigo", { y:-27*6.5  });
        
          for( j = i+1; j < n; j++){
            tl.to( "#bordacodigo", { y:-27*5.5  });

            // console.log(j)
              if(this.elementos[j] < this.elementos[min]) {
                tl.to( "#bordacodigo", { y:-27*4.5  });
                  min=j;
                  tl.to( "#bordacodigo", { y:-27*3.5  });

              }
              tl.to( "#bordacodigo", { y:-27*2.5  });
            tl.set("#j",{scale: 1})  
            // tl.fromTo( "#j",{ x:( -(largura/(this.elementos.length*2)+largura/(this.elementos.length))+(largura*j-1)/(this.elementos.length)),duration: 1,ease: "sine.out", }, {x: ( -(largura/(this.elementos.length*2)+largura/(this.elementos.length))+(largura*j)/(this.elementos.length)),duration: 1,ease: "sine.out", });
               tl.fromTo( "#j",{ x:( -0.5*(this.elementos.length-1)*document.querySelector(".box").offsetWidth+document.querySelector(".box").offsetWidth*(j-1)) }, { x:( -0.5*(this.elementos.length-1)*document.querySelector(".box").offsetWidth+document.querySelector(".box").offsetWidth*(j))  });
          }
          tl.to( "#bordacodigo", { y:-27*1.5  });
          if (min != i) {
            tl.to( "#bordacodigo", { y:-27*0.5  });

            tl.to( "#bordacodigo", { y:27*0.5  });
            tl.to( "#bordacodigo", { y:27*1.5  });
            tl.to( "#bordacodigo", { y:27*2.5  });
            
                  // console.log(this.elementos[i])
                  // console.log(this.elementos[min])


              tl.to(`#box${this.oredenados.indexOf(this.elementos[i])}`, { 
                duration: 0.3,
                backgroundColor: 'orange',
                yoyo: true,
                repeat: 2,
              });
              tl.to(`#box${this.oredenados.indexOf(this.elementos[min])}`, { 
                duration: 0.3,
                backgroundColor: 'orange',
                yoyo: true,
                repeat: 2,
              },"<");
              
              tl.to(`#box${this.oredenados.indexOf(this.elementos[i])}`, { 
              duration: 2,ease: "sine.out",
              y: -150,
            });
              tl.to(`#box${this.oredenados.indexOf(this.elementos[min])}`, { 
              duration: 2,ease: "sine.out",
              y: -150,

            },"<");
  

  
          //   tl.from(`#box${i}`, { 
          //     duration: 2,ease: "sine.out",
          //     //2-0=2
          //     x:((min-i)*largura/(this.elementos.length)),

          //   });
          //   // tl.fromTo( `#box${i}`,{ x: 0,duration: 5,ease: "sine.out", }, {x: ((min-i)*window.innerWidth/this.elementos.length),duration: 5,ease: "sine.out", });
          
          //   // console.log(this.elementos)
          //   // //-(2-0)=-2
          //     tl.from(`#box${min}`, { 
          //     duration: 2,ease: "sine.out",

          //     x:-((min-i)*largura/(this.elementos.length)) ,
          // console.log(min)
          // console.log(i)
          // console.log((min-this.elementos.indexOf(this.elementos[i])))
          // console.log((i-this.elementos.indexOf(this.elementos[i])))
          
          tl.to( `#box${this.oredenados.indexOf(this.elementos[min])}`, {x: (this.oredenados.indexOf(this.elementos[min])-i)*100,duration: 3,ease: "sine.out", });

       
    
          // tl.to(`#box${i}`,{ x: (min-this.elementos.indexOf(this.elementos[i]))*100,duration: 5,ease: "sine.out", })
      
          //   },"<");
          //   // tl.fromTo( `#box${min}`,{ x: 0,duration: 5,ease: "sine.out", }, {x: -((min-i)*window.innerWidth/this.elementos.length),duration: 5,ease: "sine.out", });
          //   // map1.set(`#box${i}`, `#box${min}`);
          //   // map1.set(`#box${min}`, `#box${i}`);
          //   // console.log(map1)
          // //            console.log(document.getElementById(`box${i}`))
          // // // document.getElementById("aux").id=`box${i}`;
          // //  document.getElementById("box0").class="box2";
          // //  console.log(document.getElementById(`box${min}`))
          // //  document.getElementById("box2").class="box0";
          //tl.fromTo( `#box${min}`,{ x: (min-this.sortedelementos.indexOf(this.elementos[i]))*100,duration: 5,ease: "sine.out", }, {x: (i-this.sortedelementos.indexOf(this.elementos[min]))*100,duration: 5,ease: "sine.out", });
          tl.to( `#box${this.oredenados.indexOf(this.elementos[i])}`, {x: (min-this.oredenados.indexOf(this.elementos[i]))*100,duration: 3,ease: "sine.out", },"<");
          // console.log( this.oredenados.indexOf(this.elementos[i]))
            
              tl.to(`#box${this.oredenados.indexOf(this.elementos[i])}`, { 
              duration: 2,ease: "sine.out",
              y: 0,
            });
              tl.to(`#box${this.oredenados.indexOf(this.elementos[min])}`, { 
              duration: 2,ease: "sine.out",
              y: 0,

            },"<");
            if((this.oredenados.indexOf(this.elementos[min])-i)==0){
              tl.to(`#box${this.oredenados.indexOf(this.elementos[min])}`, { 
                duration: 0.3,
                backgroundColor: 'green',
                yoyo: true,
                repeat: 2,
              });
            }else{
              tl.to(`#box${this.oredenados.indexOf(this.elementos[min])}`, { 
                duration: 0.3,
                backgroundColor: 'red',
              });
            }
            if((min-this.oredenados.indexOf(this.elementos[i]))==0){
              tl.to(`#box${this.oredenados.indexOf(this.elementos[i])}`, { 
                duration: 0.3,
                backgroundColor: 'green',
                yoyo: true,
                repeat: 2,
              });
            }else{
              tl.to(`#box${this.oredenados.indexOf(this.elementos[i])}`, { 
                duration: 0.3,
                backgroundColor: 'red',

              });
            }
  

              let tmp = this.elementos[i];
         
              this.elementos[i]=this.elementos[min];
      
              this.elementos[min]=tmp;
          
   
          }
          tl.to( "#bordacodigo", { y:27*3.5  });
      }
      tl.to( "#bordacodigo", { y:27*4.5  });
        // console.log(this.elementos)
        tl.set("#i",{scale: 0})
        tl.set("#j",{scale: 0})
        tl.set("#bordacodigo",{scale: 0})
    }

  }
  
}
window.addEventListener('resize', function() {
      var element = document.querySelector(".boxcontainer").getBoundingClientRect().right;
  
    // console.log(element);
     
        this.larguraDaTela=window.innerWidth;
      
        // console.log(this.larguraDaTela)
        // var offsets = document.getElementById('box').getBoundingClientRect();
        
        // var rect = document.getElementById('box').getBoundingClientRect();
        // gsap.to("#box4", { x:  3*window.innerWidth/4 ,ease: "sine.out",duration: 3});
        // gsap.to("#box2", { x:  -3*window.innerWidth/4,ease: "sine.out",duration: 3});
        // gsap.to("#box4", { x:  1*window.innerWidth/4 ,ease: "sine.out",duration: 3});
        // gsap.to("#box3", { x:  -window.innerWidth/4,ease: "sine.out",duration: 3});
        //  console.log("x")
        //  console.log(rect.left)
        // console.log("y")
        // console.log(rect.top)
        // console.log(window.innerWidth/2 )

      // console.log(document.getElementsByClassName('box').getBoundingClientRect().left);
});
</script>

<style scoped>
.box {
  background-color: red;
  height: 100px;
  width: 100px;
  color: black;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 120px;
  position: static;
}
/* #box2 {
  background-color: red;
  height:100px;
  width: 100px;
  color: black;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 120px;
  position: static;
}
#box3 {
  background-color: green;
  height:100px;
  width: 100px;
  color: black;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 120px;
}
#box4 {
  background-color: yellow;
  height:100px;
  width: 100px;
  color: black;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 120px;
} */
.boxcontainer {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 700px;
  width: 700px;

} 
.container {

  display: flex;
   align-items: center;
   
} 
.imagemContainer{
    display: flex;
   align-items: center;
   justify-content: center;
   width: 50rem;
}
#i{
  position:absolute;
  font-size: 50px;
  margin-top:57px
}
#j{
  position:absolute;
  font-size: 50px;
  margin-top:57px
}
#borda{
  background-color: white;
  border-style: solid;
  border-width: 4px;
  height: 100px;
  width: 100px;
  opacity:0.5;
}

#bordacodigo{
  height: 27px;
  width: 500px;
  position:absolute;
  background-color: white;
  border-style: solid;
  border-width: 4px;
  opacity:0.5;
}



</style>