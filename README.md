## javascript復習

# map関数

name は何の変数でも大丈夫
``` 
const nameArray = ["山田" ,"田中" , "木村"]

const nameArray = nameArray.map((name) => { 
  return name;
  })
  
  console.log(nameArray)
  /// 山田、田中、木村　
  ```
  また、map関数の第二引数にはindexを渡すことが出来る。
  ```
  const name = ["山田","田中","吉田"];
const nameArr = name.map((name,index)=> {
 
  console.log(`${index}番目は${name}です`);
} )

///0番目は山田です 
///1番目は田中です 
///2番目は吉田です 
  ```
  
  # filter関数
  numは何の変数でも大丈夫
 
 ```

const numArr = [1,2,3,4,5];
const newNumArr = numArr.filter((num) => {
  return num % 2 === 0;
});
console.log(newNumArr)
/// 2,4
 ```
