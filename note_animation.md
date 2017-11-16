# 动画

## transition(过渡)

transition-property : 规定应用效果的CSS属性名称

transition-duration : 规定完成过渡效果需要的时间

transition-timing-function : 规定速度效果的速度曲线

linear 匀速
ease-in 加速
ease-out 减速
cubic-bezier 自定义函数

transition-delay : 规定过渡效果何时开始

transition: property duration timing-function delay

使用注意

1、可以不加浏览器前缀

2、不是所有CSS属性都支持transition

3、一定要有开始和结束的数值

使用局限

1、需要事件触发

2、是一次性的

3、只能定义开始和结束状态

4、一条规则只能定义一个属性的变化

## Animation

### 基本用法

div:hover {
    animation: 1s rainbow;
}

@keyframes rainbow {
    0% { background: #c00;}
    50% { background: orange;}
    100% {background: yellowgreen;}
}

默认情况下动画只播放一次，加入infinite关键字可无限次重复，也可设置数值，表示具体的播放次数

### animation-fill-mode

设置动画结束状态

forwards： 结束状态
none：默认值，回到最开始的状态
backwrads：让动画回到第一帧的状态
both： 根据animation-direction轮流应用forwards和backwards

### animation-direction

动画每次播放都是从结束状态回到初始状态，再开始播放，animation-direction可改变这种行为

normal(默认)常用
alternate
reverse 常用
alternate-reverse

### animate-play-state

可设置触发事件不满足时动画停止的状态，是回到初始状态还是暂停

### 浏览器前缀

IE10和firefox(>=16)支持没有前缀的animation，chrome不支持，需要加-webkit前缀




