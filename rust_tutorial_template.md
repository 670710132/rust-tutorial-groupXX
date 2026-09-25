# Rust Tutorial Project — Principles of Programming Languages

> **Topic No.:** 06  
> **Topic Name:** Conditional Structures  
> **Group No.:** 06

---

## 1. Members

| # | Name | Student ID | GitHub Username | Main Responsibility |
|---|---|---|---|---|
| 1 | `[นางสาวธนัญญา พรมภักดี]` | `[670710128]` | `@[username]` | Concept + Code |
| 2 | `[นายธีทัต สุจริตพาณิช]` | `[670710130]` | `@[username]` | Code + Demo |
| 3 | `[นายนทิบดี ช้างทอง]` | `[670710131]` | `@670710131` | Rust vs Other Language + PPL |
| 4 | `[นายนนธวัช งามบุญศิริสิงห์]` | `[670710132]` | `@670710132` | Exercises + Common Mistakes |

---

## 2. Learning Objectives

หลังจากศึกษา Topic นี้แล้ว ผู้เรียนสามารถ:

1. `[อธิบายแนวคิดสำคัญได้]`
2. `[เขียนโปรแกรม Rust ที่เกี่ยวข้องได้]`
3. `[วิเคราะห์พฤติกรรม/กฎของภาษาได้]`
4. `[เปรียบเทียบ Rust กับภาษาอื่นได้]`

---

## 3. Introduction

อธิบายว่า Topic นี้คืออะไร มีความสำคัญอย่างไร และใช้แก้ปัญหาอะไรในการเขียนโปรแกรม

`[เขียนเนื้อหาที่นี่]`

---

## 4. Key Concepts

### 4.1 `[Concept 1]`

**คำอธิบาย**

`[อธิบายแนวคิด]`

**ตัวอย่าง**

```rust
fn main() {
    println!("Hello, Rust!");
}
```

**Explanation**

`[อธิบายว่า code ทำงานอย่างไร]`

---

### 4.2 `[Concept 2]`

`[อธิบายแนวคิด]`

```rust
// Rust code
```

---

### 4.3 `[Concept 3]`

`[อธิบายแนวคิด]`

```rust
// Rust code
```

---

### 4.4 `[Concept 4 — ถ้ามี]`

`[อธิบายแนวคิด]`

```rust
// Rust code
```

---

### 4.5 `[Concept 5 — ถ้ามี]`

`[อธิบายแนวคิด]`

```rust
// Rust code
```

---

## 5. Important Syntax / Rules

| Syntax / Rule | Meaning | Example |
|---|---|---|
| `[syntax/rule]` | `[ความหมาย]` | `[ตัวอย่าง]` |
| `[syntax/rule]` | `[ความหมาย]` | `[ตัวอย่าง]` |
| `[syntax/rule]` | `[ความหมาย]` | `[ตัวอย่าง]` |

### Important Rules

1. `[กฎสำคัญข้อที่ 1]`
2. `[กฎสำคัญข้อที่ 2]`
3. `[กฎสำคัญข้อที่ 3]`

---

## 6. Runnable Code Examples

> **ข้อกำหนด:** Code ทุกตัวต้อง Compile และ Run ได้จริงก่อนนำมาใส่ในเอกสาร

### Example 1 — `[ชื่อ Example]`

**Purpose:** `[ต้องการสาธิตอะไร]`

```rust
fn main() {
    // Write your runnable Rust code here
}
```

**Expected Output**

```text
[expected output]
```

**Explanation**

`[อธิบาย code ทีละส่วนที่สำคัญ]`

---

### Example 2 — `[ชื่อ Example]`

**Purpose:** `[ต้องการสาธิตอะไร]`

```rust
fn main() {
    // Write your runnable Rust code here
}
```

**Expected Output**

```text
[expected output]
```

**Explanation**

`[อธิบาย code]`

---

## 7. Common Mistakes

### Mistake 1 — การใช้ตัวเลขหรือ Type อื่นที่ไม่ใช่ Boolean ในเงื่อนไข if

**Problem**
คนที่มาจากภาษา C, C++ หรือ Python จะชินกับการใช้ตัวเลข (เช่น `0` หรือ `1`) หรือ Pointer มาเป็นเงื่อนไขหลัง `if` โดยตรง

**Incorrect Code**
```rust
fn main() {
    let number = 1;
    // Compile Error! เพราะ number เป็นประเภท i32 ไม่ใช่ bool
    if number {
        println!("Number is not zero");
    }
}
```
**Correct Code**
```rust
fn main() {
    let number = 1;
    if number != 0 { // ต้องเช็คให้ได้ค่า bool (true/false) ชัดเจน
        println!("Number is not zero");
    }
}
```
**Why?**

Rust เข้มเรื่อง Type มาก เงื่อนไขหลัง if ต้องได้ค่าออกมาเป็น bool (true หรือ false) เท่านั้น มันจะไม่แปลงตัวเลขเป็น Boolean ให้อัตโนมัติเหมือนภาษา C เพื่อป้องกันบั๊กที่เราอาจจะเผลอเขียนผิด

---

### Mistake 2 — การคืนค่าคนละ Type ออกมาจาก if Expression

**Problem**

`ใน Rust เอา if ไปกำหนดค่าให้ตัวแปรได้ แต่ดันคืนค่าปนกันคนละประเภทในแต่ละปีกกา`

**Incorrect Code**

```rust
fn main() {
    let condition = true;
    let result = if condition {
        5       // เป็นตัวเลข
    } else {
        "five"  // Compile Error เป็นข้อความ
    };
}
```

**Correct Code**

```rust
fn main() {
    let condition = true;
    let result = if condition {
        5 // เป็นตัวเลขทั้งคู่
    } else {
        6
    };
}
```

**Why?**

`Rust ต้องรู้ Data Type ของตัวแปรตั้งแต่งานยังไม่รันโปรแกรม ไม่ว่าจะเข้าเงื่อนไข if หรือ else ค่าที่ส่งออกมาต้องเป็น Type เดียวกันเสมอ`

---
### Mistake 3 — การลืมใส่ else เวลาเอา if ไปกำหนดค่าตัวแปร

**Problem**

`ใช้ if กำหนดค่าให้ตัวแปร แต่ดันเขียนแค่ if ไม่มี else`

**Incorrect Code**

```rust
fn main() {
    let is_active = true;
    // Compile Error ขาดบล็อก else
    let status_code = if is_active { 200 };
}
```

**Correct Code**

```rust
fn main() {
    let is_active = true;
    let status_code = if is_active { 200 } else { 400 };
}
```

**Why?**

`Rust มีกฎเหล็กว่าตัวแปรห้ามว่างเปล่า (Uninitialized) ถ้าไม่มี else แล้วเงื่อนไขเป็น false ตัวแปรจะไม่มีค่าใส่ ซึ่ง Rust ไม่ยินยอม`

---

## 8. Exercises

### Exercise 1 — ระบบคำนวณส่วนลดตามระดับสมาชิกและยอดซื้อ

**Problem**
จงเขียนโปรแกรมคำนวณราคาสุทธิหลังหักส่วนลดร้านค้า โดยรับค่าตัวแปร 2 ตัวคือ `is_vip: bool` และ `total_amount: f64` โดยมีเงื่อนไขการให้ส่วนลดดังนี้:
- ถ้าเป็นสมาชิก VIP (`is_vip = true`):
  - ยอดซื้อตั้งแต่ 1,000 บาทขึ้นไป ได้ส่วนลด 20%
  - ยอดซื้อน้อยกว่า 1,000 บาท ได้ส่วนลด 10%
- ถ้าไม่ได้เป็นสมาชิก VIP (`is_vip = false`):
  - ยอดซื้อตั้งแต่ 1,000 บาทขึ้นไป ได้ส่วนลด 5%
  - ยอดซื้อน้อยกว่า 1,000 บาท ไม่ได้ส่วนลด (0%)

ให้ใช้ `if - else` ในการคำนวณหาเปอร์เซ็นต์ส่วนลด นำไปหักออกจากยอดซื้อ แล้วพิมพ์ราคาสุทธิออกมาทางหน้าจอ

**Hint**
- ใช้ `if` ซ้อนภายใน `if` (Nested Condition) หรือใช้ Logical Operator `&&` ร่วมด้วย
- คำนวณส่วนลดโดย `total_amount * (1.0 - discount_rate)`

**Solution**
```rust
fn main() {
    let is_vip: bool = true;
    let total_amount: f64 = 1250.0;

    let discount_rate = if is_vip {
        if total_amount >= 1000.0 {
            0.20 // VIP ยอด 1000+ ลด 20%
        } else {
            0.10 // VIP ยอดไม่ถึง 1000 ลด 10%
        }
    } else {
        if total_amount >= 1000.0 {
            0.05 // ไม่ใช่ VIP ยอด 1000+ ลด 5%
        } else {
            0.00 // ไม่ใช่ VIP ไม่ได้ส่วนลด
        }
    };

    let final_price = total_amount * (1.0 - discount_rate);
    println!("Total Amount: {:.2} THB", total_amount);
    println!("Discount Rate: {}%", discount_rate * 100.0);
    println!("Final Price: {:.2} THB", final_price);
}
```
**Explanation**

`ใช้ if เป็น Expression หาค่าอัตราส่วนลดก่อน เริ่มตรวจเช็คจาก is_vip เมื่อเป็น true จะเข้ามาเช็คเงื่อนไขซ้อนด้านในต่อว่า total_amount >= 1000.0 หรือไม่ ซึ่ง 1250.0 >= 1000.0 เป็นจริง บล็อก if ด้านในจึงคืนค่า 0.20 ออกมาเก็บไว้ในตัวแปร discount_rate แล้วนำไปคำนวณราคาสุทธิออกมาได้ 1000.00 THB`

---

### Exercise 2 — การแกะค่า Option ด้วย if let 

**Problem**

ในภาษา Rust เมื่อทำงานกับข้อมูลที่มีโอกาสเป็นค่าว่างได้ จะใช้ Enum ประเภท `Option<T>` (ซึ่งมีค่าเป็น `Some(T)` หรือ `None`)
จงเขียนโปรแกรมรับค่าคะแนนสอบ `score: Option<i32>` แล้วใช้โครงสร้างเงื่อนไข `if let` ในการตรวจสอบว่า:
1. ถ้ามีค่าคะแนนอยู่จริง (`Some(s)`) ให้ตรวจเช็คต่อว่าคะแนน `s >= 50` หรือไม่ ถ้าถึงให้พิมพ์ `"Passed with score: X"` แต่ถ้าไม่ถึงให้พิมพ์ `"Failed with score: X"`
2. ถ้าไม่มีค่าคะแนน `(None)` ให้พิมพ์ `"No score provided"`

**Hint**

- โครงสร้าง `if let Some(s) = score { ... } else { ... }` เป็นการเช็คเงื่อนไขพร้อมแกะค่า (Pattern Matching) ในคำสั่งเดียว

**Solution**

```rust
fn main() {
    let score: Option<i32> = Some(68); 

    if let Some(s) = score {
        if s >= 50 {
            println!("Passed with score: {}", s);
        } else {
            println!("Failed with score: {}", s);
        }
    } else {
        println!("No score provided");
    }
}
```

**Explanation**

`คำสั่ง if let Some(s) = score จะทำการตรวจสอบว่าตัวแปร score มีข้อมูลประเภท Some หรือไม่ ถ้ามี มันจะแกะค่าตัวเลขข้างในออกมาใส่ไว้ในตัวแปร local ชื่อ s ทันที และทำบล็อกเงื่อนไขภายใน (พิมพ์ "Passed with score: 68") แต่ถ้า score เป็น None มันจะข้ามไปทำบล็อก else ด้านนอกสุดแทน `

---

## 9. PPL Perspective

> **ส่วนนี้เป็นหัวใจของรายวิชา Principles of Programming Languages**

วิเคราะห์ Topic นี้ในมุมมองของ Programming Languages

### 9.1 Syntax

`[Rust นั้นเป็นภาษาที่ Conditional structures มี syntax ที่ไม่เหมือนภาษาอื่นตรงที่ condition ของข้อนั้นๆ จะไม่มีการใส่วงเล็บแต่ก็ยังคงต้องใส่ {} เพื่อเป็นการทำ block ทุก statment และยังสามรถนำ if ไปใช้เป็น expression ได้โดยตรงและคืนค่าออกมาได้เลย เหมือนเป็นตัวแปรตัวหนึ่งทำให้เราเอาไป assign ใส่ตัวแปรได้เลย]`

### 9.2 Semantics

`[เพราะ if else ทำหน้าที่เป็นตัวตรวจเช็คเงื่อนไข(condition) เพื่อทำการเลือกทิศทางว่าจะทำใน if หรือ else และถ้าใช้ if เป็น expression ต้องมี else เสมอ]`

### 9.3 Type System

`[เพราะ Conditon ใน if ต้องเป็น boolean เท่านั้น และเมื่อถูกใช้เป็น expression return type ต้องเป็นชนิดเดียวกันเสมอเพราะตัวแปรใน Rust ทุกตัวต้องมี type ที่เป็น static type]`

### 9.4 Memory / Resource Management

`[เพราะเนื่องจากตัวแปรที่ประกาศภายใน {} ของแต่ละ if นั้นจะถูกจำกัดแค่ใน block นั้น และจะถูก deallocate จาก memory หลังออกจาก if ทันทีทำให้ไม่ต้องพึ่ง garbage collector ทำให้ไม่มี overhead จาก runtime memory management]`

### 9.5 Abstraction / Other PPL Concepts

`[เพราะ if ของ Rust สามารถเป็น expression สะท้อนแนวคิดจากภาษาสาย functional ที่ทุกโครงสร้างคุม flow คืนค่าได้ ต่างจาก imperative ดั้งเดิมเช่น C/Java 
 ตัวแปรที่ประกาศใน if/else block จึงมี scope จำกัดแค่ใน block
 Rust ผสม imperative paradigm เข้ากับ functional paradigm หรือเรียกว่าภาษาแบบ multi-paradigm]`

### 9.6 Why Rust?

`[เพราะ condition structure ใน Rust ทำให้เกิด Type safety เพราะทุก if ที่เป็น expression นั้นต้องมี return type เหมือนกันเสมอทำให้ compiler จับ type error ได้ตั้งแต่ compile time 
การทำ condition เป็น boolean ก็ทำให้การ check condition เช่น การเผลอ assign แทน compare (if (x = 5)) ทำให้ condition ที่ต้องเป็น boolean นั้นตรวจจับได้และทำให้เกิด Reliability
การตรวจสอบทั้งหมดเกิดขึ้น ที่ compile time เท่านั้น ไม่มีการเช็คเพิ่มตอน runtime และยังไม่ต้องมี garbage collector คอยตรวจสอบหรือ clean up memory ระหว่างรันโปรแกรม เพราะตัวแปรใน branch ต่างๆ ถูก drop ตาม scope โดยอัตโนมัติ]`

---

## 10. Rust vs. Other Language

**Comparison Language:** `[Python / C / C++ / Java / Kotlin / ...]`

| Aspect | Rust | Other Language |
|---|---|---|
| Syntax | `[ไม่ต้องใส่วงเล็บครอบเงื่อนไข แต่บังคับใส่ {} เสมอเพื่อทำ block]` | `[ไม่ต้องใส่วงเล็บและไม่มี {} เลย ใช้ indentation การเว้นวรรค หรืิ tab แทนการกำหนด block พร้อมโคลอน :]]` |
| Semantics / Behavior | `[Condition ต้องเป็น bool เท่านั้น]` | `[Condition รับได้แทบทุก type]` |
| Type System | `[Static strong typing, ตรวจตอน compile time ถ้าใช้ if เป็น expression ทุก branch บังคับ return type เดียวกัน]` | `[[Dynamic typing ตรวจตอน runtime ตัวแปรเปลี่ยน type ได้ตลอด และ conditional expression ไม่บังคับให้สอง branch คืน type เดียวกันเลย]` |
| Memory Management | `[ตัวแปรใน block ถูก drop อัตโนมัติทันทีที่ออกจาก scope ไม่มี garbage collector]` | `[ใช้ garbage collector คอยเก็บ memory ที่ไม่ใช้แล้วให้อัตโนมัติ]` |
| Safety | `[Compiler เช็ค type และ bool ตั้งแต่ compile time ป้องกัน bug ก่อนรันจริง]` | `[ไม่มีการเช็ค type ตอน compile เพราะไม่มีขั้นตอน compile แบบ static ทำให้เกิด bug บาง class จะไปโผล่ตอน runtime แทน]` |

### Rust Example

```rust
fn main() {
    let number = 3;
    if number % 2 == 0 {
        println!("{} is Even", number);
    } else {
        println!("{} is Odd", number);
    }
}
```

### `[Other Language]` Example

```python
number = 3
    if number % 2 == 0:
        print(f"{number} is Even")
    else:
        print(f"{number} is Odd")
```

### Analysis

`[อธิบายความแตกต่างที่สำคัญ และเหตุผลด้านการออกแบบภาษา]`

---

## 11. Teach Your Topic

การนำเสนอมีสมาชิก 4 คน คนละประมาณ 5 นาที

| Member | Responsibility | Time |
|---|---|---|
| Member 1 | Concept + Short Code Illustration | 5 min |
| Member 2 | Detailed Code + Live Demo | 5 min |
| Member 3 | Rust vs Other Language + PPL Analysis | 5 min |
| Member 4 | Exercises + Common Mistakes + Challenge | 5 min |

### Individual Contribution

**Member 1:** นางสาวธนัญญา พรมภักดี (670710128)
* **รับผิดชอบ:** Concept + Short Code Illustration
* **รายละเอียด:** อธิบายทฤษฎีพื้นฐาน Conditional Structures ใน Rust พร้อมยกตัวอย่างโค้ดประกอบ
>
> ---
>
**Member 2:** นายธีทัต สุจริตพาณิช (670710130)
* **รับผิดชอบ:** Detailed Code + Live Demo
* **รายละเอียด:** ลงลึกรายละเอียดโค้ดตัวอย่าง และทำ Live Demo รันโปรแกรมระหว่างนำเสนอ
>
> ---
>
**Member 3:** นายทิบดี ช้างทอง (670710131)
* **รับผิดชอบ:** Rust vs Other Language + PPL Analysis
* **รายละเอียด:** เปรียบเทียบ Rust กับภาษาอื่นตามหลัก PPL
>
> ---
>
**Member 4:** นายนนธวัช งามบุญศิริสิงห์ (670710132)
* **รับผิดชอบ:** Exercises + Common Mistakes + Challenge
* **รายละเอียด:** ออกแบบแบบฝึกหัด รวบรวมข้อผิดพลาดที่พบบ่อย และโจทย์ท้าทาย
> **Note:** สมาชิกทุกคนเข้าใจโครงสร้างและสามารถอธิบาย Code ทั้งหมดของกลุ่มได้เป็นอย่างดี
---

## 12. References

1. Klabnik, S., & Nichols, C. (2023). *Control Flow - The Rust Programming Language*. Rust Documentation. https://doc.rust-lang.org/book/ch03-05-control-flow.html
2. Rust Community. (n.d.). *If/else - Rust by Example*. Rust Documentation. https://doc.rust-lang.org/rust-by-example/flow_control/if_else.html
3. Rust Reference Team. (n.d.). *If expressions - The Rust Reference*. Rust Documentation. https://doc.rust-lang.org/reference/expressions/if-expr.html
4. Rust Community. (n.d.). *if let - Rust by Example*. Rust Documentation. https://doc.rust-lang.org/rust-by-example/flow_control/if_let.html

---

## 13. AI Usage Declaration

สามารถใช้ AI เป็นเครื่องมือช่วยเรียนรู้และพัฒนาได้ แต่สมาชิกทุกคนต้องเข้าใจและสามารถอธิบายผลงานของกลุ่มได้

| AI Tool | Purpose | How the Result Was Verified |
| :--- | :--- | :--- |
| **ChatGPT** | • ใช้ช่วยเรียบเรียงภาษาและตรวจทานคำผิดในเอกสาร <br> • ใช้ช่วยค้นหาไอเดียโจทย์แบบฝึกหัดเบื้องต้น | • สมาชิกในกลุ่มอ่านเรียบเรียงเนื้อหาใหม่ด้วยตนเอง <br> • นำโจทย์มาปรับแก้และทดสอบสั่งรันโค้ดจริงด้วย `cargo run` |
| **Gemini** | • ใช้ตรวจสอบโครงสร้างของโปรแกรม <br> | • อ่านทบทวนเนื้อหาภาษาไทยให้ถูกต้องตามคำศัพท์ทางคอมพิวเตอร์ |

### Declaration

- [x] Code ทุกส่วนที่นำเสนอได้รับการ Compile และทดสอบแล้ว
- [x] สมาชิกทุกคนสามารถอธิบาย Code ที่นำเสนอได้
- [x] ตรวจสอบข้อมูลจากแหล่งอ้างอิงที่น่าเชื่อถือแล้ว
- [x] ระบุการใช้ AI อย่างโปร่งใส

### รายละเอียดการใช้ AI

ใช้ AI เป็นเพียง **"เครื่องมือช่วยค้นหาข้อมูลและตรวจทานเอกสาร"** เพื่อความรวดเร็วในการสืบค้นวิธีแก้ปัญหาการตั้งค่าสภาพแวดล้อมการทำงาน และช่วยเกลาภาษาในเอกสารเท่านั้น 
การวิเคราะห์เนื้อหา การเขียนโค้ดตัวอย่าง การออกแบบแบบฝึกหัด ตลอดจนการทดสอบรันโปรแกรมทั้งหมด สมาชิกทุกคนในกลุ่มเป็นผู้ลงมือทำ เขียนโค้ด และตรวจสอบความถูกต้องกับเอกสารอ้างอิงทางการของ Rust (`doc.rust-lang.org`) ด้วยตนเอง

---

## 14. GitHub Contribution

| Member | Issues | Commits | Pull Requests | Code Reviews | Contribution |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **Member 1** <br> (นางสาวธนัญญา พรมภักดี) | 1 | 4 | 1 | 2 | สรุปและเขียนเนื้อหาบทเรียนส่วน Concept + Short Code บน Markdown |
| **Member 2** <br> (นายธีทัต สุจริตพาณิช) | 1 | 5 | 1 | 2 | เรียบเรียงเนื้อหา Detailed Code และอัปโหลดไฟล์โค้ดสำหรับ Live Demo |
| **Member 3** <br> (นายทิบดี ช้างทอง) | 1 | 3 | 1 | 2 | สรุปส่วน Rust vs Other Languages และเขียนวิเคราะห์เชิง PPL |
| **Member 4** <br> (นายนนธวัช งามบุญศิริสิงห์) | 1 | 6 | 1 | 2 | จัดทำโครงสร้าง Repository, เขียนแบบฝึกหัด (Exercises) และทดสอบโค้ด |

---

### Teamwork Reflection

#### How did your team collaborate?
ใช้วิธีแบ่งหัวข้อการทำงานอย่างชัดเจนโดยใช้ GitHub Repository ในการรวบรวมไฟล์เอกสารและไฟล์โค้ด สมาชิกทุกคนมีการอัปเดตไฟล์เนื้อหาผ่านการ Commit มีการพูดคุยสื่อสารช่องทางออนไลน์เพื่อตรวจสอบความถูกต้องของเนื้อหาให้สอดคล้องกันก่อนบันทึกงาน

#### Problems encountered
1. **การจัดโครงสร้างไฟล์บน GitHub:** สมาชิกในกลุ่มช่วงแรกยังไม่ชินกับการสร้างโฟลเดอร์สำหรับเก็บไฟล์โค้ด `.rs` และโครงสร้างโปรเจกต์
2. **การตั้งค่าสภาพแวดล้อมการทำงาน:** พบปัญหาการตั้งค่าและลง Extension ของเครื่องมือพัฒนาโปรแกรมก่อนการสั่งรันโค้ดจริง

#### How did you solve them?
1. ร่วมกันออกแบบโครงสร้างโฟลเดอร์กลาง `code_examples/` ให้ชัดเจน และแนะนำขั้นตอนการกดสร้างไฟล์พร้อมโฟลเดอร์ผ่านหน้าเว็บ GitHub ให้สมาชิกในกลุ่มทำตามได้ง่ายขึ้น
2. ช่วยกันสืบค้นวิธีแก้ไขข้อผิดพลาดใน Terminal จนสามารถสั่งรันและ Compile โค้ดผ่านคำสั่ง `cargo run` ได้อย่างถูกต้องครบถ้วนก่อนส่งงานครับ
---

## 15. Final Checklist

- [ ] Learning Objectives ครบ 3–4 ข้อ
- [ ] Key Concepts ครบถ้วน
- [ ] Syntax / Rules
- [ ] Runnable Code Examples
- [ ] Code Compile และ Run ได้จริง
- [ ] Common Mistakes
- [ ] Exercises 2 ข้อ พร้อม Solutions
- [ ] PPL Perspective
- [ ] Rust vs Other Language
- [ ] References อย่างน้อย 4 แหล่ง
- [ ] AI Usage Declaration
- [ ] GitHub Contribution
- [ ] สมาชิกทั้ง 4 คนมีส่วนร่วม
- [ ] สมาชิกทั้ง 4 คนพร้อมนำเสนอคนละ 5 นาที
- [ ] สมาชิกทุกคนสามารถอธิบาย Code ของกลุ่มได้

---

## Submission Information

**Repository:** `[GitHub repository URL]`

**Chapter Path:** `[เช่น chapters/01-introduction/]`

**Final PR:** `#[PR number]`

**Submitted by:** `[Group XX]`

**Date:** `[YYYY-MM-DD]`
