---
description: Асинхронный запрос, который более сложен для записи, является предпочтительным типом запроса при повлиянии на производительность системы или сети путем запроса большой группы данных.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Вызов асинхронного запроса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ae188e3826562b1de68357db34dca6cea60a40e4be07c16946b13ed3eb3007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993074"
---
# <a name="invoking-an-asynchronous-query"></a>Вызов асинхронного запроса

Асинхронный запрос, который более сложен для записи, является предпочтительным типом запроса при повлиянии на производительность системы или сети путем запроса большой группы данных. В сценарии создание объекта [**свбемсинк**](swbemsink.md) и подподпрограмм для управления событиями, которые может получить приемник, являются единственными дополнительными задачами, которые выходят за пределы базового запроса.

> [!Note]  
> Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

 

Следующие сокращенные запросы сценариев для всех файлов данных на локальном компьютере. Этот запрос может занять слишком много времени, если он был выполнен для всех компьютеров в сети. Объект [**свбемсинк**](swbemsink.md) настраивается, а единственным обрабатываемым событием является oncompleteed Event.


```VB
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
    WScript.Echo "Asynchronous operation is done."
End Sub

Set service = GetObject("winmgmts:")
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
service.ExecQueryAsync sink, "SELECT * FROM Win32_DataFile"
WScript.Echo "Waiting for instances."
sink.Cancel()
set sink= Nothing
```



Подробные сведения о создании асинхронных вызовов методов в скрипте см. в разделе [вызов метода](calling-a-method.md).

В приложениях C++ асинхронный запрос порождает отдельный процесс для получения данных запроса. Асинхронный запрос более сложен по сравнению с синхронным запросом, так как необходимо закодировать многопоточное приложение. Однако асинхронный запрос не монопольно использует основной поток приложения.

В следующей процедуре описывается выполнение асинхронного запроса в C++.

**Выполнение асинхронного запроса в C++**

1.  Реализуйте объект **ивбемсинк** .

    Объект **ивбемсинк** получает сведения об асинхронной операции.

2.  Опишите запрос в вызове [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).

    WMI немедленно перемещает процесс, который запрашивает CIM, в другой поток и освобождает поток, который выполнил запрос для другой задачи.

3.  Дождитесь, пока Инструментарий WMI вызовет метод [**ивбемобжектсинк:: обозначают**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

    По завершении Инструментарий WMI вызывает [**Указание**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) , чтобы сообщить приложению о завершении запроса. Инструментарий WMI также возвращает результаты запроса в приемник в виде указателя на указатель интерфейса [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . Как и в случае с синхронным запросом, используйте указатель для доступа к объектам, которые составляют результат запроса.

Следующий пример кода не компилируется без ошибок, так как класс Куерисинк не определен. Определение класса Куерисинк см. в разделе [**ивбемобжектсинк**](iwbemobjectsink.md). В примере кода также требуются следующие инструкции Reference и \# include.


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



В следующем примере кода показано, как выполнить асинхронный вызов для выдаче запроса.


```C++
void ExecQuery(IWbemServices *pSvc)
{
    // Create a new sink object.
    QuerySink *pSink = new QuerySink;

    // Initialize the query and query language.
    BSTR strQuery = SysAllocString(L"SELECT * FROM ClassName");
    BSTR strQueryLang = SysAllocString(L"WQL");
    
    // Issue the query.
    HRESULT hRes = pSvc->ExecQueryAsync(strQueryLang, strQuery, 0,
        NULL, pSink);

    // Clean up.
    SysFreeString(strQuery);
    SysFreeString(strQueryLang);
    
    if (hRes)
    {
        printf("ExecQueryAsync failed with = 0x%X\n", hRes);
        return;
    }
    
    printf("Completed.\n");
}
```



Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

 

 



