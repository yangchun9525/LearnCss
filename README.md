# LearnCss
个人学习css布局的代码<br>

clear:清除浮动<br>
left:左侧不允许<br>
right:右侧不允许<br>
both:2侧不允许<br>
none:2侧都允许<br>
inherit:从父元素继承clear值<br>

float
----- 
脱离文档流，像其字面意思一样，浮动在屏幕之上<br>

display
------- 
inline：行内元素<br>
block：块级元素<br>
inline-block：上面2个的结合体，当需要设置大小时一般用它,当使用它时出现间距，将font-size设置为0即可<br>

a标签
--- 
a标签中有四个：link、visited、hover、active<br>
（1）link<br>
说明：设置a对象在未被访问前的样式表属性。<br>
（2）visited<br>
说明：设置a对象在其链接地址已被访问过时的样式表属性。<br>
（3）hover<br>
说明：设置对象在其鼠标悬停时的样式表属性。<br>
（4）active<br>
说明：设置对象在被用户激活（在鼠标点击与释放之间发生的事件）时的样式表属性。<br>

background-position:10px 20px<br>
代表的意思就是离父控件左边距10px,离父控件上间距20px<br>

mufocus:<br>
http://demo.jb51.net/js/myfocus/download.html<br>

css3
----
    
    嵌入字体，使用时font-family要和@font-face的@font-face一致
    @font-face {
        font-family: "MOOC Font";
        src: url("http://www.imooc.com/Amaranth-BoldItalic.otf");
     }  
    border-raduis:50px 0px 0px 50px; 分别是左上，右上，右下，左下
    box-shadow:4px 4px 6px #666;  x偏移量，y偏移量，阴影模糊半径，阴影扩展半径，阴影颜色，投影方式（内部阴影，忽略就是外部阴影）

属性选择器：<br>
包含某一个关键字 
------- 
类开头为column的进行匹配<br>
        
        a[class^="column"]
         
 类结尾为column的进行匹配<br>
               
         a[class$="column"]
 类中包含column的进行匹配<br>
               
         a[class*="column"]
:not
------- 
div中id不为footer的执行该css<br>

        div:not([id="footer"])
   
child相关
-------      
        li:first-child 第一个元素
        li:last-child  最后一个元素
        li:nth-child(1) 第几个元素，元素从1开始，不是0开始，需注意
        li:nth-last-child(5) 倒数第几个元素，与nth-child相对应
        li:only-child  当li中仅有一个子元素时触发
        div:only-of-type 和其父元素都是div，且为唯一的子div时触发  
  
type相关
------         
        p:first-of-type 第一个p元素
        p:nth-of-type(2n) 第偶数个p元素
        p:last-of-type 最后一个p元素
        p:nth-last-of-type(n) 最后第n个p元素
        
其他选择器
-----  

        :enabled        用于表单元素为enabled状态
        :disabled       用于表单元素为disable状态
        :checked        radio或者checkbox的选中状态选择器
        ::selection     文字被选中时触发
        :read-only      元素中设置了readonly=’readonly’触发
        :read-write     与:read-only相反，默认为:read-write
        ::before和::after 这两个主要用来给元素的前面或后面插入内容，这两个常和"content"配合使用，使用的场景最多的就是清除浮动。
 
兼容性
---

     谷歌内核：-webkit；火狐内核：-moz ；IE内核：-ms；Opera内核：-o 。
     
变形与动画
-----    
        
         transform:rotate(20deg); 顺时针旋转20度  
         transform:skew(45deg);   逆时针旋转45度  
         transform: scale(0.5,0.8);    长变为0.5，高变为0.8
         opacity: .5                透明度为0.5
         transform: translate(50px,100px);  x轴移动50px，y轴移动100px
         transform-origin: top right;    修改原点，然后进行变换，比如rotate，skew
         transition-property:指定过渡或动态模拟的CSS属性
         transition-duration:指定完成过渡所需的时间
         transition-timing-function:指定过渡函数
         transition-delay:指定开始出现的延迟时间
         
         @Keyframes changecolor{
          0%{
             background: red;
           }
           20%{
             background:blue;
           }
          }
          //此处调用上面定义的动画，动画名，动画执行时间，过度函数，延迟时间
          div:hover {
            animation: changecolor 20s ease-out .2s;
          }
          //上面的animation 其实是下面这些的简写
          animation-name:changecolor;
          animation-duration: 10s;
          animation-timing-function: ease;
          animation-delay: 1s;
          animation-iteration-count:infinite;
          animation-direction                   动画播放方向
          animation-play-state                  动画的播放状态
          
 css3布局：
 
        columns：<column-width> || <column-count>  列宽和列数。
        column-gap: normal || <length>              设置列与列之间的间距，normal默认为1rem，length可为具体值
        //主要是用来定义列与列之间的边框宽度、边框样式和边框颜色。
        column-rule:<column-rule-width>|<column-rule-style>|<column-rule-color>
        //定义一个分列元素中的子元素能跨列多少
        column-span: none | all
屏幕适配 https://segmentfault.com/a/1190000004524243#articleHeader4
https://www.w3cplus.com/mobile/vw-layout-in-vue.html
