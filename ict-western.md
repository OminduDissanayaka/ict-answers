# Grade 13 - Information and Communication Technology (ICT)
## 2026 Third Term Test - Western Province Department of Education
### සම්පූර්ණ පිළිතුරු පත්‍රය (Complete Marking Scheme & Answers)

---

## I පත්‍රය - බහුවරණ ප්‍රශ්න සඳහා පිළිතුරු (Paper I - MCQ Answers)

| ප්‍රශ්න අංකය | පිළිතුරු අංකය |
| :---: | :---: |
| **1** | (3) |
| **2** | (5) |
| **3** | (5) |
| **4** | (1) |
| **5** | (3) |
| **6** | (1) |
| **7** | (3) |
| **8** | (5) |
| **9** | (2) |
| **10** | (2) |
| **11** | (4) |
| **12** | (1) |
| **13** | (5) |
| **14** | (2) |
| **15** | (4) |
| **16** | (2) |
| **17** | (5) |
| **18** | (3) |
| **19** | (2) |
| **20** | (3) |
| **21** | (5) |
| **22** | (3) |
| **23** | (5) |
| **24** | (2) |
| **25** | (2) |
| **26** | (1) |
| **27** | (4) |
| **28** | (3) |
| **29** | (4) |
| **30** | (5) |
| **31** | (2) |
| **32** | (2) |
| **33** | (4) |
| **34** | (3) |
| **35** | (2) |
| **36** | (1) |
| **37** | (2) |
| **38** | (2) |
| **39** | (4) |
| **40** | (3) |
| **41** | (4) |
| **42** | (3) |
| **43** | (1) |
| **44** | (4) |
| **45** | (1) |
| **46** | (2) |
| **47** | (5) |
| **48** | (4) |
| **49** | (4) |
| **50** | (1) |

---

## II දෙවෙනි පත්‍රය - ප්‍රශ්න සහ පිළිතුරු (Paper II - Questions & Answers)

---

### **ප්‍රශ්නය 01**

#### **(a) ප්‍රශ්නය:**
පහත HTML කේත ඛණ්ඩය වෙබ් අතිරික්සුවක් (Web Browser) මගින් නිරූපණය කරන විට අපේක්ෂිත ප්‍රතිදානය ඇඳ දක්වන්න:
```html
<u>Available Courses</u>
<ol>
  <li>Information Technology</li>
  <li>Engineering</li>
  <li>Business Management</li>
  <ul>
    <li>Accounting</li>
    <li>Marketing</li>
  </ul>
  <li>Law</li>
</ol>
```

#### **පිළිතුර:**
වෙබ් අතිරික්සුවේ දර්ශනය වන ප්‍රතිදානය:

<u>Available Courses</u>

1. Information Technology
2. Engineering
3. Business Management
   * Accounting
   * Marketing
4. Law

*(සටහන: `<ol>` ලැයිස්තුව ඇතුළත nested `<ul>` ලැයිස්තුවේ අයිතම බුලට් පොයින්ට් සහිතව ඇතුළට indented වී දර්ශනය වන අතර, අංකිත ලැයිස්තුව 4. Law ලෙස පිළිවෙලින් ඉදිරියට යයි.)*

---

#### **(b) ප්‍රශ්නය:**
ඉහත HTML ලැයිස්තුවට පහත යාවත්කාලීන කිරීම් කිරීමට නිවැරදි තනි CSS කේතය ලියන්න:
- (i) සියලුම ලැයිස්තු අයිතම Times New Roman අකුරු මගින් දර්ශනය කිරීම.
- (ii) අංක සහිත ලැයිස්තුවේ (ordered list) අයිතමවල වර්ගය රෝමන් ඉලක්කම් දක්වා වෙනස් කිරීම.
- (iii) නොඅංකිත උප-ලැයිස්තු අයිතම italic ආකාරයට වෙනස් කිරීම.
- (iv) සම්පූර්ණ ලැයිස්තු කොටස වටා 1px solid කොළ පැහැති මායිමක් (border) ප්‍රකාශ කිරීම.
- (v) පිටුවේ පසුබිම් වර්ණය ලා කහ පැහැයට වෙනස් කිරීම.

#### **පිළිතුර:**
```css
/* (i) සියලුම ලැයිස්තු අයිතම Times New Roman අකුරු කිරීම */
ol, ul, li {
    font-family: "Times New Roman", serif;
}

/* (ii) අංක සහිත ලැයිස්තුව රෝමන් ඉලක්කම් (I, II, III...) බවට පත් කිරීම */
ol {
    list-style-type: upper-roman;
}

/* (iii) නොඅංකිත උප-ලැයිස්තු අයිතම italic කිරීම */
ul li {
    font-style: italic;
}

/* (iv) සම්පූර්ණ ලැයිස්තු කොටස වටා 1px කොළ පැහැති මායිමක් යෙදීම */
ol {
    border: 1px solid green;
}

/* (v) පිටුවේ පසුබිම් වර්ණය ලා කහ (lightyellow) කිරීම */
body {
    background-color: lightyellow;
}
```

---

#### **(c) ප්‍රශ්නය:**
වෙබ් පිටුවක් මගින් විදර්ශනය කරන ලද රූපය 1 හි දක්වා ඇති HTML යෙදවුම (Library Membership Form) සලකා බලන්න. රූපයේ දැක්වෙන ප්‍රතිදානය ලබා ගැනීමට පහත HTML කේතයේ හිස්තැන් පුරවන්න:

#### **පිළිතුර:**
```html
<html>
<head>
    <title>Library Membership Form</title>
</head>
<body>
    <h1>Library Membership Form</h1>
    <form action="register.php" method="post">
        <p>Member Name: <input type="text" name="uname"></p>
        
        <p>
            <div>Enter Membership Type : 
                <input type="radio" name="mtype" value="1">1. Student</input>
                <input type="radio" name="mtype" value="2">2. Teacher</input>
            </div>
        </p>
        
        <div>
            Preferred Notification Method : 
            <input type="checkbox" name="notify" value="Email">Email</input>
            <input type="checkbox" name="notify" value="SMS">SMS</input>
        </div>
        
        <br>
        Select Library Branch : 
        <select name="branch">
            <option value="Colombo">Colombo</option>
            <option value="Kalutara">Kalutara</option>
            <option value="Gampaha">Gampaha</option>
        </select>
        <br><br>
        <input type="submit" value="Register">
    </form>
</body>
</html>
```

---

#### **(d) ප්‍රශ්නය:**
HTML පෝරමය හරහා ඇතුළත් කරන ලද විස්තර දත්ත සමුදායක (MySQL Database) `member` වගුවට ඇතුළත් කිරීමට පහත PHP කේතයේ හිස් තැන් පුරවන්න.

#### **පිළිතුර:**
```php
<?php
$connection = new mysqli("localhost", "root", "", "libraryDB");

if ($connection->connect_errno) {
    echo "Failed to connect to MySQL: " . $connection->connect_error;
    exit();
}

$mname = $_POST['uname'];
$mtype = $_POST['mtype'];
$notify = $_POST['notify'];
$branch = $_POST['branch'];

$sql = "INSERT INTO member (memberName, membershipType, notificationMethod, branch) 
        VALUES ('$mname', '$mtype', '$notify', '$branch')";

if ($connection->query($sql) === TRUE) {
    echo "New record created successfully";
} else {
    echo "Error: " . $sql . "<br>" . $connection->error;
}

$connection->close();
?>
```

---

### **ප්‍රශ්නය 02**

#### **(a) ප්‍රශ්නය:**
මෝටර් රථ කුලියට දීමේ සේවා සපයන සමාගමක් සඳහා නිර්මාණය කර ඇති ER රූප සටහන සලකා බලන්න.
- (i) ER රූප සටහනේ Driver සහ Vehicle යන එන්ටිටි අතර සන්නිවේදකතාව (Cardinality) දක්වන්න.
- (ii) රියදුරෙකු විසින් වාහනයක් ධාවනය කර ඇති වර්ෂ ගණන සටහන් කිරීමට `NoOfYears` යන උපලක්ෂණය (Attribute) ER සටහනට ඇතුළත් කරන්නේ කෙසේද?
- (iii) InsurancePolicy (රක්ෂණ ඔප්පුව) සඳහා ER සටහන යාවත්කාලීන කරන්නේ කෙසේද?

#### **පිළිතුර:**
- **(i) සන්නිවේදකතාව (Cardinality):**
  `1 : 1` (එකට එක / One-to-One) — එක් රියදුරෙකුට ධාවනය කළ හැක්කේ එක් වාහනයක් පමණි, එමෙන්ම වාහනයක් පදවනු ලබන්නේ එක් රියදුරෙකු විසිනි.

- **(ii) NoOfYears උපලක්ෂණය ඇතුළත් කිරීම:**
  `NoOfYears` යනු `drives` නමැති සම්බන්ධතාවයේ (Relationship) අඩංගු වන **සම්බන්ධතා උපලක්ෂණයකි (Relationship Attribute)**. එය `drives` දියමන්ති හැඩයට ඉලිප්සයක් ලෙස සම්බන්ධ කෙරේ.

- **(iii) InsurancePolicy ER සංකල්පිත ආකෘතිය:**
  - `InsurancePolicy` යනු **දුර්වල එන්ටිටියකි (Weak Entity)** [ද්විත්ව සෘජුකෝණාස්‍රයකින් දක්වයි].
  - Driver සහ InsurancePolicy අතර සම්බන්ධතාවය **'has'** වේ [ද්විත්ව දියමන්තියකින් දක්වයි].
  - Cardinality: **1 සිට M (1 : M)** [එක් රියදුරෙකුට රක්ෂණ ඔප්පු කිහිපයක් තිබිය හැක].
  - Participations: InsurancePolicy එන්ටිටිය සඳහා **සම්පූර්ණ සහභාගීත්වය (Total Participation / ද්විත්ව රේඛා)** පවතී.
  - උපලක්ෂණ: `InsName` (අර්ධ යතුර / Partial Key - තිත් රේඛාවකින් යටින් ඉර අඳිනු ලැබේ), `TimePeriod`, `Benefits`.

---

#### **(b) ප්‍රශ්නය:**
පාසල් පුස්තකාල පද්ධතියේ Book, Student, BorrowBook වගු ඇසුරින් පහත ප්‍රශ්න වලට පිළිතුරු සපයන්න:

- **(i) Book වගුව සෑදීමට නිවැරදි SQL විමසුම (SQL Query) ලියන්න:**
```sql
CREATE TABLE Book (
    BookId VARCHAR(10) NOT NULL,
    BookName VARCHAR(100) NOT NULL,
    NoOfCopies INT NOT NULL,
    PRIMARY KEY (BookId)
);
```

- **(ii) 'Gamperaliya' පොතේ පිටපත් ගණන (NoOfCopies) 5 දක්වා යාවත්කාලීන කිරීමේ SQL විමසුම ලියන්න:**
```sql
UPDATE Book 
SET NoOfCopies = 5 
WHERE BookName = 'Gamperaliya';
```

- **(iii) පහත SQL විමසුමේ ප්‍රතිදානය (Output) ලියන්න:**
```sql
SELECT StuName, Class 
FROM Student, BorrowBook 
WHERE BorrowDate = '2025-05-21' AND Student.StuId = BorrowBook.StuId;
```

**ප්‍රතිදාන වගුව (Output Table):**

| StuName | Class |
| :--- | :--- |
| Sanduni | 11B |
| Kamal | 10A |

---

#### **(c) ප්‍රශ්නය:**
බිටු ශ්‍රේණිය: `0110111001`
නැවත ශූන්‍ය නොවන ගුණාකාර අනුක්‍රමික ක්‍රමය **[NRZ-I (Non-Return to Zero Inverted)]** භාවිතයෙන් මෙම බිටු නිරූපණය කර දක්වන්න. (පළමු බිටුව High මට්ටමේ පවතී).

#### **පිළිතුර:**
NRZ-I කේතකරණයේදී:
- බිටු **'1'** මගින් සංඥා මට්ටමේ වෙනසක් (Transition: High $ightarrow$ Low හෝ Low $ightarrow$ High) සිදුවේ.
- බිටු **'0'** මගින් සංඥා මට්ටමේ වෙනසක් සිදු නොවේ (No Transition: පෙර පැවති මට්ටමම පවත්වා ගනී).

**මට්ටම් මාරුවීමේ අනුක්‍රමය:**
1. **0** $ightarrow$ සංඥාව High මට්ටමේ පවතී
2. **1** $ightarrow$ සංඥාව Low මට්ටමට මාරු වේ
3. **1** $ightarrow$ සංඥාව High මට්ටමට මාරු වේ
4. **0** $ightarrow$ සංඥාව High මට්ටමේ පවතී
5. **1** $ightarrow$ සංඥාව Low මට්ටමට මාරු වේ
6. **1** $ightarrow$ සංඥාව High මට්ටමට මාරු වේ
7. **1** $ightarrow$ සංඥාව Low මට්ටමට මාරු වේ
8. **0** $ightarrow$ සංඥාව Low මට්ටමේ පවතී
9. **0** $ightarrow$ සංඥාව Low මට්ටමේ පවතී
10. **1** $ightarrow$ සංඥාව High මට්ටමට මාරු වේ

---

#### **(d) ප්‍රශ්නය:**
PSTN (Public Switched Telephone Network) සහ Packet Switching ජාල අතර වෙනස්කම් සංසන්දනය කරන්න.

#### **පිළිතුර:**

| ලක්ෂණය | PSTN (Circuit Switching) | Packet Switching |
| :--- | :--- | :--- |
| **සම්බන්ධතා පථය** | දත්ත හුවමාරුවට පෙර කැපවූ භෞතික පථයක් (Dedicated Path) පිහිටුවයි. | කැපවූ පථයක් නොමැත; දත්ත පැකට් ලෙස විවිධ මාර්ග ඔස්සේ යවයි. |
| **කලාප පළල (Bandwidth)** | ස්ථාවර/වෙන්කළ කලාප පළලක් ඇත. | ගතිකව (Dynamic) කලාප පළල බෙදා ගනී (වඩාත් කාර්යක්ෂමයි). |
| **ප්‍රමාදය (Delay)** | සම්බන්ධතාවය පිහිටුවීමට කාලය ගතවන නමුත් දත්ත ගැලීම ස්ථාවරයි. | පැකට් පෝලිම්ගත වීම (Queuing) නිසා ප්‍රමාදයන් සිදු විය හැක. |

---

### **ප්‍රශ්නය 03**

#### **(a) ප්‍රශ්නය:**
රථගාල් ගාස්තු ගණනය කිරීමේ ඇල්ගොරිතමයේ ගැලීම් සටහන (Flowchart) සඳහා A සිට H දක්වා ලේබල් සඳහා සුදුසු ප්‍රකාශන/කොන්දේසි ලියන්න.

#### **පිළිතුර:**
- **A:** `Read N, VType` (හෝ පැය ගණන N සහ වාහන වර්ගය VType ආදානය කර ගැනීම)
- **B:** `Display "Invalid parking duration"` (හෝ "වැලැක්වුණු කාලය" මුද්‍රණය කිරීම)
- **C:** `N <= 2`
- **D:** `Fee = N * 100`
- **E:** `Fee = 200 + (N - 2) * 150`
- **F:** `VType == 'Van' OR VType == 'SUV'`
- **G:** `Fee = Fee + 500`
- **H:** `Fee > 5000`

---

### **ප්‍රශ්නය 05**

#### **(a) ප්‍රශ්නය:**
බූලියන් වීජ ගණිතය භාවිතයෙන් පහත බූලියන් ප්‍රකාශනය සරල කර පෙන්වන්න:
$$\overline{A}\cdot B + (B \oplus C) + (\overline{B+C})\cdot \overline{AB} = \overline{ABC}$$

#### **පිළිතුර (සුළු කිරීමේ පියවර):**

1. $B \oplus C = B\overline{C} + \overline{B}C$ (XOR ප්‍රකාශනය ප්‍රසාරණය කිරීම)
2. $\overline{B+C} = \overline{B}\cdot\overline{C}$ (De Morgan නියමය)
3. $\overline{AB} = \overline{A} + \overline{B}$ (De Morgan නියමය)

දැන් $(\overline{B+C})\cdot\overline{AB}$ පදය සුළු කරමු:
$$(\overline{B}\overline{C})(\overline{A} + \overline{B}) = \overline{A}\overline{B}\overline{C} + \overline{B}\overline{C} = \overline{B}\overline{C}(1 + \overline{A}) = \overline{B}\overline{C}$$

මුළු ප්‍රකාශනය එකතු කළ විට:
$$= \overline{A}B + B\overline{C} + \overline{B}C + \overline{B}\overline{C}$$

පද එක් රැස් කරමු ($B\overline{C} + \overline{B}\overline{C}$):
$$B\overline{C} + \overline{B}\overline{C} = (B + \overline{B})\overline{C} = 1 \cdot \overline{C} = \overline{C}$$

දැන් ප්‍රකාශනය:
$$= \overline{A}B + \overline{B}C + \overline{C}$$

Absorption නියමය යෙදීම ($\overline{C} + \overline{B}C = \overline{C} + \overline{B}$):
$$= \overline{A}B + \overline{B} + \overline{C}$$

Absorption නියමය යෙදීම ($\overline{B} + \overline{A}B = \overline{B} + \overline{A}$):
$$= \overline{A} + \overline{B} + \overline{C}$$

De Morgan නියමය යෙදීමෙන්:
$$= \overline{A \cdot B \cdot C} = \overline{ABC}$$

**(ප්‍රකාශනය සත්‍යාපනය විය.)**

---

#### **(b) ප්‍රශ්නය:**
- $P = \overline{X}$
- $Q = \overline{Y} + Z$
- $R = X + Y$
- $F = (P \cdot Q) + R$

**ගණනය කිරීම් සහ පිළිතුරු:**

**(i) සත්‍යතා වගුව (Truth Table):**

| X | Y | Z | P ($\overline{X}$) | Q ($\overline{Y}+Z$) | R ($X+Y$) | P · Q | F [$(P \cdot Q) + R$] |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 0 | 1 | **1** |
| 0 | 0 | 1 | 1 | 1 | 0 | 1 | **1** |
| 0 | 1 | 0 | 1 | 0 | 1 | 0 | **1** |
| 0 | 1 | 1 | 1 | 1 | 1 | 1 | **1** |
| 1 | 0 | 0 | 0 | 1 | 1 | 0 | **1** |
| 1 | 0 | 1 | 0 | 1 | 1 | 0 | **1** |
| 1 | 1 | 0 | 0 | 0 | 1 | 0 | **1** |
| 1 | 1 | 1 | 0 | 1 | 1 | 0 | **1** |

*(සටහන: ලකුණු සම්ප්‍රදායට අනුව (Marking Scheme), F හි අගය $F = \overline{X} \cdot (\overline{Y} + Z)$ ලෙස සලකන අවස්ථාව සඳහා K-Map එක පදනම් වේ).*

**(ii) සම්මත SOP සහ POS ප්‍රකාශන:**
- **Marking Scheme අනුකූල SOP:**
  $$F = \overline{X}\overline{Y}\overline{Z} + \overline{X}\overline{Y}Z + \overline{X}YZ$$
- **Marking Scheme අනුකූල POS:**
  $$F = (X + Y + Z)(X + Y + \overline{Z})(X + \overline{Y} + Z)(\overline{X} + Y + Z)(\overline{X} + Y + \overline{Z})(\overline{X} + \overline{Y} + Z)(\overline{X} + \overline{Y} + \overline{Z})$$

**(iii) කානෝ සිතියම (Karnaugh Map) මගින් සරල කිරීම:**

| X \ YZ | 00 | 01 | 11 | 10 |
| :-: | :-: | :-: | :-: | :-: |
| **0** | 1 | 1 | 1 | 0 |
| **1** | 0 | 0 | 0 | 0 |

K-Map එක කාණ්ඩ කිරීමෙන් සරල කළ ප්‍රකාශනය:
$$F = \overline{X}\overline{Y} + \overline{X}Z = \overline{X}(\overline{Y} + Z)$$

**(iv) අවම ද්වාර (NOR gates 3ක්) භාවිතයෙන් තාර්කික පරිපථය නිර්මාණය:**
- $F = \overline{X \cdot (\overline{Y} + Z)}$ ප්‍රකාශනය NOR ද්වාර 3ක් පමණක් භාවිත කර ක්‍රියාත්මක කළ හැක.

---

### **ප්‍රශ්නය 06**

#### **(a) ප්‍රශ්නය:**
පොදු යතුරු ගුප්ත කේතනය (Public Key Cryptography):
- **ක්‍රමය A:** ගයාන් හිරාන්ගේ Public Key එකෙන් encrypt කර, හිරාන්ගේ Private Key එකෙන් decrypt කරයි.
- **ක්‍රමය B:** ගයාන්ගේ Private Key එකෙන් encrypt කර, ගයාන්ගේ Public Key එකෙන් decrypt කරයි.

#### **පිළිතුර:**
- **(i) එක් එක් ක්‍රමයේ ප්‍රධාන අරමුණ:**
  - **ක්‍රමය A හි අරමුණ:** **රහස්‍යතාව (Confidentiality)** සුරැකීම. පණිවිඩය කියවිය හැක්කේ අදාළ රහස්‍ය පුද්ගලික යතුර හිමි හිරාන්ට පමණි.
  - **ක්‍රමය B හි අරමුණ:** **සත්‍යාපනය (Authentication) සහ අඛණ්ඩතාව (Integrity / Digital Signature)** තහවුරු කිරීම. පණිවිඩය වෙනස් නොවී පැමිණි බවත්, එය යැවූයේ ගයාන්ම බවත් තහවුරු වේ.

- **(ii) A සහ B ක්‍රම දෙකම එකට භාවිත කිරීමේ වාසිය:**
  - ප්‍රථමයෙන් ගයාන් පණිවිඩය තමාගේ Private Key එකෙන් ගුප්ත කේතනය කරයි (Digital Signature/Authentication).
  - ඉන්පසු ලබාගන්නා අගය හිරාන්ගේ Public Key එකෙන් නැවත ගුප්ත කේතනය කර යවයි (Confidentiality).
  - එමගින් **රහස්‍යතාවය (Confidentiality)** මෙන්ම **සත්‍යාපනය සහ දත්ත අඛණ්ඩතාවය (Authentication & Integrity)** යන සියලු ආරක්ෂිත අංග එකවර සාක්ෂාත් වේ.

---

#### **(b) ප්‍රශ්නය:**
විශ්වවිද්‍යාල පරිශ්‍රයේ පීඨ 3ක උපාංග ගණන:
- **ඉංජිනේරු පීඨය:** පරිගණක 58, ජාල මුද්‍රණ යන්ත්‍ර 2 (මුළු IP අවශ්‍යතාව = 60 + Gateway = 61 IP)
- **විද්‍යා පීඨය:** පරිගණක 28, මුද්‍රණ යන්ත්‍රය 1 (මුළු IP අවශ්‍යතාව = 29 + Gateway = 30 IP)
- **කලා පීඨය:** පරිගණක 18, ජාල මුද්‍රණ යන්ත්‍රය 1 (මුළු IP අවශ්‍යතාව = 19 + Gateway = 20 IP)

ලබා දී ඇති IP ලිපින ඛණ්ඩය: `172.30.54.0/25` (මුළු IP ගණන = 128)

#### **පිළිතුර:**

**(i) අනුජාලකරණ වගුව (VLSM Subnet Table):**

| පීඨය (Faculty) | ජාල ලිපිනය (Network Address) | විකාශන ලිපිනය (Broadcast Address) | අනුජාල ආවරණය (Subnet Mask) | භාවිත කළ හැකි IP ලිපින පරාසය (Usable IP Range) |
| :--- | :--- | :--- | :--- | :--- |
| **ඉංජිනේරු (Engineering)** | `172.30.54.0` | `172.30.54.63` | `255.255.255.192` (/26) | `172.30.54.1` – `172.30.54.62` |
| **විද්‍යා (Science)** | `172.30.54.64` | `172.30.54.95` | `255.255.255.224` (/27) | `172.30.54.65` – `172.30.54.94` |
| **කලා (Arts)** | `172.30.54.96` | `172.30.54.127` | `255.255.255.224` (/27) | `172.30.54.97` – `172.30.54.126` |

---

**(ii) ජාලයේ තාර්කික සැකැස්ම (Logical Network Topology Diagram Description):**

1. **අන්තර්ජාල සම්බන්ධතාවය (Internet):** Firewall සහ Router හරහා පද්ධතියට සම්බන්ධ වේ.
2. **මධ්‍යම රවුටරය / නියෝජ්‍ය සේවාදායකය (Central Router & Proxy Server):**
   - Proxy Server එක සහ Firewall එක මධ්‍යම රවුටරයට සම්බන්ධ වේ.
3. **පීඨ ස්විච (Faculty Switches):**
   - මධ්‍යම රවුටරයේ වෙනස් Inter-VLAN / Subnet Interfaces 3ක් හරහා පීඨ ස්විච 3කට සම්බන්ධ වේ.
4. **ඉංජිනේරු පීඨ LAN:**
   - Switch එකට DHCP Server, PC 58 සහ Printers 2ක් සම්බන්ධ වේ.
5. **විද්‍යා පීඨ LAN:**
   - Switch එකට PC 28 සහ Printer 1ක් සම්බන්ධ වේ.
6. **කලා පීඨ LAN:**
   - Switch එකට PC 18 සහ Printer 1ක් සම්බන්ධ වේ.

---
