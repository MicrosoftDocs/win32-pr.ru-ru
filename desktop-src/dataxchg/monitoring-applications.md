---
title: Мониторинг приложений
description: В этом разделе описывается, как можно использовать элементы библиотеки управления платформа динамических данных Exchange для создания приложения, которое наблюдает за работой динамического обмена данными в системе.
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- Пользовательский интерфейс Windows, платформа динамических данных Exchange (DDE)
- Платформа динамических данных Exchange (DDE), мониторинг приложений
- DDE (платформа динамических данных Exchange), мониторинг приложений
- Обмен данными, платформа динамических данных Exchange (DDE)
- Пользовательский интерфейс Windows, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), мониторинг приложений
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), мониторинг приложений
- Обмен данными, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f75685d4caa15e519485b2d8b37983faa35366
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067717"
---
# <a name="monitoring-applications"></a><span data-ttu-id="b0c1c-111">Мониторинг приложений</span><span class="sxs-lookup"><span data-stu-id="b0c1c-111">Monitoring Applications</span></span>

<span data-ttu-id="b0c1c-112">Элементы API платформа динамических данных библиотеки управления Exchange (ДДЕМЛ) можно использовать для создания приложения, которое отслеживает активность платформа динамических данных Exchange (DDE) в системе.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-112">The API elements of the Dynamic Data Exchange Management Library (DDEML) can be used to create an application that monitors Dynamic Data Exchange (DDE) activity in the system.</span></span> <span data-ttu-id="b0c1c-113">Как и любое приложение ДДЕМЛ, приложение мониторинга DDE содержит функцию обратного вызова DDE.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-113">Like any DDEML application, a DDE monitoring application contains a DDE callback function.</span></span> <span data-ttu-id="b0c1c-114">ДДЕМЛ уведомляет функцию обратного вызова DDE приложения мониторинга при каждом возникновении события DDE, передавая сведения о событии функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-114">The DDEML notifies a monitoring application's DDE callback function whenever a DDE event occurs, passing information about the event to the callback function.</span></span> <span data-ttu-id="b0c1c-115">Приложение обычно отображает сведения в окне или записывает их в файл.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-115">The application typically displays the information in a window or writes it to a file.</span></span>

<span data-ttu-id="b0c1c-116">Чтобы получать уведомления от ДДЕМЛ, приложение должно быть зарегистрировано в качестве монитора DDE, указав \_ флаг монитора APPCLASS в вызове функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="b0c1c-116">To receive notifications from the DDEML, an application must have registered as a DDE monitor by specifying the APPCLASS\_MONITOR flag in a call to the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="b0c1c-117">В этом же вызове приложение может указать один или несколько флагов монитора, чтобы указать типы событий, для которых ДДЕМЛ должен уведомлять функцию обратного вызова приложения.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-117">In this same call, the application can specify one or more monitor flags to indicate the types of events for which the DDEML is to notify the application's callback function.</span></span> <span data-ttu-id="b0c1c-118">Приложение может указывать следующие флаги монитора:</span><span class="sxs-lookup"><span data-stu-id="b0c1c-118">The following monitor flags can be specified by an application:</span></span>



| <span data-ttu-id="b0c1c-119">Flag</span><span class="sxs-lookup"><span data-stu-id="b0c1c-119">Flag</span></span>          | <span data-ttu-id="b0c1c-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b0c1c-120">Description</span></span>                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c1c-121">\_обратные вызовы MF</span><span class="sxs-lookup"><span data-stu-id="b0c1c-121">MF\_CALLBACKS</span></span> | <span data-ttu-id="b0c1c-122">Уведомляет функцию обратного вызова при отправке транзакции в любую функцию обратного вызова DDE в системе.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-122">Notifies the callback function whenever a transaction is sent to any DDE callback function in the system.</span></span>                                                                                                                                           |
| <span data-ttu-id="b0c1c-123">\_кредит</span><span class="sxs-lookup"><span data-stu-id="b0c1c-123">MF\_CONV</span></span>      | <span data-ttu-id="b0c1c-124">Уведомляет функцию обратного вызова при установке или завершении диалога.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-124">Notifies the callback function whenever a conversation is established or terminated.</span></span>                                                                                                                                                                |
| <span data-ttu-id="b0c1c-125">MF \_ ошибок</span><span class="sxs-lookup"><span data-stu-id="b0c1c-125">MF\_ERRORS</span></span>    | <span data-ttu-id="b0c1c-126">Уведомляет функцию обратного вызова при возникновении ошибки ДДЕМЛ.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-126">Notifies the callback function whenever a DDEML error occurs.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="b0c1c-127">\_ \_ сведения о ХСЗ MF</span><span class="sxs-lookup"><span data-stu-id="b0c1c-127">MF\_HSZ\_INFO</span></span> | <span data-ttu-id="b0c1c-128">Уведомляет функцию обратного вызова всякий раз, когда приложение ДДЕМЛ создает, освобождает или увеличивает счетчик использования строкового обработчика или при освобождении строкового маркера в результате вызова функции [**ддеунинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="b0c1c-128">Notifies the callback function whenever a DDEML application creates, frees, or increments the usage count of a string handle or whenever a string handle is freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> |
| <span data-ttu-id="b0c1c-129">\_ссылки MF</span><span class="sxs-lookup"><span data-stu-id="b0c1c-129">MF\_LINKS</span></span>     | <span data-ttu-id="b0c1c-130">Уведомляет функцию обратного вызова при запуске или завершении цикла рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-130">Notifies the callback function whenever an advise loop is started or ended.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="b0c1c-131">MF \_ постмсгс</span><span class="sxs-lookup"><span data-stu-id="b0c1c-131">MF\_POSTMSGS</span></span>  | <span data-ttu-id="b0c1c-132">Уведомляет функцию обратного вызова каждый раз, когда система или приложение отправляет сообщение DDE.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-132">Notifies the callback function whenever the system or an application posts a DDE message.</span></span>                                                                                                                                                           |
| <span data-ttu-id="b0c1c-133">MF \_ сендмсгс</span><span class="sxs-lookup"><span data-stu-id="b0c1c-133">MF\_SENDMSGS</span></span>  | <span data-ttu-id="b0c1c-134">Уведомляет функцию обратного вызова всякий раз, когда система или приложение отправляет сообщение DDE.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-134">Notifies the callback function whenever the system or an application sends a DDE message.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="b0c1c-135">В следующем примере показано, как зарегистрировать приложение мониторинга DDE, чтобы функция обратного вызова DDE получала уведомления обо всех событиях DDE.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-135">The following example shows how to register a DDE monitoring application so that its DDE callback function receives notifications of all DDE events.</span></span>


```
DWORD idInst; 
PFNCALLBACK lpDdeProc; 
hInst = hInstance; 
 
if (DdeInitialize( 
        (LPDWORD) &idInst,  // instance identifier 
        DDECallback,        // pointer to callback function 
        APPCLASS_MONITOR |  // this is a monitoring application 
        MF_CALLBACKS     |  // monitor callback functions 
        MF_CONV          |  // monitor conversation data 
        MF_ERRORS        |  // monitor DDEML errors 
        MF_HSZ_INFO      |  // monitor data handle activity 
        MF_LINKS         |  // monitor advise loops 
        MF_POSTMSGS      |  // monitor posted DDE messages 
        MF_SENDMSGS,        // monitor sent DDE messages 
        0))                 // reserved 
{
    return FALSE; 
}
```



<span data-ttu-id="b0c1c-136">ДДЕМЛ информирует приложение мониторинга о событии DDE, отправляя транзакцию [**\_ монитора кстип**](xtyp-monitor.md) в функцию обратного вызова DDE приложения.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-136">The DDEML informs a monitoring application of a DDE event by sending an [**XTYP\_MONITOR**](xtyp-monitor.md) transaction to the application's DDE callback function.</span></span> <span data-ttu-id="b0c1c-137">Во время этой транзакции ДДЕМЛ передает флаг Monitor, указывающий тип произошедшего события DDE, и обработчик объекта DDE, который содержит подробные сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-137">During this transaction, the DDEML passes a monitor flag that specifies the type of DDE event that has occurred and a handle to a DDE object that contains detailed information about the event.</span></span> <span data-ttu-id="b0c1c-138">ДДЕМЛ предоставляет набор структур, которые приложение может использовать для извлечения данных из объекта DDE.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-138">The DDEML provides a set of structures that the application can use to extract the information from the DDE object.</span></span> <span data-ttu-id="b0c1c-139">Для каждого типа события DDE существует соответствующая структура.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-139">There is a corresponding structure for each type of DDE event.</span></span>



| <span data-ttu-id="b0c1c-140">Структура</span><span class="sxs-lookup"><span data-stu-id="b0c1c-140">Structure</span></span>                                  | <span data-ttu-id="b0c1c-141">Описание</span><span class="sxs-lookup"><span data-stu-id="b0c1c-141">Description</span></span>                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="b0c1c-142">**монкбструкт**</span><span class="sxs-lookup"><span data-stu-id="b0c1c-142">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | <span data-ttu-id="b0c1c-143">Содержит сведения о транзакции.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-143">Contains information about a transaction.</span></span>                         |
| [<span data-ttu-id="b0c1c-144">**монконвструкт**</span><span class="sxs-lookup"><span data-stu-id="b0c1c-144">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | <span data-ttu-id="b0c1c-145">Содержит сведения о диалоге.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-145">Contains information about a conversation.</span></span>                        |
| [<span data-ttu-id="b0c1c-146">**монеррструкт**</span><span class="sxs-lookup"><span data-stu-id="b0c1c-146">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | <span data-ttu-id="b0c1c-147">Содержит сведения о последней ошибке DDE.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-147">Contains information about the latest DDE error.</span></span>                  |
| [<span data-ttu-id="b0c1c-148">**монлинкструкт**</span><span class="sxs-lookup"><span data-stu-id="b0c1c-148">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | <span data-ttu-id="b0c1c-149">Содержит сведения о цикле рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-149">Contains information about an advise loop.</span></span>                        |
| [<span data-ttu-id="b0c1c-150">**монхсзструкт**</span><span class="sxs-lookup"><span data-stu-id="b0c1c-150">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | <span data-ttu-id="b0c1c-151">Содержит сведения о строковом маркере.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-151">Contains information about a string handle.</span></span>                       |
| [<span data-ttu-id="b0c1c-152">**монмсгструкт**</span><span class="sxs-lookup"><span data-stu-id="b0c1c-152">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | <span data-ttu-id="b0c1c-153">Содержит сведения о отправленном или опубликованном сообщении DDE.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-153">Contains information about a DDE message that was sent or posted.</span></span> |



 

<span data-ttu-id="b0c1c-154">В следующем примере показана функция обратного вызова DDE приложения мониторинга DDE, которое форматирует сведения о каждом событии строкового обработчика, а затем отображает информацию в окне.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-154">The following example shows the DDE callback function of a DDE monitoring application that formats information about each string handle event and then displays the information in a window.</span></span> <span data-ttu-id="b0c1c-155">Функция использует структуру [**монхсзструкт**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) для извлечения сведений из объекта DDE.</span><span class="sxs-lookup"><span data-stu-id="b0c1c-155">The function uses the [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure to extract the information from the DDE object.</span></span>


```
HDDEDATA CALLBACK DDECallback(uType, uFmt, hconv, hsz1, hsz2, 
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
    LPVOID lpData; 
    CHAR *szAction; 
    CHAR szBuf[256]; 
    DWORD cb;
    HRESULT hResult; 
 
    switch (uType) 
    { 
        case XTYP_MONITOR: 
            // Obtain a pointer to the global memory object. 
 
            if (lpData = DdeAccessData(hdata, &cb)) 
            { 
                // Examine the monitor flag. 
 
                switch (dwData2) 
                { 
                    case MF_HSZ_INFO: 
 
#define PHSZS ((MONHSZSTRUCT *)lpData) 
 
                        // The global memory object contains 
                        // string handle data. Use the MONHSZSTRUCT 
                        // structure to access the data. 
 
                        switch (PHSZS->fsAction) 
                        { 
                            // Examine the action flags to determine
                            // the action performed on the handle.
 
                            case MH_CREATE: 
                                szAction = "Created"; 
                                break; 
 
                            case MH_KEEP: 
                                szAction = "Incremented"; 
                                break; 
 
                            case MH_DELETE: 
                                szAction = "Deleted"; 
                                break; 
 
                            case MH_CLEANUP: 
                                szAction = "Cleaned up"; 
                                break; 
 
                            default: 
                                DdeUnaccessData(hdata); 
                                return (HDDEDATA) 0; 
                        } 
 
                        // Write formatted output to a buffer. 
                        hResult = StringCchPrintf(szBuf, 256/sizeof(TCHAR),
                            "Handle %s, Task: %x, Hsz: %lx(%s)", 
                            (LPSTR) szAction, PHSZS->hTask, 
                            PHSZS->hsz, (LPSTR) PHSZS->str);
                        if (FAILED(hResult))
                        {
                        // TO DO: Write error handler.
                            return;
                        } 
                        // Display text or write to a file. 
 
                        break; 
 
#undef PHSZS 
 
                    // Process other MF_* flags. 
 
                    default: 
                        break; 
                } 
            } 
 
            // Free the global memory object. 
 
            DdeUnaccessData(hdata); 
            break; 
 
        default: 
            break; 
    } 
    return (HDDEDATA) 0; 
} 
```



 

 




