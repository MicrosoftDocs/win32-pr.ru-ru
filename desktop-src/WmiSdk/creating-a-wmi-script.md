---
description: Вы можете просматривать любую информацию, доступную через инструментарий WMI, или управлять ею с помощью сценариев.
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: Создание скрипта WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999654"
---
# <a name="creating-a-wmi-script"></a><span data-ttu-id="dfe88-103">Создание скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="dfe88-103">Creating a WMI Script</span></span>

<span data-ttu-id="dfe88-104">Вы можете просматривать любую информацию, доступную через инструментарий WMI, или управлять ею с помощью сценариев.</span><span class="sxs-lookup"><span data-stu-id="dfe88-104">You can view or manipulate any information made available through WMI using scripts.</span></span> <span data-ttu-id="dfe88-105">Сценарии могут быть написаны на любом языке сценариев, поддерживающем размещение сценариев Microsoft ActiveX, включая Visual Basic Scripting Edition (VBScript), PowerShell и Perl.</span><span class="sxs-lookup"><span data-stu-id="dfe88-105">Scripts can be written in any scripting language that supports Microsoft ActiveX script hosting, including Visual Basic Scripting Edition (VBScript), PowerShell, and Perl.</span></span> <span data-ttu-id="dfe88-106">Сервер сценариев Windows (WSH), Active Server страницы и Internet Explorer могут выполнять все сценарии WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-106">Windows Script Host (WSH), Active Server Pages, and Internet Explorer can all host WMI scripts.</span></span>

> [!Note]
>
> <span data-ttu-id="dfe88-107">Основным языком сценариев, который сейчас поддерживает WMI, является PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dfe88-107">The primary scripting language currently supported by WMI is PowerShell.</span></span> <span data-ttu-id="dfe88-108">Однако Инструментарий WMI также содержит надежное тело поддержки сценариев для VBScript и других языков, которые обращаются к [API скриптов для инструментария WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-108">However, WMI also contains a robust body of scripting support for VBScript and other languages that access the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

 

## <a name="wmi-scripting-languages"></a><span data-ttu-id="dfe88-109">Языки сценариев WMI</span><span class="sxs-lookup"><span data-stu-id="dfe88-109">WMI Scripting Languages</span></span>

<span data-ttu-id="dfe88-110">Инструментарий WMI поддерживает два основных языка: PowerShell и VBScript (с помощью сервера сценариев Windows или WSH).</span><span class="sxs-lookup"><span data-stu-id="dfe88-110">The two main languages supported by WMI are PowerShell and VBScript (through the Windows Script Host, or WSH).</span></span>

-   <span data-ttu-id="dfe88-111">**PowerShell** был разработан с учетом тесной интеграции с WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-111">**PowerShell** was designed with tight integration with WMI in mind.</span></span> <span data-ttu-id="dfe88-112">Таким образом, большая часть базовых элементов WMI встроена в командлеты WMI: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)и [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span><span class="sxs-lookup"><span data-stu-id="dfe88-112">As such, much of the underlying elements of WMI are built into the WMI cmdlets: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1), and [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span></span> <span data-ttu-id="dfe88-113">В следующей таблице описаны общие процессы, используемые для доступа к данным WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-113">The following table describes the general processes used for accessing WMI information.</span></span> <span data-ttu-id="dfe88-114">Обратите внимание, что хотя в большинстве этих примеров используется Get-WMIObject, многие командлеты PowerShell WMI имеют одинаковые параметры, такие как *-Class* или *-Credential*.</span><span class="sxs-lookup"><span data-stu-id="dfe88-114">Note that while most of these examples use Get-WMIObject, many of the PowerShell WMI cmdlets have the same parameters, such as *-Class* or *-Credentials*.</span></span> <span data-ttu-id="dfe88-115">Поэтому многие из этих процессов также работают и для других объектов.</span><span class="sxs-lookup"><span data-stu-id="dfe88-115">Therefore, many of these processes also work for other objects.</span></span> <span data-ttu-id="dfe88-116">Более подробное обсуждение PowerShell и инструментария WMI см. в разделе [использование командлета Get-WMiObject](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) и [Windows PowerShell — WMI-подключения](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="dfe88-116">For a more in-depth discussion of PowerShell and WMI, see [Using the Get-WMiObject Cmdlet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) and [Windows PowerShell - the WMI Connection](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span></span>

-   <span data-ttu-id="dfe88-117">Язык **VBScript**, напротив, явно обращается к [API сценариев для WMI](scripting-api-for-wmi.md), как упоминалось выше.</span><span class="sxs-lookup"><span data-stu-id="dfe88-117">**VBScript**, in contrast, explicitly makes calls to the [Scripting API for WMI](scripting-api-for-wmi.md), as mentioned above.</span></span> <span data-ttu-id="dfe88-118">Другие языки, такие как Perl, также могут использовать API скриптов для WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-118">Other languages, such as Perl, can also use the scripting API for WMI.</span></span> <span data-ttu-id="dfe88-119">Однако в рамках этой документации большинство примеров, демонстрирующих API сценариев для WMI, будут использовать VBScript.</span><span class="sxs-lookup"><span data-stu-id="dfe88-119">However, for the purposes of this documentation, most samples that demonstrate the scripting API for WMI will use VBScript.</span></span> <span data-ttu-id="dfe88-120">Однако если методика программирования относится только к VBScript, она будет называться.</span><span class="sxs-lookup"><span data-stu-id="dfe88-120">When a programming technique is specific to VBScript, however, it will be called out.</span></span>

    <span data-ttu-id="dfe88-121">В языке VBScript есть два отдельных способа доступа к инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-121">VBScript has essentially two separate ways of accessing WMI.</span></span> <span data-ttu-id="dfe88-122">Первый — использование объекта [**SWbemLocator**](swbemlocator.md) для подключения к инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-122">The first is using an [**SWbemLocator**](swbemlocator.md) object to connect to WMI.</span></span> <span data-ttu-id="dfe88-123">Кроме того, можно использовать [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) и моникер.</span><span class="sxs-lookup"><span data-stu-id="dfe88-123">Alternately, you can use [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) and a moniker.</span></span> <span data-ttu-id="dfe88-124">Моникер — это строка, которая может описывать ряд элементов: учетные данные, параметры олицетворения, компьютер, к которому необходимо подключиться, [*пространство имен*](gloss-n.md) WMI (общее расположение, в котором Инструментарий WMI хранит группы объектов) и объект WMI, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="dfe88-124">A moniker is a string that can describe a number of elements: your credentials, impersonation settings, what computer you want to connect to, the WMI [*namespace*](gloss-n.md) (ie, the general location where WMI stores groups of objects), and what WMI object you want to retrieve.</span></span> <span data-ttu-id="dfe88-125">Многие из приведенных ниже примеров описывают обе методики.</span><span class="sxs-lookup"><span data-stu-id="dfe88-125">Many of the examples below describe both techniques.</span></span> <span data-ttu-id="dfe88-126">Дополнительные сведения см. в разделе [Создание строки моникера](constructing-a-moniker-string.md) и [Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-126">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md) and [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

    <span data-ttu-id="dfe88-127">Независимо от того, какой метод используется для подключения к WMI, скорее всего, вы получите один или несколько объектов из API скриптов.</span><span class="sxs-lookup"><span data-stu-id="dfe88-127">Regardless of what technique you use to connect to WMI, you will likely retrieve one or more objects from the Scripting API.</span></span> <span data-ttu-id="dfe88-128">Наиболее распространенным является [**SWbemObject**](swbemobject.md), который WMI использует для описания объекта WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-128">The most common is [**SWbemObject**](swbemobject.md), which WMI uses to describe a WMI object.</span></span> <span data-ttu-id="dfe88-129">Кроме того, вы можете использовать объект [**SwbemServices**](swbemservices.md) для описания самой службы WMI или объект [**свбемобжектпас**](swbemobjectpath.md) для описания расположения объекта WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-129">Alternately, you may use an [**SWbemServices**](swbemservices.md) object to describe the WMI service itself, or an [**SWbemObjectPath**](swbemobjectpath.md) object to describe the location of a WMI object.</span></span> <span data-ttu-id="dfe88-130">Дополнительные сведения см. в разделе [Создание скриптов с помощью](scripting-with-swbemobject.md) [вспомогательных объектов](scripting-helper-objects.md)SWbemObject и сценариев.</span><span class="sxs-lookup"><span data-stu-id="dfe88-130">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md) and [Scripting Helper Objects](scripting-helper-objects.md).</span></span>

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a><span data-ttu-id="dfe88-131">Использование инструментария WMI и языка сценариев...</span><span class="sxs-lookup"><span data-stu-id="dfe88-131">Using WMI and a Scripting Language, How Do I...</span></span>

<dl> <dt>

<span data-ttu-id="dfe88-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... подключиться к инструментарию WMI?</span><span class="sxs-lookup"><span data-stu-id="dfe88-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>...connect to WMI?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-133">Для VBScript и API скриптов для WMI извлеките объект [**SwbemServices**](swbemservices.md) с моникером и вызовом [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span><span class="sxs-lookup"><span data-stu-id="dfe88-133">For VBScript and the Scripting API for WMI, retrieve an [**SWbemServices**](swbemservices.md) object with a moniker and a call to [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span></span> <span data-ttu-id="dfe88-134">Кроме того, можно подключиться к серверу с помощью вызова [**SWbemLocator. коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="dfe88-134">Alternately, you can connect to the server with a call to [**SWbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="dfe88-135">Затем можно использовать объект для доступа к определенному пространству имен WMI или экземпляру класса WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-135">You can then use the object to access a specific WMI namespace or WMI class instance.</span></span>

<span data-ttu-id="dfe88-136">Для PowerShell соединение с WMI обычно выполняется непосредственно в вызове командлета. Поэтому никаких дополнительных действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="dfe88-136">For PowerShell, connecting to WMI is generally done directly in the cmdlet call; as such, no additional steps are necessary.</span></span>

<span data-ttu-id="dfe88-137">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md), [Создание строки моникера](constructing-a-moniker-string.md)и [Подключение к WMI с помощью VBScript](connecting-to-wmi-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-137">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md), [Constructing a Moniker String](constructing-a-moniker-string.md), and [Connecting to WMI with VBScript](connecting-to-wmi-with-vbscript.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span data-ttu-id="dfe88-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... получить сведения из инструментария WMI?</span><span class="sxs-lookup"><span data-stu-id="dfe88-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>...retrieve information from WMI?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-139">Для VBScript и API скриптов для WMI используйте функцию извлечения, например [**вбемсервицес. Get**](swbemservices-get.md) или [**вбемсервицес. инстанцесоф**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-139">For VBScript and the Scripting API for WMI, use a retrieval function, such as [**WbemServices.Get**](swbemservices-get.md) or [**WbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span> <span data-ttu-id="dfe88-140">Вы также можете поместить имя класса объекта для извлечения в моникер, что может быть более эффективным.</span><span class="sxs-lookup"><span data-stu-id="dfe88-140">You may also place the class name of the object to retrieve in a moniker, which may be more efficient.</span></span>

<span data-ttu-id="dfe88-141">Для PowerShell используйте параметр *-Class* .</span><span class="sxs-lookup"><span data-stu-id="dfe88-141">For PowerShell, use the *-Class* parameter.</span></span> <span data-ttu-id="dfe88-142">Обратите внимание, что параметр-Class используется по умолчанию. Поэтому вам не нужно явно их задавать.</span><span class="sxs-lookup"><span data-stu-id="dfe88-142">Note that -Class is the default parameter; as such, you don't need to explicitly state it.</span></span>

<span data-ttu-id="dfe88-143">Дополнительные сведения см. в разделе [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-143">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span data-ttu-id="dfe88-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... создаете запрос WMI?</span><span class="sxs-lookup"><span data-stu-id="dfe88-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>...create a WMI query?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-145">Для VBScript и API скриптов для WMI используйте метод [**SWbemServices.Exeккуери**](swbemservices-execquery.md) .</span><span class="sxs-lookup"><span data-stu-id="dfe88-145">For VBScript and the Scripting API for WMI, use the [**SWbemServices.ExecQuery**](swbemservices-execquery.md) method.</span></span>

<span data-ttu-id="dfe88-146">Для PowerShell используйте параметр *-Query* .</span><span class="sxs-lookup"><span data-stu-id="dfe88-146">For PowerShell, use the *-Query* parameter.</span></span> <span data-ttu-id="dfe88-147">Можно также выполнить фильтрацию с помощью параметра *-Filter* .</span><span class="sxs-lookup"><span data-stu-id="dfe88-147">You can also filter using the *-Filter* parameter.</span></span>

<span data-ttu-id="dfe88-148">Дополнительные сведения см. в разделе [запрос WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-148">For more information, see [Querying WMI](querying-wmi.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span data-ttu-id="dfe88-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... перечислить список объектов WMI?</span><span class="sxs-lookup"><span data-stu-id="dfe88-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>...enumerate through a list of WMI objects?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-150">Для VBScript и API скриптов для WMI используйте объект контейнера [**SWbemObjectSet**](swbemobjectset.md) , который рассматривается в скрипте как коллекция, которую можно перечислить.</span><span class="sxs-lookup"><span data-stu-id="dfe88-150">For VBScript and the Scripting API for WMI, use the [**SWbemObjectSet**](swbemobjectset.md) container object, which is treated in script as a collection that can be enumerated.</span></span> <span data-ttu-id="dfe88-151">**SWbemObjectSet** можно извлечь из вызова из [**SwbemServices. Инстанцесоф**](swbemservices-instancesof.md) или [**SWbemServices.Exeккуери**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-151">You can retrieve an **SWbemObjectSet** from a call from [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="dfe88-152">PowerShell может извлекать и управлять перечислениями так же, как и любым другим объектом. в WMI нет ничего особенного.</span><span class="sxs-lookup"><span data-stu-id="dfe88-152">PowerShell is able to retrieve and handle enumerations as it would any other object; there is nothing particularly unique to WMI.</span></span>

<span data-ttu-id="dfe88-153">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-153">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span data-ttu-id="dfe88-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... доступ к другому пространству имен WMI?</span><span class="sxs-lookup"><span data-stu-id="dfe88-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>...access a different WMI namespace?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-155">Для VBScript и API скриптов для инструментария WMI заполните пространство имен в моникере или, в противном случае, можно явно задать пространство имен в вызове [**SwbemLocator. коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="dfe88-155">For VBScript and the Scripting API for WMI, state the namespace in the moniker, or else you can explicitly state the namespace in the call to [**SwbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

<span data-ttu-id="dfe88-156">Для PowerShell используйте параметр *-Namespace* .</span><span class="sxs-lookup"><span data-stu-id="dfe88-156">For PowerShell, use the *-Namespace* parameter.</span></span> <span data-ttu-id="dfe88-157">Пространством имен по умолчанию является root \\ cimV2, однако многие старые классы хранятся в корневом каталоге \\ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dfe88-157">The default namespace is "root\\cimV2"; however, many older classes are stored in "root\\default".</span></span>

<span data-ttu-id="dfe88-158">Чтобы найти расположение данного класса WMI, просмотрите страницу справки.</span><span class="sxs-lookup"><span data-stu-id="dfe88-158">To find the location of a given WMI class, look at the reference page.</span></span> <span data-ttu-id="dfe88-159">Кроме того, можно вручную просмотреть пространство имен с помощью Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="dfe88-159">Alternately, you can manually explore a namespace using get-WmiObject.</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span data-ttu-id="dfe88-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... получить все дочерние экземпляры класса?</span><span class="sxs-lookup"><span data-stu-id="dfe88-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>...retrieve all child instances of a class?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-161">Для языков, которые непосредственно используют API скриптов для WMI и PowerShell, WMI поддерживает получение дочерних классов базового класса.</span><span class="sxs-lookup"><span data-stu-id="dfe88-161">For languages that directly use the Scripting API for WMI and PowerShell, WMI supports retrieving the child classes of a base class.</span></span> <span data-ttu-id="dfe88-162">Таким образом, чтобы получить дочерние экземпляры, необходимо найти только родительский класс.</span><span class="sxs-lookup"><span data-stu-id="dfe88-162">As such, in order to retrieve the child instances, you need to only search for the parent class.</span></span> <span data-ttu-id="dfe88-163">В следующем примере выполняется поиск логического диска CIM, который является предварительно установленным классом WMI, представляющим логические диски в системе на основе Windows. [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldisk)</span><span class="sxs-lookup"><span data-stu-id="dfe88-163">The following example searches for [**CIM\_LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), which is a preinstalled WMI class that represents logical disks on a Windows-based computer system.</span></span> <span data-ttu-id="dfe88-164">Таким образом, при поиске этого родительского класса также возвращаются экземпляры [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), которые используются Windows для описания жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="dfe88-164">As such, searching for this parent class also returns instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which is what Windows uses to describe hard drives.</span></span> <span data-ttu-id="dfe88-165">Дополнительные сведения см. в разделе [модель CIM](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-165">For more information, see [Common Information Model](common-information-model.md).</span></span> <span data-ttu-id="dfe88-166">Инструментарий WMI предоставляет всю схему таких предустановленных классов, которые позволяют получать доступ к управляемым объектам и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="dfe88-166">WMI supplies an entire schema of such preinstalled classes that allow you to access and control managed objects.</span></span> <span data-ttu-id="dfe88-167">Дополнительные сведения см. в разделе [Классы Win32](/windows/desktop/CIMWin32Prov/win32-provider) и [классы WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-167">For more information, see [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider) and [WMI Classes](wmi-classes.md)..</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span data-ttu-id="dfe88-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... находите объект WMI?</span><span class="sxs-lookup"><span data-stu-id="dfe88-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>...locate a WMI object?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-169">Для API скриптов для WMI и PowerShell в WMI используется сочетание пространства имен, имени класса и ключевых свойств для уникальной идентификации данного экземпляра WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-169">For both the Scripting API for WMI and PowerShell, WMI uses a combination of namespace, class name, and key properties to uniquely identify a given WMI instance.</span></span> <span data-ttu-id="dfe88-170">Вместе это называется путем объекта WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe88-170">Together, this is known as the WMI object path.</span></span> <span data-ttu-id="dfe88-171">Для VBScript свойство [**SWbemObject. Path \_**](swbemobject-path-.md) описывает путь для любого объекта, возвращаемого API скриптов.</span><span class="sxs-lookup"><span data-stu-id="dfe88-171">For VBScript, the [**SWbemObject.Path\_**](swbemobject-path-.md) property describes the path for any given object returned by the scripting API.</span></span> <span data-ttu-id="dfe88-172">Для PowerShell каждый объект WMI будет иметь \_ \_ свойство Path.</span><span class="sxs-lookup"><span data-stu-id="dfe88-172">For PowerShell, every WMI object will have a \_\_PATH property.</span></span> <span data-ttu-id="dfe88-173">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md) .</span><span class="sxs-lookup"><span data-stu-id="dfe88-173">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md)</span></span>

<span data-ttu-id="dfe88-174">Помимо пространства имен и имени класса, объект WMI также имеет ключевое свойство, которое однозначно определяет этот экземпляр по сравнению с другими экземплярами на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dfe88-174">In addition to namespace and class name, a WMI object will also have a key property, which uniquely identifies that instance compared to other instances on your machine.</span></span> <span data-ttu-id="dfe88-175">Например, свойство **DeviceID** является ключевым свойством для класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="dfe88-175">For example, the **DeviceID** property is the key property for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="dfe88-176">Дополнительные сведения см. в разделе [MOF-файл (MOF)](managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-176">For more information, see [Managed Object Format (MOF)](managed-object-format--mof-.md).</span></span>

<span data-ttu-id="dfe88-177">Наконец, относительный путь представляет собой сокращенную форму пути и включает имя класса и значение ключа.</span><span class="sxs-lookup"><span data-stu-id="dfe88-177">Finally, the Relative path is simply a shortened form of the path, and includes the class name and key value.</span></span> <span data-ttu-id="dfe88-178">В приведенных ниже примерах путь может иметь \\ \\ вид "имя_компьютера \\ root \\ CIMV2: Win32 \_ LogicalDisk. DeviceID =" D: ", а относительный путь —" "Win32LogicalDisk. DeviceID =" D "" ".</span><span class="sxs-lookup"><span data-stu-id="dfe88-178">In the examples below, the path may be "\\\\computerName\\root\\cimv2:Win32\_LogicalDisk.DeviceID="D:"", while the relative path would be ""Win32LogicalDisk.DeviceID="D""".</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span data-ttu-id="dfe88-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... задать сведения в инструментарии WMI?</span><span class="sxs-lookup"><span data-stu-id="dfe88-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>...set information in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-180">Для VBScript и API скриптов для WMI используйте метод [**SWbemObject. поместил \_**](swbemobject-put-.md) .</span><span class="sxs-lookup"><span data-stu-id="dfe88-180">For VBScript and the Scripting API for WMI, use the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span>

<span data-ttu-id="dfe88-181">Для PowerShell можно либо использовать метод размещения, либо [задать параметр-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="dfe88-181">For PowerShell, you can either use the Put method, or else [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

<span data-ttu-id="dfe88-182">Дополнительные сведения см. в разделе [изменение свойства экземпляра](modifying-an-instance-property.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-182">For more information, see [Modifying an Instance Property](modifying-an-instance-property.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span data-ttu-id="dfe88-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... использовать другие учетные данные?</span><span class="sxs-lookup"><span data-stu-id="dfe88-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>...use different credentials?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-184">Для VBScript и API скриптов для WMI используйте параметры *username* и *Password* в методе [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="dfe88-184">For VBScript and the Scripting API for WMI, use the *UserName* and *Password* parameters in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

<span data-ttu-id="dfe88-185">Для PowerShell используйте параметр *-Credential* .</span><span class="sxs-lookup"><span data-stu-id="dfe88-185">For PowerShell, use the *-Credential* parameter.</span></span>

<span data-ttu-id="dfe88-186">Обратите внимание, что на удаленной системе можно использовать только альтернативные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="dfe88-186">Note that you can only use alternate credentials on a remote system.</span></span> <span data-ttu-id="dfe88-187">Дополнительные сведения см. в разделе [Защита скриптов для клиентов](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-187">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
strComputer = "remoteComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="dfe88-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... доступ к удаленному компьютеру</span><span class="sxs-lookup"><span data-stu-id="dfe88-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>...access a remote computer?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-189">Для VBScript и API скриптов для WMI следует явно указать имя компьютера в моникере или в вызове [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-189">For VBScript and the Scripting API for WMI, explicitly state the name of the computer in either the moniker, or else in the call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="dfe88-190">Дополнительные сведения см. [в статье удаленное подключение к WMI с помощью VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-190">For more information, see [Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span></span>

<span data-ttu-id="dfe88-191">Для PowerShell используйте параметр *-ComputerName* .</span><span class="sxs-lookup"><span data-stu-id="dfe88-191">For PowerShell, use the *-ComputerName* parameter.</span></span> <span data-ttu-id="dfe88-192">Дополнительные сведения см. [в статье удаленное подключение к WMI с помощью PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-192">For more information, see [Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="dfe88-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... задать уровни проверки подлинности и олицетворения?</span><span class="sxs-lookup"><span data-stu-id="dfe88-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>...set the Authentication and Impersonation levels?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-194">Для VBScript и API скриптов для WMI используйте свойство [**SwbemServices. Security \_**](swbemlocator-security-.md) для возвращенного серверного объекта или задайте соответствующие значения в моникере.</span><span class="sxs-lookup"><span data-stu-id="dfe88-194">For VBScript and the Scripting API for WMI, use the [**SWbemServices.Security\_**](swbemlocator-security-.md) property on the returned server object, or else set the relevant values in the moniker.</span></span>

<span data-ttu-id="dfe88-195">Для PowerShell используйте параметры *-authentication* и *-Impersonation* соответственно.</span><span class="sxs-lookup"><span data-stu-id="dfe88-195">For PowerShell, use the *-Authentication* and *-Impersonation* parameters, respectively.</span></span> <span data-ttu-id="dfe88-196">Дополнительные сведения см. в разделе [Защита скриптов для клиентов](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-196">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

<span data-ttu-id="dfe88-197">Дополнительные сведения см. в разделе [Защита скриптов для клиентов](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-197">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="dfe88-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... Обработайте ошибки в WMI?</span><span class="sxs-lookup"><span data-stu-id="dfe88-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>...handle errors in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="dfe88-199">Для API скриптов для инструментария WMI поставщик может предоставить объект [**свбемластеррор**](swbemlasterror.md) , чтобы получить дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="dfe88-199">For the Scripting API for WMI, the provider may supply an [**SWbemLastError**](swbemlasterror.md) object to give further information on an error.</span></span>

<span data-ttu-id="dfe88-200">В частности, в VBScript также поддерживается обработка ошибок с помощью собственного объекта **Err** .</span><span class="sxs-lookup"><span data-stu-id="dfe88-200">In VBScript in particular, error handling is also supported using the native **Err** object.</span></span> <span data-ttu-id="dfe88-201">Вы также можете получить доступ к объекту [**свбемластеррор**](swbemlasterror.md), как описано выше.</span><span class="sxs-lookup"><span data-stu-id="dfe88-201">You may also access the [**SWbemLastError**](swbemlasterror.md)object, as described above.</span></span> <span data-ttu-id="dfe88-202">Дополнительные сведения см. в разделе [Получение кода ошибки](retrieving-an-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="dfe88-202">For more information, see [Retrieving an Error Code](retrieving-an-error-code.md).</span></span>

<span data-ttu-id="dfe88-203">Для PowerShell можно использовать стандартные методы обработки ошибок PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dfe88-203">For PowerShell, you can use the standard PowerShell error handling techniques.</span></span> <span data-ttu-id="dfe88-204">Дополнительные сведения см. в статье [Введение в обработку ошибок в PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span><span class="sxs-lookup"><span data-stu-id="dfe88-204">For more information, see [An Introduction to Error Handling in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span></span>


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 
