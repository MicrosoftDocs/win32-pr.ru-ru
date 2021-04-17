---
description: Инструментарий WMI предоставляет методы в API COM и API сценариев для получения информации или работы с объектами в корпоративной системе.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Вызов метода WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693750"
---
# <a name="calling-a-wmi-method"></a><span data-ttu-id="339ff-103">Вызов метода WMI</span><span class="sxs-lookup"><span data-stu-id="339ff-103">Calling a WMI Method</span></span>

<span data-ttu-id="339ff-104">Инструментарий WMI предоставляет методы в [API COM](com-api-for-wmi.md) и [API сценариев](scripting-api-for-wmi.md) для получения информации или работы с объектами в корпоративной системе.</span><span class="sxs-lookup"><span data-stu-id="339ff-104">WMI supplies methods in the [COM API](com-api-for-wmi.md) and the [scripting API](scripting-api-for-wmi.md) to obtain information or manipulate objects in an enterprise system.</span></span> <span data-ttu-id="339ff-105">Например, метод создания сценариев WMI [**SWbemServices.Exeккуери**](swbemservices-execquery.md) запросы данных.</span><span class="sxs-lookup"><span data-stu-id="339ff-105">For example, the WMI scripting method [**SWbemServices.ExecQuery**](swbemservices-execquery.md) queries for data.</span></span> <span data-ttu-id="339ff-106">Поставщики также имеют методы, определенные в регистрируемых ими классах.</span><span class="sxs-lookup"><span data-stu-id="339ff-106">Providers also have methods defined in the classes they register.</span></span> <span data-ttu-id="339ff-107">Примерами являются [**методы \_ Win32 LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) и [**счедулеауточк**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) , предоставляемые [поставщиком Win32](/windows/desktop/CIMWin32Prov/win32-provider).</span><span class="sxs-lookup"><span data-stu-id="339ff-107">Examples are the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) methods [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) and [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) supplied by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider).</span></span>

<span data-ttu-id="339ff-108">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="339ff-108">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="339ff-109">Методы WMI по сравнению с методами поставщика</span><span class="sxs-lookup"><span data-stu-id="339ff-109">WMI Methods Compared to Provider Methods</span></span>](#wmi-methods-compared-to-provider-methods)
-   [<span data-ttu-id="339ff-110">Режимы вызова методов в WMI</span><span class="sxs-lookup"><span data-stu-id="339ff-110">Method-Calling Modes in WMI</span></span>](#method-calling-modes-in-wmi)
    -   [<span data-ttu-id="339ff-111">Синхронный режим</span><span class="sxs-lookup"><span data-stu-id="339ff-111">Synchronous Mode</span></span>](#synchronous-mode)
    -   [<span data-ttu-id="339ff-112">Асинхронный режим</span><span class="sxs-lookup"><span data-stu-id="339ff-112">Asynchronous Mode</span></span>](#asynchronous-mode)
    -   [<span data-ttu-id="339ff-113">Режим семисинчронаус</span><span class="sxs-lookup"><span data-stu-id="339ff-113">Semisynchronous Mode</span></span>](#semisynchronous-mode)
-   [<span data-ttu-id="339ff-114">См. также</span><span class="sxs-lookup"><span data-stu-id="339ff-114">Related topics</span></span>](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a><span data-ttu-id="339ff-115">Методы WMI по сравнению с методами поставщика</span><span class="sxs-lookup"><span data-stu-id="339ff-115">WMI Methods Compared to Provider Methods</span></span>

<span data-ttu-id="339ff-116">Используя вызовы [*методов WMI*](gloss-w.md) , Объединенные с вызовами [*методов поставщика*](gloss-p.md) , можно получать сведения о предприятии и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="339ff-116">By using [*WMI method*](gloss-w.md) calls combined with [*provider method*](gloss-p.md) calls, you can retrieve and manipulate information about your enterprise.</span></span> <span data-ttu-id="339ff-117">Дополнительные сведения см. [в разделе вызов метода WMI](calling-a-wmi-method.md) и [вызов метода поставщика](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="339ff-117">For more information, see [Calling a WMI Method](calling-a-wmi-method.md) and [Calling a Provider Method](calling-a-provider-method.md).</span></span>

<span data-ttu-id="339ff-118">Методы объекта сценариев WMI [**SWbemObject**](swbemobject.md) имеют особое состояние, так как они могут применяться к любому классу данных WMI.</span><span class="sxs-lookup"><span data-stu-id="339ff-118">The methods of the WMI scripting object [**SWbemObject**](swbemobject.md) have a special status because they can apply to any WMI data class.</span></span> <span data-ttu-id="339ff-119">Дополнительные сведения см. в разделе [Создание скриптов с помощью SWbemObject](scripting-with-swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="339ff-119">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md).</span></span>

<span data-ttu-id="339ff-120">В следующем примере кода вызываются методы WMI и provider.</span><span class="sxs-lookup"><span data-stu-id="339ff-120">The following code example calls both WMI and provider methods.</span></span>

<span data-ttu-id="339ff-121">Следующие методы WMI и поставщика находятся в [API скриптов для WMI](scripting-api-for-wmi.md):</span><span class="sxs-lookup"><span data-stu-id="339ff-121">The following WMI and provider methods are located in the [Scripting API for WMI](scripting-api-for-wmi.md):</span></span>

-   <span data-ttu-id="339ff-122">**objWMIService.Exeккуери** вызывает метод создания сценариев WMI [ **SWbemServices.Exeккуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span><span class="sxs-lookup"><span data-stu-id="339ff-122">**objWMIService.ExecQuery** calls the WMI scripting method [**SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span></span>
-   <span data-ttu-id="339ff-123">**обжсервице. No ()** вызывает метод поставщика [ **Win32 \_ Service.**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span><span class="sxs-lookup"><span data-stu-id="339ff-123">**objService.StopService()** calls the provider method [**Win32\_Service.StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span></span>

<span data-ttu-id="339ff-124">Вы можете найти код, который может появиться в разделе "return" раздела "коды возврата" для [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="339ff-124">You can look up the code that may appear in "Return" in the Return Codes section for [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a><span data-ttu-id="339ff-125">Режимы Method-Calling в WMI</span><span class="sxs-lookup"><span data-stu-id="339ff-125">Method-Calling Modes in WMI</span></span>

<span data-ttu-id="339ff-126">Режим вызова семисинчронаус обычно обеспечивает оптимальный баланс между безопасностью и производительностью.</span><span class="sxs-lookup"><span data-stu-id="339ff-126">The semisynchronous calling mode usually provides the best balance between security and performance.</span></span>

<span data-ttu-id="339ff-127">Дополнительные сведения о каждом из возможных режимов см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="339ff-127">For more information about each of the possible modes, see the following:</span></span>

-   [<span data-ttu-id="339ff-128">Синхронная</span><span class="sxs-lookup"><span data-stu-id="339ff-128">Synchronous</span></span>](#synchronous-mode)
-   [<span data-ttu-id="339ff-129">Асинхронный</span><span class="sxs-lookup"><span data-stu-id="339ff-129">Asynchronous</span></span>](#asynchronous-mode)
-   [<span data-ttu-id="339ff-130">семисинчронаус</span><span class="sxs-lookup"><span data-stu-id="339ff-130">Semisynchronous</span></span>](#semisynchronous-mode)

### <a name="synchronous-mode"></a><span data-ttu-id="339ff-131">Синхронный режим</span><span class="sxs-lookup"><span data-stu-id="339ff-131">Synchronous Mode</span></span>

<span data-ttu-id="339ff-132">Синхронный режим происходит, когда программа или скрипты приостанавливаются до тех пор, пока вызов метода не вернет объект коллекции [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="339ff-132">Synchronous mode occurs when the program or scripts pauses until the method call returns a [**SWbemObjectSet**](swbemobjectset.md) collection object.</span></span> <span data-ttu-id="339ff-133">Инструментарий WMI создает эту коллекцию в памяти перед возвратом объекта коллекции вызывающей программе или сценарию.</span><span class="sxs-lookup"><span data-stu-id="339ff-133">WMI builds this collection in memory before returning the collection object to the calling program or script.</span></span>

<span data-ttu-id="339ff-134">Синхронный режим может оказать негативное воздействие на производительность программы или сценария на компьютере, на котором запущена программа или сценарий.</span><span class="sxs-lookup"><span data-stu-id="339ff-134">Synchronous mode can have an adverse effect of program or script performance on the computer running the program or script.</span></span> <span data-ttu-id="339ff-135">Например, синхронное извлечение тысяч событий из журнала событий может занять много времени и использовать большой объем памяти, так как инструментарий WMI создает объект из каждого события и затем помещает эти объекты в коллекцию перед передачей коллекции в метод.</span><span class="sxs-lookup"><span data-stu-id="339ff-135">For example, synchronously retrieving thousands of events from the event log can take a long time and use a lot of memory because WMI creates an object from each event and then puts those objects into a collection before passing the collection to the method.</span></span>

<span data-ttu-id="339ff-136">Вызывать методы, которые не возвращают большие наборы данных, следует только в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="339ff-136">You should only call methods that do not return large data sets in synchronous mode.</span></span> <span data-ttu-id="339ff-137">В синхронном режиме можно безопасно вызывать следующие методы [**SwbemServices**](swbemservices.md) :</span><span class="sxs-lookup"><span data-stu-id="339ff-137">The following [**SWbemServices**](swbemservices.md) methods can be safely called in synchronous mode:</span></span>

-   [<span data-ttu-id="339ff-138">**SWbemServices. Delete**</span><span class="sxs-lookup"><span data-stu-id="339ff-138">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="339ff-139">**SWbemServices.ExeКмесод**</span><span class="sxs-lookup"><span data-stu-id="339ff-139">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="339ff-140">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="339ff-140">**SWbemServices.Get**</span></span>](swbemservices-get.md)

<span data-ttu-id="339ff-141">Любые методы [**SwbemServices**](swbemservices.md) без слова «Async» в имени могут вызываться в синхронном режиме путем установки значения **вбемфлагретурнвхенкомплете** в параметре *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="339ff-141">Any [**SWbemServices**](swbemservices.md) methods without the word, "Async" in the name can be called in synchronous mode by setting the **wbemFlagReturnWhenComplete** value in the *iFlags* parameter.</span></span>

### <a name="asynchronous-mode"></a><span data-ttu-id="339ff-142">Асинхронный режим</span><span class="sxs-lookup"><span data-stu-id="339ff-142">Asynchronous Mode</span></span>

<span data-ttu-id="339ff-143">Асинхронный режим происходит, когда программа или скрипт продолжит выполняться после вызова метода.</span><span class="sxs-lookup"><span data-stu-id="339ff-143">Asynchronous mode occurs when the program or script continues to run after calling the method.</span></span> <span data-ttu-id="339ff-144">Инструментарий WMI возвращает все объекты из метода в объект [**свбемсинк**](swbemsink.md) при создании каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="339ff-144">WMI returns all objects from the method to a [**SWbemSink**](swbemsink.md) object as each object is created.</span></span> <span data-ttu-id="339ff-145">Вызывающая программа или скрипт должны иметь объект **свбемсинк** и обработчик событий [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) для обработки возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="339ff-145">The calling program or script must have an **SWbemSink** object and an [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event handler to process the returned objects.</span></span> <span data-ttu-id="339ff-146">Дополнительные сведения о создании обработчика событий для асинхронного режима см. [в разделе Получение WMI-события](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="339ff-146">For more information about creating an event handler for asynchronous mode, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="339ff-147">Хотя в этом режиме нет потерь производительности и ресурсов в синхронном режиме, асинхронный режим может привести к серьезным угрозам безопасности, поскольку результаты, хранящиеся в объекте [**свбемсинк**](swbemsink.md) , могут не поступать из вызывающей программы или скрипта.</span><span class="sxs-lookup"><span data-stu-id="339ff-147">While this mode does not have the performance and resource penalty of synchronous mode, asynchronous mode can create serious security risks because the results stored in the [**SWbemSink**](swbemsink.md) object may not come from the calling program or script.</span></span> <span data-ttu-id="339ff-148">Инструментарий WMI понижает уровень проверки подлинности объекта **свбемсинк** до тех пор, пока метод не завершится.</span><span class="sxs-lookup"><span data-stu-id="339ff-148">WMI lowers the authentication level on the **SWbemSink** object until the method succeeds.</span></span> <span data-ttu-id="339ff-149">Дополнительные сведения об устранении этих угроз безопасности см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="339ff-149">For more information about how to mitigate these security risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="339ff-150">Методы, добавленные с помощью слова async, являются методами для асинхронного режима.</span><span class="sxs-lookup"><span data-stu-id="339ff-150">Methods appended with the word Async are methods for asynchronous mode.</span></span> <span data-ttu-id="339ff-151">Следующие методы являются асинхронными вызовами:</span><span class="sxs-lookup"><span data-stu-id="339ff-151">The following methods are asynchronous calls:</span></span>

-   [<span data-ttu-id="339ff-152">**SWbemServices. АссоЦиаторсофасинк**</span><span class="sxs-lookup"><span data-stu-id="339ff-152">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
-   [<span data-ttu-id="339ff-153">**SWbemServices. DeleteAsync**</span><span class="sxs-lookup"><span data-stu-id="339ff-153">**SWbemServices.DeleteAsync**</span></span>](swbemservices-deleteasync.md)
-   [<span data-ttu-id="339ff-154">**SWbemServices.ExeКмесодасинк**</span><span class="sxs-lookup"><span data-stu-id="339ff-154">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
-   [<span data-ttu-id="339ff-155">**SWbemServices.ExeКнотификатионкуерясинк**</span><span class="sxs-lookup"><span data-stu-id="339ff-155">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)
-   [<span data-ttu-id="339ff-156">**SWbemServices.ExeКкуерясинк**</span><span class="sxs-lookup"><span data-stu-id="339ff-156">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
-   [<span data-ttu-id="339ff-157">**SWbemServices. Инстанцесофасинк**</span><span class="sxs-lookup"><span data-stu-id="339ff-157">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)
-   [<span data-ttu-id="339ff-158">**SWbemServices. Референцестоасинк**</span><span class="sxs-lookup"><span data-stu-id="339ff-158">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="339ff-159">**SWbemServices. Субклассесофасинк**</span><span class="sxs-lookup"><span data-stu-id="339ff-159">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)

<span data-ttu-id="339ff-160">Дополнительные сведения об асинхронном режиме см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="339ff-160">For more information about asynchronous mode, see:</span></span>

-   [<span data-ttu-id="339ff-161">Создание асинхронного вызова с помощью C++</span><span class="sxs-lookup"><span data-stu-id="339ff-161">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
-   [<span data-ttu-id="339ff-162">Выполнение асинхронного вызова с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="339ff-162">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a><span data-ttu-id="339ff-163">Режим семисинчронаус</span><span class="sxs-lookup"><span data-stu-id="339ff-163">Semisynchronous Mode</span></span>

<span data-ttu-id="339ff-164">Режим семисинчронаус аналогичен асинхронному режиму в том, что программа или скрипт продолжит выполняться после вызова метода.</span><span class="sxs-lookup"><span data-stu-id="339ff-164">Semisynchronous mode is similar to asynchronous mode in that the program or script continues to run after calling the method.</span></span> <span data-ttu-id="339ff-165">В режиме семисинчронаус Инструментарий WMI получает объекты в фоновом режиме по мере продолжения выполнения скрипта или программы.</span><span class="sxs-lookup"><span data-stu-id="339ff-165">In semisynchronous mode, WMI retrieves the objects in the background as your script or program continues to run.</span></span> <span data-ttu-id="339ff-166">Инструментарий WMI возвращает каждый объект, возвращаемый вызывающему методу сразу после создания объекта.</span><span class="sxs-lookup"><span data-stu-id="339ff-166">WMI returns each object returned to the calling method right after the object is created.</span></span>

<span data-ttu-id="339ff-167">Так как инструментарий WMI управляет объектом, режим семисинчронаус более безопасен, чем асинхронный режим.</span><span class="sxs-lookup"><span data-stu-id="339ff-167">Because WMI manages the object, semisynchronous mode is more secure than asynchronous mode.</span></span> <span data-ttu-id="339ff-168">Однако если используется режим семисинчронаус с более чем 1 000 экземплярами, то извлечение экземпляра может захватить доступные ресурсы, что может привести к снижению производительности программы или сценария, а также от компьютера, использующего программу или сценарий.</span><span class="sxs-lookup"><span data-stu-id="339ff-168">However, if you use semisynchronous mode with more than 1,000 instances, instance retrieval can monopolize the available resources, which can degrade the performance of the program or script and the computer using the program or script.</span></span> <span data-ttu-id="339ff-169">Каждый объект берет необходимые ресурсы, пока память не будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="339ff-169">Each object takes up the necessary resources until the memory is released.</span></span>

<span data-ttu-id="339ff-170">Чтобы обойти это условие, можно вызвать метод с набором параметров *ифлагс* с флагами **вбемфлагфорвардонли** и **вбемфлагретурниммедиатели** , чтобы дать инструментарию WMI инструкцию вернуть [**SWbemObjectSet**](swbemobjectset.md)только в прямом направлении.</span><span class="sxs-lookup"><span data-stu-id="339ff-170">To work around this condition, you can call the method with the *iFlags* parameter set with the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags to instruct WMI to return a forward-only [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="339ff-171">Однонаправленная **SWbemObjectSet** устраняет проблему производительности, вызванную большим набором данных, освобождая память после перечисления объекта.</span><span class="sxs-lookup"><span data-stu-id="339ff-171">A forward-only **SWbemObjectSet** eliminates the performance problem caused by a large data set by releasing the memory after the object is enumerated.</span></span>

<span data-ttu-id="339ff-172">Любой метод [**SwbemServices**](swbemservices.md) , который не может быть вызван в синхронном или асинхронном режиме, вызывается в режиме семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="339ff-172">Any [**SWbemServices**](swbemservices.md) method that cannot be called in either synchronous or asynchronous mode is called in semisynchronous mode.</span></span>

<span data-ttu-id="339ff-173">В режиме семисинчронаус вызываются следующие методы:</span><span class="sxs-lookup"><span data-stu-id="339ff-173">The following methods are called in semisynchronous mode:</span></span>

-   [<span data-ttu-id="339ff-174">**SWbemServices. АссоЦиаторсоф**</span><span class="sxs-lookup"><span data-stu-id="339ff-174">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="339ff-175">**SWbemServices. Delete**</span><span class="sxs-lookup"><span data-stu-id="339ff-175">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="339ff-176">**SWbemServices.ExeКмесод**</span><span class="sxs-lookup"><span data-stu-id="339ff-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="339ff-177">**SWbemServices.ExeКнотификатионкуери**</span><span class="sxs-lookup"><span data-stu-id="339ff-177">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
-   [<span data-ttu-id="339ff-178">**SWbemServices.ExeКкуери**</span><span class="sxs-lookup"><span data-stu-id="339ff-178">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="339ff-179">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="339ff-179">**SWbemServices.Get**</span></span>](swbemservices-get.md)
-   [<span data-ttu-id="339ff-180">**SWbemServices. Инстанцесоф**</span><span class="sxs-lookup"><span data-stu-id="339ff-180">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="339ff-181">**SWbemServices. Референцесто**</span><span class="sxs-lookup"><span data-stu-id="339ff-181">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="339ff-182">**SWbemServices. Субклассесоф**</span><span class="sxs-lookup"><span data-stu-id="339ff-182">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)
-   [<span data-ttu-id="339ff-183">**SWbemServices. размещение**</span><span class="sxs-lookup"><span data-stu-id="339ff-183">**SWbemServices.Put**</span></span>](swbemservicesex-put.md)

<span data-ttu-id="339ff-184">Дополнительные сведения о режиме семисинчронаус см. в статьях [осуществление вызова семисинчронаус с помощью C++](making-a-semisynchronous-call-with-c--.md) и [выполнение семисинчронаус Call с помощью VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="339ff-184">For more information about semisynchronous mode, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="339ff-185">См. также</span><span class="sxs-lookup"><span data-stu-id="339ff-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="339ff-186">Повышение производительности перечисления</span><span class="sxs-lookup"><span data-stu-id="339ff-186">Improving Enumeration Performance</span></span>](improving-enumeration-performance.md)
</dt> <dt>

[<span data-ttu-id="339ff-187">Создание сценариев с помощью SWbemObject</span><span class="sxs-lookup"><span data-stu-id="339ff-187">Scripting with SWbemObject</span></span>](scripting-with-swbemobject.md)
</dt> <dt>

[<span data-ttu-id="339ff-188">**вбемфлаженум**</span><span class="sxs-lookup"><span data-stu-id="339ff-188">**WbemFlagEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
