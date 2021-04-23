---
description: Синхронный запрос — это запрос, который обеспечивает контроль над процессом приложения на время выполнения запроса.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Вызов синхронного запроса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d4bb2ff61a1c94bf7390a65d51e773ad943a45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684518"
---
# <a name="invoking-a-synchronous-query"></a><span data-ttu-id="d0da2-103">Вызов синхронного запроса</span><span class="sxs-lookup"><span data-stu-id="d0da2-103">Invoking a Synchronous Query</span></span>

<span data-ttu-id="d0da2-104">Синхронный запрос — это запрос, который обеспечивает контроль над процессом приложения на время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="d0da2-104">A synchronous query is a query that maintains control over the process of your application for the duration of the query.</span></span> <span data-ttu-id="d0da2-105">Синхронный запрос требует одного вызова интерфейса и, следовательно, более простой, чем асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="d0da2-105">A synchronous query requires a single interface call, and is therefore more simple than an asynchronous call.</span></span> <span data-ttu-id="d0da2-106">Однако синхронный запрос может заблокировать приложение для больших запросов или запросов по сети.</span><span class="sxs-lookup"><span data-stu-id="d0da2-106">However, a synchronous query has the potential of locking up your application for large queries or queries over a network.</span></span>

<span data-ttu-id="d0da2-107">Следующая процедура описывает, как выполнить синхронный запрос данных с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0da2-107">The following procedure describes how to issue a synchronous data query using PowerShell.</span></span>

<span data-ttu-id="d0da2-108">**Выдача синхронного запроса данных в PowerShell**</span><span class="sxs-lookup"><span data-stu-id="d0da2-108">**To issue a synchronous data query in PowerShell**</span></span>

-   <span data-ttu-id="d0da2-109">Опишите запрос к WMI с помощью командлета WMI [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) и параметра *-Query* .</span><span class="sxs-lookup"><span data-stu-id="d0da2-109">Describe your query to WMI using the WMI [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet and the *-query* parameter.</span></span> <span data-ttu-id="d0da2-110">Командлет возвращает либо один объект, либо коллекцию объектов в зависимости от того, сколько объектов соответствует запросу.</span><span class="sxs-lookup"><span data-stu-id="d0da2-110">The cmdlet returns either a single object, or a collection of objects, depending on how many objects fit the query.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="d0da2-111">Следующая процедура описывает, как выполнить синхронный запрос данных с помощью C#.</span><span class="sxs-lookup"><span data-stu-id="d0da2-111">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="d0da2-112">**Выдача синхронного запроса данных в C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="d0da2-112">**To issue a synchronous data query in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="d0da2-113">Опишите запрос к WMI с помощью CimSession. Куеринстанцес.</span><span class="sxs-lookup"><span data-stu-id="d0da2-113">Describe your query to WMI using CimSession.QueryInstances.</span></span> <span data-ttu-id="d0da2-114">Этот метод возвращает коллекцию объектов CimInstance.</span><span class="sxs-lookup"><span data-stu-id="d0da2-114">This method returns a collection of CimInstance objects.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  <span data-ttu-id="d0da2-115">Используйте стандартные методы коллекции языков C# для доступа к каждому возвращенному объекту.</span><span class="sxs-lookup"><span data-stu-id="d0da2-115">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

<span data-ttu-id="d0da2-116">Следующая процедура описывает, как выполнить синхронный запрос данных с помощью C#.</span><span class="sxs-lookup"><span data-stu-id="d0da2-116">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="d0da2-117">**Выдача синхронного запроса данных в C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="d0da2-117">**To issue a synchronous data query in C# (System.Management)**</span></span>

1.  <span data-ttu-id="d0da2-118">Создайте запрос с помощью объекта [манажементобжектсеарчер](/dotnet/api/system.management.managementobjectsearcher) и извлеките сведения с помощью вызова [манажементобжектсеарчер. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span><span class="sxs-lookup"><span data-stu-id="d0da2-118">Create the query with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) object, and retrieve the information with a call to [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span></span>

    <span data-ttu-id="d0da2-119">Этот метод возвращает объект [манажементобжектколлектион](/dotnet/api/system.management.managementobjectcollection) .</span><span class="sxs-lookup"><span data-stu-id="d0da2-119">This method returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  <span data-ttu-id="d0da2-120">Используйте стандартные методы коллекции языков C# для доступа к каждому возвращенному объекту.</span><span class="sxs-lookup"><span data-stu-id="d0da2-120">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

<span data-ttu-id="d0da2-121">Следующая процедура описывает, как выполнить синхронный запрос данных с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="d0da2-121">The following procedure describes how to issue a synchronous data query using VBScript.</span></span>

<span data-ttu-id="d0da2-122">**Выдача синхронного запроса данных в VBScript**</span><span class="sxs-lookup"><span data-stu-id="d0da2-122">**To issue a synchronous data query in VBScript**</span></span>

1.  <span data-ttu-id="d0da2-123">Опишите запрос к WMI с помощью [**SWbemServices.Exeккуери**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="d0da2-123">Describe your query to WMI using [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="d0da2-124">Этот метод возвращает [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="d0da2-124">This method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  <span data-ttu-id="d0da2-125">Для доступа к каждому возвращенному объекту используйте стандартные методики [сбора](accessing-a-collection.md) по языку сценариев.</span><span class="sxs-lookup"><span data-stu-id="d0da2-125">Use standard scripting language [collection](accessing-a-collection.md) techniques to access each returned object.</span></span>

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

<span data-ttu-id="d0da2-126">Следующая процедура описывает, как выполнить синхронный запрос данных с помощью C++.</span><span class="sxs-lookup"><span data-stu-id="d0da2-126">The following procedure describes how to issue a synchronous data query using C++.</span></span>

<span data-ttu-id="d0da2-127">**Выдача синхронного запроса в C++**</span><span class="sxs-lookup"><span data-stu-id="d0da2-127">**To issue a synchronous query in C++**</span></span>

1.  <span data-ttu-id="d0da2-128">Опишите запрос к WMI с помощью вызова [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span><span class="sxs-lookup"><span data-stu-id="d0da2-128">Describe your query to WMI through a call to [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="d0da2-129">Метод [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) принимает строку поиска WQL в качестве параметра, описывающего запрос.</span><span class="sxs-lookup"><span data-stu-id="d0da2-129">The [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) method takes a WQL search string as a parameter that describes your query.</span></span> <span data-ttu-id="d0da2-130">Инструментарий WMI выполняет запрос и возвращает указатель интерфейса [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="d0da2-130">WMI performs the query and returns an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="d0da2-131">С помощью интерфейса **иенумвбемклассобжект** можно получить доступ к классам или экземплярам, которые составляют результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="d0da2-131">Through the **IEnumWbemClassObject** interface, you can access the classes or instances that make up the result set.</span></span>

2.  <span data-ttu-id="d0da2-132">После получения запроса можно перечислить запрос с помощью вызова [**иенумвбемклассобжект:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span><span class="sxs-lookup"><span data-stu-id="d0da2-132">After you receive your query, you can enumerate your query with a call to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span></span> <span data-ttu-id="d0da2-133">Дополнительные сведения см. в разделе [перечисление WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="d0da2-133">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

    <span data-ttu-id="d0da2-134">В следующем примере кода для правильной компиляции требуются следующие ссылки и \# операторы include.</span><span class="sxs-lookup"><span data-stu-id="d0da2-134">The following code example requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    <span data-ttu-id="d0da2-135">В следующем примере кода показано, как запросить объекты, представляющие пользователей и группы в WMI.</span><span class="sxs-lookup"><span data-stu-id="d0da2-135">The following code example describes how to query for the objects that represent the users and groups in WMI.</span></span>

    ```C++
    void ExecQuerySync(IWbemServices *pSvc)
    {
        // Query for all users and groups.

        BSTR Language = SysAllocString(L"WQL");
        BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

        // Initialize the IEnumWbemClassObject pointer.
        IEnumWbemClassObject *pEnum = 0;

        // Issue the query.
        HRESULT hRes = pSvc->ExecQuery(
            Language,
            Query,
            WBEM_FLAG_FORWARD_ONLY,         // Flags
            0,                              // Context
            &pEnum
            );

        SysFreeString(Query);
        SysFreeString(Language);

        if (hRes != 0)
        {
            printf("Error\n");
            return;
        }
        
        ULONG uTotal = 0;

        // Retrieve the objects in the result set.
        for (;;)
        {
            IWbemClassObject *pObj = 0;
            ULONG uReturned = 0;

            hRes = pEnum->Next(
                0,                  // Time out
                1,                  // One object
                &pObj,
                &uReturned
                );

            uTotal += uReturned;

            if (uReturned == 0)
                break;

            // Use the object.
            
            // ...
            
            // Release it.
            // ===========
            
            pObj->Release();    // Release objects not owned.            
        }

        // All done.
        pEnum->Release();
    }
    ```

    

 

 
