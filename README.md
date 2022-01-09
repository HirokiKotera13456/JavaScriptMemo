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
 
 # React復習
 
 # inputタグをuseStateを用いて状態管理する方法
 
 input1タグには valueをつけることに注意 また、状態を変更する際にはonChange関数を用いる。onChangeがないとinput欄に何も打ち込めない。
 ```
   const onChangeTodoText = (e) => setTodoText(e.target.value) 
   return(
    <input  value={todoText} onChange = {onChangeTodoText} />
   )
 ```
 
 # inputタグに入力したものをTODOリストに追加する方法
 まず、buttonタグにonClick関数（クリックで何か起こす関数）を追加
 ```
  <button　onClick={onClickAdd}>追加</button>
 ```
 また、空文字はリストに登録されないように以下の設定をする。
 ```
 if (todoText === "") return;
 ```
 あとは、スプレッド構文を用いてtodoを追加し、set関数で値を更新する
 ```
  const onClickAdd = () => {
    if (todoText === "") return;
    const newTodos = [...incompleteTodos,todoText];
    setIncompleteTodos(newTodos);
    setTodoText("");
  }
 ```
 
  
 
