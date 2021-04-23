---
description: Перечисление — это процесс перемещения по набору объектов и, возможно, изменения каждого объекта.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Перечисление WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711737"
---
# <a name="enumerating-wmi"></a><span data-ttu-id="436bf-103">Перечисление WMI</span><span class="sxs-lookup"><span data-stu-id="436bf-103">Enumerating WMI</span></span>

<span data-ttu-id="436bf-104">Перечисление — это процесс перемещения по набору объектов и, возможно, изменения каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="436bf-104">Enumeration is the act of moving through a set of objects and possibly modifying each object as you do so.</span></span> <span data-ttu-id="436bf-105">Например, можно перечислить набор объектов [**Win32 \_ дискдриве**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , чтобы найти конкретный серийный номер.</span><span class="sxs-lookup"><span data-stu-id="436bf-105">For example, you can enumerate through a set of [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) objects to find a particular serial number.</span></span> <span data-ttu-id="436bf-106">Обратите внимание, что хотя можно перечислить любой объект, Инструментарий WMI возвращает только те объекты, к которым у вас есть доступ.</span><span class="sxs-lookup"><span data-stu-id="436bf-106">Note that although you can enumerate any object, WMI only returns objects to which you have security access.</span></span>

<span data-ttu-id="436bf-107">Перечисления больших наборов данных могут потребовать большого количества ресурсов и снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="436bf-107">Enumerations of large data sets can require a large amount of resources and degrade performance.</span></span> <span data-ttu-id="436bf-108">Дополнительные сведения см. в разделе [повышение производительности перечисления](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-108">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span> <span data-ttu-id="436bf-109">Вы также можете запросить данные с более конкретным запросом.</span><span class="sxs-lookup"><span data-stu-id="436bf-109">You also can request data with a more specific query.</span></span> <span data-ttu-id="436bf-110">Дополнительные сведения см. в разделе [запрос WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-110">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="436bf-111">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="436bf-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="436bf-112">Перечисление WMI с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="436bf-112">Enumerating WMI Using PowerShell</span></span>](#enumerating-wmi-using-powershell)
-   [<span data-ttu-id="436bf-113">Перечисление WMI с помощью C# (Microsoft. Management. Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="436bf-113">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [<span data-ttu-id="436bf-114">Перечисление WMI с помощью C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="436bf-114">Enumerating WMI Using C# (System.Management)</span></span>](#enumerating-wmi-using-c-systemmanagement)
-   [<span data-ttu-id="436bf-115">Перечисление WMI с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="436bf-115">Enumerating WMI Using VBScript</span></span>](#enumerating-wmi-using-vbscript)
-   [<span data-ttu-id="436bf-116">Перечисление WMI с помощью C++</span><span class="sxs-lookup"><span data-stu-id="436bf-116">Enumerating WMI Using C++</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a><span data-ttu-id="436bf-117">Перечисление WMI с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="436bf-117">Enumerating WMI Using PowerShell</span></span>

<span data-ttu-id="436bf-118">Если вы не узнаете путь к объекту для конкретного экземпляра или хотите получить все экземпляры для конкретного класса, используйте [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx)с именем класса в параметре *-Class* .</span><span class="sxs-lookup"><span data-stu-id="436bf-118">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), with the name of the class in the *-class* parameter.</span></span> <span data-ttu-id="436bf-119">Если вы хотите использовать запрос, можно использовать параметр *-Query* .</span><span class="sxs-lookup"><span data-stu-id="436bf-119">If you want to use a query, you can use the *-query* parameter.</span></span>

<span data-ttu-id="436bf-120">Следующая процедура описывает, как перечислить экземпляры класса с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="436bf-120">The following procedure describes how to enumerate the instances of a class using PowerShell.</span></span>

<span data-ttu-id="436bf-121">**Перечисление экземпляров класса с помощью PowerShell**</span><span class="sxs-lookup"><span data-stu-id="436bf-121">**To enumerate the instances of a class using PowerShell**</span></span>

1.  <span data-ttu-id="436bf-122">Перечислите экземпляры с помощью вызова командлета [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) .</span><span class="sxs-lookup"><span data-stu-id="436bf-122">Enumerate the instances with a call to [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

    <span data-ttu-id="436bf-123">Командлет [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) Возвращает коллекцию из одного или нескольких объектов WMI, с помощью которых можно выполнить перечисление.</span><span class="sxs-lookup"><span data-stu-id="436bf-123">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) returns a collection of one or more WMI objects, through which you can enumerate.</span></span> <span data-ttu-id="436bf-124">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-124">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

    <span data-ttu-id="436bf-125">Если вы хотите получить экземпляр класса WMI в другом пространстве имен или на другом компьютере, укажите компьютер и пространство имен в параметрах *-Computer* и *-Namespace* соответственно.</span><span class="sxs-lookup"><span data-stu-id="436bf-125">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *-computer* and *-namespace* parameters, respectively.</span></span> <span data-ttu-id="436bf-126">Дополнительные сведения см. [в разделе Создание скрипта WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="436bf-127">Это работает только при наличии соответствующих прав доступа.</span><span class="sxs-lookup"><span data-stu-id="436bf-127">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="436bf-128">Дополнительные сведения см. в разделе [поддержание безопасности WMI](maintaining-wmi-security.md) и [выполнение привилегированных операций](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-128">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="436bf-129">Получите отдельные экземпляры, в которых вы хотите использовать элементы коллекции.</span><span class="sxs-lookup"><span data-stu-id="436bf-129">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="436bf-130">В следующем примере кода извлекается коллекция PowerShell, а затем отображается свойство Size для всех экземпляров логических дисков на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="436bf-130">The following code example retrieves an PowerShell collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
$objCol = get-wmiobject -class "Win32_LogicalDisk"

# Or, alternately
#$objCol = get-wmiobject -Query "SELECT * FROM Win32_LogicalDisk"

foreach ($Drive in $objCol)
{
    if ($Drive.size -ne $null)
    { "Drive " + $Drive.deviceID + " contains " + $Drive.size + " bytes" }
    else
    { "Drive " + $Drive.deviceID + " is not available." }
}
```



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a><span data-ttu-id="436bf-131">Перечисление WMI с помощью C# (Microsoft. Management. Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="436bf-131">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>

1.  <span data-ttu-id="436bf-132">Добавьте ссылку на сборку ссылки на **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="436bf-132">Add a reference to the **Microsoft.Management.Infrastructure** reference assembly.</span></span> <span data-ttu-id="436bf-133">(Эта сборка входит в состав [пакета средств разработки программного обеспечения (SDK) для Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)</span><span class="sxs-lookup"><span data-stu-id="436bf-133">(This assembly ships as part of the [Windows Software Development Kit (SDK) for Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)</span></span>
2.  <span data-ttu-id="436bf-134">Добавьте инструкцию **using** для пространства имен **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="436bf-134">Add a **using** statement for the **Microsoft.Management.Infrastructure** namespace.</span></span>

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  <span data-ttu-id="436bf-135">Создайте экземпляр объекта [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="436bf-135">Instantiate a [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object.</span></span> <span data-ttu-id="436bf-136">В следующем фрагменте используется стандартное значение localhost для метода [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="436bf-136">The following snippet uses the standard "localhost" value for the [**CimSession.Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) method.</span></span>

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  <span data-ttu-id="436bf-137">Вызовите метод [**CimSession. куеринстанцес**](https://www.bing.com/search?q=**CimSession.QueryInstances**) , передав требуемое пространство имен CIM и WQL для использования.</span><span class="sxs-lookup"><span data-stu-id="436bf-137">Call the [**CimSession.QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) method passing the desired CIM namespace and WQL to use.</span></span> <span data-ttu-id="436bf-138">Следующий фрагмент кода возвратит два экземпляра, представляющие два стандартных процесса Windows, где свойство Handle (представляющее идентификатор процесса или PID) имеет значение 0 или 4.</span><span class="sxs-lookup"><span data-stu-id="436bf-138">The following snippet will return two instances representing two standard Windows processes where the handle property (representing a process ID, or PID) has a value of either 0 or 4.</span></span>

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  <span data-ttu-id="436bf-139">Перебрать возвращенные объекты [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) .</span><span class="sxs-lookup"><span data-stu-id="436bf-139">Loop through the returned [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) objects.</span></span>

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

<span data-ttu-id="436bf-140">В следующем образце кода перечисляются все экземпляры класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) (который представляет активные процессы) на локальном компьютере и выводится имя каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="436bf-140">The following code sample enumerates all instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class (which represents active processes) on the local machine, and prints the name of each process.</span></span>

> [!Note]  
> <span data-ttu-id="436bf-141">В реальном приложении вы определите в качестве параметров имя компьютера ("localhost") и пространство имен CIM ("root \\ CIMV2").</span><span class="sxs-lookup"><span data-stu-id="436bf-141">In a real application you would define as parameters the computer name ("localhost") and CIM namespace ("root\\cimv2").</span></span> <span data-ttu-id="436bf-142">В этом примере в целях простоты они были жестко закодированы.</span><span class="sxs-lookup"><span data-stu-id="436bf-142">For purposes of simplicity, these have been hardcoded in this example.</span></span>

 


```CSharp
using System;
using System.Collections.Generic;
using Microsoft.Management.Infrastructure;

public partial class MI
{
    static void PrintCimInstance(CimInstance cimInstance)
    {
        Console.ForegroundColor = ConsoleColor.Blue;
        Console.WriteLine("{0} properties", cimInstance.CimSystemProperties.ClassName);
        Console.ResetColor();

        Console.WriteLine(String.Format("{0,-5}{1,-30}{2,-15}{3,-10}", 
                                        "Key?", "Property", "Type", "Value"));

        foreach (var enumeratedProperty in cimInstance.CimInstanceProperties)
        {
            bool isKey = ((enumeratedProperty.Flags & CimFlags.Key) == CimFlags.Key);

            if (enumeratedProperty.Value != null)
            {
                Console.WriteLine(
                    "{0,-5}{1,-30}{2,-15}{3,-10}",
                    isKey == true ? "Y" : string.Empty,
                    enumeratedProperty.Name,
                    enumeratedProperty.CimType,
                    enumeratedProperty.Value);
            }
        }
        Console.WriteLine();
    }

    public static void QueryInstance(string query)
    {
        try
        {
            CimSession cimSession = CimSession.Create("localhost");

            IEnumerable<CimInstance> queryInstances = 
              cimSession.QueryInstances(@"root\cimv2", "WQL", query);
            foreach (CimInstance cimInstance in queryInstances)
            {
                //Use the current instance. This example prints the instance. 
                PrintCimInstance(cimInstance);
            }
        }
         catch (CimException ex) 
        { 
            // Handle the exception as appropriate.
            // This example prints the message.
            Console.WriteLine(ex.Message); 
        }
    }
}
```


```CSharp

using System;

namespace MIClientManaged
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Write(&quot;Enter WQL (x = Quit): &quot;);
                string query = Console.ReadLine().ToUpper();
                if (query.CompareTo(&quot;X&quot;) == 0) break;
                MI.QueryInstance(query);
            }
        }
    }
}
```





## <a name="enumerating-wmi-using-c-systemmanagement"></a><span data-ttu-id="436bf-143">Перечисление WMI с помощью C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="436bf-143">Enumerating WMI Using C# (System.Management)</span></span>

<span data-ttu-id="436bf-144">Если вы не узнаете путь к объекту для конкретного экземпляра или хотите получить все экземпляры для конкретного класса, используйте объект [манажементкласс](/dotnet/api/system.management.managementclass) для получения [манажементобжектколлектион](/dotnet/api/system.management.managementobjectcollection) , содержащего все экземпляры данного класса в пространстве имен WMI.</span><span class="sxs-lookup"><span data-stu-id="436bf-144">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [ManagementClass](/dotnet/api/system.management.managementclass) object to retrieve a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains all instances of a given class in the WMI namespace.</span></span> <span data-ttu-id="436bf-145">Кроме того, можно запросить WMI с помощью [манажементобжектсеарчер](/dotnet/api/system.management.managementobjectsearcher) , чтобы получить один и тот же набор объектов.</span><span class="sxs-lookup"><span data-stu-id="436bf-145">Alternately, you can query WMI through a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) to obtain the same set of objects.</span></span>

> [!Note]  
> <span data-ttu-id="436bf-146">**System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="436bf-146">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="436bf-147">В следующей процедуре описывается перечисление экземпляров класса с помощью C#.</span><span class="sxs-lookup"><span data-stu-id="436bf-147">The following procedure describes how to enumerate the instances of a class using C#.</span></span>

<span data-ttu-id="436bf-148">**Перечисление экземпляров класса с помощью C #**</span><span class="sxs-lookup"><span data-stu-id="436bf-148">**To enumerate the instances of a class using C#**</span></span>

1.  <span data-ttu-id="436bf-149">Перечислите экземпляры с помощью вызова [манажементкласс.](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances)GetEnumerator.</span><span class="sxs-lookup"><span data-stu-id="436bf-149">Enumerate the instances with a call to [ManagementClass.GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span></span>

    <span data-ttu-id="436bf-150">Метод [WebMethod](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) Возвращает коллекцию или набор объектов, с помощью которых можно выполнить перечисление.</span><span class="sxs-lookup"><span data-stu-id="436bf-150">The [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="436bf-151">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-151">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="436bf-152">Возвращаемая коллекция фактически является объектом [манажементобжектколлектион](/dotnet/api/system.management.managementobjectcollection) , поэтому можно вызывать любой из методов этого объекта.</span><span class="sxs-lookup"><span data-stu-id="436bf-152">The returned collection is actually an [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="436bf-153">Если вы хотите получить экземпляр класса WMI в другом пространстве имен или на другом компьютере, укажите компьютер и пространство имен в параметре *path* .</span><span class="sxs-lookup"><span data-stu-id="436bf-153">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *path* parameter.</span></span> <span data-ttu-id="436bf-154">Дополнительные сведения см. [в разделе Создание скрипта WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-154">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="436bf-155">Это работает только при наличии соответствующих прав доступа.</span><span class="sxs-lookup"><span data-stu-id="436bf-155">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="436bf-156">Дополнительные сведения см. в разделе [поддержание безопасности WMI](maintaining-wmi-security.md) и [выполнение привилегированных операций](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-156">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="436bf-157">Получите отдельные экземпляры, в которых вы хотите использовать элементы коллекции.</span><span class="sxs-lookup"><span data-stu-id="436bf-157">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="436bf-158">В следующем примере кода извлекается коллекция C#, а затем отображается свойство Size для всех экземпляров логических дисков на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="436bf-158">The following code example retrieves an C# collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
using System.Management;
...

ManagementClass mc = new ManagementClass("Win32_LogicalDisk");
ManagementObjectCollection objCol = mc.GetInstances();

//or, alternately
//ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
//ManagementObjectCollection objCol = mgmtObjSearcher.Get();

if (objCol.Count != 0)
{
   foreach (ManagementObject Drive in objCol)
   {
      if (Drive["size"] != null)
      {
         Console.WriteLine("Drive {0} contains {1} bytes.", Drive["deviceID"], Drive["size"]);
      }
      else
      {
         Console.WriteLine("Drive {0} is not available.", Drive["deviceID"]);
      }
   }
}
Console.ReadLine();
```



## <a name="enumerating-wmi-using-vbscript"></a><span data-ttu-id="436bf-159">Перечисление WMI с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="436bf-159">Enumerating WMI Using VBScript</span></span>

<span data-ttu-id="436bf-160">Если вы не узнаете путь к объекту для конкретного экземпляра или хотите получить все экземпляры для конкретного класса, используйте метод [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md) , чтобы вернуть перечисление [**SWbemObjectSet**](swbemobjectset.md) для всех экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="436bf-160">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method to return an [**SWbemObjectSet**](swbemobjectset.md) enumeration of all the instances of a class.</span></span> <span data-ttu-id="436bf-161">Кроме того, можно запросить WMI с помощью [**SWbemServices.Exeккуери**](swbemservices-execquery.md) , чтобы получить тот же набор объектов.</span><span class="sxs-lookup"><span data-stu-id="436bf-161">Alternatively you can query WMI through [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to obtain the same set of objects.</span></span>

<span data-ttu-id="436bf-162">Следующая процедура описывает, как перечислить экземпляры класса с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="436bf-162">The following procedure describes how to enumerate the instances of a class using VBScript.</span></span>

<span data-ttu-id="436bf-163">**Перечисление экземпляров класса с помощью VBScript**</span><span class="sxs-lookup"><span data-stu-id="436bf-163">**To enumerate the instances of a class using VBScript**</span></span>

1.  <span data-ttu-id="436bf-164">Перечислите экземпляры с помощью вызова метода [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md) .</span><span class="sxs-lookup"><span data-stu-id="436bf-164">Enumerate the instances with a call to the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method.</span></span>

    <span data-ttu-id="436bf-165">Метод [**инстанцесоф**](swbemservices-instancesof.md) Возвращает коллекцию или набор объектов, с помощью которых можно выполнить перечисление.</span><span class="sxs-lookup"><span data-stu-id="436bf-165">The [**InstancesOf**](swbemservices-instancesof.md) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="436bf-166">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-166">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="436bf-167">Возвращаемая коллекция фактически является объектом [**SWbemObjectSet**](swbemobjectset.md) , поэтому можно вызывать любой из методов этого объекта.</span><span class="sxs-lookup"><span data-stu-id="436bf-167">The returned collection is actually an [**SWbemObjectSet**](swbemobjectset.md) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="436bf-168">Если вы хотите получить экземпляр класса WMI в другом пространстве имен или на другом компьютере, укажите компьютер и пространство имен в моникере.</span><span class="sxs-lookup"><span data-stu-id="436bf-168">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the moniker.</span></span> <span data-ttu-id="436bf-169">Дополнительные сведения см. [в разделе Создание скрипта WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-169">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="436bf-170">Это работает только при наличии соответствующих прав доступа.</span><span class="sxs-lookup"><span data-stu-id="436bf-170">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="436bf-171">Дополнительные сведения см. в разделе [поддержание безопасности WMI](maintaining-wmi-security.md) и [выполнение привилегированных операций](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-171">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="436bf-172">Получите отдельные экземпляры, которые вы хотите использовать с помощью методов коллекций.</span><span class="sxs-lookup"><span data-stu-id="436bf-172">Retrieve any individual instances you wish using the collections methods.</span></span>

<span data-ttu-id="436bf-173">В следующем примере кода извлекается объект [**SwbemServices**](swbemservices.md) , а затем выполняется метод [**инстанцесоф**](swbemservices-instancesof.md) для вывода свойства Size для всех экземпляров логических дисков на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="436bf-173">The following code example retrieves an [**SWbemServices**](swbemservices.md) object and then executes the [**InstancesOf**](swbemservices-instancesof.md) method to display the size property for all instances of logical drives on the local computer.</span></span>


```VB
Set objCol = GetObject("WinMgmts:").InstancesOf("Win32_LogicalDisk")
For Each Drive In objCol
    If Not IsNull(Drive.Size) Then    
       WScript.Echo ("Drive " & Drive.deviceid & " contains " & Drive.Size & " bytes")
    Else
       WScript.Echo ("Drive " & Drive.deviceid & " is not available.")
    End If
Next
```



## <a name="enumerating-wmi-using-c"></a><span data-ttu-id="436bf-174">Перечисление WMI с помощью C++</span><span class="sxs-lookup"><span data-stu-id="436bf-174">Enumerating WMI Using C++</span></span>

<span data-ttu-id="436bf-175">Помимо выполнения базового перечисления, можно задать несколько флагов и свойств, чтобы повысить производительность перечисления.</span><span class="sxs-lookup"><span data-stu-id="436bf-175">In addition to performing basic enumeration, you can set several flags and properties to increase the performance of your enumeration.</span></span> <span data-ttu-id="436bf-176">Дополнительные сведения см. в разделе [повышение производительности перечисления](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-176">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span>

<span data-ttu-id="436bf-177">**Перечисление набора объектов в WMI**</span><span class="sxs-lookup"><span data-stu-id="436bf-177">**To enumerate an object set in WMI**</span></span>

1.  <span data-ttu-id="436bf-178">Создайте интерфейс [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) , описывающий набор объектов, которые требуется перечислить.</span><span class="sxs-lookup"><span data-stu-id="436bf-178">Create an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface describing the set of objects you wish to enumerate.</span></span>

    <span data-ttu-id="436bf-179">Объект [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) содержит список, описывающий набор объектов WMI.</span><span class="sxs-lookup"><span data-stu-id="436bf-179">An [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object contains a list describing a set of WMI objects.</span></span> <span data-ttu-id="436bf-180">Можно использовать методы **иенумвбемклассобжект** для перечисления пересылаемых объектов, пропустить объекты, начать с начала и скопировать перечислитель.</span><span class="sxs-lookup"><span data-stu-id="436bf-180">You can use the **IEnumWbemClassObject** methods to enumerate forwards, skip objects, begin at the beginning, and copy the enumerator.</span></span> <span data-ttu-id="436bf-181">В следующей таблице перечислены методы, используемые для создания перечислителей для различных типов объектов WMI.</span><span class="sxs-lookup"><span data-stu-id="436bf-181">The following table lists the methods use to create enumerators for different types of WMI objects.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="436bf-182">Объект</span><span class="sxs-lookup"><span data-stu-id="436bf-182">Object</span></span></th>
    <th><span data-ttu-id="436bf-183">Метод</span><span class="sxs-lookup"><span data-stu-id="436bf-183">Method</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="436bf-184">Класс</span><span class="sxs-lookup"><span data-stu-id="436bf-184">Class</span></span></td>
    <td><dl><span data-ttu-id="436bf-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices:: Креатеклассенум</strong></a></span><span class="sxs-lookup"><span data-stu-id="436bf-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices::CreateClassEnum</strong></a></span></span><br />
<span data-ttu-id="436bf-186">[<strong>IWbemServices:: креатеклассенумасинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-креатеклассенумасинк)</span><span class="sxs-lookup"><span data-stu-id="436bf-186">[<strong>IWbemServices::CreateClassEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="436bf-187">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="436bf-187">Instance</span></span></td>
    <td><dl><span data-ttu-id="436bf-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices:: CreateInstanceEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="436bf-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices::CreateInstanceEnum</strong></a></span></span><br />
<span data-ttu-id="436bf-189">[<strong>IWbemServices:: креатеинстанцеенумасинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-креатеинстанцеенумасинк)</span><span class="sxs-lookup"><span data-stu-id="436bf-189">[<strong>IWbemServices::CreateInstanceEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="436bf-190">Результат запроса</span><span class="sxs-lookup"><span data-stu-id="436bf-190">Query result</span></span></td>
    <td><dl><span data-ttu-id="436bf-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices:: ExecQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="436bf-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices::ExecQuery</strong></a></span></span><br />
<span data-ttu-id="436bf-192">[<strong>IWbemServices:: ексеккуерясинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-ексеккуерясинк)</span><span class="sxs-lookup"><span data-stu-id="436bf-192">[<strong>IWbemServices::ExecQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="436bf-193">Уведомление о событии</span><span class="sxs-lookup"><span data-stu-id="436bf-193">Event notification</span></span></td>
    <td><dl><span data-ttu-id="436bf-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices:: Ексекнотификатионкуери</strong></a></span><span class="sxs-lookup"><span data-stu-id="436bf-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices::ExecNotificationQuery</strong></a></span></span><br />
<span data-ttu-id="436bf-195">[<strong>IWbemServices:: ExecNotificationQueryAsync</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-ексекнотификатионкуерясинк)</span><span class="sxs-lookup"><span data-stu-id="436bf-195">[<strong>IWbemServices::ExecNotificationQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="436bf-196">Пройдите по возвращенному перечислению, используя несколько вызовов [**иенумвбемклассобжект:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) или [**Иенумвбемклассобжект:: некстасинк**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span><span class="sxs-lookup"><span data-stu-id="436bf-196">Traverse through the returned enumeration using multiple calls to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span></span>

<span data-ttu-id="436bf-197">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="436bf-197">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 
