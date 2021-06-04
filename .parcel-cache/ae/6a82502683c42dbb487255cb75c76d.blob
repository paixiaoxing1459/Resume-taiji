let html = document.querySelector('#html');
let style = document.querySelector('#style');

let string = `/*
* 你好，我是一名前端新人。
* 接下来我演示一下我的前端功底
* 首先我要准备一个div
*/
#div1{
    border: 1px solid red;
    width: 200px;
    height: 200px;
}
/*
* 接下来我将把div变成一个八卦图
* 注意看好
* 首先，将div变成一个圆圈
*/
#div1{
    border-radius: 50%;
    box-shadow: 0 0 3px rgba(0,0,0,0.5);
    border: none;
}
/* 
* 八卦是阴阳融合形成的
* 一黑一白
*/
#div1{
    background: linear-gradient(90deg, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 50%, rgba(0,0,0,1) 50%, rgba(0,0,0,1) 100%);
}
/* 
* 加两个神秘的小球
*/
#div1::before{
    width: 100px;
    height:  100px;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    background: #000;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 23%, rgba(0,0,0,1) 25%, rgba(0,0,0,1) 100%);
}
#div1::after{
    width: 100px;
    height:  100px;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    background: #fff;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(0,0,0,1) 0%, rgba(0,0,0,1) 23%, rgba(255,255,255,1) 25%, rgba(255,255,255,1) 100%);
`;

// string = string.replace(/\n/g, '<br>');   //正则表达式将所有 "\n" 变成 "<br>"

let string2 = '';
let n = 0;

// setInterval(() => {
//     n = n + 1;
//     html.innerHTML = n;
// },1000);

// 使用 setTimeout 递归实现 setInterval 功能
// 这样的好处是，可以控制什么时候停止 使用 if-else 实现

let step = () => {
    setTimeout(() =>{
        if (string[n] === "\n"){
            //是回车的情况下就将 '\n' 替换为 '<br>'
            string2 += '<br>';
        }else if(string[n] === " "){
            string2 += "&nbsp;";
        }else{
            //其它情况下就照搬
            string2 +=  string[n];
        }
        html.innerHTML = string2;  
        style.innerHTML = string.substring(0,n);
        window.scrollTo(0,9999);
        html.scrollTo(0,9999);

        if (n < string.length-1){
            //n不是最后一个
            step();
            n += 1;
        }else{
            //n是最后一个
        }
    }, 5);
};

step(); 



