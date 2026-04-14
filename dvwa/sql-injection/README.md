# SQL Injection (DVWA)

---

## 🇬🇧 English

### Description
SQL Injection is a critical web application vulnerability that allows attackers to manipulate database queries and gain unauthorized access to sensitive data.

---

### Explanation
This vulnerability occurs because user input is directly embedded into SQL queries without proper sanitization or validation.

As a result, attackers can alter the query logic and execute arbitrary SQL commands, leading to unauthorized access, data leakage, or complete database compromise.

---

### Vulnerability Details
- Type: SQL Injection  
- Severity: High  
- Impact: Full database compromise  

---

### Payloads Used
- ' OR '1'='1'-- -
- ' UNION SELECT user, password FROM users-- -

---

### Exploitation Steps
1. Intercepted HTTP request using Burp Suite  
2. Identified vulnerable parameter (id)  
3. Tested basic payload (' OR '1'='1')  
4. Confirmed SQL Injection vulnerability  
5. Performed UNION-based injection  
6. Extracted usernames and password hashes from the database  

---

### Result
- Successfully bypassed authentication logic  
- Extracted multiple user records  
- Retrieved password hashes from database  

---

### Password Cracking
Identified MD5 hashed passwords and successfully cracked them using common wordlists.

Example:  
5f4dcc3b5aa765d61d8327deb882cf99 → password

---

### Impact
An attacker can extract sensitive data such as usernames and passwords, leading to full account takeover and database compromise.

---

### Tools Used
- Burp Suite  
- DVWA (Damn Vulnerable Web Application)  
- Kali Linux

- ## 📸 Proof of Exploitation

### SQL Injection Result (User Enumeration)
![SQL](sql.png)

### Database Dump (Credentials Extraction)
![DB](db.png)

### Burp Suite Request Manipulation
![Burp](burp.png)

### Password Cracking
![Hash](hash.png)

⚠️ All tests are performed in a controlled lab environment (DVWA).
---

## 🇹🇷 Türkçe

### Açıklama
SQL Injection, saldırganların veritabanı sorgularını manipüle ederek yetkisiz verilere erişmesini sağlayan kritik bir web güvenlik zafiyetidir.

---

### Detay
Bu zafiyet, kullanıcıdan alınan verinin herhangi bir filtreleme veya doğrulama yapılmadan SQL sorgularına dahil edilmesinden kaynaklanır.

Bu sayede saldırganlar sorgu mantığını değiştirerek hassas verilere erişebilir veya veritabanını tamamen ele geçirebilir.

---

### Zafiyet Detayları
- Tür: SQL Injection  
- Seviye: Yüksek  
- Etki: Veritabanının tamamen ele geçirilmesi  

---

### Kullanılan Payloadlar
- ' OR '1'='1'-- -  
- ' UNION SELECT user, password FROM users-- -  

---

### İstismar Adımları
1. Burp Suite ile HTTP isteği yakalandı  
2. Zafiyetli parametre (id) tespit edildi  
3. Temel payload (' OR '1'='1') test edildi  
4. SQL Injection zafiyeti doğrulandı  
5. UNION tabanlı saldırı gerçekleştirildi  
6. Veritabanından kullanıcı adı ve şifre hash'leri çekildi  

---

### Sonuç
- Kimlik doğrulama mantığı bypass edildi  
- Birden fazla kullanıcı verisi elde edildi  
- Veritabanından şifre hash'leri çekildi  

---

### Şifre Kırma
MD5 ile hashlenmiş şifreler tespit edildi ve yaygın wordlist kullanılarak çözüldü.

Örnek:  
5f4dcc3b5aa765d61d8327deb882cf99 → password  

---

### Etki
Saldırgan, kullanıcı adı ve şifre gibi hassas verileri ele geçirerek hesapları tamamen ele geçirebilir ve veritabanına tam erişim sağlayabilir.

---

### Kullanılan Araçlar
- Burp Suite  
- DVWA (Damn Vulnerable Web Application)  
- Kali Linux  

---

## 📸 Kanıtlar (İstismarın Kanıtı)

### SQL Injection Sonucu (Kullanıcı Listeleme)
![SQL](sql.png)

### Veritabanı Dump (Kimlik Bilgileri Çekimi)
![DB](db.png)

### Burp Suite İstek Manipülasyonu
![Burp](burp.png)

### Şifre Kırma
![Hash](hash.png)

---
  
⚠️ Tüm testler kontrollü bir lab ortamında (DVWA) gerçekleştirilmiştir.
