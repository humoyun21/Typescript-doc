TypeScriptda ma'lumot turlari (data types) quyidagi usullarda foydalaniladi:

Primitive Types (Oddiy turlar)
number : Sonlar (int, float)
string : Matnlar
boolean : Mantiqiy qiymatlar (true yoki false )
null : Bo'shlik
undefined : Aniqlik mahsuloti
symbol : Unikal (unique ) qiymatlar
Compound Types (Jamiy turlar)
Array : Massivlar
Tuple : Ixtiyoriy ma'lumotlarni o'z ichiga olgan to'plamlar
Object : Ob'ektlar
Function : Funksiyalarni aytuvchi tur
Additional Types (Qo'shimcha turlar)
any : Har qanday tur
void : Bo'sh funksiya qaytish qiymati
never : Nikohsiz faqat xato xodisada qaytamaydigan funksiya qaytish qiymati
Misolin $```typescript // Misol let count: number = 5; let message: string = "Hello, TypeScript";

// Massiv turidagi ma'lumotlar let numbers: number[] = [1, 2, 3, 4, 5];

// Tuple let person: [string, number] = ['John', 30];

// Ob'ekt let user: {name: string, age: number} = {name: 'Alice', age: 25};

// Funksiya function add(x: number, y: number): number { return x + y; }

// Har qanday tur let dynamicData: any = 5; dynamicData = "Hello";

// Bo'sh qaytish qiymati function doSomething(): void { console.log("Do something"); }

1. **Boolean:** _Boshqa tillardagi booleantip, true yoki false qiymatlarini qabul qiladi._

```
let isDone: boolean = false;
console.log(isDone); // false
```

2.  **Number:** _Butun va o'nlik sonlarni ifodalaydi. Masalan, 5, 10.5, -3.14 kabi._

```
let decimal: number = 6;
let hex: number = 0xf00d;
let binary: number = 0b1010;
let octal: number = 0o744;
console.log(decimal, hex, binary, octal); // 6 61453 10 484
```

3. **String:** _Matnlar, qo'shimcha belgilar yoki satrlar. Misol uchun: "Salom", "TypScript", "123"._

```
let color: string = "blue";
color = 'red'; // Double quotes va single quotes ishlatish mumkin
console.log(color); // red
```

4. **Array:** _Massivlar, biror turdagi elementlarni o'z ichiga oladi. [1, 2, 3] yoki ['salom', 'dunyo'] kabi._

```
let list: number[] = [1, 2, 3];
console.log(list); // [1, 2, 3]

let names: Array<string> = ['John', 'Doe'];
console.log(names); // ['John', 'Doe']
```

5. **Tuple:** _Tartiblangan elementlarga ega massivlar. Misol uchun, [string, number] turidagi tartiblangan massivda birinchi element matn va ikkinchi element son bo'ladi._

```
let x: [string, number];
x = ['hello', 10]; // To'g'ri
x = [10, 'hello']; // Xato
console.log(x[0].substring(1)); // ello
```

6. **Enum:** _O'zgaruvchilarni belgilash uchun ishlatiladi. Masalan, enum Color {Red, Green, Blue}. Bu, Color.Red, Color.Green, Color.Blue qiymatlariga ega bo'ladi._

```
enum Color {Red, Green, Blue}
let c: Color = Color.Green;
console.log(c); // 1
```

7. **Any:** _Har qanday turdagi qiymatni qabul qiladi. Ammo, bu turdan foydalanish tilning dinamik xususiyatlariga qo'shimcha yuklanishga olib kelishi mumkin._

```
let notSure: any = 4;
notSure = "maybe a string instead";
notSure = false; // Hech qanday tur qiymat qabul qiladi
console.log(notSure); // false
```

8. **Void:** _Agar funksiya hech qanday qiymat qaytarmasa, unda void turi ishlatiladi._

```
function warnUser(): void {
    console.log("This is a warning message");
}
warnUser();
```

9. **Null va Undefined:** _Misol uchun, biror o'zgaruvchiga bosh qiymat berish uchun ishlatiladi._

```
let u: undefined = undefined;
let n: null = null;
console.log(u, n); // undefined null
```

10. **Never:** _Ushbu turi asosan funksiyalarda ishlatiladi va u faqatgi funksiya yoki xatolikni aniqlash uchun ishlatiladi._

```
function error(message: string): never {
    throw new Error(message);
}
error("Something went wrong");
```

11. **Object:** _JS obyektlari uchun umumiy turi._

```
let obj: object = {};
console.log(obj); // {}
```

12. **Symbol:** _Unikal belgilar yaratish uchun ishlatiladi._

```
let sym1 = Symbol();
let sym2 = Symbol("key");
console.log(sym1, sym2); // Symbol() Symbol(key)
```

13. **BigInt:** _Katta butun sonlarni ifodalaydi._

```
const bigNumber: bigint = BigInt(Number.MAX_SAFE_INTEGER) + BigInt(1);
console.log(bigNumber); // 9007199254740992n
```
