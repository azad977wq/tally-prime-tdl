````markdown
# Tally Prime 6.0 - Bags Column ইনস্টলেশন গাইড

## 📥 কিভাবে ইনস্টল করবেন?

### **ধাপ ১: TDL ফাইল ডাউনলোড করুন**

```
GitHub রিপোজিটরি থেকে bags_column.tdl ফাইল ডাউনলোড করুন:
https://github.com/azad977wq/tally-prime-tdl
```

**অথবা:**
- Code → Download ZIP ক্লিক করুন
- ZIP ফাইল এক্সট্র্যাক্ট করুন
- `bags_column.tdl` ফাইলটি খুঁজে নিন

---

### **ধাপ २: Tally প্রোগ্রাম বন্ধ করুন**

```
⚠️ গুরুত্বপূর্ণ: সমস্ত Tally প্রসেস বন্ধ করুন
- Multi-User Mode বন্ধ করুন
- Tally সম্পূর্ণভাবে বন্ধ করুন
```

---

### **ধাপ ३: TDL ফাইল কপি করুন**

#### **Windows এ লোকেশন:**

**Tally Prime ইনস্টলেশন ফোল্ডার খুঁজুন:**
- সাধারণত: `C:\Tally.ERP9\`
- বা: `C:\Program Files\Tally.ERP9\`

**একাধিক পথ চেষ্টা করুন:**

```
C:\Tally.ERP9\Plugin\bags_column.tdl
C:\Program Files\Tally.ERP9\Plugin\bags_column.tdl
C:\Program Files (x86)\Tally.ERP9\Plugin\bags_column.tdl
```

**Plugin ফোল্ডার না থাকলে:**
```
१. Tally.ERP9 ফোল্ডারে যান
२. নতুন ফোল্ডার তৈরি করুন: Plugin
३. bags_column.tdl সেখানে রাখুন
```

---

### **ধাপ ४: TDL ফাইল যোগ করুন Tally-তে**

```
१. Tally Prime খুলুন
२. Gateway of Tally → F12 (Configure)
३. নির্বাচন করুন: Load TDL

অথবা:

१. Gateway of Tally
२. Ctrl+Alt+Shift+I (Import TDL)
३. bags_column.tdl সিলেক্ট করুন
```

---

### **ধাপ ५: Tally রিস্টার্ট করুন**

```
१. Tally বন্ধ করুন (সম্পূর্ণভাবে)
२. २-३ সেকেন্ড অপেক্ষা করুন
३. Tally আবার খুলুন
```

---

## ✅ ইনস্টলেশন যাচাই করুন

### **চেকপয়েন্ট १: Bags কলাম যাচাই করুন**

**Purchase ভাউচারে:**
```
१. Gateway of Tally
२. Accounting Vouchers → Purchase
३. নতুন ভাউচার খুলুন (Ctrl+A)
४. পণ্য লাইনে "Bags" কলাম দেখুন
```

**Sales ভাউচারে:**
```
१. Gateway of Tally
२. Accounting Vouchers → Sales
३. নতুন ভাউচার খুলুন (Ctrl+A)
४. পণ্য লাইনে "Bags" কলাম দেখুন
```

**Stock Journal ভাউচারে:**
```
१. Gateway of Tally
२. Inventory Vouchers → Stock Journal
३. নতুন ভাউচার খুলুন (Ctrl+A)
४. পণ্য লাইনে "Bags" কলাম দেখুন
```

---

### **চেকপয়েন্ট २: Godown Summary রিপোর্ট চেক করুন**

```
१. Gateway of Tally
२. Display → Inventory Books
३. Godowns → Godown Summary
४. নতুন কলাম "Bags" দেখুন (Opening, Inward, Outward, Closing)
```

---

## 🛠️ সমস্যা সমাধান

### **সমস্যা १: Bags কলাম দেখাচ্ছে না**

**সমাধান:**
```
१. Tally সম্পূর্ণ বন্ধ করুন
२. bags_column.tdl ফাইলটি সঠিক স্থানে আছে কিনা চেক করুন
३. ফাইলের অনুমতি (Permission) চেক করুন
४. Tally আবার খুলুন
५. F२ চেষ্টা করুন (Company Data)
```

---

### **সমস্যা २: TDL লোড হচ্ছে না**

**সমাধান:**
```
१. Tally.ini ফাইল চেক করুন:
   Location: C:\Tally.ERP9\
   
२. এই লাইন যোগ করুন:
   [LoadTDL]
   १=bags_column.tdl
   
३. Tally রিস্টার্ট করুন
```

---

### **সমস্যা ३: Multi-User Mode এ সমস্যা**

**সমাধান:**
```
१. সার্ভারে bags_column.tdl রাখুন
   Path: Server_Tally_Folder\Plugin\
   
२. সমস্ত ক্লায়েন্টে Tally রিস্টার্ট করুন
```

---

## 📋 ডেটা এন্ট্রি করার সময়

### **Bags কলামে ডেটা কিভাবে এন্টার করবেন:**

**Purchase ভাউচারে:**
```
Item Name: Wheat (গম)
Item Quantity: १०० (একক: কেজি)
Bags: ५ (ব্যাগ সংখ্যা)
```

**Sales ভাউচারে:**
```
Item Name: Wheat (গম)
Item Quantity: ५० (একক: কেজি)
Bags: २ (ব্যাগ সংখ্যা)
```

**Stock Journal ভাউচারে:**
```
Item Name: Wheat (গম)
Item Quantity: २५ (একক: কেজি)
Bags: १ (ব্যাগ সংখ्या)
```

---

## 📊 Godown Summary রিপোর্ট দেখুন

```
१. Gateway of Tally
२. Display → Inventory Books
३. Godowns → Godown Summary
४. "Godown Summary with Bags" সিলেক্ট করুন
५. রিপোর্টে Bags কলাম দেখুন:
   - Opening Bags
   - Inward Bags
   - Outward Bags
   - Closing Bags
```

---

## 🔄 আপডেট করা হলে

নতুন সংস্করণ ডাউনলোড করে:
```
१. পুরনো bags_column.tdl মুছে দিন
२. নতুন ফাইল কপি করুন
३. Tally রিস্টার্ট করুন
```

---

## 📞 সাপোর্ট টিপস

**Tally Log File দেখুন:**
```
Location: C:\Tally.ERP9\
File: Tally_Error.log
```

**কনফিগারেশন ফাইল:**
```
Location: C:\Tally.ERP9\
File: Tally.ini
```

---

## ✨ সফল ইনস্টলেশন অনুভব করবেন যখন:

✅ Purchase ভাউচারে Bags কলাম দেখা যাবে
✅ Sales ভাউচারে Bags কলাম দেখা যাবে
✅ Stock Journal ভাউচারে Bags কলাম দেখা যাবে
✅ Godown Summary রিপোর্টে Bags তথ্য দেখা যাবে
✅ ডেটা সংরক্ষণ হবে সঠিকভাবে

---

**ইনস্টলেশন সম্পন্ন! ✨**

পরবর্তী: দেখুন [USAGE.md](./USAGE.md) ব্যবহারের জন্য বিস্তারিত নির্দেশনা
````
