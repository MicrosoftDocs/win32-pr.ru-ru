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
# <a name="retrieving-an-error-code"></a><span data-ttu-id="84772-103">Получение кода ошибки</span><span class="sxs-lookup"><span data-stu-id="84772-103">Retrieving an Error Code</span></span>

<span data-ttu-id="84772-104">Как и в случае со всеми приложениями, Инструментарий WMI получает коды ошибок из операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="84772-104">As with all applications, WMI receives error codes from the Windows operating system.</span></span>

<span data-ttu-id="84772-105">При получении кода ошибки доступны следующие варианты.</span><span class="sxs-lookup"><span data-stu-id="84772-105">When you receive an error code, you have the following options:</span></span>

-   <span data-ttu-id="84772-106">Просмотрите журнал событий.</span><span class="sxs-lookup"><span data-stu-id="84772-106">Look at the event log.</span></span>

    <span data-ttu-id="84772-107">Инструментарий WMI отправляет сообщения об ошибках в службу журнала событий, которая проверяет журналы событий, чтобы помочь определить причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="84772-107">WMI sends error messages to the Event Log service that checks the event logs to help determine the cause of an error.</span></span> <span data-ttu-id="84772-108">Для программного доступа к журналам событий можно использовать классы, поддерживаемые поставщиком [журналов событий](/previous-versions/windows/desktop/eventlogprov/event-log-provider) .</span><span class="sxs-lookup"><span data-stu-id="84772-108">You can use the classes that the [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supports to access event logs programmatically.</span></span>

-   <span data-ttu-id="84772-109">Извлеките код ошибки обычным образом.</span><span class="sxs-lookup"><span data-stu-id="84772-109">Retrieve the error code normally.</span></span>

    <span data-ttu-id="84772-110">Инструментарий WMI поддерживает стандартные методы получения кодов ошибок, которые являются кодами ошибок COM для C++, и собственными объектами ошибок, такими как [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), или [**свбемластеррор**](swbemlasterror.md) , если поставщик предоставляет сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="84772-110">WMI supports the standard techniques to retrieve error codes, which are COM error codes for C++, and native error objects, such as [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), or [**SWbemLastError**](swbemlasterror.md) if the provider supplies error information.</span></span>

<span data-ttu-id="84772-111">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="84772-111">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="84772-112">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="84772-112">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="84772-113">Обработка ошибки с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="84772-113">Handling an Error with VBScript</span></span>](#handling-an-error-with-vbscript)
-   [<span data-ttu-id="84772-114">Обработка ошибки с помощью C++</span><span class="sxs-lookup"><span data-stu-id="84772-114">Handling an Error Using C++</span></span>](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a><span data-ttu-id="84772-115">Обработка ошибки с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="84772-115">Handling an Error with VBScript</span></span>

<span data-ttu-id="84772-116">Если вызов WMI через API-интерфейс для инструментария WMI вызывает ошибку, доступны следующие варианты для доступа к сведениям об ошибке:</span><span class="sxs-lookup"><span data-stu-id="84772-116">If a call to WMI through the Scripting API for WMI causes an error, you have the following options to access the error information:</span></span>

-   <span data-ttu-id="84772-117">Используйте собственные механизмы обработки ошибок языка сценариев, например в VBScript, чтобы поддерживать обработку ошибок, используйте [объект Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="84772-117">Use native error mechanisms of the scripting language, for example, in VBScript use [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) to support error handling.</span></span>
-   <span data-ttu-id="84772-118">Создайте объект [**свбемластеррор**](swbemlasterror.md) для получения отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="84772-118">Create an [**SWbemLastError**](swbemlasterror.md) object to get an error report.</span></span>

<span data-ttu-id="84772-119">В следующем скрипте показано использование собственного [объекта Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="84772-119">The following script shows use of the native [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span> <span data-ttu-id="84772-120">При указании неверного значения для обработчика процесса возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="84772-120">When an incorrect value for the process handle is given, an error is generated.</span></span>


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> <span data-ttu-id="84772-121">Свойство **Description** [объекта Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) пусто при подключении к WMI с помощью моникера "винмгмтс:".</span><span class="sxs-lookup"><span data-stu-id="84772-121">The **Description** property of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) is empty when connecting to WMI through the "winmgmts:" moniker.</span></span> <span data-ttu-id="84772-122">Однако при подключении с помощью [**SWbemLocator**](swbemlocator.md)описание становится доступным.</span><span class="sxs-lookup"><span data-stu-id="84772-122">However, if you connect using [**SWbemLocator**](swbemlocator.md), the description is available.</span></span>
>
> <span data-ttu-id="84772-123">В следующей таблице перечислены свойства [объекта Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="84772-123">The following table lists the properties of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span>
>
> 
>
> | <span data-ttu-id="84772-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="84772-124">Property</span></span>                   | <span data-ttu-id="84772-125">Содержит</span><span class="sxs-lookup"><span data-stu-id="84772-125">Contains</span></span>                                                       |
> |----------------------------|----------------------------------------------------------------|
> | <span data-ttu-id="84772-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="84772-126">**Description**</span></span><br/> | <span data-ttu-id="84772-127">Локализованное, понятное описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="84772-127">Localized, human-readable description of the error.</span></span><br/> |
> | <span data-ttu-id="84772-128">**Число**</span><span class="sxs-lookup"><span data-stu-id="84772-128">**Number**</span></span><br/>      | <span data-ttu-id="84772-129">**Значение HRESULT** , возвращенное API скриптов для WMI.</span><span class="sxs-lookup"><span data-stu-id="84772-129">**HRESULT** returned by the Scripting API for WMI.</span></span><br/>  |
> | <span data-ttu-id="84772-130">**Источник**</span><span class="sxs-lookup"><span data-stu-id="84772-130">**Source**</span></span><br/>      | <span data-ttu-id="84772-131">Определяет объект, вызвавший ошибку.</span><span class="sxs-lookup"><span data-stu-id="84772-131">Identifies the object that raised the error.</span></span><br/>        |
>
> 
>
>  

 

<span data-ttu-id="84772-132">В следующем скрипте показано использование объекта [**свбемластеррор**](swbemlasterror.md) для получения подробных сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="84772-132">The following script shows use of an [**SWbemLastError**](swbemlasterror.md) object to obtain detailed error information.</span></span> <span data-ttu-id="84772-133">Обратите внимание, что не все поставщики предоставляют сведения для **свбемластеррор**.</span><span class="sxs-lookup"><span data-stu-id="84772-133">Note that not all providers supply information to **SWbemLastError**.</span></span> <span data-ttu-id="84772-134">Дополнительные сведения о кодах ошибок в скрипте см. в разделе [вбемерроренум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="84772-134">For more information about error codes in script, see [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a><span data-ttu-id="84772-135">Обработка ошибки с помощью C++</span><span class="sxs-lookup"><span data-stu-id="84772-135">Handling an Error Using C++</span></span>

<span data-ttu-id="84772-136">Клиентское приложение WMI может получить специфические для COM или WMI ошибки.</span><span class="sxs-lookup"><span data-stu-id="84772-136">A WMI client application can receive either COM-specific or WMI-specific errors.</span></span> <span data-ttu-id="84772-137">Ошибки COM соответствуют структуре кодов ошибок COM.</span><span class="sxs-lookup"><span data-stu-id="84772-137">The COM errors conform to the structure of COM error codes.</span></span> <span data-ttu-id="84772-138">Все интерфейсы WMI могут возвращать характерную для COM ошибку, за исключением интерфейсов [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)и [**ивбемкуалифиерсет**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) .</span><span class="sxs-lookup"><span data-stu-id="84772-138">All WMI interfaces can return a COM-specific error except the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject), and [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interfaces.</span></span> <span data-ttu-id="84772-139">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="84772-139">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span> <span data-ttu-id="84772-140">На страницах справочника по интерфейсам WMI перечислены соответствующие коды ошибок WMI в разделе Коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="84772-140">The reference pages of the WMI interfaces list the appropriate WMI error codes in the Error Codes section.</span></span>

<span data-ttu-id="84772-141">Клиентское приложение должно соответствовать стандартам COM для проверки состояния и кодов возврата ошибок.</span><span class="sxs-lookup"><span data-stu-id="84772-141">A client application must follow the COM standards for checking status and error return codes.</span></span> <span data-ttu-id="84772-142">Основное различие заключается в том, нужно ли получить код ошибки из синхронного, семисинчронаус или асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="84772-142">The main difference you must choose is whether you wish to retrieve the error code from a synchronous, semisynchronous, or asynchronous call.</span></span>

<span data-ttu-id="84772-143">**Получение синхронных и семисинчронаус сообщений об ошибках с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="84772-143">**To access synchronous and semisynchronous error messages using C++**</span></span>

1.  <span data-ttu-id="84772-144">Получите сведения об ошибке с помощью вызова функции COM [жетерроринфо]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="84772-144">Retrieve the error information with a call to the [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) COM function.</span></span>

    <span data-ttu-id="84772-145">Убедитесь, что вызывается [жетерроринфо]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) сразу после того, как метод интерфейса указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="84772-145">Make sure to call [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immediately after an interface method indicates an error.</span></span> <span data-ttu-id="84772-146">Сюда входят любые методы [**ивбемкаллресулт**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) , которые вызываются во время обработки семисинчронаус процесса.</span><span class="sxs-lookup"><span data-stu-id="84772-146">This includes any of the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) methods you call while processing a semisynchronous process.</span></span>

2.  <span data-ttu-id="84772-147">Изучите возвращенный объект ошибки COM с помощью вызова метода [**иерроринтерфаце:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="84772-147">Examine the returned COM error object with a call to the [**IErrorInterface::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span>

    <span data-ttu-id="84772-148">Не забудьте указать IID \_ вбемклассобжект для параметра *riid* в вызове [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="84772-148">Make sure to specify IID\_WbemClassObject for the *riid* parameter in the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) call.</span></span> <span data-ttu-id="84772-149">Метод **QueryInterface** возвращает экземпляр класса WMI, обычно [**\_ \_ екстендедстатус**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="84772-149">The **QueryInterface** method returns an instance of a WMI class, typically [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

<span data-ttu-id="84772-150">Инструментарий WMI не доставляет объект Error через [жетерроринфо]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) для асинхронного вызова, так как не существует способа выяснить, когда или в каком потоке произошло асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="84772-150">WMI does not deliver the error object through [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) for an asynchronous call because there is no way to know when, or on which thread the asynchronous call occurred.</span></span> <span data-ttu-id="84772-151">Поэтому код может обрабатывать только определенные ошибки или передавать ошибку вызова через COM.</span><span class="sxs-lookup"><span data-stu-id="84772-151">Therefore, your code can only handle specific errors or pass the call failure through COM.</span></span>

> [!Note]  
> <span data-ttu-id="84772-152">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="84772-152">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="84772-153">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="84772-153">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="84772-154">**Доступ к асинхронным сообщениям об ошибках с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="84772-154">**To access asynchronous error messages using C++**</span></span>

-   <span data-ttu-id="84772-155">Получите объект ошибки COM из реализации [**ивбемобжектсинк:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="84772-155">Retrieve the COM error object from your implementation of [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span>

    <span data-ttu-id="84772-156">В следующем псевдокоде показана типичная реализация обработки ошибок для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="84772-156">The following pseudocode shows a typical error handling implementation for a client application.</span></span>

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

    

 

