---
description: Выполнение асинхронного вызова метода WMI или метода поставщика позволяет скрипту продолжать выполнение, пока объекты возвращают в объект Свбемсинк и обрабатываются такими методами, как Свбемсинк. Онобжектреади.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Выполнение асинхронного вызова с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702298"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a><span data-ttu-id="7c5a8-103">Выполнение асинхронного вызова с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="7c5a8-103">Making an Asynchronous Call with VBScript</span></span>

<span data-ttu-id="7c5a8-104">Выполнение асинхронного вызова [*метода WMI*](gloss-w.md) или [*метода поставщика*](gloss-p.md) позволяет скрипту продолжать выполнение, пока объекты возвращают в объект [**свбемсинк**](swbemsink.md) и обрабатываются такими методами, как [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md).</span><span class="sxs-lookup"><span data-stu-id="7c5a8-104">Making an asynchronous call to a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) allows a script to continue executing while objects return to an [**SWbemSink**](swbemsink.md) object, and are handled by methods such as [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md).</span></span> <span data-ttu-id="7c5a8-105">Однако асинхронные вызовы не рекомендуются, так как данные могут не возвращаться на том же уровне безопасности, что и вызов метода.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-105">However, asynchronous calls are not recommended because the data may not be returned at the same level of security as the call is made.</span></span>

<span data-ttu-id="7c5a8-106">При использовании асинхронных вызовов приемника, таких как [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) , для получения возвращаемых данных можно задать следующее значение реестра.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-106">When using asynchronous sink calls like [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) to get returned data, you can set the following registry value.</span></span>

<span data-ttu-id="7c5a8-107">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **унсекаппакцессконтролдефаулт**</span><span class="sxs-lookup"><span data-stu-id="7c5a8-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault**</span></span>

<span data-ttu-id="7c5a8-108">Установка этого значения реестра гарантирует проверку подлинности объектов данных, возвращаемых в приемник.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-108">Setting this registry value ensures authentication of the data objects returned to the sink.</span></span> <span data-ttu-id="7c5a8-109">Если для **унсекаппакцессконтролдефаулт** задано значение One (1), WMI выполняет проверку доступа к возвращаемым данным.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-109">If **UnsecAppAccessControlDefault** is set to one (1), then WMI performs access checking of the data return.</span></span> <span data-ttu-id="7c5a8-110">Проверки доступа проверяют, поступают ли данные из правильного источника.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-110">Access checks verify that the data comes from the correct source.</span></span> <span data-ttu-id="7c5a8-111">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="7c5a8-111">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="7c5a8-112">Асинхронные методы с именами, заканчивающимися на "Async \_ ", всегда возвращают немедленно после вызова, чтобы программа могла продолжить выполнение.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-112">Asynchronous methods with names that end in "Async\_" always return immediately after being called so that a program can continue executing.</span></span> <span data-ttu-id="7c5a8-113">Например, [**SWbemServices.Exeккуери**](swbemservices-execquery.md) является синхронным и блокирует выполнение до тех пор, пока не будут возвращены все объекты.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-113">For example, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) is synchronous and blocks execution until all of the objects are returned.</span></span> <span data-ttu-id="7c5a8-114">[**SWbemServices.Exeметод ккуерясинк**](swbemservices-execqueryasync.md) является неблокирующей асинхронной версией.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-114">The [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method is the nonblocking asynchronous version.</span></span> <span data-ttu-id="7c5a8-115">Более безопасный способ вызоваSWbemServices.Exeнеблокировке **ккуери** заключается в вызове [*полусинхронном*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="7c5a8-115">A more secure way to make the call to **SWbemServices.ExecQuery** nonblocking is by making the call [*semisynchronously*](gloss-s.md).</span></span> <span data-ttu-id="7c5a8-116">Дополнительные сведения см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md) и [вызов Семисинчронаус с помощью VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="7c5a8-116">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="7c5a8-117">Параметр *ифлагс* для асинхронных вызовов всегда имеет значение по умолчанию (0).</span><span class="sxs-lookup"><span data-stu-id="7c5a8-117">The *iFlags* parameter for asynchronous calls always defaults to zero (0).</span></span> <span data-ttu-id="7c5a8-118">Асинхронные методы не предоставляют коллекцию [**SWbemObjectSet**](swbemobjectset.md) для подпрограммы приемника.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-118">Asynchronous methods do not supply an [**SWbemObjectSet**](swbemobjectset.md) collection to the sink subroutine.</span></span> <span data-ttu-id="7c5a8-119">Вместо этого подпрограммы события [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) в скрипте или приложении получают каждый объект, как он предоставляется.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-119">Instead, the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event subroutine in your script or application receives each object as it is provided.</span></span>

<span data-ttu-id="7c5a8-120">После завершения исходного асинхронного вызова он вызывает событие [**свбемсинк. OnComplete**](swbemsink-oncompleted.md) в приемнике объекта и выполняет код, который вы поместите в него, чтобы обработать результат вызова.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-120">When the original asynchronous call is complete, it calls the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the object sink, and executes the code you place there to process the result of the call.</span></span>

> [!Note]  
> <span data-ttu-id="7c5a8-121">Страница Active Server (ASP) в качестве сервера скриптов не поддерживает асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-121">An Active Server Page (ASP) as a script host does not support an asynchronous call.</span></span>

 

<span data-ttu-id="7c5a8-122">Следующая процедура описывает, как выполнить асинхронный вызов с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-122">The following procedure describes how to make an asynchronous call by using VBScript.</span></span>

<span data-ttu-id="7c5a8-123">**Выполнение асинхронного вызова с помощью VBScript**</span><span class="sxs-lookup"><span data-stu-id="7c5a8-123">**To make an asynchronous call using VBScript**</span></span>

1.  <span data-ttu-id="7c5a8-124">Подключитесь к инструментарию WMI и получите объект [**SwbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="7c5a8-124">Connect to WMI and get an [**SWbemServices**](swbemservices.md) object.</span></span>

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  <span data-ttu-id="7c5a8-125">Создайте приемник объекта с помощью функции [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) или (для сервера скриптов Windows 2,0) тег объекта с атрибутом Events, имеющим значение **true**.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-125">Create the object sink using either [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) or (for Windows Script Host 2.0 only) the OBJECT tag with an events attribute set to **TRUE**.</span></span>

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    <span data-ttu-id="7c5a8-126">-или-</span><span class="sxs-lookup"><span data-stu-id="7c5a8-126">-or-</span></span>

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  <span data-ttu-id="7c5a8-127">Создайте подпрограммы для каждого события, которое может быть активировано асинхронным событием.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-127">Create a subroutine for each event an asynchronous event can trigger.</span></span> <span data-ttu-id="7c5a8-128">Эти события определяются как методы в [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="7c5a8-128">These events are defined as methods on [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="7c5a8-129">Например, Инструментарий WMI выполняет обратный вызов к [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) по мере того, как каждый экземпляр возвращает.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-129">For example, WMI makes a callback to [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) as each instance returns.</span></span>

    <span data-ttu-id="7c5a8-130">При создании подпрограммы разместите код в подпрограмме, чтобы обрабатывались все события при его получении.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-130">When you create the subroutine, place code in the subroutine to handle each event when it is received.</span></span>

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    <span data-ttu-id="7c5a8-131">Изучите параметр *ихресулт* , возвращаемый [**oncompleteed**](swbemsink-oncompleted.md) , чтобы определить, завершился ли асинхронный вызов успешно, или если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-131">Examine the *iHresult* parameter returned by the [**OnCompleted**](swbemsink-oncompleted.md) event to determine whether or not the asynchronous call is successful, or if an error occurred.</span></span> <span data-ttu-id="7c5a8-132">В случае успеха значение, передаваемое в параметре *ихресулт* , равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="7c5a8-132">If successful, the value passed in the *iHresult* parameter is equal to zero (0).</span></span> <span data-ttu-id="7c5a8-133">Любое другое значение может указывать на ошибку, поэтому следует проверить значения в объекте Error, возвращенном в параметре *обжерроробжект* .</span><span class="sxs-lookup"><span data-stu-id="7c5a8-133">Any other value may indicate an error, and you should check the values in the error object that is returned in the *objErrorObject* parameter.</span></span>

4.  <span data-ttu-id="7c5a8-134">Выполните асинхронный вызов и передайте имя приемника в параметр *обжвбемсинк* .</span><span class="sxs-lookup"><span data-stu-id="7c5a8-134">Make an asynchronous call and pass the name of your sink in the *objWbemSink* parameter.</span></span>

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  <span data-ttu-id="7c5a8-135">Выполните вызов, который предотвращает завершение скрипта до получения всех событий.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-135">Make a call that prevents the script from ending before all of the events are received.</span></span> <span data-ttu-id="7c5a8-136">Если сценарий может работать с интерфейсом экрана, простой способ сделать это — использовать команду сервера сценариев Windows (WSH) `Echo` , которая показана в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-136">If your script can run with a screen interface, a simple way to do this is to use a Windows Script Host (WSH) `Echo` command, which is shown in the following example.</span></span>

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    <span data-ttu-id="7c5a8-137">При выполнении этого скрипта может отобразиться первый экземпляр, возвращаемый перед сообщением **ожидания экземпляров** , либо он появится после.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-137">When you execute this script you may see the first instance return before the **Waiting for instances** message or you may see it after.</span></span> <span data-ttu-id="7c5a8-138">Это характер асинхронной обработки.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-138">This is the nature of asynchronous processing.</span></span> <span data-ttu-id="7c5a8-139">Если закрыть окно сообщения **Waiting of Instances (ожидание экземпляров** ), возможно, вы не увидите все экземпляры.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-139">If you close the **Waiting for instances** message box too soon, you may not see all of the instances.</span></span>

6.  <span data-ttu-id="7c5a8-140">Если имеются результаты из нескольких различных асинхронных вызовов, возвращающих один и тот же приемник, сохраните все необходимые отличительные данные в параметре контекста *обжвбемасинкконтекст* .</span><span class="sxs-lookup"><span data-stu-id="7c5a8-140">If you have results from several different asynchronous calls returning to the same sink, store any necessary distinguishing data in the *objWbemAsyncContext* context parameter.</span></span>

7.  <span data-ttu-id="7c5a8-141">По завершении работы с приемником отмените асинхронный вызов с помощью метода [**Cancel**](swbemsink-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="7c5a8-141">When finished with the sink, cancel your asynchronous call with the [**Cancel**](swbemsink-cancel.md) method.</span></span>

    ```VB
    objwbemsink.Cancel()
    ```

    

    <span data-ttu-id="7c5a8-142">Метод [**Cancel**](swbemsink-cancel.md) предписывает WSH отменить все асинхронные вызовы, связанные с данным объектом-приемником.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-142">The [**Cancel**](swbemsink-cancel.md) method instructs WSH to cancel all of the asynchronous calls associated with a given sink object.</span></span> <span data-ttu-id="7c5a8-143">Таким образом, может потребоваться использовать отдельные приемники для асинхронных операций, которые должны быть независимыми.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-143">Thus, you may want to use separate sinks for asynchronous operations that must be independent.</span></span>

8.  <span data-ttu-id="7c5a8-144">Освободите объект приемника, назначив объекту приемника значение `Nothing` .</span><span class="sxs-lookup"><span data-stu-id="7c5a8-144">Release the sink object by assigning the sink object to `Nothing`.</span></span>

    ```VB
    set objwbemsink= Nothing
    ```

    

<span data-ttu-id="7c5a8-145">В следующем примере кода показан асинхронный запрос для всех экземпляров [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7c5a8-145">The following code example shows an asynchronous query for all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the local machine.</span></span> <span data-ttu-id="7c5a8-146">Сведения о семисинчронаус версии того же метода см. в разделе [вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7c5a8-146">For a semisynchronous version of the same method, see [Calling a Method](calling-a-method.md).</span></span>


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a><span data-ttu-id="7c5a8-147">См. также</span><span class="sxs-lookup"><span data-stu-id="7c5a8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c5a8-148">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="7c5a8-148">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="7c5a8-149">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="7c5a8-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
