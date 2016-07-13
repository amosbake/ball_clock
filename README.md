# 具有掉落小球特效的时钟

采用canvas绘制时钟

#Canvas 相关知识

## 相关方法

### 绘制方法
``` js
    var canvas = document.getElementById('canvas'); //获取html中对应的canvas
    var context = canvas.getContext("2d"); //获取绘制2d图像的上下文
    context.lineWidth; //绘制线段宽度
    context.strokeStyle;//线段绘制属性(通常是颜色)
    context.fillStyle;//线段填充属性(通常为颜色)
    context.moveTo();//移动路径到指定点
    context.lineTo();//绘制线段到指定点
    context.arc();//创建弧线
    context.beginPath();起始一条路径(想绘制新图形时使用)
    context.closePath();创建返回其实点的路径
    context.strke();//绘制路径
    context.fill();//填充路径
    context.clearRect();//擦除区域内的绘画(为新绘画做准备)
```

### 动画方法
由于canvas是基于路径的状态绘制的,所以我们只用定时改变数据的状态,再重新绘制,就能达到动画的效果了
``` 
 setInterval(
  function(){
    render();
    update();
  },
  50
 );
```

代码参考慕课网canvas相关课程
