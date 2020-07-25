# TypeScript

## Strong Type

強型別語言對於變數的定義檢查比較嚴謹，未依照指定型別傳入參數，在編譯時期就會拋出 Exception。

![img](../captures/anjee_typescript_001.png)

JavaScript 是偏向弱型別的語言，它也擁有基本型別，但並未禁止不同型別的語法，而是自己判斷目前應該執行的型別進行自動轉換，但也很有可能引發一些預期之外的錯誤。

![img](../captures/anjee_typescript_002.png)

TypeScript 基於 JavaScript 之語言特性前提供了強型別語法的特性，在編譯時期就可以提醒我們使用了不對的型別，將原本的 JavaScript 改寫也不太費功，只需要替原本的 JavaScript 程式碼補上型別即可。

![img](../captures/anjee_typescript_003.png)

相較於之前的程式碼，只有額外指定參數的型別，但在執行之前，編輯器就提示可能有錯誤，即可以提前發現問題。

## Primitive Type

TypeScript 預設支援所有 JavaScript 的型別（例如 Boolean、Number、String、Array等等），並額外增加的 Enum 列舉類型。除此之外，所有變數宣告都必須明確指定變數的型別！

![img](../captures/anjee_typescript_004.png)

### Boolean Type

布林類型 (Boolean) 表示值為 ture/ false ，TypeScript 中使用 Boolean 的方法與 JavaScript 無異，可透過以下方式明確指定變數的類型為 Boolean

```typescript
var isReady: boolean = true;
```

宣告變數之後，使用變數如以下範例：

```typescript
if(isReady){
    //// 程式碼放這裡
}

if(isReady === true) {
    //// 程式碼放這裡
}
```

### Number Type

在 TypeScript 中所有的數值都是 浮點數 (float) ，在 TypeScript 進行數值運算時，要特別小心小數點的數值運算，用 number 指定 TypeScript 的變數為數值類型。

```typescript
var total: number = 0;
```

在 TypeScript 之中，數值類型的使用方法與 JavaScript 沒有太大的差別，但型別檢查，可以省去很多傳入不正確資料產生的錯誤。

```typescript
//// 宣告變數
var a: number = 1;
var b: number = 2;
var c: string = 'Hello';

// 新增一個限定只能傳入 number 的 function
function Add(a: number, b: number) {
    return a + b;
}
    
Add(a, b);    // 3
Add(a, c);    // 錯誤提示，若在 JavaScript 會直接回傳 '1Hello'
```

### String

字串類型用來儲存文字資料，例：動態顯示的文章標題，或是要推出的折扣條件等等，在 TypeScript 中同樣使用 string 代表字串類型，指定的時候可以使用 單引號 (') 或 雙引號 (") 標示文字。

```typescript
var title = 'CNN新聞';
var content = "新聞內容如下，da la de la la";
```


在 TypeScript 1.4 的版本之後，為了增加組合字串的便利性，增加了 Template Literals 功能，使用 ` - 重音符號 包圍文字，表示這串文字為 Template String，而在 Template 中可以隨意的使用 ${variable} 的方式放置變數，大大增加動態組合字串的可讀性，請參考下面的使用範例。

```typescript
var name = 'John';                 // 宣告要組合使用的字串

console.log(`Hello, ${name}!`);    // TypeScript 發現這是 Template，會自動把 name代入
                                   // 結果為 Hello, John!
```


因為 TypeScript 把字串組裝的事情透過編譯處理，實際編譯 JavaScript成果如下：

```typescript
// 編譯後的 JavaScript ，其實就是使用字串相加的方式
// 但並非必要
var name = 'John'; 
console.log("Hello, " + name + "!");
```

Enum

列舉類型 (Enum) 是 TypeScript 獨有而 JavaScript 沒有的型別，需要宣告固定種類的變數時相當好用，例如衣服的尺寸可能有大、中、小三種，就可以使用 Enum 來定義

```typescript
enum Size {
    Large = 0,
    Medium = 1,
    Small = 2    
}
```


Enum某程度上可以讓 TypeScript 可以引用其自定義的關鍵字便於判別

```typescript
// 用 Enum 判別
if(size === Size.Large){
    // 程式碼放這裡
}
```

