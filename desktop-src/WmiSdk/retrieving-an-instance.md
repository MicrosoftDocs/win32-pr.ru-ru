---
description: Получение экземпляра является одной из наиболее распространенных процедур извлечения, которые, скорее всего, будут выполняться в инструментарии WMI.
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: Получение экземпляра WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdacf5fe5c86618eb84d70a5505897a94a7ace2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081522"
---
# <a name="retrieving-a-wmi-instance"></a><span data-ttu-id="a903d-103">Получение экземпляра WMI</span><span class="sxs-lookup"><span data-stu-id="a903d-103">Retrieving a WMI Instance</span></span>

<span data-ttu-id="a903d-104">Получение экземпляра является одной из наиболее распространенных процедур извлечения, которые, скорее всего, будут выполняться в инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="a903d-104">Retrieving an instance is one of the most common retrieval procedures you are likely to perform in WMI.</span></span> <span data-ttu-id="a903d-105">Можно получить существующий экземпляр или создать новый неименованный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a903d-105">You can retrieve an existing instance or create a new unnamed instance.</span></span> <span data-ttu-id="a903d-106">Путь WMI к существующему экземпляру является обязательным параметром.</span><span class="sxs-lookup"><span data-stu-id="a903d-106">The WMI path to the existing instance is a required parameter.</span></span> <span data-ttu-id="a903d-107">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="a903d-107">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

> [!Note]  
> <span data-ttu-id="a903d-108">При предоставлении экземпляра поставщик может не предоставить значение для определенных свойств.</span><span class="sxs-lookup"><span data-stu-id="a903d-108">When providing an instance, a provider may be unable to provide a value for certain properties.</span></span> <span data-ttu-id="a903d-109">Если не указано иное в описании свойства, невозможно определить любое значение из пустого значения.</span><span class="sxs-lookup"><span data-stu-id="a903d-109">Unless otherwise stated in the property description, you cannot infer any meaning from an empty value.</span></span> <span data-ttu-id="a903d-110">Это не следует путать со строкой, имеющей значение **null** .</span><span class="sxs-lookup"><span data-stu-id="a903d-110">This is not to be confused with a string which has a **NULL** value.</span></span> <span data-ttu-id="a903d-111">В этом случае значение заполняется.</span><span class="sxs-lookup"><span data-stu-id="a903d-111">In this case, the value is populated.</span></span> <span data-ttu-id="a903d-112">Он пуст, но имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a903d-112">It is empty but has a value: **NULL**.</span></span>

 

<span data-ttu-id="a903d-113">Получите локальную копию экземпляра с помощью вызова командлета [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a903d-113">Retrieve a local copy of the instance with a call to the PowerShell [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

<span data-ttu-id="a903d-114">**Извлечение экземпляра класса WMI с помощью PowerShell**</span><span class="sxs-lookup"><span data-stu-id="a903d-114">**To retrieve an instance of a WMI class using PowerShell**</span></span>

-   <span data-ttu-id="a903d-115">Вы можете получить конкретные экземпляры с помощью параметров *-Class* и *-Filter* .</span><span class="sxs-lookup"><span data-stu-id="a903d-115">You can retrieve specific instances using the *-class* and *-filter* parameters.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="a903d-116">Экземпляр WMI можно получить с помощью C#, создав объект поиска с помощью [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), а затем заполняя его соответствующими значениями ключа, а затем выполнив поиск этого объекта с помощью вызова [CimSession.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) GetObject.</span><span class="sxs-lookup"><span data-stu-id="a903d-116">You can retrieve a WMI instance using C# by creating a search object using [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), and then filling it with the relevant key values, and then searching for that object with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

<span data-ttu-id="a903d-117">**Извлечение экземпляра класса WMI с помощью C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="a903d-117">**To retrieve an instance of a WMI class using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="a903d-118">Используя пространство имен [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , создайте новый объект [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) с соответствующим именем класса и пространством имен.</span><span class="sxs-lookup"><span data-stu-id="a903d-118">Using the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, create a new [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) object with the relevant class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="a903d-119">Создайте [Цимпроперти](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) , содержащий имя и значение ключевого свойства экземпляра, который нужно найти, и добавьте это свойство в объект класса.</span><span class="sxs-lookup"><span data-stu-id="a903d-119">Create a [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) that contains the name and value of the key property of the instance you wish to search for, and add that property to your class object.</span></span>

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  <span data-ttu-id="a903d-120">Получите объект из WMI с помощью вызова [CimSession.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) GetObject.</span><span class="sxs-lookup"><span data-stu-id="a903d-120">Retrieve the object from WMI with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

<span data-ttu-id="a903d-121">Можно получить либо конкретный экземпляр класса WMI, либо коллекцию экземпляров класса WMI с помощью классов в пространстве имен [System. Management](/dotnet/api/system.management) .</span><span class="sxs-lookup"><span data-stu-id="a903d-121">You can retrieve either a specific WMI class instance, or a collection of WMI class instances, using classes in the [System.Management](/dotnet/api/system.management) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="a903d-122">**System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="a903d-122">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="a903d-123">**Извлечение экземпляра класса WMI с помощью C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="a903d-123">**To retrieve an instance of a WMI class using C# (System.Management)**</span></span>

1.  <span data-ttu-id="a903d-124">Получите локальную копию определенного экземпляра, создав новый [ManagementObject](/dotnet/api/system.management.managementobject)с именем и конкретным значением экземпляра, которое передается в параметре *манажементпас* .</span><span class="sxs-lookup"><span data-stu-id="a903d-124">Retrieve a local copy of a specific instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject), with the name and specific instance value passed in though the *ManagementPath* parameter.</span></span> <span data-ttu-id="a903d-125">Затем можно получить данные экземпляра, явно вызвав [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span><span class="sxs-lookup"><span data-stu-id="a903d-125">You can then retrieve the instance data by explicitly calling [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  <span data-ttu-id="a903d-126">Кроме того, можно получить все экземпляры класса WMI, выполнив поиск их с помощью [манажементобжектсеарчер](/dotnet/api/system.management.managementobjectsearcher), а затем перечислить возвращенные [манажементобжектколлектион](/dotnet/api/system.management.managementobjectcollection).</span><span class="sxs-lookup"><span data-stu-id="a903d-126">Alternately, you can retrieve all instances of a WMI class by searching for them with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher), and then enumerating through the returned [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

    foreach (ManagementObject objDisk in colDisks)
    {
       Console.WriteLine("Device ID : {0}", objDisk["DeviceID"]);
    }

    Console.ReadLine();
    ```

    

    <span data-ttu-id="a903d-127">Можно неявно вызвать метод **Get** , обратившись к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="a903d-127">You can implicitly call the **Get** method by accessing the instance.</span></span> <span data-ttu-id="a903d-128">Дополнительные сведения см. в разделе [получение части экземпляра WMI](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="a903d-128">For more information, see [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

<span data-ttu-id="a903d-129">Получите локальную копию экземпляра, вызвав метод VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) .</span><span class="sxs-lookup"><span data-stu-id="a903d-129">Retrieve a local copy of the instance with a call to the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) method.</span></span>

<span data-ttu-id="a903d-130">**Получение экземпляра класса WMI с помощью VBScript**</span><span class="sxs-lookup"><span data-stu-id="a903d-130">**To retrieve an instance of a WMI class using VBScript**</span></span>

-   <span data-ttu-id="a903d-131">Вызовите GetObject с [**путем к объекту**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) экземпляра, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="a903d-131">Call [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) with the object path of the instance as shown in the following example.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    <span data-ttu-id="a903d-132">Для получения конкретного экземпляра необходимо указать имя как часть пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a903d-132">Retrieving a specific instance requires giving a name as part of the object path.</span></span>

<span data-ttu-id="a903d-133">В C++ вызовите [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="a903d-133">In C++, call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="a903d-134">**Извлечение экземпляра класса WMI с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="a903d-134">**To retrieve an instance of a WMI class using C++**</span></span>

-   <span data-ttu-id="a903d-135">Получите локальную копию экземпляра с вызовом [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="a903d-135">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="a903d-136">Необходимо добавить путь WMI к объекту.</span><span class="sxs-lookup"><span data-stu-id="a903d-136">The WMI path to the object must be included.</span></span>

    <span data-ttu-id="a903d-137">Как следует из названия, [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) получает экземпляр асинхронно, а [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) получает экземпляр синхронно.</span><span class="sxs-lookup"><span data-stu-id="a903d-137">As the name implies, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) retrieves the instance asynchronously, while [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retrieves the instance synchronously.</span></span> <span data-ttu-id="a903d-138">Если вы хотите использовать асинхронный выбор, необходимо реализовать интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="a903d-138">If you want to use asynchronous retrieval, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="a903d-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="a903d-139">Examples</span></span>

<span data-ttu-id="a903d-140">Пример сценария VBScript, используемый в качестве шаблона для получения сведений о классе и экземпляре, см. в разделе пример [скрипта шаблона WMI](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) в коллекции TechNet.</span><span class="sxs-lookup"><span data-stu-id="a903d-140">For a VBScript example to use as a template to retrieve class and instance information, see the [WMI Template Script](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) example on TechNet Gallery.</span></span> <span data-ttu-id="a903d-141">В этом конкретном примере для получения службы WMI используется GetObject.</span><span class="sxs-lookup"><span data-stu-id="a903d-141">This particular example uses GetObject to retrieve the WMI Service.</span></span>

 

 
