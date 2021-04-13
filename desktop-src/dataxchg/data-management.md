---
title: Управление данными
description: В этом разделе описано, как объекты памяти передают данные из одного приложения в другое.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Пользовательский интерфейс Windows, платформа динамических данных Exchange (DDE)
- Платформа динамических данных Exchange (DDE), управление данными
- DDE (платформа динамических данных Exchange), управление данными
- Обмен данными, платформа динамических данных Exchange (DDE)
- Пользовательский интерфейс Windows, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), управление данными
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), управление данными
- Обмен данными, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
- Платформа динамических данных Exchange (DDE), объекты
- DDE (платформа динамических данных Exchange), объекты
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), объекты
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc5178f636cf4b75111d4fc48e17fd144400a91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411410"
---
# <a name="data-management"></a>Управление данными

Поскольку платформа динамических данных Exchange (DDE) использует объекты памяти для передачи данных из одного приложения в другое, платформа динамических данных Библиотека управления Exchange (ДДЕМЛ) предоставляет набор функций, которые приложения DDE могут использовать для создания объектов DDE и управления ими.

Все транзакции, включающие обмен данными, требуют, чтобы приложение, предоставляя данные, создали локальный буфер, содержащий данные, а затем вызывал функцию [**ддекреатедатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) . Эта функция выделяет объект DDE, копирует данные из буфера в объект и возвращает маркер данных. Маркер данных — это значение **типа DWORD** , которое ддемл использует для предоставления доступа к данным в объекте DDE. Чтобы предоставить общий доступ к данным в объекте DDE, приложение передает этот обработчик данных в ДДЕМЛ, а ДДЕМЛ передает его функции обратного вызова DDE приложения, получающего транзакцию данных.

В следующем примере показано, как создать объект DDE и получить маркер для объекта. Во время транзакции [**кстип \_ Адврек**](xtyp-advreq.md) функция обратного вызова Преобразует текущее время в строку ASCII, копирует строку в локальный буфер, а затем создает объект DDE, содержащий строку. Функция обратного вызова возвращает маркер объекта DDE (ХДДЕДАТА) в ДДЕМЛ, который передает этот обработчик клиентскому приложению.


```
typedef struct tagTIME 
{ 
    INT     hour;   // 0 - 11 hours for analog clock 
    INT     hour12; // 12-hour format 
    INT     hour24; // 24-hour format 
    INT     minute; 
    INT     second; 
    INT     ampm;   // 0 - AM , 1 - PM 
} TIME; 
 
HDDEDATA EXPENTRY DdeCallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
 
    CHAR szBuf[32];
    HRESULT hResult;
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uType) 
    { 
    case XTYP_ADVREQ: 
        if ((hsz1 == hszTime && hsz2 == hszNow) && 
                (uFmt == CF_TEXT)) 
        { 
            // Copy the formatted string to a buffer. 
 
            itoa(tmTime.hour, szBuf, 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.minute < 10)
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
                if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            } 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.minute, &szBuf[*pcch], 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.second < 10) 
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.second, &szBuf[*pcch], 10);
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            } 
            szBuf[*pcch] = '\0'; 
 
            // Create a global object and return its data handle. 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            return (DdeCreateDataHandle( 
                idInst, 
                (LPBYTE) szBuf,     // instance identifier 
                *pcch + 1,          // source buffer length 
                0,                  // offset from beginning 
                hszNow,             // item name string 
                CF_TEXT,            // clipboard format 
                0));                // no creation flags 
        } else return (HDDEDATA) NULL; 
 
    // Process other transactions. 
    } 
} 
```



Принимающее приложение получает указатель на объект DDE, передавая ему обработчик данных в функцию [**ддеакцессдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) . Указатель, возвращенный **ддеакцессдата** , предоставляет доступ только для чтения. Приложение должно использовать указатель для просмотра данных, а затем вызывать функцию [**ддеунакцессдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) , чтобы сделать указатель недействительным. Приложение может копировать данные в локальный буфер с помощью функции [**ддежетдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) .

В следующем примере получается указатель на объект DDE, определенный параметром *хдата* , копирует содержимое в локальный буфер, а затем делает недействительным указатель.


```
HDDEDATA hdata; 
LPBYTE lpszAdviseData; 
DWORD cbDataLen; 
DWORD i; 
char szData[32]; 
 
// 
case XTYP_ADVDATA: 
    lpszAdviseData = DdeAccessData(hdata, &cbDataLen); 
    for (i = 0; i < cbDataLen; i++) 
        szData[i] = *lpszAdviseData++; 
    DdeUnaccessData(hdata); 
    return (HDDEDATA) TRUE; 
//
```



Как правило, когда приложение, создавшее маркер данных, передает этот обработчик в ДДЕМЛ, этот обработчик станет недопустимым в создаваемом приложении. Такая ситуация не является проблемой, если приложение должно обмениваться данными только с одним приложением. Если приложение должно совместно использовать одни и те же данные с несколькими приложениями, то при создании приложения следует указать \_ флаг хдата апповнед в [**ддекреатедатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle). Это дает право владения объектом DDE созданию приложения и предотвращает недействительность ДДЕМЛ. После этого приложение может передавать обработку данных в любое количество раз после вызова **ддекреатедатахандле** только один раз.

Если в приложении указан флаг ХДАТА \_ апповнед в параметре *афкмд* [**ддекреатедатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), он должен вызвать функцию [**ддефридатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) , чтобы освободить маркер памяти, независимо от того, передан ли этот обработчик в ддемл. Перед завершением приложение должно вызвать **ддефридатахандле** , чтобы освободить любой созданный им обработчик данных, но он не был передан в ддемл.

Приложение, которое еще не прошло обработку объекта DDE в ДДЕМЛ, может добавлять данные в объект или перезаписывать данные в объект с помощью функции [**ддеадддата**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) . Как правило, приложение использует **ддеадддата** для заполнения неинициализированного объекта DDE. После того как приложение передаст обработчик данных в ДДЕМЛ, объект DDE, идентифицируемый этим маркером, изменить нельзя. его можно освободить только.

 

 




