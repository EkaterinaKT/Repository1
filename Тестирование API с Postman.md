# Тестирование API https://fakerestapi.azurewebsites.net/index.html с Postman 

# Activities

#### Activities: получение списка активностей GET ​/api​/v1​/Activities (200)

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities
- Ожидаемый результат: статус-код ответа: 200 ОК
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3f443090-dfab-4169-95a5-53e605c469fa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутствует
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 20:16:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа: 
```
 {
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-06-20T21:32:35.1095222+00:00",
        "completed": false
    },
```

#### Activities: отправка списка активностей POST ​/api​/v1​/Activities (201)

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities
- Ожидаемый результат: статус-код ответа: 201 Created
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3f443090-dfab-4169-95a5-53e605c469fa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: 
```
{
 "id": 0,
 "title": "string",
 "dueDate": "2023-06-17T08:46:41.648Z",
 "completed": true
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 20:16:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа: 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-17T08:46:41.648Z",
    "completed": true
}
```

#### Activities: отправка списка активностей POST ​/api​/v1​/Activities (400) некорректный JSON

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3f443090-dfab-4169-95a5-53e605c469fa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": 0
 "title": "string"
 "dueDate": "2023-06-17T08:46:41.648Z",
 "completed": true
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 20:16:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-9f21b35c15959646a6cb8bc58fdda9fe-dcc74baeb70fb64f-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 4 | BytePositionInLine: 1."
        ]
    }
}
```
#### Activities: отправка списка активностей POST ​/api​/v1​/Activities (400) id некорректный


- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities
- Ожидаемый результат: статус-код ответа: 400  Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 795f1557-7355-4227-9864-7896eea14fe2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{activity_id}},
 "title": "string",
 "dueDate": "2023-06-17T11:56:31.897Z",
 "completed": true
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 20:45:57 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e0253f2735f2184d9e3c042a3ea3d039-12bd54707a98f842-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 17."
        ]
    }
}
```

#### Activities: отправка списка активностей POST ​/api​/v1​/Activities (400) пустой запрос

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities
- Ожидаемый результат: статус-код ответа: 400  Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 795f1557-7355-4227-9864-7896eea14fe2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутствует
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 20:45:57 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-61fe57a59fa65449ae5243f1aaf1ffda-630d2e1db238414d-00"
}
```

#### Activities: отправка списка активностей POST ​/api​/v1​/Activities (400) id -1

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 795f1557-7355-4227-9864-7896eea14fe2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{minus}} ,
 "title": "string",
 "dueDate": "2023-06-17T08:46:41.648Z",
 "completed": true
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 20:45:57 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "id": -1,
    "title": "string",
    "dueDate": "2023-06-17T08:46:41.648Z",
    "completed": true
}
```

#### Activities: получение определенной активности GET ​/api​/v1​/Activities​/{1} (200)

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{ID (+)}}
- Ожидаемый результат: статус-код ответа: 200 ОК
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6505d36d-7d4d-4b8b-9a96-bb387715213b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутствует
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 21:03:00 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-06-20T22:03:00.775398+00:00",
    "completed": false
}
```
#### Activities: получение определенной активности GET ​/api​/v1​/Activities​/{9999999999} (400) id некорректный

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: db98947a-45e8-43fe-83af-e7e9b0014625
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсу3тствует
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 21:20:21 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-7964dfa972886e46bd5d854d4cc310ce-20fc4e941ce8e74c-00",
    "errors": {
        "id": [
            "The value '9999999999' is not valid."
        ]
    }
}
```

####
- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{minus}}
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a1cbd65d-fe45-4c8a-907a-66b3b0cf40fe
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутствует
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 21:26:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-5752157051b7e2488092d7a44364b6d5-c8798f6f854ada49-00"
}
```

#### Activities: изменение активности PUT ​/api​/v1​/Activities​/{1} (200)
- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{ID (+)}}
- Ожидаемый результат: статус-код ответа: 200 ОК
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: fc361238-72e1-4843-b2c7-c8f73dde3656
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{ID (+)}},
 "title": "string",
 "dueDate": "2023-06-18T11:46:43.228Z",
 "completed": true
}
```
- Заголовки ответа:
```Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 21:32:42 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 1,
    "title": "string",
    "dueDate": "2023-06-18T11:46:43.228Z",
    "completed": true
}
```

#### Activities: изменение активности PUT ​/api​/v1​/Activities​/{1} (400) некорректный JSON

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{ID (+)}}
- Ожидаемый результат: 
статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ae498e64-f6f3-47d2-ada2-6ad35ccacc80
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{ID (+)}},
 "title": "",
 "dueDate": "2023-06-18T11:46:43.228Z",
 "completed":
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 21:35:57 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-286f7db2df3dd645a3b00a6fe0973e5f-b872901afcf92e44-00",
    "errors": {
        "$.completed": [
            "'}' is an invalid start of a value. Path: $.completed | LineNumber: 10 | BytePositionInLine: 0."
        ]
    }
}
```

#### Activities: изменение активности PUT ​/api​/v1​/Activities​/{9999999999} (400) id некорректный

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}
- Ожидаемый результат: 
статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: d6d8f9ae-3f61-4e79-be37-db63806dc247
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{activity_id}},
 "title": "string",
 "dueDate": "2023-06-18T12:19:53.920Z",
 "completed": true
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 21:41:31 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-90bc519f1be81847bf559a6f786dcb6a-3c1d0ca06b100048-00",
    "errors": {
        "id": [
            "The value '9999999999' is not valid."
        ]
    }
}
```

#### Activities: изменение активности PUT ​/api​/v1​/Activities​/{1} (400) пустой запрос

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{ID (+)}}
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 92a63f60-e67f-45d7-af8b-b410b1b6a966
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутствует
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 21:44:00 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-ea192ce01e7a86479c2ec46624d749b6-3bcaefdf1a2afa42-00"
}
```

#### Activities: изменение активности PUT ​/api​/v1​/Activities​/{-1} (400) id -1

- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{minus}}
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ca0f07bc-add0-4bd7-b201-2f982c9530c7
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{minus}},
 "title": "string",
 "dueDate": "2023-06-18T12:19:53.920Z",
 "completed": true
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 21:55:40 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": -1,
    "title": "string",
    "dueDate": "2023-06-18T12:19:53.92Z",
    "completed": true
}
```

#### Activities: удаление активности DELETE ​/api​/v1​/Activities​​/{1} (200)
- URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{ID (+)}}
- Ожидаемый результат: статус-код ответа: 200 ОК
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ff1adc00-215d-4f04-a6a9-c3179c84ebeb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутствует
- Заголовки ответа:
```
Content-Length: 0
Date: Tue, 20 Jun 2023 21:57:48 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа: отсутствует


# Users

#### Users: получение списка пользователей GET ​/api​/v1​/Users (200)

- URL: https://fakerestapi.azurewebsites.net/api/v1/Users
- Ожидаемый результат: статус-код ответа: 200 ОК
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 4a8d4598-c70c-41cb-adb7-077bb3b556ba
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутствует
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 22:03:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
[
    {
        "id": 1,
        "userName": "User 1",
        "password": "Password1"
    },
```

#### Users: получение списка пользователей POST ​/api​/v1​/Users (201)

- URL: https://fakerestapi.azurewebsites.net/api/v1/Users
- Ожидаемый результат: статус-код ответа: 201 Created
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 82ceeec1-f972-4f24-9ba8-52395a38b570
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": 0,
 "userName": "string",
 "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 22:06:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 0,
    "userName": "string",
    "password": "string"
}
```

#### Users: отправка списка пользователей POST ​/api​/v1​/Users (400) некорректный JSON

- URL: https://fakerestapi.azurewebsites.net/api/v1/Users
- Ожидаемый результат: статус-код ответа:400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 14a4bb98-cd54-4388-a27e-b9e8dfe8f898
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": 0
 "userName": "string"
 "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 22:09:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-eb3991caf1d5654a816884e02bce8e00-0066f0a44a448647-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 4 | BytePositionInLine: 1."
        ]
    }
}
```

#### Users: отправка списка пользователей POST ​/api​/v1​/Users (400) некорректный id

- URL: https://fakerestapi.azurewebsites.net/api/v1/Users
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7b8ea9e6-f2b6-4667-8f71-144590a3fae4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{activity_id}},
 "userName": "string",
 "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 22:13:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-149135b83d84654685d6852a4040554a-763dc926d44ff04e-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 17."
        ]
    }
}
```

#### Users: отправка списка пользователей POST ​/api​/v1​/Users (400) пустой запрос

- URL: https://fakerestapi.azurewebsites.net/api/v1/Users
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 5830b415-1e64-4cd8-a0a8-765c2ffa0b89
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутсвует 
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 22:15:27 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-a293d70954707a4ea4547ed07c19b15b-75415f16c1274840-00"
}
```

#### Users: отправка списка пользователей POST ​/api​/v1​/Users (400) id -1

- URL: https://fakerestapi.azurewebsites.net/api/v1/Users
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: d0b82bae-2ccc-4906-93fe-214ab11268c2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{minus}},
 "userName": "string",
 "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 22:20:38 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": -1,
    "userName": "string",
    "password": "string"
}
```

#### Users: получение определенного пользователя GET ​/api​/v1​/Users​/{1} (200)

- URL: https://fakerestapi.azurewebsites.net/api/v1/Users/{{ID (+)}}
- Ожидаемый результат: 
статус-код ответа: 200 ОК
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: be64a33d-b942-40f1-8e30-4824c5ac968a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутсвует
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 22:22:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
}
```

#### Users: получение определенного пользователя GET ​/api​/v1​/Users​/{9999999999} (400) некорректный id


- URL: https://fakerestapi.azurewebsites.net/api/v1/Users/{{activity_id}}
- Ожидаемый результат: 
статус-код ответа:  400 Error: Bad Request
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3a30f1f7-4eb8-425e-9a7b-0ce53441657b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутсвует
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 22:24:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b01c876347656845a94397916f211ff6-c27d059a05c27542-00",
    "errors": {
        "id": [
            "The value '9999999999' is not valid."
        ]
    }
}
```

####  Users: получение определенного пользователя GET ​/api​/v1​/Users​/{-1} (400) id -1

- URL: https://fakerestapi.azurewebsites.net/api/v1/Users/{{minus}}
- Ожидаемый результат: статус-код ответа:  400 Error: Bad Request
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a77aceee-9a87-419f-b5ba-31dad5c2af11
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутсвует
- Заголовки ответа:
```Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 22:26:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-404ebba1d6d2e44fbdef89878883c2d8-3c9ad78619f19e4b-00"
}
```

#### 
Users: изменение пользователей PUT ​/api​/v1​/Users​/{1} (200)

- URL: https://fakerestapi.azurewebsites.net/api/v1/Users/{{ID (+)}}
- Ожидаемый результат: статус-код ответа: 200 ОК
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: d539275e-0a7e-423e-9409-7573eb50a201
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{ID (+)}},
 "userName": "string",
 "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 22:28:44 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 1,
    "userName": "string",
    "password": "string"
}
```

#### Users: изменение пользователей PUT ​/api​/v1​/Users​/{1} (400) некорректный JSON


- URL:https://fakerestapi.azurewebsites.net/api/v1/Users/{{ID (+)}}
- Ожидаемый результат: 
статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b44dd5e6-a846-44a5-ac89-9c9b79dd7553
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": 0
 "userName": 
 "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 22:31:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-bcecadd641eda8498f4c7b624bd43a0e-d81129b03edaae4e-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 4 | BytePositionInLine: 1."
        ]
    }
}
```

#### Users: изменение пользователей PUT ​/api​/v1​/Users​/{9999999999} (400) id некорректный

- URL: https://fakerestapi.azurewebsites.net/api/v1/Users/{{activity_id}}
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b993850c-5734-4f7b-8828-a34d138006aa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{activity_id}},
 "userName": "string",
 "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 22:33:37 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-1b084ce002b381429f9441f5e085502b-171006199d72fd47-00",
    "errors": {
        "id": [
            "The value '9999999999' is not valid."
        ],
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 17."
        ]
    }
}
```

#### Users: изменение пользователей PUT ​/api​/v1​/Users​/{1} (400) пустой запрос


- URL: https://fakerestapi.azurewebsites.net/api/v1/Users/{{ID (+)}}
- Ожидаемый результат: статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 2c182f6e-9658-4424-b335-99e953d5f8cc
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутствует
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 20 Jun 2023 22:36:07 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-b6d18f518698f54996d3afaf1347d616-20da45f593b83b4b-00"
}
```

#### Users: изменение пользователей PUT ​/api​/v1​/Users​/{-1} (400) id -1


- URL: https://fakerestapi.azurewebsites.net/api/v1/Users/{{minus}}
- Ожидаемый результат: 
статус-код ответа: 400 Error: Bad Request
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 625ede76-cfde-450a-9b25-5dd4ed301d59
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
 "id": {{minus}},
 "userName": "string",
 "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 20 Jun 2023 22:37:41 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": -1,
    "userName": "string",
    "password": "string"
}
```

#### Users: удаление пользователей DELETE ​/api​/v1​/Users​/{1} (200)


- URL: https://fakerestapi.azurewebsites.net/api/v1/Users/{{ID (+)}}
- Ожидаемый результат: статус-код ответа: 200 ОК
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: c9bf62e0-ab89-4298-bbf9-1ec90f75396d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутсвует
- Заголовки ответа:
```
Content-Length: 0
Date: Tue, 20 Jun 2023 22:39:34 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа: отсутсвует

