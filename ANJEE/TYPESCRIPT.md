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