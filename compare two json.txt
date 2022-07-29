//How to compare two JSON have the same properties without order?

let obj1 = { name: "Person 1", age:5 };
let obj2 = { age:5, name: "Person 1" };

_.isEqual(obj1, obj2)  

//OUTPUT: True

let obj3 = { name: "Person 1", age: 25, };
let obj4 = { age:5, name: "Person 1" };

_.isEqual(obj3, obj4) 

//OUTPUT: False