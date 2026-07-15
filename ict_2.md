# කොටස A - ව්‍යූහගත රචනා (Structured Essay)

## ප්‍රශ්නය 1

### (a) පහත HTML කේත ඛණ්ඩය වෙබ් බ්‍රවුසරයක් මඟින් නිරූපණය වන විට අපේක්ෂිත ප්‍රතිදානය ඇඳ දක්වන්න:

```html
<u>Available Courses</u>
<ol>
  <li>Information Technology</li>
  <li>Engineering</li>
  <li>Business Management
    <ul>
      <li>Accounting</li>
      <li>Marketing</li>
    </ul>
  </li>
  <li>Law</li>
</ol>

```

**පිළිතුර:**

**Available Courses**

1. Information Technology
2. Engineering
3. Business Management
* Accounting
* Marketing


4. Law

---

### (b) ඉහත HTML ලැයිස්තුවට පහත හැඩ ගැන්වීම් යෙදීමට නිවැරදි බාහිර CSS කේතය ලියන්න:

* **(i) සියලුම ලැයිස්තු අයිතම Times New Roman අකුරු ක්‍රමයෙන් දර්ශනය කිරීම:**
```css
li {
    font-family: "Times New Roman";
}

```


* **(ii) අංක සහිත ලැයිස්තුවේ ලැයිස්තු අයිතමවල පැහැය තද කොළ පාටට වෙනස් කිරීම:**
```css
ol > li {
    color: darkgreen;
}

```


* **(iii) අංක රහිත උප-ලැයිස්තු අයිතම italic ආකාරයට වෙනස් කිරීම:**
```css
ul li {
    font-style: italic;
}

```


* **(iv) සම්පූර්ණ ලැයිස්තු කොටස වටා 1-pixel ඝනකමකින් යුතු කළු පැහැති බෝඩරයක් එකතු කරන්න:**
```css
ol {
    border: 1px solid black;
}

```


* **(v) පිටුවේ පසුබිම් වර්ණය ලා අළු පාටට වෙනස් කිරීම:**
```css
body {
    background-color: lightgray;
}

```



---

### (c) වෙබ් බ්‍රවුසරයක් මඟින් නිරූපණය කරන ලද Library Membership Form එක සඳහා වන HTML කේතයේ හිස්තැන් පුරවන්න:

**පිළිතුර:**

```html
<html>
<head>
<title>Library Membership Form</title>
</head>
<body>
<h3>Library Membership Form</h3>
<form action="register.php" method="post">
<div>Member Name: <input type="text" name="mname"></div>
<p><div>Enter Membership Type: <input type="text" name="memtype" size="10">
<ol><li>Student</li><li>Teacher</li></ol>
</div>
<hr>
<div>
Preferred Notification Method:
<input type="radio" name="notify" value="Email">Email
<input type="radio" name="notify" value="SMS">SMS
</div>
<br><div>
Select Library Branch:
<select name="branch">
<option value="Colombo">Colombo</option>
<option value="Kalutara">Kalutara</option>
<option value="Gampaha">Gampaha</option>
</select></div><br>
<input type="submit" value="Register">
</form>
</body>
</html>

```

---

### (d) ඉදිරිපත් කරන ලද ෆෝරම් දත්ත සාමාජික වගුවට ඇතුළත් කිරීමට පහත PHP කේතයේ හිස්තැන් පුරවන්න:

**පිළිතුර:**

```php
<?php
$connection = new mysqli("localhost", "root", "", "libraryDB");
if ($connection->connect_errno) {
    echo "Failed to connect to MySQL: ", $connection->connect_error;
    exit();
}

$mname = $_POST['mname'];
$memtype = $_POST['memtype'];
$notify = $_POST['notify'];
$branch = $_POST['branch'];

$sql = "INSERT INTO member (memberName, membershipType, notificationMethod, branch)
        VALUES ('$mname', '$memtype', '$notify', '$branch')";

if ($connection->query($sql) === TRUE) {
    echo "New record created successfully";
} else {
    echo "Error: " . $sql . "<br>" . $connection->error;
}
$connection->close();
?>

```

---

---

## ප්‍රශ්නය 2

### (a) වාහන කුලියට දීමේ සේවාවක් සඳහා වන ER රූප සටහන ඇසුරෙන් පහත ප්‍රශ්නවලට පිළිතුරු සපයන්න:

* **(i) Driver සහ Vehicle යන ස්ථූලතා අතර සන්නිවේදකතාව (cardinality) දක්වන්න:**
* **1:1 (One-to-One)**
*(පැහැදිලි කිරීම: එක් රියදුරෙකුට පැදවිය හැක්කේ එක් වාහනයක් පමණි, එමෙන්ම වාහනයක් පැදවිය හැක්කේ එක් රියදුරෙකුට පමණි.)*


* **(ii) රියදුරෙකු විසින් වාහනයක් ධාවනය කර ඇති වර්ෂ ගණන සටහන් කිරීමට 'NoOfYears' යන උපලක්ෂණය (attribute) ER සටහනට ඇතුළත් කළ යුතු ආකාරය:**
* `NoOfYears` යනු සම්බන්ධතා උපලක්ෂණයක් (Relationship Attribute) වේ. එබැවින් එය **`drives` සම්බන්ධතාවයට (diamond හැඩයට) සම්බන්ධ වන පරිදි ඉලිප්සයකින් (oval)** ඇඳිය යුතුය.


* **(iii) රියදුරන්ට හිමිවන රක්ෂණ ඔප්පුව (InsurancePolicy) දුර්වල ස්ථූලතාවයක් (Weak Entity) ලෙස ER සටහනට ඇතුළත් කරන ආකාරය:**
* `InsurancePolicy` යන්න **ද්විත්ව සෘජුකෝණාස්‍රයකින් (Double Rectangle)** ඇඳිය යුතුය.
* `Driver` සහ `InsurancePolicy` අතර සම්බන්ධතාවය **ද්විත්ව දියමන්ති හැඩයකින් (Double Diamond - Identifying Relationship)** සම්බන්ධ කළ යුතුය.
* එහි උපලක්ෂණ වන `TimePeriod` සහ `Benefits` සාමාන්‍ය ඉලිප්ස වලින්ද, අර්ධ යතුර (Partial Key) වන `InsName` **තිත් ඉරක් සහිත ඉලිප්සයකින් (Dashed Underlined Oval)** ද ඇඳිය යුතුය.



---

### (b) පාසල් පුස්තකාල දත්ත ගබඩාවේ වගු ඇසුරෙන් පහත ප්‍රශ්නවලට පිළිතුරු සපයන්න:

* **(i) Book වගුව සෑදීම සඳහා වන SQL විමසුම ලියන්න:**
```sql
CREATE TABLE Book (
    BookId VARCHAR(10) NOT NULL,
    BookName VARCHAR(100) NOT NULL,
    NoOfCopies INT NOT NULL,
    PRIMARY KEY (BookId)
);

```


* **(ii) "Gamperaliya" පොතේ පිටපත් ගණන 3 කින් වැඩි කිරීමට අදාළ SQL විමසුම:**
```sql
UPDATE Book
SET NoOfCopies = NoOfCopies + 3
WHERE BookName = 'Gamperaliya';

```


* **(iii) දී ඇති SQL විමසුමේ ප්‍රතිදානය (Output) ලියන්න:**
```sql
SELECT StuName, Class
FROM Student, BorrowBook
WHERE BorrowDate = '2025-05-21' AND Student.StuId = BorrowBook.StuId;

```


**ප්‍රතිදානය:**
| StuName | Class |
| --- | --- |
| Sanduni | 11B |
| Nalian | 11B |



---

### (c) බිටු අනුක්‍රමය `0110111001` සඳහා NRZ-I (Non-Return to Zero Inverted) සංඥා තරංගය ඇඳ දක්වන්න:

**NRZ-I රීතිය:** '1' බිටුවක් හමුවන සෑම අවස්ථාවකදීම සංඥාවේ මට්ටම (High සිට Low හෝ Low සිට High) ප්‍රතිලෝම (invert) වන අතර, '0' බිටුවකදී සංඥා මට්ටම එලෙසම පවතී.

* **බිටු 1 (0):** High මට්ටමේ පවතී (දී ඇති පරිදි).
* **බිටු 2 (1):** High සිට Low දක්වා වෙනස් වේ.
* **බිටු 3 (1):** Low සිට High දක්වා වෙනස් වේ.
* **බිටු 4 (0):** High මට්ටමේම පවතී (වෙනස් නොවේ).
* **බිටu 5 (1):** High සිට Low දක්වා වෙනස් වේ.
* **බිටු 6 (1):** Low සිට High දක්වා වෙනස් වේ.
* **බිටු 7 (1):** High සිට Low දක්වා වෙනස් වේ.
* **බිටු 8 (0):** Low මට්ටමේම පවතී (වෙනස් නොවේ).
* **බිටු 9 (0):** Low මට්ටමේම පවතී (වෙනස් නොවේ).
* **බිටු 10 (1):** Low සිට High දක්වා වෙනස් වේ.

---

### (d) PSTN එකක් හරහා පරිගණක දෙකක් අතර සම්බන්ධතාවය පෙන්වීමට ක්‍රියාකාරී සටහනක් ඇඳ දක්වන්න:

```
[පරිගණකය A] <---> [මොඩමයක් (Modem) A] <---> [PSTN ජාලය] <---> [මොඩමයක් (Modem) B] <---> [පරිගණකය B]

```

---

---

## ප්‍රශ්නය 3

### (a) වාහන නැවැත්වීමේ පද්ධතියේ ගැලීම් සටහන සඳහා වන ලේබල (A සිට H දක්වා) ලියා දක්වන්න:

* **A:** `Input Hours, VehicleType` (පැය ගණන සහ වාහන වර්ගය ආදානය කිරීම)
* **B:** `Print "Invalid parking duration"` ("Invalid parking duration" යන්න මුද්‍රණය කිරීම)
* **C:** `Hours <= 2` (පැය ගණන 2 ට වඩා අඩු හෝ සමාන ද?)
* **D:** `Fee = Hours * 100` (ගාස්තුව = පැය ගණන × 100)
* **E:** `Fee = 200 + (Hours - 2) * 150` (ගාස්තුව = 200 + (පැය ගණන - 2) × 150)
* **F:** `Fee = Fee + 500` (ගාස්තුව = ගාස්තුව + 500)
* **G:** `Fee = Fee * 0.95` (හෝ `Fee = Fee - (Fee * 0.05)`)
* **H:** `Fee > 5000` (ගාස්තුව 5000 ට වඩා වැඩි ද?)

---

### (b) හිස්තැන් පුරවා පයිතන් ක්‍රමලේඛය සම්පූර්ණ කරන්න:

**පිළිතුර:**

```python
while True:
    fnum = int(input("Enter the first number: "))
    snum = int(input("Enter the second number: "))
    if fnum < snum:
        break
    else:
        print("Invalid Input. Please re-enter the numbers.")

total = 0
current = fnum
while current <= snum:
    total += current
    current += 1

print("The sum is:", total)

```

---

### (c) ලැයිස්තු දෙකක ඇති දත්ත 'students.txt' ගොනුවට ලිවීමේ පයිතන් කේතයේ හිස්තැන් පුරවන්න:

* **A:** `"w"` (හෝ `'w'`)
* **B:** `len`
* **C:** `str`
* **D:** `close()`

---

---

## ප්‍රශ්නය 4

### (a) (i) P1 සහ P2 ක්‍රියාවලිවල (Process States) තත්ත්වය ලියන්න:

* **P1:** **Ready State (සූදානම් තත්ත්වය)** *(පැහැදිලි කිරීම: ඉහළ ප්‍රමුඛතා P3 පැමිණි නිසා P1 තාවකාලිකව නවතා සූදානම් තත්ත්වයට පත් කරයි.)*
* **P2:** **Blocked Suspended State (අත්හිටුවන ලද අවහිර තත්ත්වය)** *(පැහැදිලි කිරීම: මතකයෙන් පිටත් කර ද්විතීයික ගබඩාවට ගෙන ගිය නිසා.)*

### (ii) තත්ත්ව පරිවර්තනයේදී OS මඟින් සිදුකරන ලද කාර්යයන් දෙකක්:

1. **ප්‍රකරණ මාරුව (Context Switching):** P1 හි වත්මන් තත්ත්වය (Registers, PC අගයන්) එහි PCB එකෙහි සුරැකීම සහ P3 හි සුරැකි තත්ත්වයන් CPU එක වෙත ප්‍රතිපූරණය කිරීම.
2. **ක්‍රියාවලි පාලන කොටස් (PCB) යාවත්කාලීන කිරීම:** P1 හි තත්ත්වය 'Running' සිට 'Ready' ලෙසද, P3 හි තත්ත්වය 'Ready' සිට 'Running' ලෙසද වෙනස් කිරීම.

---

### (b) ගොනුව සොයා ගැනීම සඳහා OS එක මඟින් ගොනු නාමාවලියෙහි (Directory) තබා ගන්නා දත්ත:

* **(i) යාබද විභේදනය (Contiguous Allocation):** ආරම්භක කොටස (Starting block address) සහ දිග/ප්‍රමාණය (Length/Size)
* **(ii) සබැඳි විභේදනය (Linked Allocation):** ආරම්භක කොටස (Starting block address) සහ අවසාන කොටස (Ending block address)
* **(iii) පටුන්ගත විභේදනය (Indexed Allocation):** දර්ශක කොටසේ ලිපිනය (Index block address)

---

### (c) අභ්‍යන්තර ඛණ්ඩනය වීමේ (Internal Fragmentation) ප්‍රමාණය ගණනය කරන්න:

* පොකුරක ප්‍රමාණය (Cluster size) = $4\text{ KB}$
* ගොනුවේ ප්‍රමාණය (File size) = $125\text{ KB}$
* අවශ්‍ය වන පොකුරු ගණන = $\lceil \frac{125}{4} \rceil = \lceil 31.25 \rceil = 32\text{ Clusters}$
* වෙන් කරන ලද මුළු ඉඩ ප්‍රමාණය = $32 \times 4\text{ KB} = 128\text{ KB}$
* **අභ්‍යන්තර ඛණ්ඩනය (Internal Fragmentation) = $128\text{ KB} - 125\text{ KB} = 3\text{ KB}$**

---

### (d) (i) පද්ධතියේ මුළු පිටු ගණන (Number of Pages) ගණනය කරන්න:

* අතථ්‍ය මතකයේ ප්‍රමාණය (Virtual Memory size) = $4\text{ GB} = 4 \times 1024 \times 1024\text{ KB} = 2^{22}\text{ KB}$
* පිටුවක ප්‍රමාණය (Page size) = $4\text{ KB}$
* **පිටු ගණන = $\frac{4\text{ GB}}{4\text{ KB}} = \frac{2^{22}\text{ KB}}{2^2\text{ KB}} = 2^{20} = 1,048,576\text{ Pages}$**

### (ii) පිටු වගුවේ උපරිම ප්‍රමාණය $m \times 2^n$ bits වේ. $m$ සහ $n$ හි අගයන්:

* පිටු වගුවේ ඇති මුළු පේළි ගණන (Entries) = $2^{20}$
* එක් පේළියක ප්‍රමාණය (Entry size) = $18\text{ bits}$
* මුළු ප්‍රමාණය = $18 \times 2^{20}\text{ bits}$
* **$m = 18$, $n = 20$**

### (iii) පිටු වගුව තුළ ඇති වෙනස් කරන ලද (modified/dirty) බිටුවෙහි කාර්යය:

* ප්‍රධාන මතකයේ (RAM) ඇති පිටුවක අඩංගු දත්ත වෙනස් කර ඇත්දැයි හඳුනා ගැනීමට මෙය භාවිතා කරයි. පිටුව ඉවත් කිරීමේදී මෙම බිටුව '1' (Dirty) නම්, එම වෙනස්කම් ද්විතීයික මතකයේ නැවත ලිවිය (write-back) යුතුය. '0' නම් කෙලින්ම ඉවත් කළ හැක.

### (iv) පිටු අංක 2 ඉල්ලා සිටින විට OS එක මඟින් සිදු කරන කාර්යයන්:

1. පිටු වගුවේ (Page table) පිටු අංක 2 හි Present/Absent bit එක '0' බැවින් **පිටු දෝෂයක් (Page Fault)** ඇතිවේ.
2. OS එක මඟින් ද්විතීයික මතකයේ පිටුව පවතින ස්ථානය සොයා ගනී.
3. ප්‍රධාන මතකයේ (RAM) හිස් රාමුවක් (Free Frame) සොයා ගනී. (හිස් රාමු නැත්නම් Page Replacement ක්‍රමවේදයකින් රාමුවක් නිදහස් කරයි).
4. අවශ්‍ය පිටුව ද්විතීයික මතකයෙන් RAM එකේ අදාළ රාමුවට පටවනු ලබයි.
5. පිටු වගුව යාවත්කාලීන කර (Present/Absent bit එක '1' කර, අදාළ Frame අංකය ඇතුළත් කරයි) නැවත ක්‍රියාවලිය ක්‍රියාත්මක කරයි.

---

---

# කොටස B - රචනා (Essay)

## ප්‍රශ්නය 5

### (a) බූලියන් වීජගණිතය ඇසුරෙන් සරල කිරීම:

$$\bar{A}\bar{B} \cdot \overline{(\bar{B} \oplus C)} + \overline{(\bar{B} + C)} \cdot \bar{A}\bar{B} = \bar{A}\bar{B}C\text{ බව පෙන්වන්න.}$$

**සාධනය:**
පළමුව දෙවන පදය සලකමු:


$$\overline{(\bar{B} + C)} \cdot \bar{A}\bar{B}$$


ද මෝගන් නීතියට අනුව, $\overline{(\bar{B} + C)} = \overline{\overline{B}} \cdot \bar{C} = B\bar{C}$ වේ.
එම නිසා:


$$B\bar{C} \cdot \bar{A}\bar{B} = \bar{A} \cdot (B \cdot \bar{B}) \cdot \bar{C}$$


බූලියන් නීති වලට අනුව $B \cdot \bar{B} = 0$ වේ.


$$= \bar{A} \cdot 0 \cdot \bar{C} = 0$$

දැන් පළමු පදය සලකමු:


$$\bar{A}\bar{B} \cdot \overline{(\bar{B} \oplus C)}$$


මෙහි $\overline{(\bar{B} \oplus C)}$ යනු XNOR ද්වාරයකි.


$$\overline{(\bar{B} \oplus C)} = \overline{\bar{B}}\bar{C} + \bar{B}C = B\bar{C} + \bar{B}C$$


එය පළමු පදයට ආදේශ කළ විට:


$$\bar{A}\bar{B}(B\bar{C} + \bar{B}C) = \bar{A}\bar{B}B\bar{C} + \bar{A}\bar{B}\bar{B}C$$

$$\bar{B}B = 0\text{ සහ }\bar{B}\bar{B} = \bar{B}\text{ නිසා:}$$

$$= 0 + \bar{A}\bar{B}C = \bar{A}\bar{B}C$$

LHS එකතු කළ විට:


$$\text{LHS} = \bar{A}\bar{B}C + 0 = \bar{A}\bar{B}C = \text{RHS}$$


**(LHS = RHS බව ඔප්පු විය.)**

---

### (b) (i) සත්‍යතා වගුව (Truth Table):

| $X$ | $Y$ | $Z$ | $P = \bar{X}$ | $Q = \bar{Y} + Z$ | $R = \overline{X+Y}$ | $P \cdot Q$ | $F = PQ + R$ |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 1 | 1 | 1 | 1 | **1** |
| 0 | 0 | 1 | 1 | 1 | 1 | 1 | **1** |
| 0 | 1 | 0 | 1 | 0 | 0 | 0 | **0** |
| 0 | 1 | 1 | 1 | 1 | 0 | 1 | **1** |
| 1 | 0 | 0 | 0 | 1 | 0 | 0 | **0** |
| 1 | 0 | 1 | 0 | 1 | 0 | 0 | **0** |
| 1 | 1 | 0 | 0 | 0 | 0 | 0 | **0** |
| 1 | 1 | 1 | 0 | 1 | 0 | 0 | **0** |

---

### (ii) සම්මත SOP සහ සම්මත POS ප්‍රකාශන:

* **සම්මත SOP (Sum of Products):**

$$F(X, Y, Z) = \bar{X}\bar{Y}\bar{Z} + \bar{X}\bar{Y}Z + \bar{X}YZ$$


* **සම්මත POS (Product of Sums):**

$$F(X, Y, Z) = (X + \bar{Y} + Z)( \bar{X} + Y + Z)( \bar{X} + Y + \bar{Z})( \bar{X} + \bar{Y} + Z)( \bar{X} + \bar{Y} + \bar{Z})$$



---

### (iii) කානෝ සිතියම් (K-Map) මඟින් POS ප්‍රකාශනය සරල කිරීම:

0 අගයන් (Maxterms) සිතියම් ගත කළ විට:

| $X \setminus YZ$ | 00 | 01 | 11 | 10 |
| --- | --- | --- | --- | --- |
| **0** | 1 | 1 | 1 | **0** |
| **1** | **0** | **0** | **0** | **0** |

* **කාණ්ඩ 1 (Group of 4):** පහළ පේළිය ($X=1$) සම්පූර්ණයෙන්ම 0 වේ $\implies \bar{X}$
* **කාණ්ඩ 2 (Group of 2):** සිරස්ව ඇති 0 දෙක (සෛල 2 සහ 6) $\implies (\bar{Y} + Z)$

**සරල කළ POS ප්‍රකාශනය:**


$$F = \bar{X}(\bar{Y} + Z)$$

---

### (iv) නැන්ඩ් (NAND) ද්වාර පමණක් භාවිතයෙන් පරිපථය:

$$F = \bar{X}(\bar{Y} + Z) = \overline{ \overline{\bar{X} \cdot \overline{Y \cdot \bar{Z}}} }$$

```
X -----[NAND]-----\             
                   [NAND]-----[NAND]---- F
Y -----\          /
        [NAND]---/
Z -----[NAND]---/

```

---

---

## ප්‍රශ්නය 6

### (a) (i) ක්‍රම දෙකෙහි ප්‍රධාන අරමුණු:

* **ක්‍රමය A:** **රහස්‍යභාවය (Confidentiality / Privacy)** ආරක්ෂා කිරීම. (පණිවිඩය කියවිය හැක්කේ නිරුන්ට පමණි).
* **ක්‍රමය B:** **අනන්‍යතාවය තහවුරු කිරීම (Authentication / Digital Signature)**. (පණිවිඩය එවනු ලැබුවේ ගයාන් විසින්ම බව තහවුරු වේ).

### (ii) ක්‍රම දෙකම එකට භාවිතයෙන් ආරක්ෂාව වැඩිවන ආකාරය:

* ගයාන් පණිවිඩය මුලින්ම තම පෞද්ගලික යතුරෙන් (Private key) Encrypt කර (Digital Signature ලබා දී), ඉන්පසු එය නිරුන්ගේ පොදු යතුරෙන් (Public key) නැවත Encrypt කරයි. මෙයින් රහස්‍යභාවය (Confidentiality) මෙන්ම අනන්‍යතාවය (Authentication) යන දෙකම එකවර තහවුරු වේ.

---

### (b) (i) උපජාලකරණය (Subnetting Table):

මුළු ලිපින පරාසය: `172.30.54.0/25` (මුළු ලිපින ගණන 128)

| පීඨය | අවශ්‍ය ලිපින | ජාල ලිපිනය (Network IP) | විකාශන ලිපිනය (Broadcast IP) | උපජාල ආවරණය (Subnet Mask) | භාවිත කළ හැකි IP ලිපින පරාසය |
| --- | --- | --- | --- | --- | --- |
| **ඉංජිනේරු** | 60 | `172.30.54.0/26` | `172.30.54.63` | `255.255.255.192` | `172.30.54.1` - `172.30.54.62` |
| **විද්‍යා** | 29 | `172.30.54.64/27` | `172.30.54.95` | `255.255.255.224` | `172.30.54.65` - `172.30.54.94` |
| **කලා** | 15 | `172.30.54.96/27` | `172.30.54.127` | `255.255.255.224` | `172.30.54.97` - `172.30.54.126` |

---

### (ii) විශ්ව විද්‍යාලීය ජාලයේ තාර්කික සැලසුම (Logical Network Diagram):

```
                       [ Internet ]
                            |
                       [ Firewall ]
                            |
                        [ Router ] <------> [ Proxy Server ]
                        /   |    \
                       /    |     \
                 [Switch] [Switch] [Switch]
                    |        |        |
                  (Eng)    (Sci)    (Arts)
               (DHCP Server)

```

---

### (iii) ප්‍රොටෝකෝල තේරීම:

* **A (සජීවී වීඩියෝ):** **UDP** (වේගය සහ අඩු ප්‍රමාද කාලය වඩාත් වැදගත් වන නිසා).
* **B (ගොනු බාගත කිරීම):** **TCP** (දත්ත නිවැරදිව හා සම්පූර්ණයෙන් ලැබීම අත්‍යවශ්‍ය වන නිසා).
* **C (මාර්ගගත ප්‍රශ්න විචාරාත්මක):** **TCP** (පිළිතුරු නිවැරදි අනුපිළිවෙලින් සහ විශ්වාසදායකව ලැබිය යුතු නිසා).

---

---

## ප්‍රශ්නය 7

### (a) (i) IoT සටහනේ කොටස් ලේබල් කිරීම:

* **A:** හෘද ස්පන්දන වේග සංවේදකය (Heart-rate Sensor)
* **B:** සන්නිවේදන මොඩියුලයක් සහිත Arduino පුවරුව (Arduino microcontroller board)
* **C:** ධ්වනිකාරකය / එලාම් එක (Alarm / Actuator)

### (ii) M සංකේතයෙන් දැක්වෙන රැහැන් රහිත සන්නිවේදනය:

* Wi-Fi, Bluetooth හෝ Cellular ජාල හරහා සිදුවන ද්වි-මාර්ග රැහැන් රහිත සන්නිවේදනය (Two-way Wireless Communication). මෙඟින් සංවේදක දත්ත ජංගම යෙදුමට යවන අතර පාලන විධාන ජංගම යෙදුමෙන් ලබා ගනී.

---

### (b) ඇල්ගොරිතමයේ X, Y, Z අගයන්:

* **X:** `4` (හෘද ස්පන්දනය 4 ට වඩා අඩු නම්)
* **Y:** `Alarm = True` (හෝ `Alarm ON`)
* **Z:** `6` (හෘද ස්පන්දනය 6 ට වඩා වැඩි නම්)

---

### (c) උෂ්ණත්ව සංවේදකයක් මඟින් රෝගී කාමරය නිරීක්ෂණය කරන ආකාරය:

* කාමරයේ උෂ්ණත්වය අඛණ්ඩව මැන බලා සංඥා Microcontroller එක වෙත යවයි. උෂ්ණත්වය නියමිත සීමාව ඉක්මවා ගියහොත් වායුසමීකරණ පද්ධතිය ක්‍රියාත්මක කිරීම හෝ හෙදියන් දැනුවත් කිරීම සිදු කරයි.

---

### (d) (i) බහු-නියෝජිත පද්ධතියේ වර්ගය:

* **සහයෝගී බහු-නියෝජිත පද්ධතිය (Collaborative Multi-Agent System)**

### (ii) P, R, Q, S අන්තර්ක්‍රියා:

* **P:** වෛද්‍යවරයා/හෙදිය සහ පළමු නියෝජිතයා (Agent 1) අතර පරිශීලක අන්තර්ක්‍රියාව.
* **R:** Agent 1 සහ රෝහල් දත්ත ගබඩාව (Hospital Database) අතර දත්ත කියවීම/ලිවීම.
* **Q:** Agent 1 සහ Agent 2 අතර තොරතුරු හුවමාරුව සහ සහයෝගීතාවය.
* **S:** Agent 2 සහ සෙවුම් නියෝජිතයා (Search Agent) අතර අන්තර්ජාලය හරහා තොරතුරු සෙවීම.

### (iii) මෙවැනි පද්ධතියක ඇති ප්‍රධාන වාසියක්:

* **ස්වයංක්‍රීයතාවය සහ කාර්යක්ෂමතාවය (Autonomy and Efficiency):** මිනිස් මැදිහත් වීමකින් තොරව තොරතුරු සෙවීම, දත්ත යාවත්කාලීන කිරීම් සමාන්තරව සිදු කරමින් ඉක්මන් තීරණ ගැනීමට උපකාරී වීම.

---

---

## ප්‍රශ්නය 8

### (a) දී ඇති මිල ගණන් ඇතුළත් කළ විට ලැබෙන ප්‍රතිදානය (Output):

```python
# ප්‍රතිදානය:
[1200.0, 850.0, 650.0, 1300.0]
4000.0

```

---

### (b) ExpensiveItem() ශ්‍රිතය සඳහා වන Python කේතය:

**උපකල්පනය:** ලැයිස්තු දෙකෙහිම එකම ප්‍රමාණයකින් දත්ත පවතින අතර ඒවා හිස් නොවේ.

```python
def ExpensiveItem(names, prices):
    if not names or not prices:
        return None
    
    max_price = prices[0]
    max_index = 0
    
    for i in range(1, len(prices)):
        if prices[i] > max_price:
            max_price = prices[i]
            max_index = i
            
    return names[max_index], max_price

```

---

### (c) ද්විමාන අරාව සඳහා වන Python ක්‍රමලේඛය:

```python
temp = [[180, 200, 190], [210, 205, 195], [175, 185, 220]]

# ඉහළම උෂ්ණත්වය සෙවීම
max_temp = temp[0][0]
for row in temp:
    for t in row:
        if t > max_temp:
            max_temp = t

print("Highest Temperature:", max_temp)

# ආරක්ෂිත බව පරීක්ෂා කිරීම
if max_temp <= 220:
    print("Safe")
else:
    print("Unsafe")

```

---

---

## ප්‍රශ්නය 9

### (a) (i) බැංකු පද්ධතිය සඳහා වන ER රූප සටහන (ER Diagram Description):

* **ස්ථූලතා (Entities) සහ උපලක්ෂණ (Attributes):**
* **Bank:** `RegCode` (ප්‍රාථමික යතුර - Underlined), `BankName`
* **Branch:** `BrNo` (ප්‍රාථමික යතුර - Underlined), `BrName`, `Address`
* **Account:** `AccNo` (ප්‍රාථමික යතුර - Underlined), `AccType`, `DepPrice`, `TimePeriod`, `Interest`, `DepDate`, `MatureDate`
* **Customer:** `NIC` (ප්‍රාථමික යතුර - Underlined), `CusName`, `DOB`, `Address`, `Email`
* **MobileNo:** බහු-අගයැති උපලක්ෂණය (Multi-valued Attribute) $\implies$ ද්විත්ව ඉලිප්සය.


* **සම්බන්ධතා (Relationships):**
* **Bank (1) -- Has -- (N) Branch**
* **Branch (1) -- Manages -- (N) Account**
* **Customer (M) -- Opens -- (N) Account** (සම්බන්ධතා උපලක්ෂණ: `OpenDate`, `AccountStatus`)



---

### (ii) අදාළ සම්බන්ධතා ආකෘතිය (Relational Schema):

* **Bank** (RegCode, BankName)
* **Branch** (BrNo, BrName, Address, *RegCode*)
* **Account** (AccNo, AccType, DepPrice, TimePeriod, Interest, DepDate, MatureDate, *BrNo*)
* **Customer** (NIC, CusName, DOB, Address, Email)
* **Customer_Mobile** (NIC, MobileNo)
* **Customer_Account** (NIC, AccNo, OpenDate, AccountStatus)

---

### (b) (i) වගුව ප්‍රසාමාන්‍යකරණය වී නොමැති බව පැහැදිලි කිරීම:

* වගුවේ එක් සේවකයෙකුට දුරකථන අංක කිහිපයක් පැවතීම නිසා පරමාණුක අගයන් (Atomic values) නොමැත. එමෙන්ම මෙහි ආන්තරික පරායත්තතා (Transitive Dependencies) පවතී (උදා: `MID` හරහා `MName` තීරණය වීම).

### (ii) පවතින ප්‍රසාමාන්‍යකරණ මට්ටම:

* **පළමු ප්‍රසාමාන්‍යකරණ මට්ටම (1NF)** - පුනරාවර්තන කාණ්ඩ ඉවත් කළ පසු සියලු දත්ත පේළි තනි අගයන් ගනී. නමුත් අර්ධ පරායත්තතා පවතින බැවින් 2NF නොවේ.

### (iii) 3NF දක්වා විභේදනය කළ වගු:

* **Project** (PCode, PTitle, Budget, *MID*, *DepNo*)
* **Manager** (MID, MName)
* **Department** (DepNo, DepName)
* **Employee** (EmpNo, EmpName, MobileNo, *PCode*)

---

---

## ප්‍රශ්නය 10

### (a) (i) සන්දර්භ රූප සටහන (Context Diagram):

```
                   [ ලියාපදිංචි විස්තර / ගෙවීම් ]
                  -------------------------------->
 [ Student ] <----                                  [ Workshop Management System ]
                  -------------------------------->             |
                    [ ශිෂ්‍ය අංකය / විද්‍යුත් රිසිට්පත ]              |
                                                                | (මාසික වාර්තා)
   [ Bank System ] <--------------------------------------------|
                    <-------------------------------------------|
                     [ ගෙවීම් තහවුරු කිරීමේ දත්ත ]              v
                                                    [ Academic Manager ]

```

---

### (ii) මට්ටම-1 දත්ත ගැලීම් රූප සටහන (Level-1 DFD):

* **පද්ධති ක්‍රියාවලි (Processes):**
1. `1.0 Handle Online Registration`
2. `2.0 Handle Online Payments`
3. `3.0 Handle Workshop Materials & Reporting`


* **දත්ත ගබඩා (Data Stores):**
* `D1: Workshop Database`
* `D2: Student Database`
* `D3: Payment Database`



---

### (b) ශක්‍යතා අධ්‍යයනය (Feasibility Study) ගැළපීම:

* **(i) මූල්‍යමය ප්‍රතිපාදන සහ පිරිවැය:**
* **ආර්ථික ශක්‍යතාවය (Economic Feasibility)**


* **(ii) ප්‍රමාණවත් පරිගණක සහ අන්තර්ජාල පහසුකම්:**
* **තාක්ෂණික ශක්‍යතාවය (Technical Feasibility)**


* **(iii) කාර්ය මණ්ඩලයේ කැමැත්ත සහ පුහුණුව:**
* **ක්‍රියාකාරී ශක්‍යතාවය (Operational Feasibility)**


* **(iv) ලබා දී ඇති කාලරාමුව තුළ නිම කිරීම:**
* **කාලරාමු ශක්‍යතාවය (Schedule Feasibility)**
