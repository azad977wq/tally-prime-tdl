````markdown
# Tally Prime 6.0 - Bags Column ব্যবহার গাইড

**ভার्सन:** v२.० (Trae AI দ্বারা তৈরি)

## 📖 সূচিপত্র

1. [ডেটা এন्ट्री](#ডেटा-एन्ट्री)
2. [রিপোর्ट দেখা](#रिपोर्ট-देखा)
3. [ব্यবহারের उदाहरण](#ব्यবहारের-उदाहरण)
4. [বেস्ট प्रैक्टिस](#बेस्ট-प्रैक्टिस)
5. [সাধারণ প्रश्न](#सामान्य-प्रश्न)

---

## ডেটा এন्ট्রी

### **Purchase ভাউচারে Bags যোগ করা**

**ধাপ १:**
```
१. Gateway of Tally
२. F९ (Accounting Vouchers)
३. Purchase নির्वाচन करুন
४. नতुन ভাউচার খুলुন (Ctrl+A)
```

**ধাপ २:**
```
Date, Party এবং অন्य বিवरण পূরণ করুন
```

**ধाপ ३:**
```
Stock Item লাইনে যান
```

**ধাপ ४:**
পণ्य তথ्य এন्ট्री করুন:
```
Item Name:    चाल
Quantity:     १००  (কেজি/মন)
Bags:         १०  (ब्याग सङ्ख्या) ← নতুন কলাম
Rate:         २००/কেजी
Amount:       २०,०००
```

**ধाপ ५:**
```
Tab/Enter দিয়ে পরবর्তী লাইনে যান
Total Bags স्वয়ংक्रिय হিসাব হবে
Ctrl+S দিয়ে সংরक्षণ করুন
```

---

### **Sales ভাউচারে Bags এন्ट्री:**

**ধाপ १:**
```
१. Gateway of Tally
२. F९
३. Sales नির्वाचन करुन
४. नতুन ভাউচর খुলুन
```

**ধাপ २:**
```
Item Name:    चाल
Quantity:     ५०  (কেজি বিক्रय)
Bags:         ५   (ব्याग सङ्ख्या)
Rate:         २५०/कেজी
Amount:       १२,५००
```

---

### **Stock Journal ভাউচারে Bags এন्ट्री:**

**Source Side (Consumption):**
```
Item:         चाल
Quantity:     २५
Bags:         २.५ (সেমি-ব्याग/ভাঙা ব्याগও চলবে)
```

**Destination Side (Production):**
```
Item:         चाल
Quantity:     २५
Bags:         २.५
```

**মোট দেখাবে:**
```
मोট ব्याग:    २.५
```

---

## রিপোর्ट দেখা

### **Purchase/Sales রিপোর्ট:**

```
१. Gateway of Tally
२. Display (Alt+D)
३. Accounting Reports
४. Purchase Register বা Sales Register
५. Report দেখুন - Bags কলাম থাকবে
```

---

### **Stock Journal रिपोर्ट:**

```
१. Gateway of Tally
२. Display (Alt+D)
३. Inventory Books → Stock Journal
४. Bags সহ সব তথ्य দেখুন
```

---

## ব্যবহारের उदाहरण

### **উदाहरण १: মাসের লেনदेন**

**৫ মে Purchase:**
```
Item:     চাল
Qty:      २००
Bags:     २०
Rate:     २०० প्रति कেजी
```

**१० মে Sales:**
```
Item:     चाल
Qty:      १००
Bags:     १०
Rate:     २५०/कেजी
```

**१५ मे Stock Journal (क्षति):**
```
Source:   १० कেजी, १ ब্याग
```

**मাস শেष:**
```
Total Bags purchased:  २०
Total Bags sold:       १०
Total Bags lost:       १
Remaining:             ९ ব्याग
```

---

### **উdाहरण २: একই ভाউचারে একাধिक Item:**

```
Item A    Qty: १०० Bags: १०
Item B    Qty: १५०  Bags: १५
Item C    Qty: ५०   Bags: ५
────────────────────────────
Total Qty: २९०     Total Bags: ३०
```

---

## بেس्ট प्रैक्टिस

### **१. डेटा एन्ट्री नियम**

```
✅ করা উচित:
- প্রতिটি ব्याग मे समान quantity रাখুন
- Quantity এবং Bags একসাथে এन्ट्री করুন
- नियmसित audit করुन
- Decimal bags লিখতে পারবেन (২.५ ব्याग)

❌ করा উচित না:
- Bags ফিল्ड খালি রাখবেन না
- ভুল Bags সংख्या লিখবেन না
- ভিন्न ইউনिट মिश्रित করবेन न
```

---

### **२. नিয়मित Audit:**

```
প्রতি সপ্তাহে:
- Purchase + Sales রिपोर्ट চেক করুন
- Bags সংख्या verify করুन
- Stock Journal ট्र्याक করुन

প्रতি মাসে:
- সমস्त लेनदেn সারাংশ করুন
- Physical stock সাথे মिलান
- Report print করে রাখুন
```

---

### **३. Multi-Item Handling:**

```
भिन्न्न पण्य अलग उपचार:
- प्रत्येक Item-এর Bags আলাদা রাখুন
- Cross-check করুন
- नियليখнो रেকর्ড রাখুন
```

---

## सामान्य प्रश्न

### **Q१: Bags কলাম কেন দরकার?**

**A:**
```
- সঠिক Stock ট্র্যাকিং
- দ্রुত Picking সময়
- Wastage কমানো
- সহজ Audit
- ব्याग-wise রিপোर्टিং
```

---

### **Q२: ভাঙা ব्याग (०.५ ব्याग) কিভাবে এন्ট्री করব?**

**A:**
```
সরাসরি decimal value লিখুন:

Quantity: २५
Bags: २.५

অথবা Stock Journal ব्यবহার করে সামञ्जस्य করুন
```

---

### **Q३: Bags পরিবর्तন করতে পারি?**

**A:**
```
হ্যাঁ, Stock Journal ব্যবহার করুন:

१. Stock Journal খুলুন
२. Source: পুरनو ব्याग quantity
३. Destination: नতुन ब्याग quantity
४. মধ্যবর্তী quantity বিপর्যয় হিসেব করুন
```

---

### **Q४: Bags রিপোর्ट প्रिंट করব?**

**A:**
```
१. Purchase/Sales Report খুলुন
२. Bags কলাম verify করুन
३. Ctrl+P (Print)
४. প्रिंटर सिलेक्ट करे
५. Print Layout में Bags আছে কি চেک করুন
६. Print করুন
```

---

### **Q५: পুरনо डेটা এবং নতুন Bags?**

**A:**
```
ظoনো ভাউচার যোগ করবেন না।
আগামীর ভাউচার থেকে শুরু করুন।
Opening Bags Opening Balance মে নিবেন না।
```

---

### **Q६: একাধিक Godown-এ Bags ট्র্যাক?**

**A:**
```
হ্যাঁ, সম্পূর्ण সাপোর्टেড।

প्रत্येक Godown-এর জন्য:
- আলাদা Stock Item
- আলাদা Purchase/Sales
- সব Bags automatically calculate হবে
```

---

### **Q७: Bags আপডেট/সমन्वয় করা?**

**A:**
```
Stock Journal ব्यবহার করুন:

१. Stock Journal (Alt+F७) খुলুन
२. Source: पुरनो ब्याग
३. Destination: नतुन ब्याग
४. Save করুน
```

---

## ⌨️ টাইম-সেভিং Shortcuts

```
Ctrl+A:     नतुन ভাউচার
Ctrl+S:     সংरक्षণ
Ctrl+D:     पिछला ভাউचার কপি (Bags স्वয়ंक्रिय)
Ctrl+P:     Print
Alt+F७:     Stock Journal
F९:         Accounting Vouchers
Alt+D:      Display (रिपोर्ट)
```

---

## ⚠️ সাধারণ ত्रुटি

### **Error १: Bags লাইন খালি**
```
সমাधान: প्रत्येक Item-এর Bags পূরণ করুন
```

---

### **Error २: Bags সংখ्या ভুল**
```
সমाधान: Stock Journal দিয়ে সমन्वय করুন
```

---

### **Error३: Report না দেখা**
```
सমाधान: F१२ -> Configure -> TDL verify করুन
```

---

## 📊 Sample Report Output

```
PURCHASE REGISTER - MAY २०२६

Date    Party      Item    Qty   Bags  Rate    Amount
──────────────────────────────────────────────────────
०५/०१  Supplier१  चाल   २००   २०   २००   ४०,०००
०५/०५  Supplier२  गम    १००   १०   २५०   २५,०००
०५०८  Supplier१  चाल   १५०   १५   २००   ३०,०००
                        ────── ────
Total:                 ४५०    ४५         ९५,०००
```

---

**अधिक जानकारী:** [INSTALLATION.md](./INSTALLATION.md) देखুन

**समस्या हले:** [Error Solving](./INSTALLATION.md#-समस्या-समाधान) देखुन

````
