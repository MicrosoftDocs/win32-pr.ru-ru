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
# <a name="invoking-a-synchronous-query"></a>Вызов синхронного запроса

Синхронный запрос — это запрос, который обеспечивает контроль над процессом приложения на время выполнения запроса. Синхронный запрос требует одного вызова интерфейса и, следовательно, более простой, чем асинхронный вызов. Однако синхронный запрос может заблокировать приложение для больших запросов или запросов по сети.

Следующая процедура описывает, как выполнить синхронный запрос данных с помощью PowerShell.

**Выдача синхронного запроса данных в PowerShell**

-   Опишите запрос к WMI с помощью командлета WMI [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) и параметра *-Query* . Командлет возвращает либо один объект, либо коллекцию объектов в зависимости от того, сколько объектов соответствует запросу.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

Следующая процедура описывает, как выполнить синхронный запрос данных с помощью C#.

**Выдача синхронного запроса данных в C# (Microsoft. Management. Infrastructure)**

1.  Опишите запрос к WMI с помощью CimSession. Куеринстанцес. Этот метод возвращает коллекцию объектов CimInstance.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  Используйте стандартные методы коллекции языков C# для доступа к каждому возвращенному объекту.

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

Следующая процедура описывает, как выполнить синхронный запрос данных с помощью C#.

**Выдача синхронного запроса данных в C# (System. Management)**

1.  Создайте запрос с помощью объекта [манажементобжектсеарчер](/dotnet/api/system.management.managementobjectsearcher) и извлеките сведения с помощью вызова [манажементобжектсеарчер. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).

    Этот метод возвращает объект [манажементобжектколлектион](/dotnet/api/system.management.managementobjectcollection) .

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  Используйте стандартные методы коллекции языков C# для доступа к каждому возвращенному объекту.

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

Следующая процедура описывает, как выполнить синхронный запрос данных с помощью VBScript.

**Выдача синхронного запроса данных в VBScript**

1.  Опишите запрос к WMI с помощью [**SWbemServices.Exeккуери**](swbemservices-execquery.md). Этот метод возвращает [**SWbemObjectSet**](swbemobjectset.md).

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  Для доступа к каждому возвращенному объекту используйте стандартные методики [сбора](accessing-a-collection.md) по языку сценариев.

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

Следующая процедура описывает, как выполнить синхронный запрос данных с помощью C++.

**Выдача синхронного запроса в C++**

1.  Опишите запрос к WMI с помощью вызова [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    Метод [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) принимает строку поиска WQL в качестве параметра, описывающего запрос. Инструментарий WMI выполняет запрос и возвращает указатель интерфейса [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . С помощью интерфейса **иенумвбемклассобжект** можно получить доступ к классам или экземплярам, которые составляют результирующий набор.

2.  После получения запроса можно перечислить запрос с помощью вызова [**иенумвбемклассобжект:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next). Дополнительные сведения см. в разделе [перечисление WMI](enumerating-wmi.md).

    В следующем примере кода для правильной компиляции требуются следующие ссылки и \# операторы include.

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    В следующем примере кода показано, как запросить объекты, представляющие пользователей и группы в WMI.

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

    

 

 
