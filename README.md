我们来解一个问题

1. 写一个函数, 可以连接字符数组, 如 f(['1','2']) => '12'

好吧,如果不用柯里化, 怎么写? 啊哈 reduce

var concatArray = function(chars){
  return chars.reduce(function(a, b){
    return a.concat(b);
  });
}
concat(['1','2','3']) // => '123'
很简单,对吧.
