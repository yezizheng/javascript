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
  fn()
  arrow_fn()
  obj.arrow()
  objj.arrow()()
}
taskA()
