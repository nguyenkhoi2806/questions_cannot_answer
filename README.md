## Javascript

### Ưu điểm:
- Thoải mái khi sử dụng, không bị ràng buộc kiểu dữ liệu.
- Ðỡ tốn thời gian setup ban đầu, vào dự án là có thể code liền dược.
- Code một mình là bao sướng.

### Nhược điểm:
- Lâu lâu quay lại, ko nhớ tên thuộc tính hay phương thức phải tra cứu lại. (nó hổng có nhắc 😅 )
- Phải hiểu cách hoạt động của JS, nhiều lúc nó hơi ma thuật 🤣 Ðiều này gây hơi khó khắn tí cho mấy bạn mới.

### Nên dùng cho:
- Dự án vừa và nhỏ.
- Team ít người (1-5 người)
- Có kinh nghiệm làm việc với Javascript.

### Bind là gì
- Cho phép ràng buộc this cho một phương thức (function)
- Phương thức bin sẽ trả vể 1 hàm mới với context được bind
- Hàm được trả về từ bind vẫn có thể nhận các đối số của hàm gốc

### Synchronous là gì ? 
- Có nghĩa là xử lý đồng bộ, chương trình sẽ chạy theo từng bước và chỉ khi nào bước 1 thực hiện xong thì mới nhảy sang bước 2, khi nào chương trình này chạy xong mới nhảy qua chương trình khác. 
#### Mặt tốt của Synchronous: 
- Chương trình sẽ chạy theo đúng thứ tự và có nguyên tắc nên sẽ không mắc phải các lỗi về tiến trình không cần thiết.
#### Mặt xấu của Synchronous
- Chương trình chạy theo thứ tự đồng bộ nên sẽ sinh ra trạng thái chờ và là không cần thiết trong một số trường hợp, lúc này bộ nhớ sẽ dễ bị tràn vì phải lưu trữ các trạng thái chờ không cần thiết.

### Asynchronous là gì? 
- là xử lý bất động bộ, nghĩa là chương trình có thể nhảy đi bỏ qua một bước nào đó,  được ví như một chương trình hoạt động không chặt chẽ và không có quy trình nên việc quản lý rất khó khăn
#### Mặt tốt của Asynchronous: 
- Có thể xử lý nhiều công việc một lúc mà không cần phải chờ đợi nên tạo cảm giác thoải mái 
#### Mắt xấu: 
- Nếu một chuong trình đòi hỏi phải có quy trình thì bạn không thể sử dụng Asynchronous được. vd: Một thao tác thêm dữ liệu phải thông qua hai công đoạn là validate dữ liệu và thêm dữ liệu, nếu thao tác validate xảy ra sau thao tác thêm thì còn gì tệ hại hơn nữa 😃.

### Set Timer function
- setImmediate() : chạy ngay lập tức (như cái tên của nó) =))
- setTimeout() : chạy trong một khoảng thời gian. thường được sử dụng nếu  muốn hàm của mình thực thi bao nhiêu mili giây kể từ khi gọi method setTimeout()
- setInterval(): lặp đi lặp lại trong khoảng thời gian

### Clear timer functions
- clearImmediate() : dừng một setImmediate objects, tạo bởi hàm setImmediate()
- clearTimeout() : dừng một setTimeout objects, tạo bởi hàm setTimeout()
- clearInterval() : dừng một setInterval objects, tạo bởi hàm setInterval()

### Server side rendering 
- Khi người dùng vào một trang web, trình duyệt sẽ gửi GET request tới web server
- Web server sẽ nhận request, đọc dữ liệu từ database.
- Web server sẽ render HTML, trả về cho browser để hiển thị cho người dùng
### Ưu 
- Initial load nhanh, dễ otpimize, vì toàn bộ dữ liệu đã được xử lý ở server. Client chỉ việc hiển thị.
- SEO tốt vì khi bot của Google
- Chạy được trên phần lớn mọi trình duyệt, kể cả disable JavaScript vẫn chạy tố
### Nhược
- Mỗi lần người dùng chuyển trang là site phải load lại nhiều lần
- Nặng server vì server phải xử lý nhiều logic và dữ liệu. 
- Tốn băng thông vì server phải gửi nhiều dữ liệu thừa và trùng  (HTML, header, footer).
- Tương tác không tốt như Client Side rendering vì trang phải refresh, load lại nhiều lần.

### Client Side redering
- SPA – Single Page Application. Ứng dụng nằm trong 1 page duy nhất nên được gọi là Single Page Application.
#### Ưu: 
- Page chỉ cần load một lần duy nhất. Khi user chuyển trang hoặc thêm dữ liệu, JavaScript sẽ lấy và gửi dữ liệu từ server qua AJAX
- Chuyển logic sang client nên giảm tải được một phần cho server.
- Giảm được băng thông do chỉ cần lấy JSON và dữ liệu cần thiết, thay vì phải lấy toàn bộ trang
- SPA hoạt động mượt mà hơn vì code chạy trên browser, không cần load đi loại lại nhiều
#### Nhược điểm: 
- Initial load sẽ chậm hơn nếu không biết optimize. 
- Đòi hỏi project phải chia làm 2 phần riêng là back-end (REST api) và front-end
- Không chạy được nếu JavaScript bị disable, hoặc ở các trình duyệt cũ không nhận JavaScript ES6
- SEO không tốt bằng Server Side Rendering 

## instance of la gi 
- Nó trả về true nếu obj thuộc về Class hoặc một lớp kế thừa từ nó.
```
let arr = [1, 2, 3];
alert( arr instanceof Array ); // true
```

## Rest Parameter là gì?
- Rest Parameter (hay còn gọi là đại diện của các tham số còn lại) cho phép bạn biểu diễn một số lượng vô hạn đối số dưới dạng một mảng.
```
function myFunc(a, b, ...args) {
   // code
}
```

## ++ 
- Phép tăng giá trị hiện tại lên 1 đơn vị. Phép này có hai cách sử dụng đó là đặt nó trước biến và đặt nó sau biến.
- Trường hợp đứng trước biến thì nó sẽ tăng trước khi lấy giá trị, ví dụ: 
```
var c = 12;
alert(++c); // kết quả là 13
alert(c); // kết quả là 13
```
- Trường hợp đứng sau biến thì nó sẽ lấy giá trị rồi tăng lên: 
```
var c = 12;
alert(c++); // kết quả là 12
alert(c); // kết quả là 13
```

## arrown function vs function 
- Arrow function không định nghĩa giá trị this của riêng nó giống như function.
- Arrow function không phù hợp làm phương thức cho object
- Arrow function không thể sử dụng làm hàm constructor
- Arrow function không có thuộc tính prototype
- Arrow function không được hoisted
- Arrow function không bind arguments 

## Temporay dead zone la gi 
- Temporal Dead Zone (TDZ), nghĩa là sẽ đưa ra một ReferenceError khi ta truy cập một biến trước khi nó được khởi tạo, thay vì trả về undefined như cách khai báo var

## Xử lý bất đồng bô có 3 cách: 
- callback
- Promise
- Async / Await

## Promise: 
- resolve: một function sẽ được gọi nếu đoạn code bất đồng bộ trong Promise chạy thành công.
- reject: một function sẽ được gọi nếu đoạn code bất đồng bộ trong Promise có lỗi xảy ra.
- then: Dùng để xử lý sau khi Promise được thực hiện thành công (khi resolve được gọi) 
- catch: Dùng để xử lý sau khi Promise có bất kỳ lỗi nào đó (khi reject được gọi).
- finally: là những câu lệnh nằm trong khối mã finally phải được chạy hay được thực thi ở cuối cho dù có lỗi hay không

## High order function 
là function chấp nhận đầu vào và/hoặc đầu ra là một function được gọi là higher order function.

``
const plus2 = (number) => number + 2
console.log(plus2(3)) // 5
``


## Equality trong JavaScript?
- Strict comparison (ví dụ: ===) kiểm tra giá trị bằng nhau mà không tự động ép kiểu.
- Abstract comparison (ví dụ: ==) kiểm tra giá trị bằng nhau có tự động ép kiểu.
- So sánh object: Đối với so sánh object bằng tham chiếu: hai object được gọi là bằng nhau khi và chỉ khi chúng cùng tham chiếu đến cùng một địa chỉ bộ nhớ. Hay nói ngắn gọn là chúng hoàn toàn giống nhau.

``
let x = {};
let y = {}; // khởi tạo object độc lập
console.log(y == x); // false
console.log(y === x); // false
``

## Các loại dữ liệu tích hợp sẵn trong Javascript?
- string
- number
- boolean
- null và undefined
- object
- symbol (từ ES6)

## Scope
- Global scope: có phạm vị hoạt động ở bất kỳ trong mã javascript của bạn.
- Function scope: có phạm vi hoạt động trong function mà bạn khai báo biến đó.
- Block scope: có phạm vị trong cặp dấu {} mà bạn khai báo biến đó. (ES6)

## Javarcript la ngon ngu gi 
JavaScript mà hiện giờ có thể được coi là một ngôn ngữ lai, vừa là thông dịch vừa là biên dịch.
JavaScript có thể chạy, thực hiện các cậu lệnh từng dòng một trên trình duyệt mà không cần phải compiled.

biên dịch => V8 Engine  chuyển code JavaScript thành mã thay vì dùng interpreter.  Engine compile những dòng code trong lúc thực thi bằng việc thực hiện thông qua một JIT compiler (Just in Time Compilation)

## This trong javscript 
This trong javscript để đại diện cho một đối tượng (Object).

## Khac nhau của var, let, const
### var 
- Phạm vi hàm (function scope) hoặc phạm vi toàn cục (global scope)
- Có thể gán lại (Re-assignable) và có thể khai báo lại (Re-declarable)
- Không thuộc vùng chết tạm thời (Temporal Dead Zone - TDZ)

### let 
- Phạm vi khối (Block scope)
- Có thể gán lại nhưng không thể khai báo lại
- Phụ thuộc vào vùng chết tạm thời (TDZ) 

### const
- Phạm vi khối
- Không thể gán lại cũng không thể khai báo lại
- Phụ thuộc vào vùng chết tạm thời


## ES5 vs ES6 khac nhau nhu the nao
- es5 khac vs es6 co arrow function, co const let, promises, class, module, rest parameter, spread.

## Hoisting javascript?
 hoisting là cơ chế của JavaScript cho phép các khai báo biến hoặc hàm được dời lên trên đầu phạm vi của chúng trước khi thực thi đoạn code.
 
```
example: 
- console.log(hoist);
 var hoist = 500; output undefined
 => after hoiting 
 var hoist 
  console.log(hoist);
 var hoist = 500; 


- say_something('YOLO'); 
function say_something(a){
    console.log(a);
} 
`output: YOLO`

- do_something();
function do_something(){
    console.log(a);
    var a = 'fly';
}
`output: undefined`
```

## Usetrict trong Javascript
- Khi mot doan code co khai bao usestrict thi tat ca dong code o ben duoi phai dc quan ly 1 cach nghiem ngac ve cu phap 
```
vd x = 0;
console.log(windown.x) = 0;
khai vs usetrict se la undifine 
```

## Prototype
- Prototype là 1 phương thức dùng để hình thành lên 1 đối tượng của hàm contructor 
- Việc sử dụng prototype sẽ giúp tiết kiệm được bộ nhớ, có thể dùng chung cho các tối tượng được tạo ra từ phương thức new User ( ví dụ trực tiếp khai báo phương thức trong object constructor sẽ không hay bằng thêm qua prototype )

```
- example: 
// Tạo một hàm constructor function rỗng 
function Person(){
}

// Thêm thuộc tính name, age cho prototype property của hàm Person constructor 
Person.prototype.name = "Kien" ;
Person.prototype.age = 24;
Person.prototype.sayName = function(){
	console.log(this.name);
}

// Khởi tạo object sử dụng hàm khởi tạo của Person
var person1 = new Person();

// Truy cập tới thuộc tính name sử dụng đối tượng person
console.log(person1.name) // Output" Kien
```

## Event loop
- Event Loop là cơ chế giúp Javascript có thể thực hiện nhiều thao tác cùng một lúc
- Nhiệm vụ của Event Loop rất đơn giản đó là đọc Stack và Event Queue. Nếu nhận thấy Stack rỗng nó sẽ nhặt Event đầu tiên trong Event Queue và handler (callback hoặc listener) gắn với Event đó và đẩy vào Stack.


## Closure
-  closure là một hàm lưu nhớ nơi nó tạo  có thể truy cập tham chiếu các biến có phạm vi ngoài phạm vi của nó. Để sử dụng closure, đơn giản là bạn khai báo một function bên trong một function khác và return nó ra.
- Ứng dụng viết code ngắn hơn, thể hiện tính private trong oop 
```
example: 
function showName (firstName, lastName) {
   var nameIntro = "Your name is ";
   function makeFullName () {
        return nameIntro + firstName + " " + lastName;
   }
    return makeFullName ();
}
showName ("Michael", "Jackson"); //
```

## PureFunction
- Luôn trả về kết quả giống nhau khi tham số truyền vào giống nhau. Nó không bị phụ thuộc bởi bất cứ tham số nào ngoài hàm mà chỉ phụ thuộc duy nhất vào tham số truyền vào.
```
example: 
function priceAfterTax(productPrice) {
 return (productPrice * 0.1) + productPrice;
}
```

## yarn vs npm 
### npm 
- lấy các dependencies từ kho chứa của nó, nó sẽ cài đặt các dependencies từng cái một sau khi một cái khác được cài đặt xong, vì vậy sẽ mất rất nhiều thời gian.
- Nếu như một package không có trong NpmJS, hãy quên nó đi.
- Không hỗ trợ cài đặt offline

### yarn
- Nếu bạn đã cài đặt một package trước đó, Yarn sẽ tạo một bản sao trong bộ nhớ cached để hỗ trợ việc cài đặt offline.
- Yarn cung cấp một cấu trúc các dependencies bằng phẳng so với cấu trúc lồng nhau của npm.

## Callback
Là một hàm truyèn qua đối số khi gọi hàm khác
```
- example 
function doHomework(subject, callback) {
    setTimeout( function(){
        console.log(`Bắt đầu làm bài tập ${subject}.`);
        callback();
    }, 5000);
}
function alertFinished(){
    console.log('Làm bài tập xong!');
}
doHomework('Toán', alertFinished);
```

## Set
- Set trong JavaScript là một loại object dùng để lưu trữ dữ liệu mà không trùng lặp.
```
- example: 
  `const myArray = [1, 2, 3, 4, 5, 5, 5, 2];
   const mySet = new Set(myArray);
   console.log(mySet);
    // Set {1, 2, 3, 4, 5};`
```

## Map
- Map trong JavaScript là một cấu trúc dữ liệu cho phép lưu trữ dữ liệu theo kiểu key-value, tương tự như object.
- Tuy nhiên, chúng khác nhau ở chỗ là:
- Object chỉ cho phép sử dụng String hay Symbol làm key.
- Map cho phép mọi kiểu dữ liệu (String, Number, Boolean, NaN, Object,...) có thể làm key.

```
- example: 
function func4() {
  const map4 = new Map(arguments);
  console.log(map4);
}
func4(["one", 1], ["two", 2], ["three", 3]);
// Map(3) {"one" => 1, "two" => 2, "three" => 3}
```

## Array map 
đây là hàm dùng để lặp qua các phần tử của mảng và cho phép xử lý giá trị của phần tử đó.

## Array reduce 
là một phương thức được sử dụng để thực thi một hàm lên các phần tử của mảng (từ trái sang phải) với một biến tích lũy để thu về một giá trị duy nhất. 
```
- example: 
const data = [5, 10, 15, 20, 25];
const res = data.reduce((total,currentValue) => {
  return total + currentValue;
});
console.log(res); // 75


## Khác nhau localStorage vs sessionStorage vs Cookie
### LocalStorage 
- giống như một database của browser sẽ được lưu trử những thông tin của người dùng browser. Thông tin này được lưu trữ vĩnh viễn tới khi bạn xóa nó đi 
Vd: theme, danh mục sản phẩm được chọn, giao diện tuỳ chỉnh, dashboard, layout ...

### SessionStorage 
- khá giống với localStorage. Ngoại trừ sessionStorage sẽ mất đi khi chúng ta đóng tab, đóng trình duyệt.
- 1 Khuyết điểm của session Storage vs Local Storage là có thể bị đọc bởi Javascript. Do đó dễ bị đánh cắp thông tin. Vì vậy, chúng ta không nên lưu trữ những thông tin nhạy cảm như token ID, password, username, email của người dùng vào localStorage hay sessionStorage.

### Cookie 
- là một bản ghi đơn giản gồm key, value và được gửi kèm theo request của browser cho nên bạn có thể truy cập và xử lý cookie ở server side dựa vào cookie được gắn kèm với request, giới hạn về dung lượng lưu trữ khoảng 4KB
- Khi đóng một tab, Cookie vẫn còn được lưu trên trình duyệt.
- Cookie có thể mất đi sau khi đóng trình duyệt nếu nó được set expires là N/A
- Cookie có option để chúng ta set ngày quá hạn cho nó. Nghĩa là có thể định nghĩa khi nào nó tự động xoá được. 

## Các mã status trong http: 
### 1xx (100 – 199): 
- Yêu cầu đã được chấp nhận và quá trình xử lý yêu cầu của bạn đang được tiếp tục.

### 2xx (200 – 299): 
- Yêu cầu của bạn đã được máy chủ tiếp nhận, hiểu và xử lý thành công.

### 3xx (300 – 399): 
- Phía client cần thực hiện hành động bổ sung để hoàn tất yêu cầu.

### 4xx (400 – 499): 
- Lỗi phía client – Yêu cầu không thể hoàn tất hoặc yêu cầu chứa cú pháp không chính xác. 4xx sẽ hiện ra khi có lỗi từ phía client do không đưa ra yêu cầu hợp lệ.

### 5xx (500 – 599): 
- Server errors / Lỗi phía máy chủ – Máy chủ không thể hoàn thành yêu cầu được cho là hợp lệ. Khi 5xx xảy ra, bạn chỉ có thể đợi để bên hệ thống máy chủ xử lý xong.


## ReactJs

###  React hoạt động như thế nào?
- React tạo ra một DOM ảo.
- Khi trạng thái thay đổi trong một component, trước tiên nó chạy một thuật toán "khác biệt (diffing)", xác định những gì đã thay đổi trong DOM ảo.
- Bước thứ hai là điều chỉnh (reconciliation), nơi nó cập nhật DOM với kết quả của khác biệt.

### Ưu 
- Dễ dàng chia và sử dụng lại component
- Sử dụng mấy thằng thứ 3 để lên layout, UI như Ant Design rất tiện, đẹp, nhanh chóng.
- Làm việc với vấn đề test giao diện.
- Compile source tương đối nhẹ, source tầm 200MB mà deploy ra chỉ tầm gần 1MB.
- Nhiều thư viện hổ trợ 
- Biết Reacjs bạn có thể code luôn mobile app.

### Nhược điểm
- Reactjs chỉ phục vụ cho tầng View
- Khó tiếp cận cho người mới học Web
- SEO khong hiệu quả 

### Khách nhau Virtualral Dom vs Dom thiệt
- Real DOM: Update chậm, Có thể update trực tiếp HTML, Tạo ra DOM mới nếu element update,  Lãng phí nhiều bộ nhớ
- Virtual DOM: Update nhanh, Không thể update trực tiếp HTML, Update JSX nếu element update, Không lãng phí bộ nhớ

### Dom là gì
- DOM là tên gọi viết tắt của (Document Object Model). Là một chuẩn được định nghĩa bởi W3C. DOM được dùng để truy xuất và thao tác trên các tài liệu có cấu trúc dạng HTML hay XML bằng các ngôn ngữ lập trình thông dụng như Javascript, PHP

### Virtural Dom 
-  là một Abstraction nhẹ của DOM. việc cập nhập không gây ảnh hưởng tới DOM thực Nó có tất cả các thuộc tính giống như object DOM thật, nhưng nó không có khả năng update trực tiếp như DOM thật. Trong thực tế, các Virtual DOM mới sẽ được tạo sau khi render lại.

### React Dom là gì ? 
- Thư viện để render element, và dùng element đó render vào Dom là cầu nối giữa React và DOm

### Tại sao function phải bind ở Contructstor
- Lấy đúng context (ngữ cảnh) mà mình cần để dùng ở trong function đó.
- Tránh việc sinh ra một method mới.

### Supper trong reactjs 
- Việc gọi super ở đây nhằm mục đích khởi tạo biến this từ Parent, vì  1 Component được thừa kế từ React.Component. Sau khi gọi super, chúng ta sẽ truy cập được this một cách bình thường.
- Khi làm việc với React thì khi viết constructor mà không có super() thì sẽ lỗi. Không viết super(props) thì sẽ không thể dùng được this.props.
- Trong Javascript super như là "hàm khởi tạo của class cha" (parent class constructor). 
  
### Vong doi reactjs 
gom 3 pha chinh, Mounting, updating, Unmounting: 
- Mounting: gom cac ham: constructor, render, componentDidmount, 
- Updating: gom cac ham : render(), ShouldComponentUpdate, ComponentDiDUpdate, ComponentWillRecieveProps: 
- ComponentDidUpdate se chay khi tat ca cac component Da dc update, 
- ShouldComponentuPdate: se ngan chan lai viec co nen Render lai khi state cap nhat khong thay doi gia tri moi 

- UnMounting: la giai doan khi component do bi xoa ra khoi Dom.

### Middleware trong reacjs
1 mot ham ma khi 1 component goi 1 action truoc khi tra ve store  de update se thong 1 ham moddiware modify sau tra nguoc ve store de update
thong thuong o day la async wait

### PureComponent 
chính xác giống như Component ngoại trừ việc đó là nó xử lý shouldComponentUpdate cho bạn. Khi su dung Purecomponent se han che duoc hop khi nao can rerender khi nao khong 
vi du chi render khi props vs state thay doi.
PureComponent dùng cho các React Class Component, còn React Functional Component thì dùng... memo.
 
### Global state
la 1 state dc su dung o nhieu component khac nhau 

### Local state: 
la state dc su dung cho 1 component khai bao state do ma thoi 

### Su dung componentWillUnmount nhu the nao trong react hook
```
useEffect(() => {
  // almost same as componentDidMount
  console.log('mounted!');
  return () => {
    // almost same as componentWillUnmount
    console.log('unmount!');
  };
}, []);
```
### Higher-Order component (HOC)
- là một hàm nhận một component và trả về một component mới

### Refs la gì 
- Refs thường được dùng để trả về một tham chiếu tới 1 phần tử. Refs cho phép bạn truy cập trực tiếp vào phần tử DOM hoặc một phiên bản của thành phần.

### Stateless component 
- là component không phụ thuộc vào life circle

### Statefull component 
- Nếu hành vi của một component phụ thuộc vào state của component thì nó có thể được gọi là Stateful component.

### Memoization
- Tính toán và lưu kết quả cho từng bộ input.
- Khi gặp lại bộ input đã từng làm thì không tính toán lại, mà trả về kết quả sẵn có.

### React.Memo
- React.memo là một higher order component, được sử dụng để bọc các component. ghi nhớ lại prop cua component để quyết có render lại hay không.  => Tránh đến việc render lại component ko cần 
- 

### Khi nào sử dụng React.memo ? 
- Component là functional component
- Component luôn luôn bị re-render mặc dù prop không thay đổi
- Component của bạn chứa một lượng lớn tính toán logic và UI như Chart, Canvas, 3D library

### Khi nào không nên React.memo ?
- Nếu component của bạn prop không thay đổi
- Component của bạn là class component
- Component của bạn đã được memo bởi một HOC khác, ví dụ connect() của Redux.

### useSelector = mapStateToProps
### useDispatch = dispatch 

### useMemo
-  Tránh thực hiện 1 logic nào đó không cần thiết.  
-  Chỉ tính toán value mới khi dependencies thay đổi.
```
 const squaredNum = useMemo(()=> {
    return squareNum(number);
  }, [number]);
  
const squareNum(number){
  console.log("Squaring will be done!");
  return Math.pow(number, 2);
}
 return (<>{ squaredNum }</>)
```
 
### useCallback
- Giúp mình tránh tạo ra hàm mới 1 cách không cần thiết, và chỉ tạo ra function mới khi dêpndencies thay đổi .
- Nếu dùng empty dependencies thì không bao giờ tạo ra function mới ,
- Tránh đến việc rerender không cần thiết giữa component cha va component con 

### So sánh useCallback() vs useMemo()
#### GIỐNG NHAU: 
- Đều áp dụng kĩ thuật memoization.
- Đều nhận vào 2 tham số: function và dependencies.
- Đều là react hooks, dùng cho functional component.
- Dùng để hạn chế những lần re-render dư thừa (micro improvements).

#### KHÁC NHAU:
- useCallback dùng để memoized callback
- UseMemo memoized value

### Có nên sử dụng useCallback() vs useMemo() hay không?
- Nên dùng cho: đồ thị, biểu đồ, animations, những component nặng phần render.

### React.memo vs shouldComponentUpdate
-  React.memo là một higher order component (HOC) được sinh ra nhằm sử dụng cho các functional component trong việc tối ưu hiệu suất render,  React.memo chỉ có thể xác định việc rerender dựa trên sự thay đổi của props 
-  shouldComponentUpdate là một method của class based component, shouldComponentUpdate có thể xác định việc rerender dựa trên sự thay đổi của cả props và state.

### Custom hook 
- Là một function, nhận input và trả output.
- Tên của nó bắt đầu bởi use như useQuery, useColor, …
- Khác với functional component, custom hooks trả về một dữ liệu bình thường, không phải là jsx.
- Tại sao sử dụng custom hook : 
- Tái sử dụng ở nhiều component khác nhau có cùng logic xử lý. Từ đó nếu logic thay đổi thì chỉ cần sửa tại một nơi duy nhất.
- Chia sẻ dữ liệu, logic giữa các component.
- Ẩn các đoạn code có logic phức tạp của một component, giúp component dễ đọc hơn.

### React fragment
- React Fragment cho phép bọc các elemnt bên trong. 

### React và ReactDOM
- React và ReactDOM chỉ mới được chia thành hai thư viện khác nhau. ReactDOM trưng bày các phương thức dành riêng cho DOM, trong khi React có các công cụ cốt lõi được React chia sẻ trên các nền tảng khác nhau

### Design parten pho bien react
- Condition Rendering
- High order component 
- Container component
- Layout component
- Style component
- Stateless Component

### StrictMode là gì ? 
- React là một component trợ giúp sẽ giúp các React component tốt hơn nhiệm vụ chính: 
- Xác minh rằng các component bên trong đang tuân theo một số phương pháp được đề xuất và cảnh nếu không có trong bảng điều khiển.
- Xác minh rằng các method không được sử dụng sẽ cảnh báo bạn trong bảng điều khiển.
- Giúp ngăn ngừa một số tác dụng phụ bằng cách xác định các nguy cơ tiềm ẩn


## Redux
### Cách tổ chức Redux 
- Cách chia store: store sẽ chia theo từng đối tượng. 
- Sử dụng selectors để lấy các giá trị trong store. tái sử dụng lại các selectors đó. 
- Sử dụng middleware redux-thunk hoặc saga 
- Đưa nhiều logic và trong Reducer 
- Tách các logic phức tạp ra khỏi component
- Đảm bảo state được tạo ra và sử dụng cho nhiều component. Tránh duplicate state.

### Cách cải thiện Performance Redux 
- Sử dụng createSelector  
- Sử dụng duy nhất 1 action 
- Sử dụng batch trong redux 

### Ưu điểm của Redux
- Dể debug vs test 
- Có tool monitor  
- Sử dụng dc nhiêu cho thư viện như react vs angular, vujes. 
- Đoán trước dc stage thay đỗi la 

### Nhược điểm Redux
- Phải hiểu được cách hoạt động của Redux. 
- Chỉ có 1 store ko chia thành nhiều store => sẽ dẫn đến tình trạng state sẽ bị trùng 
- Tăng độ phức tap cho codeing  

### Redux-Thunk 
- là một middleware phổ biến nhất được dùng để xử lý các action bất đồng bộ trong Redux

### Selectors là gì?
- Nói một cách đơn giản, Selectors một đoạn logic được sử dụng để tính toán ra một giá trị nào đó từ các giá trị có sẵn trong Store hoặc chỉ đơn giản là lấy một giá trị có sẵn trong Store.
- Tại sao sử dụng selector: 
- Selectors giúp chúng ta dễ dàng lấy hoặc tính toán một giá trị có sẵn trong Store.
- Một selectors sẽ không tính toán lại trừ khi một trong các đối số của nó thay đổi.
- Selectors dễ dàng tái sử dụng, và nó có thể sử dụng để làm đầu vào cho các selector khác.

### Reselect để tạo selectors? 
- Reselect giúp cải thiện performance vì nó cung cấp một cách để tạo selectors được ghi nhớ và chỉ tính toán lại khi đầu vào của chúng thay đổi. 

### Reducers 
- là những action handler, nó hoạt động kết nối giữa action và store và biến thành những thay đổi trong state. 

## Typescript: 
### Typescript là gì: 
- TypeScript là một ngôn ngữ, hướng đối tượng và biên dịch. Được phát triển bơi Microsoft. Nó là một phần mở rộng của JavaScript.

### Ưu điểm: 
- Typescript thêm tính năng Static Typing vào JavaScript, giúp dễ dàng phát triển và duy trì các ứng dụng phức tạp hơn 
- Hỗ trợ OOP mạnh
- Với static typing (kiểm tra lỗi lúc compile time), code viết bằng TypeScript dễ dự đoán hơn, và dễ debug hơn.
- Nhắc code tuyệt vời 😍
- Truyền sai kiểu dữ liệu là nó chửi =))
- Lâu lâu quay lại code hoặc người khác code cho mình thì đều được nhắc tên thuộc tính, phương thức

### Nhược điểm
- Bắt buộc dùng biên dịch
- Phải tốn thời gian setup ban đầu + khai báo kiểu dữ liệu.
- Ðôi khi việc khai báo kiểu dữ liệu nhiều quá khiến code trở nên rườm rà.
- Giữ phần khai báo dữ liệu up to date.

### Nên dùng cho:
- Dự án lớn.
- Team có nhiều người cùng code (>5 người)
- Chưa quen làm việc với kiểu dynamic type của JS.


### Tại sao Typescript hỗ trợ Opp tót hơn javscript 
- Hổ trợ nhiều biến dữ liệu mà  javscript ko có
- có protect public private readly 

### Static Typing là gì?
- Mỗi biến (variable) có một kiểu cố định liên kết với nó. Kiểu của biến được kiểm tra lúc compiled-time và trình biên dịch yêu cầu ta phải khai báo rõ kiểu của biến trước khi sử dụng.

###  Interface trong Typescript là gì? 
- interface là một cấu trúc khai báo các tiêu chuẩn. Các lớp được dẫn xuất (derived) từ một interface phải tuân thủ các tiêu chuẩn do interface đặt ra.

### Public, Private, Protected và Readonly modifiers trong Typescript là gì?
- Public: Nó được truy xuất ở mọi nơi.
- Private: không thể truy xuất chúng từ ngoài class của nó.
- Protected giống như Private nhưng khác 1 điểm là nó có thể được truy xuất bởi instance của lớp kế thừa.
- Readonly: được sử dụng để làm cho một thuộc tính ở dạng chỉ đọc, có thể được truy cập bên ngoài lớp, nhưng giá trị của chúng không thể thay đổi

### Optional parameters là gì: 
- là một thuộc tính có thể có hoặc không có 

## Tại sao quan tâm Mobile first
- Tối ưu cho người dùng di động
- Đở tốn thơi gian làm App

## Put Api, Patch Api 
- put update toan bo entity 
- patch update 1 phan entity

## CI/CD
 - CI (Continuous Integration) và CD (Continuous Delivery), ý nói là quá trình tích hợp (integration) thường xuyên, nhanh chóng hơn khi code cũng như thường xuyên cập nhật phiên bản mới (delivery).

## Webback 
- Chia nhỏ toàn bộ tài nguyên các thư viện và các tài nguyên phụ thuộc thành các "chunk" và chỉ tải các thành phần nhỏ này khi cần thiết.
- Giúp quá trình tải các tài nguyên nhanh.
- Mọi file tĩnh sau quá trình đóng gói sẽ ở dạng module.
- Cho phép tích hợp các thư viên bên thứ ba ở dạng module.

## Restful API là gì?
- Restful API là một trong những tiêu chuẩn được sử dụng để thiết kế API cho các ứng dụng web,  truyền tải thông qua HTTP. Một chức năng quan trọng nhất của REST là: quy định các cách sử dụng HTTP method chẳng hạn như: Post, Get, Delete, Put,..

## Tai sao viet Unitest
- Tạo ra môi trường lý tưởng để kiểm tra bất kỳ đoạn code nào
- Phát hiện các thuật toán thực thi không hiệu quả,
- Phát hiện các vấn đề về thiết kế, xử lý hệ thống,
- Phát hiện các lỗi nghiêm trọng có thể xảy ra trong những tình huống rất hẹp.

## Sass
- Các chức năng của sass: Variables, Mixin, Import, Function,  Loops, Extends

## Lợi ích của Sass
- Code nhanh chóng hơn. hiệu quả hơn và tiết kiệm hơn thời gian và công sức trong việc viết CSS
- Có nhiều features trong sass

## Điểm bất lợi của Sass
- Phải combile ra css tốn thơi gian 
- phải tốn thời gian học thêm  về sass 

## Cach de optomize Fe nhanh hơn
- Han che render nhung html ko can thiet vi du br space 
- Nen su dung before after de thay the. 
- css nen viet ngan gon 
```
vi du: 
padding-top: 10px;
padding: 10 0 0 10px; 
```
- Nen load nhung data nao that su can thiet cho page. 
- Nen chia cac file css thanh nhieu file thay vi gom chung lai 1 file. 
- Han che plugin lib khong can thiet 
- xu thu vien nhu webpack gulp de nen file css lai 
- Khong dc style inline trong html 

## Css

### FlexBox:
- Gồm Container và items; 
- Container:
- main-axis: quyết định hướng của các items 
- main-start: quyết định item hiện thị theo hướng nào 
- cross-axis: luôn vuông góc với trục chính: gồm cross-start, cross-end

- Items: 
- cross-size: kích thước với chiều song song với cross axis 
- main-size: kích thước với chiều song song với main axis

- Thuộc tính bao gồm: 
- display: flex: quyết định có sử dụng layout flexbox hay không. 
- flex-direction: row | collumn: thay đổi được phương hướng của main-axis mặc định là row.
- flex-wrap: norwrap | wrap | wrap-reverse quyết định item hiển thị theo cách nào xuống dòng hoặc nằm ngang. 
- flex-axis: xét kích thước của main-size
- justify-content: canh các item theo phương.
- align-content: giống justify-content nhưng trùng phương hướng với trục cross size
- flex-grow: Dùng để thay đổi kích thước của main-size 
- flex-shrink: Dùng để thu nhỏ lại
- order: quuyết định thứ tự item. 

### BEM 
- viet tac cua Block Element Modifier

### Css Unit
- Asolute unit: px, pt, cm, pc. S
- Relative unit: 
- %: Kích thước phụ thuộc vào thẻ chứa nó. 
- rem: phụ thuộc vào thẻ html
- em: phục thuộc vào font-size thẻ gần nhất chưá nó
- vw (viewport width): ví dụ (1vw: có nghĩa là 1% chiều dọc ngang của kích thuớc trình duyệt)
- vh (viewport hieght): ví dụ (1vh: có nghĩa là 1% chiều dọc đứng của kích thuớc trình duyệt)

### Background-clip: 
- Quyết định background đổ từ ranh giới nào.
- border-box: đổ background từ border vào bên trong
- padding-box: đổ backgrounnd từ padding
- content-box: đổ background từ content. 

### Background-size
- contain: lấy chiều dài nhất có thể đảm bảo hình ảnh không bị cắt xén
- cover: chọn chiều nhất của ảnh nhưng sẽ che khuất ảnh và sẻ không hở khoảng trắng
 
### Background-origin: giong background-clip nhưng dùng đi kèm với background-image

### Function css
- var(): đặt biến cho css; 
- linear-gradient: tạo ra 1 dải màu chuyễn đều đặn từ trái sang phải hoặc từ trên xuống dưới
- rgba: red, green, blue, alpha ( độ trong suốt) 
- calc: tính toán 
- attr: lấy dc content attr trong html

### Pseduo-classes
 - lớp giả
 - :root: tham chiếu đến phần tử gốc html 
 - :hover: tham chiếu đến phần tử đang được hover
 - :active: tham chiếu đến phần tử đang được click vào
 - :first-child: tham chiếu đến phần tử đầu tiên của class đó
 - :last-child: tham chiếu đến phần tử cuối cùng của class đó

### Pseduo-element 
- phần tử giả
- ::before 
- ::after
- ::first-letter: ký tự đầu tiên của chữ
- ::first-line: dòng chữ đầu tiên 
- ::selection: tham chiếu khi select nôi dung trên trình duyệt

### Position
- Thiết lập vị trí cho các element
- Relative: tương đối, sẽ không phụ thuộc vào đối tượng nào khác chỉ phụ thuộc vào chính element đó
- Absolute: vị trí tuyệt đối sẽ phụ thuộc vào thẻ cha gần nhất có thuộc tính position. 
- fixed: sẽ phụ thuộc vào trình duyệt.
- sticky: sẽ cố định phần tử khi trình duyệt scroll đến phần tử đó

## Câu hỏi ngoài lề

### Solid principle: 
- single responsiple principle: moi 1 calss chi dam nhiem 1 chuc nang duy nhat
- open close: khi co 1 chuc nang moi thi nen mo rorng class, hoa viet 1 class moi ke thua class do khong nen ssua lai class cu 
- linkos principle: Cac interface class con co the thay class cha ma kohng gay ra loi 
- interface segregration: 1 tinterface lon  nen chia ra nhieu interface nho 
- depenci inversion: cac thanh phan trong module phu thuoc vao class abtract khong nen phu thuoc vao ca

### Design parten
Nói một cách đơn giản, design pattern là các mẫu thiết kế có sẵn, dung để giải quyết một vấn đề, Áp dụng mẫu thiết kế này sẽ làm code dễ bảo trì, mở rộng hơn, 3 loại chính
- Creational Pattern tập hợp các giải pháp liên quan đến khởi tạo đối tượng.
Nhóm này gồm 5 mẫu thông dụng: 
Factory Method, Abstract Factory, Builder, Prototype, Singleton
- Structural Pattern tập hợp các giải pháp liên quan đến thiết lập kết cấu, liên hệ giữa các đối tượng.
Nhóm này gồm 7 mẫu thông dụng: Adapter, Bridge, Composite, Decorator, Facade
- Behavioral Pattern: tập hợp các giải pháp liên quan đến các hành vi của đối tượng và giao tiếp giữa các đối tượng khác nhau.
Nhóm này gồm 11 mẫu thông dụng: Strategy, State, Observer

