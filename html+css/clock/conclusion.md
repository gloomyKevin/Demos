背景平铺
background-size:cover

常用高度设置技巧
100vh

对rem，px的彻底了解

```css
.clock {
            display: flex;
            position: relative;
            width: 30rem;
            height: 30rem;
            margin: 20rem auto;
            justify-content: center;
            align-items: center;
            border: 30px solid #fff;
            border-radius: 50%;
        }
```

rem和px的值转换
又根元素html的font-size决定
px = font-size*rem
如果css里面没有设定html的font-size，则默认浏览器以1rem=16px来换算
```css
.clock-face {
            position: relative;
            width: 100%;
            height: 100px;
            transform: translateY(-3px);
        }

        .hand {
            position: absolute;
            top: 50%;
            width: 50%;
            height: 6px;
            background-color: #000;

        }
```
在top: 50%之后，再利用父元素的transform: translateY(-3px);使指针上移动半个height大小

bug解决
secondHand.style.transform = `rotate:(${secondDegrees}deg)`;
改为
secondHand.style.transform = `rotate(${secondDegrees}deg)`;

`....`的用法

第二次bug原因
const second = date.getSeconds();
const secondDeg = ((360 / 60) * second) + 90;
改为
const second = date.getSeconds();
secondDeg = ((360 / 60) * second) + 90;

加深对const的理解

todo
怎样展示数字（尽量只用css）

todo
css样式优化
