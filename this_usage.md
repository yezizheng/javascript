# javascript

function taskA() {
  name = 'hello'
  
  var fn = function() {
    console.log(this.name)
  }
  
  var arrow_fn = () => {
    console.log(this.name)
  }
  
  var obj = {
    name:"Hi",
    arrow(){
      console.log(this.name);
    }
  }
  
  var objj = {
    name:"Good",
    arrow: function(){
      return () => console.log(this.name)
    }
  }
  fn() // hello
  arrow_fn() // hello
  obj.arrow() // Hi
  objj.arrow()() // Good
}
taskA()
