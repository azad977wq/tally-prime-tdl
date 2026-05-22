````markdown
# Tally Prime 6.0 - Bags Column ইনস্টলেশন গাইড

**⚠️ গুরুত্বপূর্ণ:** এটি Trae AI দ্বারা তৈরি এবং পরীক্ষিত সংস্করণ (v2.0)

## 📥 কিভাবে ইনস্টল করবেন?

### **ধাপ १: TDL ফাইল ডাউনলোড করুন**

```
GitHub রিপোজিটরি থেকে bags_column.tdl ফাইল ডাউনলোড করুন:
https://github.com/azad977wq/tally-prime-tdl/raw/main/bags_column.tdl
```

---

### **ধাপ २: Tally প্রোগ্রাম সম্পূর্ণ বন্ধ করুন**

```
⚠️ গুরুত্বপূর্ণ: সমস্ত Tally প্রক্রিয়া বন্ধ করুন
- Multi-User Mode বন্ধ করুন
- Tally সম্পূর্ণভাবে বন্ধ করুন
- কিছুক্ষণ অপেক্ষা করুন
```

---

### **ধাপ ३: TDL ফাইল কপি করুন**

#### **Windows এ লোকেশন:**

**Tally Prime ইনস্টলেশন ফোল্ডার খুঁজুন:**
- সাধারণত: `C:\Tally.ERP9\`
- বা: `C:\Program Files\Tally.ERP9\`

**Plugin ফোল্ডার তৈরি করুন (যদি নেই):**

```
१. Tally.ERP9 ফোল্ডারে যান
२. নতুন ফোল्डर তৈরি করুন: Plugin
३. bags_column.tdl সেখানে কপি করুন
```

**সঠিক পথ:**
```
C:\Tally.ERP9\Plugin\bags_column.tdl
অথবা
C:\Program Files\Tally.ERP9\Plugin\bags_column.tdl
```

---

### **ধাপ ४: Tally খুলুন এবং TDL লোড করুন**

```
१. Tally Prime খুলুন
२. Gateway of Tally
३. F१२ (Configure) → Enter
४. টেলি ডিফিনিশন ল্যাঙ্গুয়েজ (Load TDL) খুঁজুন
५. bags_column.tdl সিলেক্ট করুন এবং লোড করুন
```

**অথবা এই পদ্ধতিতে:**

```
१. Gateway of Tally
२. Ctrl+Alt+Shift+I (Import TDL)
३. bags_column.tdl সিলেক্ট করুন
४. Open ক্লিক করুন
```

---

### **ধাপ ५: Tally রিস্টার्ट করুন**

```
१. Tally সম্পূর्ण বন्द करुन (Alt+Q)
२. २-३ সেकেंड अपेक्षा করুন
३. Tally আবার খুলুন
```

---

## ✅ ইনস्टलेশन যাচাই করুন

### **চেকপয়েন्ট १: Purchase ভাউচার**

```
१. Gateway of Tally
२. F९ (Accounting Vouchers)
३. Purchase নির्वाचन करुน
४. नতुน ভाউचर खुलुन (Ctrl+A)
५. Item লাইনে "Bags" कॉलम देखুन
```

**যা দেখতে হবে:**
```
Item Name | Quantity | Bags | Rate | Amount
```

---

### **চেকপয়েন्ट २: Sales ভাউचার**

```
१. Gateway of Tally
२. F९ (Accounting Vouchers)
३. Sales नির्वाचन करुन
४. नতुন ভাউचер खुलुन
५. Item লাইনে "Bags" कॉलम দেখুন
```

---

### **চেকপয়েন्ट ३: Stock Journal ভাউচার**

```
१. Gateway of Tally
२. Alt+F७ (Inventory Vouchers)
३. Stock Journal नির्वाचन करुन
४. नতুন ভाউচर খुলুন
५. Item লাইনে "Bags" कॉलम দেখুন
```

---

## 🛠️ সমস्या সমाधान

### **সমस्या १: TDL লোড হচ્ছে না (Error 70005)**

**সমाধान:**
```
१. Tally.ini ফাইल খুলুন:
   Path: C:\Tally.ERP9\Tally.ini
   
२. এই লাইন যোগ করুন:
   [TDL]
   Path=Plugin\bags_column.tdl
   
३. ফাইল সংরক्षণ করুন
४. Tally রিস్్टার্ট করুন
```

---

### **সমस्या २: Bags কলাম দেখাচ્ছে না**

**সমাধান:**
```
१. Tally সম્पूর्ण बंद करुन
२. bags_column.tdl फाइल सही स्थानে आছে की नहीं चेक करুन
३. ফাइলের অनুमতি (Permission) चेक करুन
४. Tally আবার খুলুন
५. F१२ (Configure) থেকে TDL আবার লোড করুন
```

---

### **সमस्या ३: Multi-User Mode এ সমस्या**

**সমাधान:**
```
१. সার्भरে bags_column.tdl रাखুन:
   Path: Server_Tally_Folder\Plugin\
   
२. সभी ক्लायентে Tally रिस्टार्ट करুन
३. प्रत्येक ক्लायentsে F१२ থেকে TDL লোड করুন
```

---

## 📋 ডেটা এन्ट्री করার সময়

### **Purchase ভাউचারে Bags এন्ট्री:**

```
Item Name: চাল/গম
Quantity: १००  (কেজি বা মন)
Bags: २०      (ব্যাग সংख्या)
Rate: २००/कেজি
Amount: २०,०००
```

**মোট Bags স্বয়ংক्রিয়ভাবে গণনা হবে:**
```
Total Bags: २०
```

---

### **Sales ভাউচারে Bags এन्ट्री:**

```
Item Name: चाल
Quantity: ५०
Bags: १०
Rate: २५०/कেजी
Amount: १२,५००
```

---

### **Stock Journal ভাউচারে Bags এн्ट्री:**

```
Source Side (Consumption):
Item: चाल
Quantity: २५
Bags: ५

Destination Side (Production):
Item: चाल
Quantity: २५
Bags: ५
```

**মোট Bags উভয় পাশে দেখা যাবে:**
```
मोट ব্যाগ: ५
```

---

## 📊 Features (বৈশিষ्ট्য)

✅ **Purchase ভাউচারে Bags কলাম**
- Quantity এর পাশাপাশি Bags লিখুন
- Total Bags স্বয়ংক্রিয়ভাবে গণনা হবে

✅ **Sales ভাউচারে Bags কলাম**
- বিক্রয় পণ্যের Bags ট्র्যাক করুন
- Total Bags দেখুন

✅ **Stock Journal ভাউচারে Bags**
- Source এবং Destination দুই পাশে Bags এন्ট्री করুন
- Total Bags স্বয়ংক्রिय

✅ **স্বয়ংক्रिय গণনা**
- প्रत्येक লাইনের Bags যোগ হবে
- মোট Bags স্বয়ংক্রিয়ভাবে প्রদর্शিত হবে

---

## 📞 গুরুত्वपूর्ण নোট

### **UDF সिस्टেম:**
- Bags একটি **User Defined Field (UDF)** হিসেবে কাজ করে
- এটি Tally-এর নেটিভ সিস্টেম থেকে আলাদা
- Fixed conversion এর প্রয়োজন নেই

### **Compatibility:**
- Tally Prime 6.0 এবং উপরে কাজ করে
- Multi-User মোডে সাপোর्টেড

---

## ✨ সফল ইনস्टলেशন চিহ্ন

✅ Purchase ভাউচারে Bags কলাম আছে
✅ Sales ভাউচারে Bags কলাম আছে
✅ Stock Journal ভাউচারে Bags কলাম আছে
✅ Total Bags স্বয়ংক्রিয় গণনা হচ್ছে
✅ Bags ডেটা সংরक्षণ হচ્ছে

---

**ইনস्টলেশন সম्पन्न! ✨**

পরবর্তী: দেখুন [USAGE.md](./USAGE.md) ব्যবহারের জন्য বিস्তারिত নির्দেশনা

---

**संस्करण:** v२.० (Trae AI द्वारा তৈরি)
**আপডেট:** २०२६-०५-२२
````
