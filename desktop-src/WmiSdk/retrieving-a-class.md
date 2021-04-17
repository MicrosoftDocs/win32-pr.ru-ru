---
description: Первый тип объекта, который можно извлечь, — это класс WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Получение класса WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9378854eb483c6cdac7ddee47d581d8876270e97
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "105693886"
---
# <a name="retrieving-a-wmi-class"></a><span data-ttu-id="c000a-103">Получение класса WMI</span><span class="sxs-lookup"><span data-stu-id="c000a-103">Retrieving a WMI Class</span></span>

<span data-ttu-id="c000a-104">Первый тип объекта, который можно извлечь, — это класс WMI.</span><span class="sxs-lookup"><span data-stu-id="c000a-104">The first type of object you can retrieve is a WMI class.</span></span> <span data-ttu-id="c000a-105">При извлечении класса WMI фактически извлекается определение класса, которое представляет собой список свойств, квалификаторов и методов, которые полностью описывают класс.</span><span class="sxs-lookup"><span data-stu-id="c000a-105">When retrieving a WMI class, you actually retrieve a class definition, which is a listing of the properties, qualifiers, and methods that fully describe the class.</span></span> <span data-ttu-id="c000a-106">Однако определение класса по сути является самим классом.</span><span class="sxs-lookup"><span data-stu-id="c000a-106">However, a class definition is basically the class itself.</span></span>

<span data-ttu-id="c000a-107">PowerShell использует стандартный запрос для получения определений классов с помощью класса **мета- \_ класса** .</span><span class="sxs-lookup"><span data-stu-id="c000a-107">PowerShell uses a standard query to retrieve class definitions, using the **meta\_class** class.</span></span>

<span data-ttu-id="c000a-108">**Извлечение определения класса в PowerShell**</span><span class="sxs-lookup"><span data-stu-id="c000a-108">**To retrieve a class definition in PowerShell**</span></span>

-   <span data-ttu-id="c000a-109">Используйте [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) с запросом к **\_ классу meta** с предложением WHERE, содержащим имя класса, который вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="c000a-109">Use the [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    <span data-ttu-id="c000a-110">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) — это стандартный командлет, используемый PowerShell для получения сведений о классах и экземплярах из WMI.</span><span class="sxs-lookup"><span data-stu-id="c000a-110">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) is the standard cmdlet PowerShell uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="c000a-111">Класс **мета- \_ класса** определяет запрос в виде запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="c000a-111">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="c000a-112">Без класса **\_ класса meta** этот запрос возвратит все экземпляры Win32 \_ LogicalDisk.</span><span class="sxs-lookup"><span data-stu-id="c000a-112">Without the **meta\_class** class, this query would return all instances of Win32\_LogicalDisk.</span></span> <span data-ttu-id="c000a-113">Дополнительные сведения о запросах WMI см. в разделе [инструкция SELECT для запросов схемы](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="c000a-113">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="c000a-114">Текущим процессом получения определения WMI в C# является использование класса **CIMInstance** .</span><span class="sxs-lookup"><span data-stu-id="c000a-114">The current process for retrieving a WMI definition in C# is to use **CIMInstance** class.</span></span>

<span data-ttu-id="c000a-115">**Извлечение определения класса в C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="c000a-115">**To retrieve a class definition in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="c000a-116">С помощью пространства имен **Microsoft. Management. Infrastructure** создайте класс **CIMInstance** с указанным пространством имен и именем класса.</span><span class="sxs-lookup"><span data-stu-id="c000a-116">Using the **Microsoft.Management.Infrastructure** namespace, create a **CIMInstance** class with the specified namespace and class name.</span></span>

    <span data-ttu-id="c000a-117">Созданный класс будет содержать все сведения о классе, но не данные экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c000a-117">The created class will contain all of the class information, but no instance data.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="c000a-118">Кроме того, как и в случае с PowerShell, можно также выполнить запрос, используя тег **мета- \_ класса** в составе запроса.</span><span class="sxs-lookup"><span data-stu-id="c000a-118">Alternately, as with PowerShell, you could also perform a query, using the **meta\_class** tag as part of the query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

<span data-ttu-id="c000a-119">Как и в PowerShell, в C# для получения определений классов используется запрос **мета- \_ класса** .</span><span class="sxs-lookup"><span data-stu-id="c000a-119">As with PowerShell, C# uses a **meta\_class** query to retrieve class definitions.</span></span> <span data-ttu-id="c000a-120">Кроме того, можно создать объект **манажементкласс** для непосредственного доступа к определению класса.</span><span class="sxs-lookup"><span data-stu-id="c000a-120">Alternately, you can create a **ManagementClass** object to access the class definition directly.</span></span>

> [!Note]  
> <span data-ttu-id="c000a-121">**System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="c000a-121">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="c000a-122">**Извлечение определения класса в C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="c000a-122">**To retrieve a class definition in C# (System.Management)**</span></span>

1.  <span data-ttu-id="c000a-123">Можно использовать [манажементобжектсерарчер](/dotnet/api/system.management.managementobjectsearcher) с запросом к **\_ классу meta** с предложением WHERE, содержащим имя класса, который вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="c000a-123">You can use the [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    <span data-ttu-id="c000a-124">[Манажементобжектсерарчер](/dotnet/api/system.management.managementobjectsearcher) — это стандартный класс, используемый .NET для получения сведений о классе и экземпляре из WMI.</span><span class="sxs-lookup"><span data-stu-id="c000a-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) is the standard class .NET uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="c000a-125">[Манажементобжектсерарчер. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) возвращает [манажементобжектколлектион](/dotnet/api/system.management.managementobjectcollection) , содержащий класс определения схемы.</span><span class="sxs-lookup"><span data-stu-id="c000a-125">[ManagementObjectSerarcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains the schema definition class.</span></span> <span data-ttu-id="c000a-126">Класс **мета- \_ класса** определяет запрос в виде запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="c000a-126">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="c000a-127">Без класса **\_ класса meta** этот запрос возвратит все экземпляры [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="c000a-127">Without the **meta\_class** class, this query would return all instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="c000a-128">Дополнительные сведения о запросах WMI см. в разделе [инструкция SELECT для запросов схемы](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="c000a-128">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

2.  <span data-ttu-id="c000a-129">Кроме того, можно создать новый объект [манажементкласс](/dotnet/api/system.management.managementclass) с именем в качестве пути, чтобы получить класс.</span><span class="sxs-lookup"><span data-stu-id="c000a-129">Alternately, create a new [ManagementClass](/dotnet/api/system.management.managementclass) object, with the name as the path, to retrieve the class.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

<span data-ttu-id="c000a-130">Вы можете получить определение класса в VBScript аналогичным образом, чтобы извлечь конкретный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="c000a-130">You can retrieve a class definition in VBScript in a similar way to retrieving a specific instance.</span></span>

<span data-ttu-id="c000a-131">**Извлечение определения класса в VBScript**</span><span class="sxs-lookup"><span data-stu-id="c000a-131">**To retrieve a class definition in VBScript**</span></span>

1.  <span data-ttu-id="c000a-132">Вызовите [**SwbemServices. Get**](swbemservices-get.md) , но не вызывайте конкретный экземпляр в пути объекта для класса.</span><span class="sxs-lookup"><span data-stu-id="c000a-132">Call [**SWbemServices.Get**](swbemservices-get.md) but do not identify a specific instance in the object path for the class.</span></span>
2.  <span data-ttu-id="c000a-133">В следующем примере кода извлекается определение класса, описывающего логические диски на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c000a-133">The following code example retrieves the class definition for the class that describes logical drives on your computer.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    <span data-ttu-id="c000a-134">Сервер сценариев Windows (WSH) также поддерживает следующие сценарии.</span><span class="sxs-lookup"><span data-stu-id="c000a-134">Windows Script Host (WSH) also supports the following.</span></span>

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    <span data-ttu-id="c000a-135">На Active Server страницах (ASP) используйте [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) или [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) в скрипте на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="c000a-135">On Active Server Pages (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) or [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) in the server-side script.</span></span> <span data-ttu-id="c000a-136">Дополнительные сведения см. в разделе [Создание страниц Active Server для инструментария WMI](creating-active-server-pages-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c000a-136">For more information, see [Creating Active Server Pages for WMI](creating-active-server-pages-for-wmi.md).</span></span>

3.  <span data-ttu-id="c000a-137">Можно также указать класс или экземпляр, в этом случае возвращаемый объект является объектом WMI, например, экземпляром [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), а не объектом служб.</span><span class="sxs-lookup"><span data-stu-id="c000a-137">A class or instance can also be specified, in which case the returned object is a WMI object, for example, an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), rather than a services object.</span></span> <span data-ttu-id="c000a-138">Обратите внимание, что функции языка VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) нельзя использовать для создания экземпляра универсального объекта [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="c000a-138">Note that you cannot use the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) functions to create an instance of the generic object [**SWbemObject**](swbemobject.md).</span></span>
4.  <span data-ttu-id="c000a-139">В HTML-страницах, выполняющихся в Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) и [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) могут завершиться ошибкой, так как объекты сценариев WMI, такие как элементы управления ActiveX, не помечены как надежные для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="c000a-139">In HTML pages running in Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) and [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) can fail because WMI scripting objects, like ActiveX controls, are not marked as safe for scripting.</span></span> <span data-ttu-id="c000a-140">Единственным исключением является объект [**SWbemDateTime**](swbemdatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="c000a-140">The one exception is the [**SWbemDateTime**](swbemdatetime.md) object.</span></span> <span data-ttu-id="c000a-141">Единственный способ, которым эти вызовы могут быть выполнены, — это понизить параметры безопасности ОБОЗРЕВАТЕЛЯ, что не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c000a-141">The only way that these calls can succeed is when you lower the IE security settings, which is not recommended.</span></span>

<span data-ttu-id="c000a-142">При извлечении класса в C++ вызывайте версию [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) [**объекта GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="c000a-142">When retrieving a class in C++, call the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) version of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="c000a-143">**Извлечение определения класса в C++**</span><span class="sxs-lookup"><span data-stu-id="c000a-143">**To retrieve a class definition in C++**</span></span>

1.  <span data-ttu-id="c000a-144">Вызовите методы [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) , чтобы получить определение класса.</span><span class="sxs-lookup"><span data-stu-id="c000a-144">Call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to retrieve the definition of a class.</span></span>
2.  <span data-ttu-id="c000a-145">Один класс может иметь несколько определений классов, что обычно происходит при загрузке нескольких поставщиков классов в одно пространство имен.</span><span class="sxs-lookup"><span data-stu-id="c000a-145">One class can have multiple class definitions, which happens typically when you have more than one class provider loaded into one namespace.</span></span> <span data-ttu-id="c000a-146">Если класс имеет несколько определений классов, Инструментарий WMI возвращает первое обнаруженное определение и код состояния для **\_ \_ дублирования \_ объектов WBEM** .</span><span class="sxs-lookup"><span data-stu-id="c000a-146">When a class has multiple class definitions, WMI returns the first definition discovered and the **WBEM\_S\_DUPLICATE\_OBJECTS** status code.</span></span>

<span data-ttu-id="c000a-147">Поскольку [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) Возвращает определение класса, он обычно используется в качестве первого шага при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c000a-147">Because [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) returns a class definition, it is commonly used as the first step in creating an instance.</span></span> <span data-ttu-id="c000a-148">Дополнительные сведения об использовании **GetObject** см. в разделе [Создание и объявление экземпляра с помощью C++](creating-and-declaring-an-instance-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="c000a-148">For more information on how to use **GetObject**, see [Creating and Declaring an Instance Using C++](creating-and-declaring-an-instance-using-c-.md).</span></span>

 

 
