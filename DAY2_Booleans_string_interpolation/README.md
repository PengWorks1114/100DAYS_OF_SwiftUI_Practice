
# Swift 基礎語法筆記

本專案整理了 Swift 的基礎資料型別與操作方式，內容分為三個章節，分別介紹 **布林值 (Booleans)**、**字串拼接 (Strings Joining)** 與 **簡單資料總結 (Summary of Simple Data)**，並搭配範例程式碼說明。

---

## 📂 檔案結構

```

├── 01.How\_to\_store\_truth\_with\_Booleans.md
├── 02.How\_to\_join\_strings\_together.md
└── 03.Summary\_Simple\_data.md

````

---

## 📄 章節內容

### 1️⃣ How to store truth with Booleans

布林值 (Boolean, 簡寫為 `Bool`) 主要用來表示「真」或「假」的狀態。  
常見用法如下：

```swift
let filename = "paris.jpg"
print(filename.hasSuffix("jpg")) // true

let number = 120
print(number.isMultiple(of: 3)) // true
````

宣告與操作布林值：

```swift
let goodDogs = true
var gameOver = false // 初始為 false
gameOver.toggle()    // 轉換為 true

let isMultiple = 120.isMultiple(of: 3)
```

布林值也能透過「反轉運算子」來切換狀態：

```swift
var isAuthenticated = false // false
isAuthenticated = !isAuthenticated // true
```

🔑 **布林值的實用功能**：

1. `!` 反轉布林值
2. `.toggle()` 直接切換 `true` / `false`

---

### 2️⃣ How to join strings together

Swift 提供兩種方式來組合字串：

1. **使用加號 (+)**

   ```swift
   let firstPart = "Hello "
   let secondPart = "world"
   let greeting = firstPart + secondPart
   let greeting2 = firstPart + secondPart + ", this is Swift"
   ```

2. **使用字串插值 (String Interpolation)**
   可在字串中直接嵌入變數或運算式：

   ```swift
   let name = "Andy"
   let age = 26
   let message = "Hello, my name is \(name) and I'm \(age) years old."
   print(message)
   ```

   ⚠️ 注意：數字不可直接與字串用 `+` 連接，需使用插值方式：

   ```swift
   let number = 11
   // ❌ 錯誤
   // let missionMessage = "apollo" + number + "landed on the moon."

   // ✅ 正確
   let missionMessage = "apollo \(number) landed on the moon."
   ```

---

### 3️⃣ Summary of Simple Data

Swift 的基本資料型別整理如下：

* 使用 `let` 宣告常數，`var` 宣告變數。
* **字串 (String)**：存放文字，範圍可從簡短字串到整本小說。使用 `""` 包裹。
* **整數 (Int)**：存放整數值。
* **浮點數 (Double)**：存放小數值。
* **布林值 (Bool)**：存放 `true` 或 `false`。
* **字串插值 (String Interpolation)**：讓我們能將資料嵌入字串中。

範例：

```swift
let title = "Swift"
let year = 2025
let isReleased = true
let description = "The language \(title) was released before \(year). Released: \(isReleased)"
```

---

## 🚀 學習重點

1. **Booleans**

   * 使用 `true` / `false` 表示狀態
   * 支援 `!` 與 `.toggle()` 操作

2. **Strings**

   * 透過 `+` 或字串插值 `\( )` 進行組合
   * 插值能避免型別錯誤並提供更高可讀性

3. **Simple Data**

   * `let` 與 `var` 的區別
   * 主要資料型別：`String`, `Int`, `Double`, `Bool`
   * 字串插值是高效整合資料的方式

---

## 🛠️ 執行方式

在 Swift Playground 或 Xcode 專案中，建立 `.swift` 檔並貼上範例程式碼即可測試。

---

## 📚 延伸閱讀

* [Apple Developer - Swift Language Guide](https://docs.swift.org/swift-book/)
* [Swift.org Documentation](https://swift.org)

```
