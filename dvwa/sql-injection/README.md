# SQL Injection (DVWA)

---

## 🇬🇧 English

### Description
SQL Injection allows attackers to retrieve and manipulate database data.

### Explanation

This vulnerability occurs because user input is not properly sanitized before being used in SQL queries.

As a result, attackers can manipulate the query structure and gain unauthorized access to the database.

### Vulnerability Details
- Type: SQL Injection
- Severity: High
- Impact: Full database access

### Payloads Used

- ' OR '1'='1
- UNION SELECT user, password FROM users

### Exploitation Steps
1. Intercepted request using Burp Suite
2. Modified parameter (id)
3. Injected SQL payload
4. Extracted user data
5. Used UNION SELECT to dump database

### Result
- Retrieved usernames
- Retrieved password hashes (MD5)

- ### Password Cracking

Identified MD5 hashed passwords and cracked them using common wordlists.

Example:
5f4dcc3b5aa765d61d8327deb882cf99 → password


---

## 📸 Evidence

### SQL Injection Result
![SQL](SQL%20injection.png)

### Database Dump
![DB](database_dump.png)

### Burp Suite Request
![Burp](burpsuite.png)

### Password Crack
![Hash](hash_karma.png)

---

⚠️ All tests are performed in a controlled lab environment (DVWA).
---

## 🇹🇷 Türkçe

### Açıklama
Bu zafiyet, kullanıcıdan alınan verinin SQL sorgularında kullanılmadan önce filtrelenmemesinden kaynaklanır.
Bu durum, saldırganların sorgu yapısını değiştirmesine ve veritabanına yetkisiz erişim sağlamasına imkan tanır.

### Zafiyet Detayları
- Tür: SQL Injection
- Seviye: Yüksek
- Etki: Tam veritabanı erişimi

### Kullanılan Payloadlar

- ' OR '1'='1
- UNION SELECT user, password FROM users

### Yapılan Adımlar
1. Burp Suite ile request yakalandı
2. Parametre değiştirildi
3. SQL payload enjekte edildi
4. Kullanıcı verileri çekildi
5. UNION SELECT ile veritabanı dump alındı

### Sonuç
- Kullanıcı adları elde edildi
- MD5 hash'li şifreler elde edildi

- ### Şifre Kırma

MD5 ile hashlenmiş şifreler tespit edildi ve yaygın wordlist kullanılarak çözüldü.

Örnek:
5f4dcc3b5aa765d61d8327deb882cf99 → password

---

## 📸 Kanıtlar

### SQL Injection Result
![SQL](SQL%20injection.png)

### Database Dump
![DB](database_dump.png)

### Burp Suite Request
![Burp](burpsuite.png)

### Password Crack
![Hash](hash_karma.png)

⚠️ All tests are performed in a controlled lab environment (DVWA).
