# JavaScriptCode

~~~

//指定目標
document.getElementById('ID');
document.getElementsByClassName('CLASS');
document.querySelector('#id');
document.querySelectorAll('.className');
document.getElementsByTagName("li");



//function 函數 ； 一連串的指令
function bark() {
	console.log('bark!!!');
}
bark();




// function 自帶變數
function functionName1 (man){
	var content = man + '超帥ber！！！';
	console.log(content);
}
functionName1 ('Vulcan');




// function 帶入變數
var varName = 'Ar Hung';
function functionName2 (man){
	var content = man + '超帥ber！！！';
	console.log(content);
}
functionName2 (varName);




// function 帶入多組變數
var varName1 = 'Hung';
var varName2 = '帥呆了！';
function functionName3 (man1, man2){
	var content = man1 + man2;
	console.log(content);
}
functionName3 (varName1, varName2);




// function 取值 改值
function functionName4 (){
	var varName3 = document.getElementById('abc').value;
	console.log(varName3);

	document.getElementById('abc').value = '12345';
	console.log(document.getElementById('abc').value);

}
functionName4 ();




// function 綁定按鈕事件
var myBtn = document.getElementById('btnName');
// 方法一
myBtn.onclick = function () {
	console.log('目前文字欄位是：'+ document.getElementById('abc').value);
}
// 方法二
myBtn.addEventListener('click', function() {
	 console.log('目前文字欄位是：'+ document.getElementById('abc').value);
});





// var score1 = 50;
// var score2 = 88;
// var score3 = 90;

// array(陣列)
var score = [50,88,90];

// 添加內容在陣列最後一個欄位
score.push(100);
console.log(score);

// 陣列從 [0] 開始計算第一位
console.log('第一位學生的分數是：' + score[0]);







// object(物件) 屬性：value
var home = {
	father: 'Tom',
	mom : 'Mary',
	sons: ['John','Bob']
}
console.log(home.mom);
console.log(home.sons[0]);







// 鄉鎮  50000 家庭
// array(陣列) 裡面包物件的方式
var country = [
	{
		father:'bob',
		mom:'mary'
	},
	{
		father:'tom',
		mom:'jane'
	}
];
console.log(country[0]);

// 第一個家庭的媽媽姓名
console.log('第一個家庭的媽媽姓名：' + country[0].mom);








// i++ 觀念
var num = 3;

num = num + 1; //4
num += 1; //num + 1
num++; //num + 1

console.log(num);


// for 迴圈 (初始化；條件為 true；累加 i)
for (var i=0;10>i;i++){
	console.log(i);
}


// 小鎮村  2戶家庭
var  country = [
	{father: 'tom'}
	,{father: 'bob'}
]
var len = country.length; //總數
for(var i=0;len>i;i++){
	console.log(country[i].father)
}



// document.getElementById('LIST').innerHTML = '<li>插入 HTML Code</li>';
// document.getElementById('ID').textContent = '插入文字';

var data = [
	{Name:'AAA'},
	{Name:'BBB'}
];
var len = data.length;
var str = '';
for(var i = 0;len>i;i++){
	var content = '<li>'+data[i].Name+'</li>'
	str += content;
}
document.getElementById('LIST').innerHTML = str;


// ES6
// var myCLASS = document.querySelectorAll('.CLASS');
// [...myCLASS].addEventListener('touchstart', function (e){
[...document.querySelectorAll('.CLASS')].addEventListener('touchstart', function (e){
	var myHref = this.href;
	location.href = myHref;
})

~~~
