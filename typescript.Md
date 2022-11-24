# Typescript

1. Kiểu dữ liệu
const num = 5 + 5
const str = "hello ae wibu"

type Person = {
	age : number
	deptrai : boolean
}

const viet:Person = {
	age: 10,
	deptrai : true
}

const long = {
	age : 13,
	deptrai : false
}





2 Cách khai báo
- String trong Typescript
let firstname  = "Viet"
let lastname:string;

- number trong Typescript
let age:number;
age = 30

- undefine trong typescript
let k:undefined;
let m = null;

- any trong Typescript: có thể ghi đè với mọi kiểu dữ liệu
let viet:any;
viet = 13;
viet = "Hello ae wibu";

- **Object Type trong Typescript**
let single = {}; // Khai báo 1 object bên trong không có kiểu propertye nào, ta không thể gán: single.name = "viet";

let single = {name : "Vietdz", dz : true};
single.name = "hello";

let single = {name:string, age:number};
single.age = 23;

 let single = {name : string, age : number} = {"viet", 23}; // Bắt buộc phải có đủ 2 thuộc tính cho Object, để có thể gán hoặc ko gán các thuộc tính ta thêm dấu ? như sau:
 let single = {name : string, age?: number} = {name : "viet vip pro"};
 
 - **Array trong Typescript**
let array = [];  // Khai báo như này thì mảng dữ liệu có kiểu any
array.push(6);
array.push("hello");

let array = {"a", "b"}; //Khai báo mảng có kiểu String
array.push("hellu");


let array: number[];
array.push(3);

let blogs:{title: string, body: string}[];
blog.push({body: "hello", title:"vippro"};

- **Function TYPE trong Typescript**
const sum = (num1, num2) => {  //Khia báo như này thì sum1 và sum2 có kiểu any và trả về có kiểu any;
	return num1+num2;
}
sum("hello", 2);

const sum = (num1:number, num2: number) : number => {
	return num1+num2;
}

const sum = (num1:number, num2: number) => {  //Tự hiểu trả về giá trị number;
	return num1+num2;
}
 
type functiotype = (num1:number, num2: number) => number; //**function type**
const sum:functionType = (num1, num2) => {
	return num 1 + num2;
}

const hello = () => {
	console.log("hello");
}

const hello = (): void => {
	console.log("hi");
}

- **UNION TYPE và ENUM TYPE trong Typescript**
// *union*
let size : string | number; //Khia báo như này thì size vừa có kiểu là string và vừa có kiểu number;
size = "XL";
size = 30;

let size : string | string[];

// *enum*
enum color {
	RED = "RED",  
	GREEN = "GREEN",
	BLUE = "BLUE"
}

let color = Color.GREEN

- **Interface Type trong Typescript**
export interface Person{ //Để sử dụng Person trong file khác ta sử dụng export, file nào cần thì import
	name: string
	age?: number
}
let actor:Person;
actor  = {age: 30, name: "viet"};
actor1 = {name: "hello"};

- **Generic Type trong Typescript**
const hello = <Type> (a:Type) => { //khai báo như này thì ta bắt buộc người dùng phải nhập kiểu dữ liệu muốn truyền vào biến a, như dưới.
	const.log(a);
	return 3;
	
}
hello<number>("30);


- **Class trong Typescript**
class car {
	public name: string;
	private year: number;
	readonly Id : number;
	constructor (name: string, year: number, Id: number) {
		this.name = name;
		this.year = year;
		this.Id = Id;
		
	}
}
let carl = new Car("Xe hơi", 1995, 1);
carl.name = "Hello ae wibu"


// phiên banr ngắn hơn của class
class car {
	constructor (name: string, year: number, Id: number) {
		this.name = name;
		this.year = year;
		this.Id = Id;
		
	}
}
let carl = new Car("Xe hơi", 1995, 1);

















