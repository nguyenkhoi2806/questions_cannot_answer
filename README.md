## Javascript

## High order function 
là function chấp nhận đầu vào và/hoặc đầu ra là một function được gọi là higher order function.

``
const plus2 = (number) => number + 2
console.log(plus2(3)) // 5
``


## Equality trong JavaScript?
- Strict comparison (ví dụ: ===) kiểm tra giá trị bằng nhau mà không tự động ép kiểu.
- Abstract comparison (ví dụ: ==) kiểm tra giá trị bằng nhau có tự động ép kiểu.

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
# var 
- Phạm vi hàm (function scope) hoặc phạm vi toàn cục (global scope)
- Có thể gán lại (Re-assignable) và có thể khai báo lại (Re-declarable)
- Không thuộc vùng chết tạm thời (Temporal Dead Zone - TDZ)

# let 
- Phạm vi khối (Block scope)
- Có thể gán lại nhưng không thể khai báo lại
- Phụ thuộc vào vùng chết tạm thời (TDZ) 

# const
- Phạm vi khối
- Không thể gán lại cũng không thể khai báo lại
- Phụ thuộc vào vùng chết tạm thời


## ES5 vs ES6 khac nhau nhu the nao
- es5 khac vs es6 co arrow function, co const let, promises, class, module

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
- Prototype là cơ chế mà các object trong javascript kế thừa các tính năng từ một object khác.

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
- là một Queue, tất cả cá event được push vào Queue này, mỗi khi một sự kiện được phát ra nó sẽ được push vào Queue. Trong Queue này, thứ tự thực hiện là vào trước thì sẽ được xử lí trước, vào sau thì được xử lí sau.

## Closure
- Trong javascript, closure là một hàm tham chiếu các biến có phạm vi ngoài phạm vi của hàm đó. Nó cho phép bạn truy cập các biến hoặc tham số có phạm vị ngoài phạm vị hàm đó. Để sử dụng closure, đơn giản là bạn khai báo một function bên trong một function khác và return nó ra.
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
npm 
- lấy các dependencies từ kho chứa của nó, nó sẽ cài đặt các dependencies từng cái một sau khi một cái khác được cài đặt xong, vì vậy sẽ mất rất nhiều thời gian.
- Nếu như một package không có trong NpmJS, hãy quên nó đi.
- Không hỗ trợ cài đặt offline

yarn
- Nếu bạn đã cài đặt một package trước đó, Yarn sẽ tạo một bản sao trong bộ nhớ cached để hỗ trợ việc cài đặt offline.
- Yarn cung cấp một cấu trúc các dependencies bằng phẳng so với cấu trúc lồng nhau của npm.

## Callback
Callback là một hàm sẽ được thực hiện sau khi một hàm khác đã thực hiện xong - vì thế nó có tên là callback.
Callback là một cách để đảm bảo code nhất định không thực thi cho đến khi code khác thực hiện xong.
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
```

## Khác nhau localStorage vs sessionStorage vs Cookie
# LocalStorage 
- giống như một database của browser sẽ được lưu trử những thông tin của người dùng browser. Thông tin này được lưu trữ vĩnh viễn tới khi bạn xóa nó đi 
Vd: theme, danh mục sản phẩm được chọn, giao diện tuỳ chỉnh, dashboard, layout ...

# SessionStorage 
- khá giống với localStorage. Ngoại trừ sessionStorage sẽ mất đi khi chúng ta đóng tab, đóng trình duyệt.
- 1 Khuyết điểm của session Storage vs Local Storage là có thể bị đọc bởi Javascript. Do đó dễ bị đánh cắp thông tin. Vì vậy, chúng ta không nên lưu trữ những thông tin nhạy cảm như token ID, password, username, email của người dùng vào localStorage hay sessionStorage.

# Cookie 
- là một bản ghi đơn giản gồm key, value và được gửi kèm theo request của browser cho nên bạn có thể truy cập và xử lý cookie ở server side dựa vào cookie được gắn kèm với request, giới hạn về dung lượng lưu trữ khoảng 4KB
- Khi đóng một tab, Cookie vẫn còn được lưu trên trình duyệt.
- Cookie có thể mất đi sau khi đóng trình duyệt nếu nó được set expires là N/A
- Cookie có option để chúng ta set ngày quá hạn cho nó. Nghĩa là có thể định nghĩa khi nào nó tự động xoá được. 

## Các mã status trong http: 
# 1xx (100 – 199): 
- Yêu cầu đã được chấp nhận và quá trình xử lý yêu cầu của bạn đang được tiếp tục.

# 2xx (200 – 299): 
- Yêu cầu của bạn đã được máy chủ tiếp nhận, hiểu và xử lý thành công.

# 3xx (300 – 399): 
- Phía client cần thực hiện hành động bổ sung để hoàn tất yêu cầu.

# 4xx (400 – 499): 
- Lỗi phía client – Yêu cầu không thể hoàn tất hoặc yêu cầu chứa cú pháp không chính xác. 4xx sẽ hiện ra khi có lỗi từ phía client do không đưa ra yêu cầu hợp lệ.

# 5xx (500 – 599): 
- Server errors / Lỗi phía máy chủ – Máy chủ không thể hoàn thành yêu cầu được cho là hợp lệ. Khi 5xx xảy ra, bạn chỉ có thể đợi để bên hệ thống máy chủ xử lý xong.


## ReactJs

## Supper trong reactjs 
la khi viet contructor phai co supper, vi khi khau bao supper chung ta se xu dung dc this trong component do , va neu khong khai bao trong contustor thi se bi loi 

## Vong doi reactjs 
gom 3 pha chinh, Mounting, updating, Unmounting: 
- Mounting: gom cac ham: constructor, render, componentDidmount, 

- Updating: gom cac ham : render(), ShouldComponentUpdate, ComponentDiDUpdate, ComponentWillRecieveProps: 
- ComponentDidUpdate se chay khi tat ca cac component Da dc update, 
- ShouldComponentuPdate: se ngan chan lai viec co nen Render lai khi state cap nhat khong thay doi gia tri moi 

- UnMounting: la giai doan khi component do bi xoa ra khoi Dom.

## Middleware trong reacjs
1 mot ham ma khi 1 component goi 1 action truoc khi tra ve store  de update se thong 1 ham moddiware modify sau tra nguoc ve store de update
thong thuong o day la async wait

## PureComponent 
chính xác giống như Component ngoại trừ việc đó là nó xử lý shouldComponentUpdate cho bạn. Khi su dung Purecomponent se han che duoc hop khi nao can rerender khi nao khong 
vi du chi render khi props vs state thay doi.
PureComponent dùng cho các React Class Component, còn React Functional Component thì dùng... memo.
 
## global state
la 1 state dc su dung o nhieu component khac nhau 

## local state: 
la state dc su dung cho 1 component khai bao state do ma thoi 

## Su dung componentWillUnmount nhu the nao trong react hook
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

##  React hoạt động như thế nào?
- React tạo ra một DOM ảo.
- Khi trạng thái thay đổi trong một component, trước tiên nó chạy một thuật toán "khác biệt (diffing)", xác định những gì đã thay đổi trong DOM ảo.
- Bước thứ hai là điều chỉnh (reconciliation), nơi nó cập nhật DOM với kết quả của khác biệt.

## Higher-Order component (HOC)
- là một hàm nhận một component và trả về một component mới

## Refs la gì 
- Refs thường được dùng để trả về một tham chiếu tới 1 phần tử. Refs cho phép bạn truy cập trực tiếp vào phần tử DOM hoặc một phiên bản của thành phần.


## Redux-Thunk 
- là một middleware phổ biến nhất được dùng để xử lý các action bất đồng bộ trong Redux

## Stateless component 
- là component không phụ thuộc vào life circle


## Statefull component 
- Nếu hành vi của một component phụ thuộc vào state của component thì nó có thể được gọi là Stateful component.


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

## Các position
- static: Đưa phần tử về hiển thị theo kiểu mặc định.
- fixed: Hiển thị luôn đi theo trình duyệt khi cuộn trang.
- top:  Căn vị trí hiển thị của phần tử theo hướng từ trên xuống dưới. Giá trị càng cao thì phần tử càng thụt xuống dưới.
- bottom:  Căn vị trí hiển thị của phần tử theo hướng từ dưới lên trên. Giá trị càng cao thì phần tử càng hiển thị lên cao.
- left: Căn vị trí hiển thị từ trái sang phải. Giá trị càng cao thì phần tử sẽ càng thụt về bên phải.
- right: Căn vị trí hiển thị từ phải sang trái. Giá trị càng cao thì phần tử sẽ càng thụ về bên trái.
- relative: Dùng để thiết lập một phần tử sử dụng các thuộc tính position mà không làm ảnh hưởng đến việc hiển thị ban đầu.
- absolute: Dùng để thiết lập vị trí của một phần tử nhưng nó sẽ luôn nằm trong một phần tử mẹ đang là relative.

## Flexbox
Flexbox Layout là một kiểu bố cục trang có khả năng tự cân đối kích thước, chiều rộng/chiều cao và thứ tự phần tử bên trong để phù hợp với tất cả các loại thiết bị màn hình.
thành phần gồm
- Container: là thành phần lớn bao quanh các phần tử bên trong, các item bên trong sẽ hiển thị dựa trên thiết lập của container này.
- item: là phần tử con của container, bạn có thể thiết lập nó sẽ sử dụng bao nhiêu cột trong một container, hoặc thiết lập thứ tự hiển thị của nó.


## Câu hỏi ngoài lề
## Khi lap trinh can quan tam dieu gi:
- Xac dinh tinh nang cua feature do la gi ? 
- Xac dinh cac step de code feature do: - luot so qa, nhung function nao se duoc su dung lai, function nao chua co thi viet ra cai moi.   
- Neu Feature business do phuc tap thi viet lai document
- Code: => test => clean lai code dư thì bỏ, xem lại tên biến , function có hợp lý chưa


## Solid principle: 
- single responsiple principle: moi 1 calss chi dam nhiem 1 chuc nang duy nhat
- open close: khi co 1 chuc nang moi thi nen mo rorng class, hoa viet 1 class moi ke thua class do khong nen ssua lai class cu 
- linkos principle: Cac interface class con co the thay class cha ma kohng gay ra loi 
- interface segregration: 1 tinterface lon  nen chia ra nhieu interface nho 
- depenci inversion: cac thanh phan trong module phu thuoc vao class abtract khong nen phu thuoc vao ca


## Design parten
Nói một cách đơn giản, design pattern là các mẫu thiết kế có sẵn, dung để giải quyết một vấn đề, Áp dụng mẫu thiết kế này sẽ làm code dễ bảo trì, mở rộng hơn, 3 loại chính
- Creational Pattern tập hợp các giải pháp liên quan đến khởi tạo đối tượng.
Nhóm này gồm 5 mẫu thông dụng: 
Factory Method, Abstract Factory, Builder, Prototype, Singleton
- Structural Pattern tập hợp các giải pháp liên quan đến thiết lập kết cấu, liên hệ giữa các đối tượng.
Nhóm này gồm 7 mẫu thông dụng: Adapter, Bridge, Composite, Decorator, Facade
- Behavioral Pattern: tập hợp các giải pháp liên quan đến các hành vi của đối tượng và giao tiếp giữa các đối tượng khác nhau.
Nhóm này gồm 11 mẫu thông dụng: Strategy, State, Observer


## Cau hoi cho cong ty
Quy trinh lam viec
- Sprint keo dai bao lau 
- 1 Sprint co bao nhieu ticket cho moi nguoi 
- 1 Co tong ket srpint hay khong 
- Co stand up meeting hay khong 
- Khi co 1 van de ve teachnical chua co huong giai queyt thi ben anh xu ly nhu the nao? 
- Ben anh co meeting technical moi tuan ko 
- Benh anh co code review hay khong
- Ben anh Devops hay khong
- Ben xu dung autoload deploy hay khong
- Co OT hay khong va OT nhieu hay it
- ben a code co theo cau truc nao hk
- Ben a co app dung TDD cho project khong. 



