# SQL Injection (DVWA)

---

## 🇬🇧 English

### Description
SQL Injection is a web vulnerability that allows attackers to manipulate database queries and access unauthorized data.

---

### Explanation
This vulnerability occurs because user input is directly included in SQL queries without proper sanitization.

As a result, attackers can modify the query structure and execute malicious SQL commands to retrieve sensitive information.

---

### Vulnerability Details
- Type: SQL Injection
- Severity: High
- Impact: Full database compromise

---

### Payloads Used
- ' OR '1'='1
- UNION SELECT user, password FROM users

---

### Exploitation Steps
1. Intercepted HTTP request using Burp Suite  
2. Identified vulnerable parameter (id)  
3. Injected SQL payload  
4. Retrieved multiple user records  
5. Used UNION SELECT to extract database contents  

---

### Result
- Successfully extracted user data  
- Retrieved password hashes  
- Demonstrated database access  

---

### Password Cracking
Identified MD5 hashed passwords and successfully cracked them using common wordlists.

Example:  
5f4dcc3b5aa765d61d8327deb882cf99 → password  

---

### Impact
An attacker can extract sensitive data such as usernames and passwords, leading to full account compromise.

---

### Tools Used
- Burp Suite  
- DVWA  
- Kali Linux  

---

## 📸 Evidence (Proof of Exploitation)

### SQL Injection Result (User Enumeration)
![SQL](sql.png)

### Database Dump (Credentials Extraction)
![DB](db.png)

### Burp Suite Request Manipulation
![Burp](burp.png)

### Password Cracking
![Hash](hash.png)

---

⚠️ All tests are performed in a controlled lab environment (DVWA).
---

## 🇹🇷 Türkçe

### Açıklama
SQL Injection, saldırganların veritabanı sorgularını manipüle ederek yetkisiz verilere erişmesini sağlayan bir zafiyettir.

---

### Detay
Bu zafiyet, kullanıcıdan alınan verinin filtrelenmeden SQL sorgularına dahil edilmesinden kaynaklanır.

Bu sayede saldırganlar sorgu yapısını değiştirerek hassas bilgilere erişebilir.

---

### Zafiyet Detayları
- Tür: SQL Injection  
- Seviye: Yüksek  
- Etki: Veritabanının tamamen ele geçirilmesi  

---

### Kullanılan Payloadlar
- ' OR '1'='1  
- UNION SELECT user, password FROM users  

---

### İstismar Adımları
1. Burp Suite ile HTTP isteği yakalandı  
2. Zafiyetli parametre (id) tespit edildi  
3. SQL payload enjekte edildi  
4. Birden fazla kullanıcı verisi çekildi  
5. UNION SELECT ile veritabanı içeriği alındı  

---

### Sonuç
- Kullanıcı verileri başarıyla çekildi  
- Şifre hash'leri elde edildi  
- Veritabanına erişim sağlandı  

---

### Şifre Kırma
MD5 ile hashlenmiş şifreler tespit edildi ve yaygın wordlist kullanılarak çözüldü.

Örnek:  
5f4dcc3b5aa765d61d8327deb882cf99 → password  

---

### Etki
Saldırgan kullanıcı adı ve şifre gibi hassas verileri ele geçirerek hesapları tamamen ele geçirebilir.

---

### Kullanılan Araçlar
- Burp Suite  
- DVWA  
- Kali Linux  

---

## 📸 Evidence (Proof of Exploitation)

### SQL Injection Result (User Enumeration)
SQL

### Database Dump (Credentials Extraction)
DB

### Burp Suite Request Manipulation
Burp

### Password Cracking
Hash

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
--- 
