# Rust Tutorial Project — Principles of Programming Languages

> **สำหรับนักศึกษา:** ใช้ไฟล์นี้เป็น Template สำหรับจัดทำบทเรียน Rust ของกลุ่ม  
> **Topic No.:** `XX`  
> **Topic Name:** `[ชื่อหัวข้อ]`  
> **Group No.:** `XX`

---

## 1. Members

| # | Name | Student ID | GitHub Username | Main Responsibility |
|---|---|---|---|---|
| 1 | `[ชื่อ-นามสกุล]` | `[รหัส]` | `@[username]` | Concept + Code |
| 2 | `นายธีทัต สุจริตพาณิช` | `670710130` | `@670710130` | Code + Demo |
| 3 | `[ชื่อ-นามสกุล]` | `[รหัส]` | `@[username]` | Rust vs Other Language + PPL |
| 4 | `[ชื่อ-นามสกุล]` | `[รหัส]` | `@[username]` | Exercises + Common Mistakes |

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
| `if condition {statement}` | `ทำคำสั่งใน statement ในวงเล็บปีกกา {...} ถ้าเงื่อนไข (condition) เป็นจริง` | `if x > 0 {println("Positive");}` |
| `if condition1 {statement1}      else if condition2{statement2}  else {statement3}` | `ถ้า condition1 เป็นจริง ทำ statement1 , ถ้า condition1 เป็นเท็จ และ condition2 เป็นจริง ทำ statement2 , ถ้าทั้งสองเงื่อนไขเป็นเท็จ ทำ statement3 ในส่วน else` | `if x > 0 {println!("Positive");}         else if x < 0 {println!("Negative");}      else {println!("Zero");}                                                            ` |
| `if condition1 {if condition2 {statement}}` | `หาก condition1 ของ if ด้านนอกเป็นจริง จะทำ condition2 ของ if ด้านใน และหาก condition2 เป็นจริงโปรแกรมจะทำงานในส่วนของ statement` | `if x != 0 {if x > 0 {println!("Positive");}}่` |

### Important Rules

1. `เงื่อนไข(condition)ของ if ต้องเป็น Boolean เท่านั้น เพราะ Rust จะไม่แปลงค่าให้อัตโนมัติเหมือนบางภาษา`
2. `ต้องมีเครื่องหมายปีกกา '{...}' ครอบการทำงานของ statement เสมอ`
3. `ไม่จำเป็นต้องใส่เครื่องหมายวงเล็บ '(...)' ครอบส่วนของเงื่อนไข(condition) (complier จะเตือน unnecessary parentheses)`

---

## 6. Runnable Code Examples

> **ข้อกำหนด:** Code ทุกตัวต้อง Compile และ Run ได้จริงก่อนนำมาใส่ในเอกสาร

### Example 1 — `[SimpleGrade]`

**Purpose:** `[แสดงการใช้เงื่อนไข if, else if, else อย่างง่ายที่รวมเข้าด้วยกันเป็น code เดียว]`

```rust
fn main() {
    let score:i32 = 90;
    
    if score >= 80{
        println!("Grade A");
    }
    else if score >= 60{
        println!("Grade B");
    }
    else if score >= 40{
        println!("Grade C");
    }
    else{
        println!("Grade F");
    }
}
```

**Expected Output**

```text
[Grade A]
```

**Explanation**

`- กำหนดคะแนนที่ใช้ในการตรวจเงื่อนไขให้มีค่า 90`

`- เมื่อเข้าเงื่อนไข if score >= 80 หากคะแนน มากกว่าหรือเท่ากับ 80 จะพิมพ์ "Grade A" ออกมา `

`- หากเงื่อนไขแรกเป็นเท็จ จะตรวจเงื่อนไขที่สอง  else if score >= 60 หากคะแนนมีค่า มากกว่าหรือเท่ากับ 60 จะพิมพ์ "Grade B" ออกมา `

`- หากเงื่อนไขที่สองยังคงเป็นเท็จ จะตรวจเงื่อนไขที่สาม  else if score >= 40 หากคะแนนมีค่า มากกว่าหรือเท่ากับ 40 จะพิมพ์ "Grade C" ออกมา`

`- สุดท้ายหากไม่เข้าเงื่อนไขก่อนหน้าอันใดเลย จะทำสิ่งที่อยู่ใน else เป็นการพิมพ์ "Grade F" ออกมา`

`- ในตัวอย่างนี้ score = 90 ซึ่งจะทำเงื่อนไข if เป็นจริง และพิมพ์ "Grade A" ออกมา`




# Example 2 — `[NestedGrade]`

**Purpose:** `[แสดงการใช้ Nested-if ที่เป็นการใช้ if ซ้อนใน if อีกชั้นหนึ่ง ซึ่งเป็นวิธีการทำเงื่อนไขซ้อนเงื่อนไข]`

```rust
fn main() {
    let score:i32 = 39;

    if score >= 60 {
        if score >= 80 {
            println!("Grade A");
        } 
        else {
            println!("Grade B");
        }
    } 
    else {
        if score >= 40 {
            println!("Grade C");
        } 
        else {
            println!("Grade F");
        }
    }
}
```

**Expected Output**

```text
[Grade F]
```

**Explanation**

`- กำหนดคะแนนที่ใช้ในการตรวจให้มีค่า 39`

`- เมื่อเข้าเงื่อนไข if score >= 60 หากคะแนน มากกว่าหรือเท่ากับ 60 จะตรวจสอบ  if score >= 80 เป็นตัวถัดไป หากคะแนน มากกว่าหรือเท่ากับ 80 เป็นจริงจะพิมพ์ "Grade A" ออกมา แต่หากเป็นเท็จจะเข้าไปทำในส่วนของ else คือ พิมพ์ "Grade B" ออกมา
`

`- ในส่วนของ else ด้านนอกจะทำงานเมื่อคะแนนน้อยกว่า 60 (ไม่เข้าเงื่อนไข if) โดยด้านในจะตรวจสอบ if score >= 40 หากคะแนน มากกว่าหรือเท่ากับ 40 เป็นจริงจะพิมพ์ "Grade C" ออกมา แต่หากเป็นเท็จจะเข้าไปทำในส่วนของ else คือ พิมพ์ "Grade F" ออกมา
`

`- ในตัวอย่างนี้ score = 39 ซึ่งจะทำงานจาก else ด้านนอกสุด และตรวจสอบด้านในเริ่มจาก if score >= 40 เป็นเท็จ ทำให้ขั้นตอนสุดท้ายต้องทำงานในส่วนของ else ด้านใน ซึ่งผลลัพธ์ที่ได้ คือการพิมพ์ "Grade F" อกกมา 
`


## 7. Common Mistakes

### Mistake 1 — `[ชื่อข้อผิดพลาด]`

**Problem**

`[อธิบายปัญหา]`

**Incorrect Code**

```rust
// Incorrect example
```

**Correct Code**

```rust
// Correct example
```

**Why?**

`[อธิบายสาเหตุ]`

---

### Mistake 2 — `[ชื่อข้อผิดพลาด]`

**Problem**

`[อธิบายปัญหา]`

**Incorrect Code**

```rust
// Incorrect example
```

**Correct Code**

```rust
// Correct example
```

**Why?**

`[อธิบายสาเหตุ]`

---

## 8. Exercises

> จัดทำแบบฝึกหัด **2 ข้อ** ที่สอดคล้องกับ Topic และมีระดับความยากเหมาะสม

### Exercise 1 — `[ชื่อโจทย์]`

**Problem**

`[เขียนโจทย์]`

**Hint**

`[คำใบ้]`

**Solution**

```rust
// Solution code
```

**Explanation**

`[อธิบายแนวทางแก้]`

---

### Exercise 2 — `[ชื่อโจทย์]`

**Problem**

`[เขียนโจทย์]`

**Hint**

`[คำใบ้]`

**Solution**

```rust
// Solution code
```

**Explanation**

`[อธิบายแนวทางแก้]`

---

## 9. PPL Perspective

> **ส่วนนี้เป็นหัวใจของรายวิชา Principles of Programming Languages**

วิเคราะห์ Topic นี้ในมุมมองของ Programming Languages

### 9.1 Syntax

`[Topic นี้เกี่ยวข้องกับ syntax อย่างไร]`

### 9.2 Semantics

`[คำสั่ง/construct เหล่านี้มีความหมายหรือพฤติกรรมอย่างไร]`

### 9.3 Type System

`[เกี่ยวข้องกับ type system อย่างไร ถ้ามี]`

### 9.4 Memory / Resource Management

`[เกี่ยวข้องกับ memory หรือ resource management อย่างไร ถ้ามี]`

### 9.5 Abstraction / Other PPL Concepts

`[อธิบาย abstraction, scope, binding, paradigm หรือแนวคิด PPL อื่นที่เกี่ยวข้อง]`

### 9.6 Why Rust?

`[Rust ใช้แนวคิดนี้เพื่อเพิ่ม safety, reliability หรือ performance อย่างไร]`

---

## 10. Rust vs. Other Language

**Comparison Language:** `[Python / C / C++ / Java / Kotlin / ...]`

| Aspect | Rust | Other Language |
|---|---|---|
| Syntax | `[อธิบาย]` | `[อธิบาย]` |
| Semantics / Behavior | `[อธิบาย]` | `[อธิบาย]` |
| Type System | `[อธิบาย]` | `[อธิบาย]` |
| Memory Management | `[อธิบาย]` | `[อธิบาย]` |
| Safety | `[อธิบาย]` | `[อธิบาย]` |

### Rust Example

```rust
// Rust code
```

### `[Other Language]` Example

```python
# Other language code
```

### Analysis

`[อธิบายความแตกต่างที่สำคัญ และเหตุผลด้านการออกแบบภาษา]`

---

## 11. Teach Your Topic

การนำเสนอมีสมาชิก **4 คน คนละประมาณ 5 นาที**

| Member | Responsibility | Time |
|---|---|---:|
| Member 1 | Concept + Short Code Illustration | 5 min |
| Member 2 | Detailed Code + Live Demo | 5 min |
| Member 3 | Rust vs Other Language + PPL Analysis | 5 min |
| Member 4 | Exercises + Common Mistakes + Challenge | 5 min |

### Individual Contribution

**Member 1**

`[สิ่งที่รับผิดชอบ]`

**Member 2**

`[สิ่งที่รับผิดชอบ]`

**Member 3**

`[สิ่งที่รับผิดชอบ]`

**Member 4**

`[สิ่งที่รับผิดชอบ]`

> สมาชิกทุกคนต้องสามารถอธิบาย Code ของกลุ่มได้ ไม่ใช่เฉพาะส่วนที่ตนเองเขียน

---

## 12. References

> แนะนำให้มีอย่างน้อย **4 แหล่งอ้างอิง** และควรใช้เอกสารทางการเป็นหลัก

1. `[The Rust Programming Language — Rust Book]`
2. `[Rust by Example / Rust Reference]`
3. `[Official documentation ที่เกี่ยวข้องกับ Topic]`
4. `[แหล่งอ้างอิงเพิ่มเติม]`

---

## 13. AI Usage Declaration

สามารถใช้ AI เป็นเครื่องมือช่วยเรียนรู้และพัฒนาได้ แต่สมาชิกทุกคนต้องเข้าใจและสามารถอธิบายผลงานของกลุ่มได้

| AI Tool | Purpose | How the Result Was Verified |
|---|---|---|
| `[เช่น ChatGPT]` | `[ใช้เพื่ออะไร]` | `[ตรวจสอบอย่างไร]` |
| `[AI tool]` | `[ใช้เพื่ออะไร]` | `[ตรวจสอบอย่างไร]` |

### Declaration

- [ ] Code ทุกส่วนที่นำเสนอได้รับการ Compile และทดสอบแล้ว
- [ ] สมาชิกทุกคนสามารถอธิบาย Code ที่นำเสนอได้
- [ ] ตรวจสอบข้อมูลจากแหล่งอ้างอิงที่น่าเชื่อถือแล้ว
- [ ] ระบุการใช้ AI อย่างโปร่งใส

**รายละเอียดการใช้ AI**

`[อธิบายว่าใช้ AI ในขั้นตอนใด และสมาชิกตรวจสอบผลลัพธ์อย่างไร]`

---

## 14. GitHub Contribution

| Member | Issues | Commits | Pull Requests | Code Reviews | Contribution |
|---|---:|---:|---:|---:|---|
| Member 1 | `[จำนวน]` | `[จำนวน]` | `[จำนวน]` | `[จำนวน]` | `[รายละเอียด]` |
| Member 2 | `[จำนวน]` | `[จำนวน]` | `[จำนวน]` | `[จำนวน]` | `[รายละเอียด]` |
| Member 3 | `[จำนวน]` | `[จำนวน]` | `[จำนวน]` | `[จำนวน]` | `[รายละเอียด]` |
| Member 4 | `[จำนวน]` | `[จำนวน]` | `[จำนวน]` | `[จำนวน]` | `[รายละเอียด]` |

### Teamwork Reflection

**How did your team collaborate?**

`[อธิบายกระบวนการทำงานร่วมกัน]`

**Problems encountered**

`[ปัญหาที่พบ]`

**How did you solve them?**

`[วิธีแก้ปัญหา]`

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
