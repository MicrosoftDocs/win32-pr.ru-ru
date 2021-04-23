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
# <a name="data-management"></a><span data-ttu-id="1c7ef-115">Управление данными</span><span class="sxs-lookup"><span data-stu-id="1c7ef-115">Data Management</span></span>

<span data-ttu-id="1c7ef-116">Поскольку платформа динамических данных Exchange (DDE) использует объекты памяти для передачи данных из одного приложения в другое, платформа динамических данных Библиотека управления Exchange (ДДЕМЛ) предоставляет набор функций, которые приложения DDE могут использовать для создания объектов DDE и управления ими.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-116">Because Dynamic Data Exchange (DDE) uses memory objects to pass data from one application to another, the Dynamic Data Exchange Management Library (DDEML) provides a set of functions that DDE applications can use to create and manage DDE objects.</span></span>

<span data-ttu-id="1c7ef-117">Все транзакции, включающие обмен данными, требуют, чтобы приложение, предоставляя данные, создали локальный буфер, содержащий данные, а затем вызывал функцию [**ддекреатедатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) .</span><span class="sxs-lookup"><span data-stu-id="1c7ef-117">All transactions that involve the exchange of data require the application supplying the data to create a local buffer containing the data and then to call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function.</span></span> <span data-ttu-id="1c7ef-118">Эта функция выделяет объект DDE, копирует данные из буфера в объект и возвращает маркер данных.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-118">This function allocates a DDE object, copies the data from the buffer to the object, and returns a data handle.</span></span> <span data-ttu-id="1c7ef-119">Маркер данных — это значение **типа DWORD** , которое ддемл использует для предоставления доступа к данным в объекте DDE.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-119">A data handle is a **DWORD** value that the DDEML uses to provide access to data in the DDE object.</span></span> <span data-ttu-id="1c7ef-120">Чтобы предоставить общий доступ к данным в объекте DDE, приложение передает этот обработчик данных в ДДЕМЛ, а ДДЕМЛ передает его функции обратного вызова DDE приложения, получающего транзакцию данных.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-120">To share the data in a DDE object, an application passes the data handle to the DDEML, and the DDEML passes the handle to the DDE callback function of the application that is receiving the data transaction.</span></span>

<span data-ttu-id="1c7ef-121">В следующем примере показано, как создать объект DDE и получить маркер для объекта.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-121">The following example shows how to create a DDE object and obtain a handle to the object.</span></span> <span data-ttu-id="1c7ef-122">Во время транзакции [**кстип \_ Адврек**](xtyp-advreq.md) функция обратного вызова Преобразует текущее время в строку ASCII, копирует строку в локальный буфер, а затем создает объект DDE, содержащий строку.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-122">During the [**XTYP\_ADVREQ**](xtyp-advreq.md) transaction, the callback function converts the current time to an ASCII string, copies the string to a local buffer, and then creates a DDE object that contains the string.</span></span> <span data-ttu-id="1c7ef-123">Функция обратного вызова возвращает маркер объекта DDE (ХДДЕДАТА) в ДДЕМЛ, который передает этот обработчик клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-123">The callback function returns the handle to the DDE object (HDDEDATA) to the DDEML, which passes the handle to the client application.</span></span>


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



<span data-ttu-id="1c7ef-124">Принимающее приложение получает указатель на объект DDE, передавая ему обработчик данных в функцию [**ддеакцессдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) .</span><span class="sxs-lookup"><span data-stu-id="1c7ef-124">The receiving application obtains a pointer to the DDE object by passing the data handle to the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function.</span></span> <span data-ttu-id="1c7ef-125">Указатель, возвращенный **ддеакцессдата** , предоставляет доступ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-125">The pointer returned by **DdeAccessData** provides read-only access.</span></span> <span data-ttu-id="1c7ef-126">Приложение должно использовать указатель для просмотра данных, а затем вызывать функцию [**ддеунакцессдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) , чтобы сделать указатель недействительным.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-126">The application should use the pointer to review the data and then call the [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) function to invalidate the pointer.</span></span> <span data-ttu-id="1c7ef-127">Приложение может копировать данные в локальный буфер с помощью функции [**ддежетдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) .</span><span class="sxs-lookup"><span data-stu-id="1c7ef-127">The application can copy the data to a local buffer by using the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function.</span></span>

<span data-ttu-id="1c7ef-128">В следующем примере получается указатель на объект DDE, определенный параметром *хдата* , копирует содержимое в локальный буфер, а затем делает недействительным указатель.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-128">The following example obtains a pointer to the DDE object identified by the *hData* parameter, copies the contents to a local buffer, and then invalidates the pointer.</span></span>


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



<span data-ttu-id="1c7ef-129">Как правило, когда приложение, создавшее маркер данных, передает этот обработчик в ДДЕМЛ, этот обработчик станет недопустимым в создаваемом приложении.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-129">Usually, when an application that created a data handle passes that handle to the DDEML, the handle becomes invalid in the creating application.</span></span> <span data-ttu-id="1c7ef-130">Такая ситуация не является проблемой, если приложение должно обмениваться данными только с одним приложением.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-130">This situation is not a problem if the application must share data with only a single application.</span></span> <span data-ttu-id="1c7ef-131">Если приложение должно совместно использовать одни и те же данные с несколькими приложениями, то при создании приложения следует указать \_ флаг хдата апповнед в [**ддекреатедатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle).</span><span class="sxs-lookup"><span data-stu-id="1c7ef-131">If an application must share the same data with multiple applications, however, the creating application should specify the HDATA\_APPOWNED flag in [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle).</span></span> <span data-ttu-id="1c7ef-132">Это дает право владения объектом DDE созданию приложения и предотвращает недействительность ДДЕМЛ.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-132">Doing so gives ownership of the DDE object to the creating application and prevents the DDEML from invalidating the data handle.</span></span> <span data-ttu-id="1c7ef-133">После этого приложение может передавать обработку данных в любое количество раз после вызова **ддекреатедатахандле** только один раз.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-133">The application can then pass the data handle any number of times after calling **DdeCreateDataHandle** only once.</span></span>

<span data-ttu-id="1c7ef-134">Если в приложении указан флаг ХДАТА \_ апповнед в параметре *афкмд* [**ддекреатедатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), он должен вызвать функцию [**ддефридатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) , чтобы освободить маркер памяти, независимо от того, передан ли этот обработчик в ддемл.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-134">If an application specifies the HDATA\_APPOWNED flag in the *afCmd* parameter of [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), it must call the [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) function to free the memory handle, regardless of whether it passed the handle to the DDEML.</span></span> <span data-ttu-id="1c7ef-135">Перед завершением приложение должно вызвать **ддефридатахандле** , чтобы освободить любой созданный им обработчик данных, но он не был передан в ддемл.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-135">Before it terminates, an application must call **DdeFreeDataHandle** to free any data handle that it created but did not pass to the DDEML.</span></span>

<span data-ttu-id="1c7ef-136">Приложение, которое еще не прошло обработку объекта DDE в ДДЕМЛ, может добавлять данные в объект или перезаписывать данные в объект с помощью функции [**ддеадддата**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) .</span><span class="sxs-lookup"><span data-stu-id="1c7ef-136">An application that has not yet passed the handle to a DDE object to the DDEML can add data to the object or overwrite data in the object by using the [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) function.</span></span> <span data-ttu-id="1c7ef-137">Как правило, приложение использует **ддеадддата** для заполнения неинициализированного объекта DDE.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-137">Typically, an application uses **DdeAddData** to fill an uninitialized DDE object.</span></span> <span data-ttu-id="1c7ef-138">После того как приложение передаст обработчик данных в ДДЕМЛ, объект DDE, идентифицируемый этим маркером, изменить нельзя. его можно освободить только.</span><span class="sxs-lookup"><span data-stu-id="1c7ef-138">After an application passes a data handle to the DDEML, the DDE object identified by the handle cannot be changed; it can only be freed.</span></span>

 

 




