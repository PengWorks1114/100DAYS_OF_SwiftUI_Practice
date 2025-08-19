# Swift 基礎語法教學筆記

---

## 01. 為什麼選擇 Swift

* Swift 語言自 2014 年推出，相對年輕。
* 設計目標：

  * 降低撰寫不安全程式碼的可能性。
  * 讓程式碼更清晰易讀。
  * 原生支援全球多種語言。

---

## 02. 建立變數與常數

Swift 提供兩種方式儲存資料，依是否需要改變決定：

* **`var`** → 變數，可變動。

```swift
import Cocoa
var greeting = "Hello, playground"

var name = "Ted"
name = "Rebecca"
name = "Keeley"  // 可重複賦值
```

* **`let`** → 常數，不可變動。

```swift
let character = "Daphne"
character = "Rebecca" // error
```

---

## 03. 建立字串

* **跳脫字元**

```swift
let quote = "Then he tapped a sign saying \"Believe\" and walked away,"
```

* **多行字串**

```swift
let movie = """
A day in
the life of an
Apple engineer
"""
```

* **實用方法**

```swift
let actor = "Denzal Washington"
let result = "you win"

// count
print(actor.count)        // 17
// uppercased
print(result.uppercased()) // "YOU WIN"
// hasPrefix
print(movie.hasPrefix("A day")) // true (大小寫敏感)
```

---

## 04. 儲存整數

```swift
import Cocoa
let score = 10
let reallyBig = 100_100_100 // Swift 允許底線分隔數字

let lowerScore = score - 2
let higherScore = score + 10
let doubledScore = score * 2
let squaredScore = score * score
let halvedScore = score / 2

var counter = 10
counter += 5
print(counter) // 15
```

---

## 05. 儲存小數（浮點數）

* **浮點數運算**

```swift
let number = 0.1 + 0.2
print(number) // 0.300000000000004 (浮點數精度問題)
```

* Swift 預設將浮點數視為 **Double**。

* **型別錯誤範例**

```swift
let a = 1     // Int
let b = 2.0   // Double
let c = a + b // error: Int 與 Double 無法直接相加
```

* **正確作法：型別轉換**

```swift
let c = a + Int(b)
let d = Double(a) + b
```
