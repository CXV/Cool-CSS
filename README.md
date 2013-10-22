Cool-CSS
========

move('#example-1 .box')
  .set('margin-left', 200)
  .end();
  
move('#example-2 .box')
  .add('margin-left', 200)
  .end();
  
            
move('#example-3 .box')
  .sub('margin-left', 100)
  .end();
          
          
move('#example-4 .box')
  .rotate(140)
  .end();
          
          
move('#example-5 .box')
  .set('background-color', 'blue')
  .duration('2s')
  .end();          
       
move('#example-6 .box')
  .translate(300, 80)
  .end();
          
          
move('#example-7 .box')
  .x(300)
  .y(20)
  .end();
  
  
move('#example-8 .box')
  .x(300)
  .skew(50)
  .set('height', 20)
  .end();
          
          
move('#example-9 .box')
  .scale(3)
  .end();
  
move('#example-10 .box1').x(400).end();
move('#example-10 .box2').ease('in').x(400).end();
move('#example-10 .box3').ease('out').x(400).end();
move('#example-10 .box4').ease('in-out').x(400).end();
move('#example-10 .box5').ease('snap').x(400).end();
move('#example-10 .box6').ease('cubic-bezier(0,1,1,0)').x(400).end();

setTimeout(function(){
  move('#example-10 .box1').x(0).end();
  move('#example-10 .box2').x(0).end();
  move('#example-10 .box3').x(0).end();
  move('#example-10 .box4').x(0).end();
  move('#example-10 .box5').x(0).end();
  move('#example-10 .box6').x(0).end();
}, 1200);
          

move('#example-11 .box')
  .set('background-color', 'red')
  .duration(1000)
  .end(function(){
    move('#example-11 .box')
      .set('background-color', 'white')
      .end();
  });
          
          
move('#example-12 .box')
  .set('background-color', 'blue')
  .delay('2s')
  .end();
          
var moveBack = move('#example-13 .box')
  .set('background-color', 'white')
  .x(0);

move('#example-13 .box')
  .set('background-color', 'red')
  .x(500)
  .then(moveBack)
  .end();

move('#example-13 .box2')
  .set('background-color', 'red')
  .x(500)
  .scale(.5)
  .rotate(60)
    .then()
      .rotate(30)
      .scale(1.5)
      .set('border-radius', 5)
      .set('background-color', 'white')
      .then()
        .set('opacity', 0)
        .pop()
      .pop()
  .end();
          
          
move.select = function(selector){
  return $(selector).get(0);
};
          
move.defaults = {
  duration: 500
};
          
        
          
move.ease = {
    'in': 'ease-in'
  , 'out': 'ease-out'
  , 'in-out': 'ease-in-out'
  , 'snap': 'cubic-bezier(0,1,.5,1)'
};
          

move.version = "n.n.n";
