# Laboratorul 1
## Sarcina nr. 1. Analiza cererilor HTTP

### Răspundeți la următoarele întrebări:
1. Ce metodă HTTP a fost utilizată pentru a trimite cererea? 
POST

2. Ce anteturi au fost trimise în cerere?
``` 
Accept: */*
Accept-Encoding: gzip, deflate
Accept-Language: ru,en;q=0.9,ro;q=0.8
Connection: keep-alive
Content-Length: 37
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Host: sandbox.usm.md
Origin: http://sandbox.usm.md
Referer: http://sandbox.usm.md/login/
User-Agent:
Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/126.0.0.0 YaBrowser/24.7.0.0 Safari/537.36
X-Requested-With: XMLHttpRequest
```

3. Ce parametri au fost trimiși în cerere?
username: student
password: studentpass

4. Ce cod de stare a fost returnat de server?
Status Code: 401 Unauthorized

5. Ce anteturi au fost trimise în răspuns?
``` 
Connection: keep-alive
Content-Type: text/plain; charset=UTF-8
Date: Thu, 12 Sep 2024 08:54:40 GMT
Server: nginx/1.24.0 (Ubuntu)
Transfer-Encoding: chunked
```

6. Repetați pașii 3-5, introducând date corecte pentru autentificare (username: admin, password: password).

* Ce metodă HTTP a fost utilizată pentru a trimite cererea?

* Ce anteturi au fost trimise în cerere?
```  
Accept: */*
Accept-Encoding: gzip, deflate
Accept-Language: ru,en;q=0.9,ro;q=0.8
Connection: keep-alive
Content-Length: 32
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Host: sandbox.usm.md
Origin: http://sandbox.usm.md
Referer: http://sandbox.usm.md/login/
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/126.0.0.0 YaBrowser/24.7.0.0 Safari/537.36
X-Requested-With: XMLHttpRequest
```

* Ce parametri au fost trimiși în cerere?
```  
username: admin
password: password
```

* Ce cod de stare a fost returnat de server?
Status Code: 200 OK

* Ce anteturi au fost trimise în răspuns?
```   
Connection: keep-alive
Content-Type: text/plain; charset=UTF-8
Date: Thu, 12 Sep 2024 09:27:23 GMT
Server: nginx/1.24.0 (Ubuntu)
Transfer-Encoding: chunked
```

## Sarcina nr. 2. Crearea cererilor HTTP

1. Scrieți o cerere de tip GET către server la adresa http://sandbox.com, indicând în antetul User-Agent numele și prenumele dvs.
```   
GET / HTTP/1.1
Host: sandbox.com
User-Agent: Cibotaru Daniela
Connection: keep-alive
Content-Type: text/html; charset=UTF-8
```

2. Scrieți o cerere de tip POST către server la adresa http://sandbox.com/cars, indicând în corpul cererii următorii parametri:
- make: Toyota
- model: Corolla
- year: 2020
```  
POST /cars HTTP/1.1
Host: sandbox.com
Content-Type: application/x-www-form-urlencoded

make=Toyota&model=Corolla&year=2020
```

3. Scrieți o cerere de tip PUT către server la adresa http://sandbox.com/cars/1, indicând în antetul User-Agent numele și prenumele dvs., în antetul Content-Type valoarea application/json, iar în corpul cererii următorii parametri: json { "make": "Toyota", "model": "Corolla", "year": 2021 }
```   
PUT /cars HTTP/1.1
Host: sandbox.com
User-Agent: Cibotaru Daniela
Content-Type: application/json

{
 "make": "Toyota",
 "model": "Carolla",
 "year": "2021"
}
```
 
4. Scrieți unul dintre posibilele răspunsuri ale serverului la cererea anterioară. http POST /cars HTTP/1.1 
```
Host: sandbox.com 
Content-Type: application/json 
User-Agent: John Doe 
model=Corolla&make=Toyota&year=2020 
Presupuneți situațiile în care serverul poate returna codurile de stare HTTP 200, 201, 400, 401, 403, 404, 500.

HTTP/1.1 200 OK -cererea pprocesata cu succes
Content-Type: application/json

{
 "model": "Carolla",
 "make": "Toyota",
 "year": "2020"
}

HTTP/1.1 201 Created - cererea pprocesata cu succes + crearea unuei resurse noi

HTTP/1.1 400 Bad Request - serverul nu poate procesa cererea din cauza sintaxei gresite

HTTP/1.1 401 Unauthorized - autorizarea user-ului este necesara

HTTP/1.1 403 Forbidden - serverul nu permite accesul la resursa

HTTP/1.1 404 Not Found - sursa nu a fost gasita 

HTTP/1.1 500 Internal Server Error - serverul intampina o eroare la procesarea solicitarii

```

5. Scrieți o cerere de tip DELETE la alegerea dvs. și să explicați de ce, în acest caz, este potrivit să utilizați metoda DELETE.

```
DELETE /cars/89 HTTP/1.1
Host: 999.md
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.3
Connection: keep-alive
Content-Type: application/json
```

Am utilizat DELETE in acest caz pentru a sterge concret car 89 de pe pagina cars de pe pagina host: 999.md. Doar metoda DELETE poate sa stearga atat cateva elemente, cat si pagini dupa conditii.


## Sarcina nr. 3

1. Congratulations, Cibotaru Daniela! You have successfully completed the quest! Here is your secret: KiUNGREoERBsJRUaDEQFLUJEVQ==
2. secret: KiUNGREoERBsJRUaDEQFLUJEVQ==