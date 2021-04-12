---
description: Объект скриптов SWbemObject — это универсальный объект WMI, определяющий свойства и методы, которые могут использоваться независимо от конкретного объекта WMI, к которому привязан объект SWbemObject.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Создание сценариев с помощью SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155854"
---
# <a name="scripting-with-swbemobject"></a><span data-ttu-id="4b0e5-103">Создание сценариев с помощью SWbemObject</span><span class="sxs-lookup"><span data-stu-id="4b0e5-103">Scripting with SWbemObject</span></span>

<span data-ttu-id="4b0e5-104">Объект скриптов [**SWbemObject**](swbemobject.md) — это универсальный объект WMI, определяющий свойства и методы, которые могут использоваться независимо от конкретного объекта WMI, к которому привязан объект **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="4b0e5-104">The [**SWbemObject**](swbemobject.md) scripting object is the generic WMI object, defining properties and methods that can be used regardless of the specific WMI object to which the **SWbemObject** object is bound.</span></span> <span data-ttu-id="4b0e5-105">Все объекты WMI, такие как экземпляр [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) или любого другого класса данных WMI, представлены [**SWbemObject**](swbemobject.md) и могут использовать общие свойства и методы **SWbemObject** в дополнение к их собственным свойствам и методам.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-105">All WMI objects, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or any other WMI data class, are represented by [**SWbemObject**](swbemobject.md) and can use the **SWbemObject** common properties and methods in addition to their own particular properties and methods.</span></span>

<span data-ttu-id="4b0e5-106">Например, используйте следующий скрипт, чтобы получить все экземпляры [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , вызвав метод [**SWbemObject \_ . Instances**](swbemobject-instances-.md) .</span><span class="sxs-lookup"><span data-stu-id="4b0e5-106">For example, use the following script to obtain all of the instances of a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) by calling the [**SWbemObject.Instances\_**](swbemobject-instances-.md) method.</span></span> <span data-ttu-id="4b0e5-107">Клсобжпроцесс представляет как определение класса **\_ процесса Win32** , так и [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="4b0e5-107">The clsobjProcess represents both the **Win32\_Process** class definition and an [**SWbemObject**](swbemobject.md).</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="4b0e5-108">В следующем примере получается экземпляр [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) , который представляет службу оповещений, и сохраняет ее в обжалертер.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-108">The following example obtains a specific instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) that represents the Alerter service and stores it in objAlerter.</span></span> <span data-ttu-id="4b0e5-109">Затем можно вызвать либо методы [**SWbemObject**](swbemobject.md) , такие как WScript. Echo Обжалертер. Path \_ , либо методы, определенные классом данных, такие как WScript. Echo обжалертер. State.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-109">You can then call either [**SWbemObject**](swbemobject.md) methods, such as WScript.Echo objAlerter.Path\_, or methods defined by the data class, such as WScript.Echo objAlerter.State.</span></span> <span data-ttu-id="4b0e5-110">Обжалертер, который представляет экземпляр \_ службы Win32 и **SWbemObject**.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-110">objAlerter which represents both an instance of Win32\_Service and an **SWbemObject**.</span></span>


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



<span data-ttu-id="4b0e5-111">Вызов [**SWbemObject. Instances \_**](swbemobject-instances-.md) получает другой универсальный объект скрипта WMI, [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="4b0e5-111">The call to [**SWbemObject.Instances\_**](swbemobject-instances-.md) obtains another generic WMI scripting object, [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="4b0e5-112">Как показано на рисунке, объект **SWbemObjectSet** можно рассматривать как [коллекцию](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="4b0e5-112">As shown, the **SWbemObjectSet** object can be treated as a [collection](accessing-a-collection.md).</span></span>


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



<span data-ttu-id="4b0e5-113">Вы можете найти методы [**SWbemObject**](swbemobject.md) , так как они заканчиваются символом подчеркивания ( \_ ), например [**SWbemObject. Instances \_**](swbemobject-instances-.md).</span><span class="sxs-lookup"><span data-stu-id="4b0e5-113">You can identify the [**SWbemObject**](swbemobject.md) methods because they all end with an underscore (\_), for example, [**SWbemObject.Instances\_**](swbemobject-instances-.md).</span></span>

<span data-ttu-id="4b0e5-114">[**Свбемобжектекс**](swbemobjectex.md) расширяет свойства [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="4b0e5-114">[**SWbemObjectEx**](swbemobjectex.md) extends the properties of [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="4b0e5-115">Например, теперь можно обновить данные любого объекта WMI, например экземпляра [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process), путем вызова [**\_ свбемобжектекс. Refresh**](swbemobjectex-refresh-.md).</span><span class="sxs-lookup"><span data-stu-id="4b0e5-115">For example, you can now update the data of any WMI object, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process), by a call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md).</span></span>

<span data-ttu-id="4b0e5-116">В следующем примере показано, как данные об ошибках на странице системных процессов можно обновлять каждые пять секунд.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-116">The following example shows how the system process page fault data can be refreshed every five seconds.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



<span data-ttu-id="4b0e5-117">Дополнительные сведения об обновлении данных с помощью объекта [**свбемрефрешер**](swbemrefresher.md) см. [в разделе Обновление данных WMI в скриптах](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="4b0e5-117">For more information about refreshing data using an [**SWbemRefresher**](swbemrefresher.md) object, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="4b0e5-118">[**SWbemObject. \_**](swbemobject-put-.md) Write и [**путасинк \_**](swbemobject-putasync-.md) позволяют записывать изменения обратно в любой объект WMI.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-118">The [**SWbemObject.Put\_**](swbemobject-put-.md) and [**PutAsync\_**](swbemobject-putasync-.md) allow you to write changes back to any WMI object.</span></span> <span data-ttu-id="4b0e5-119">Эти методы фиксируют изменения только в объекте в пространстве имен, в котором был создан объект.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-119">These methods only commit changes to an object in the namespace where the object was created.</span></span> <span data-ttu-id="4b0e5-120">Объект можно записать в другое пространство имен с помощью [**свбемсервицесекс.**](swbemservicesex-put.md) WHERE или [**свбемсервицесекс. путасинк**](swbemservicesex-putasync.md).</span><span class="sxs-lookup"><span data-stu-id="4b0e5-120">You can write the object to a different namespace using [**SWbemServicesEx.Put**](swbemservicesex-put.md) or [**SWbemServicesEx.PutAsync**](swbemservicesex-putasync.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b0e5-121">См. также</span><span class="sxs-lookup"><span data-stu-id="4b0e5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b0e5-122">API сценариев для инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="4b0e5-122">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="4b0e5-123">Создание скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="4b0e5-123">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="4b0e5-124">Обновление всего экземпляра</span><span class="sxs-lookup"><span data-stu-id="4b0e5-124">Updating an Entire Instance</span></span>](updating-an-entire-instance.md)
</dt> <dt>

[<span data-ttu-id="4b0e5-125">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="4b0e5-125">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
