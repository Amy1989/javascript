#### 导语
 >在计算机科学中，柯里化（英语：Currying），又译为卡瑞化或加里化，是把接受多个参数的函数变换成接受一个单一参数（最初函数的第一个参数）的函数，并且返回接受余下的参数而且返回结果的新函数的技术。这个技术由 Christopher Strachey 以逻辑学家哈斯凯尔·加里命名的，尽管它是 Moses Schönfinkel 和 Gottlob Frege 发明的。

这是来自维基百科的名词解释。顾名思义，柯里化其实本身是固定一个可以预期的参数，并返回一个特定的函数，处理批特定的需求。这增加了函数的适用性，但同时也降低了函数的适用范围。
  
    var add = function(a){
      return function(b){
        return a+b+'';
      }
    }
    var multi = function(a){
      return function(b){
        return a*b+"";
      } 
    }
    var arr = function(arg,stylishChar){
      return arg.map(stylishChar).reduce(function(a,b){
          return a.concat(b)
      });
    } 
    console.log(arr([5,2,3], add(1)));
    console.log(arr([5,2,3], multi(2)));
