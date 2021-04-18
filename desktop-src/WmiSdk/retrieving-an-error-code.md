---
description: Как и в случае со всеми приложениями, Инструментарий WMI получает коды ошибок из операционной системы Windows.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Получение кода ошибки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c42dbd160ef6412c332e2da2c01f6590e10966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711667"
---
# <a name="retrieving-an-error-code"></a>Получение кода ошибки

Как и в случае со всеми приложениями, Инструментарий WMI получает коды ошибок из операционной системы Windows.

При получении кода ошибки доступны следующие варианты.

-   Просмотрите журнал событий.

    Инструментарий WMI отправляет сообщения об ошибках в службу журнала событий, которая проверяет журналы событий, чтобы помочь определить причину ошибки. Для программного доступа к журналам событий можно использовать классы, поддерживаемые поставщиком [журналов событий](/previous-versions/windows/desktop/eventlogprov/event-log-provider) .

-   Извлеките код ошибки обычным образом.

    Инструментарий WMI поддерживает стандартные методы получения кодов ошибок, которые являются кодами ошибок COM для C++, и собственными объектами ошибок, такими как [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), или [**свбемластеррор**](swbemlasterror.md) , если поставщик предоставляет сведения об ошибках.

Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).

В этом разделе обсуждаются следующие разделы:

-   [Обработка ошибки с помощью VBScript](#handling-an-error-with-vbscript)
-   [Обработка ошибки с помощью C++](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a>Обработка ошибки с помощью VBScript

Если вызов WMI через API-интерфейс для инструментария WMI вызывает ошибку, доступны следующие варианты для доступа к сведениям об ошибке:

-   Используйте собственные механизмы обработки ошибок языка сценариев, например в VBScript, чтобы поддерживать обработку ошибок, используйте [объект Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) .
-   Создайте объект [**свбемластеррор**](swbemlasterror.md) для получения отчета об ошибке.

В следующем скрипте показано использование собственного [объекта Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)). При указании неверного значения для обработчика процесса возникает ошибка.


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> Свойство **Description** [объекта Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) пусто при подключении к WMI с помощью моникера "винмгмтс:". Однако при подключении с помощью [**SWbemLocator**](swbemlocator.md)описание становится доступным.
>
> В следующей таблице перечислены свойства [объекта Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).
>
> 
>
> | Свойство                   | Содержит                                                       |
> |----------------------------|----------------------------------------------------------------|
> | **Описание**<br/> | Локализованное, понятное описание ошибки.<br/> |
> | **Число**<br/>      | **Значение HRESULT** , возвращенное API скриптов для WMI.<br/>  |
> | **Источник**<br/>      | Определяет объект, вызвавший ошибку.<br/>        |
>
> 
>
>  

 

В следующем скрипте показано использование объекта [**свбемластеррор**](swbemlasterror.md) для получения подробных сведений об ошибке. Обратите внимание, что не все поставщики предоставляют сведения для **свбемластеррор**. Дополнительные сведения о кодах ошибок в скрипте см. в разделе [вбемерроренум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a>Обработка ошибки с помощью C++

Клиентское приложение WMI может получить специфические для COM или WMI ошибки. Ошибки COM соответствуют структуре кодов ошибок COM. Все интерфейсы WMI могут возвращать характерную для COM ошибку, за исключением интерфейсов [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)и [**ивбемкуалифиерсет**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) . Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md). На страницах справочника по интерфейсам WMI перечислены соответствующие коды ошибок WMI в разделе Коды ошибок.

Клиентское приложение должно соответствовать стандартам COM для проверки состояния и кодов возврата ошибок. Основное различие заключается в том, нужно ли получить код ошибки из синхронного, семисинчронаус или асинхронного вызова.

**Получение синхронных и семисинчронаус сообщений об ошибках с помощью C++**

1.  Получите сведения об ошибке с помощью вызова функции COM [жетерроринфо]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .

    Убедитесь, что вызывается [жетерроринфо]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) сразу после того, как метод интерфейса указывает на ошибку. Сюда входят любые методы [**ивбемкаллресулт**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) , которые вызываются во время обработки семисинчронаус процесса.

2.  Изучите возвращенный объект ошибки COM с помощью вызова метода [**иерроринтерфаце:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

    Не забудьте указать IID \_ вбемклассобжект для параметра *riid* в вызове [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) . Метод **QueryInterface** возвращает экземпляр класса WMI, обычно [**\_ \_ екстендедстатус**](--extendedstatus.md).

Инструментарий WMI не доставляет объект Error через [жетерроринфо]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) для асинхронного вызова, так как не существует способа выяснить, когда или в каком потоке произошло асинхронный вызов. Поэтому код может обрабатывать только определенные ошибки или передавать ошибку вызова через COM.

> [!Note]  
> Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

 

**Доступ к асинхронным сообщениям об ошибках с помощью C++**

-   Получите объект ошибки COM из реализации [**ивбемобжектсинк:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).

    В следующем псевдокоде показана типичная реализация обработки ошибок для клиентского приложения.

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

