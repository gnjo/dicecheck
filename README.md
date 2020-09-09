# dicecheck
diceCheck   3d5t7c10

```
//usage

let a=diceCheck("3d5t1c10") //0 or 1
console.log(a)
let a2=diceCheck("3d5t1")//3-15 
console.log(a2)
;
function diceCheck(v){
 //
 function fr(a,b){return Math.floor(Math.random()*(b-a)+a)}
 function fn(a){return a-0}
 ;
 v=v+''
 let wk,n,d,t,c,ans
 ;
 wk=v.split('d')
 n=fn(wk[0]),wk=wk.pop().split('t')
 d=fn(wk[0]),wk=wk.pop().split('c')
 t=fn(wk[0]),wk=wk.pop()
 c=fn(wk)
 //console.log('the c',c,wk)
 ;
 ans=Array.from({length:t}).map(dd=>fr(n,n*d+1)).reduce((a,b)=>Math.max(a,b))
 //console.log('the ans',ans)
 ;
 return (/c/.test(v))?fn(ans>=c):ans
}
```
