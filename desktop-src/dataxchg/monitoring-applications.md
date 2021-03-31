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
# <a name="monitoring-applications"></a>Мониторинг приложений

Элементы API платформа динамических данных библиотеки управления Exchange (ДДЕМЛ) можно использовать для создания приложения, которое отслеживает активность платформа динамических данных Exchange (DDE) в системе. Как и любое приложение ДДЕМЛ, приложение мониторинга DDE содержит функцию обратного вызова DDE. ДДЕМЛ уведомляет функцию обратного вызова DDE приложения мониторинга при каждом возникновении события DDE, передавая сведения о событии функции обратного вызова. Приложение обычно отображает сведения в окне или записывает их в файл.

Чтобы получать уведомления от ДДЕМЛ, приложение должно быть зарегистрировано в качестве монитора DDE, указав \_ флаг монитора APPCLASS в вызове функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . В этом же вызове приложение может указать один или несколько флагов монитора, чтобы указать типы событий, для которых ДДЕМЛ должен уведомлять функцию обратного вызова приложения. Приложение может указывать следующие флаги монитора:



| Flag          | Описание                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_обратные вызовы MF | Уведомляет функцию обратного вызова при отправке транзакции в любую функцию обратного вызова DDE в системе.                                                                                                                                           |
| \_кредит      | Уведомляет функцию обратного вызова при установке или завершении диалога.                                                                                                                                                                |
| MF \_ ошибок    | Уведомляет функцию обратного вызова при возникновении ошибки ДДЕМЛ.                                                                                                                                                                                       |
| \_ \_ сведения о ХСЗ MF | Уведомляет функцию обратного вызова всякий раз, когда приложение ДДЕМЛ создает, освобождает или увеличивает счетчик использования строкового обработчика или при освобождении строкового маркера в результате вызова функции [**ддеунинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) . |
| \_ссылки MF     | Уведомляет функцию обратного вызова при запуске или завершении цикла рекомендаций.                                                                                                                                                                         |
| MF \_ постмсгс  | Уведомляет функцию обратного вызова каждый раз, когда система или приложение отправляет сообщение DDE.                                                                                                                                                           |
| MF \_ сендмсгс  | Уведомляет функцию обратного вызова всякий раз, когда система или приложение отправляет сообщение DDE.                                                                                                                                                           |



 

В следующем примере показано, как зарегистрировать приложение мониторинга DDE, чтобы функция обратного вызова DDE получала уведомления обо всех событиях DDE.


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



ДДЕМЛ информирует приложение мониторинга о событии DDE, отправляя транзакцию [**\_ монитора кстип**](xtyp-monitor.md) в функцию обратного вызова DDE приложения. Во время этой транзакции ДДЕМЛ передает флаг Monitor, указывающий тип произошедшего события DDE, и обработчик объекта DDE, который содержит подробные сведения о событии. ДДЕМЛ предоставляет набор структур, которые приложение может использовать для извлечения данных из объекта DDE. Для каждого типа события DDE существует соответствующая структура.



| Структура                                  | Описание                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [**монкбструкт**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | Содержит сведения о транзакции.                         |
| [**монконвструкт**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | Содержит сведения о диалоге.                        |
| [**монеррструкт**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | Содержит сведения о последней ошибке DDE.                  |
| [**монлинкструкт**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | Содержит сведения о цикле рекомендаций.                        |
| [**монхсзструкт**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | Содержит сведения о строковом маркере.                       |
| [**монмсгструкт**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | Содержит сведения о отправленном или опубликованном сообщении DDE. |



 

В следующем примере показана функция обратного вызова DDE приложения мониторинга DDE, которое форматирует сведения о каждом событии строкового обработчика, а затем отображает информацию в окне. Функция использует структуру [**монхсзструкт**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) для извлечения сведений из объекта DDE.


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



 

 




