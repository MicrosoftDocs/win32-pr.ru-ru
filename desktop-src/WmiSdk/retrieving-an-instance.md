---
description: Получение экземпляра является одной из наиболее распространенных процедур извлечения, которые, скорее всего, будут выполняться в инструментарии WMI.
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: Получение экземпляра WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5cc3b52a236eeccf422ee334cba5aa6de98c9aa08864ec7273a7ba2f84008e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816931"
---
# <a name="retrieving-a-wmi-instance"></a>Получение экземпляра WMI

Получение экземпляра является одной из наиболее распространенных процедур извлечения, которые, скорее всего, будут выполняться в инструментарии WMI. Можно получить существующий экземпляр или создать новый неименованный экземпляр. Путь WMI к существующему экземпляру является обязательным параметром. Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).

> [!Note]  
> При предоставлении экземпляра поставщик может не предоставить значение для определенных свойств. Если не указано иное в описании свойства, невозможно определить любое значение из пустого значения. Это не следует путать со строкой, имеющей значение **null** . В этом случае значение заполняется. Он пуст, но имеет значение **null**.

 

Получите локальную копию экземпляра с помощью вызова командлета [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) PowerShell.

**Извлечение экземпляра класса WMI с помощью PowerShell**

-   Вы можете получить конкретные экземпляры с помощью параметров *-Class* и *-Filter* .

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

Экземпляр WMI можно получить с помощью C#, создав объект поиска с помощью [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), а затем заполняя его соответствующими значениями ключа, а затем выполнив поиск этого объекта с помощью вызова [CimSession.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) GetObject.

**Извлечение экземпляра класса WMI с помощью C# (Microsoft. Management. Infrastructure)**

1.  Используя пространство имен [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , создайте новый объект [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) с соответствующим именем класса и пространством имен.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  Создайте [Цимпроперти](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) , содержащий имя и значение ключевого свойства экземпляра, который нужно найти, и добавьте это свойство в объект класса.

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  Получите объект из WMI с помощью вызова [CimSession.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) GetObject.

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

Можно получить либо конкретный экземпляр класса WMI, либо коллекцию экземпляров класса WMI с помощью классов в пространстве имен [System. Management](/dotnet/api/system.management) .

> [!Note]  
> **System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .

 

**Извлечение экземпляра класса WMI с помощью C# (System. Management)**

1.  Получите локальную копию определенного экземпляра, создав новый [ManagementObject](/dotnet/api/system.management.managementobject)с именем и конкретным значением экземпляра, которое передается в параметре *манажементпас* . Затем можно получить данные экземпляра, явно вызвав [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  Кроме того, можно получить все экземпляры класса WMI, выполнив поиск их с помощью [манажементобжектсеарчер](/dotnet/api/system.management.managementobjectsearcher), а затем перечислить возвращенные [манажементобжектколлектион](/dotnet/api/system.management.managementobjectcollection).

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

    

    Можно неявно вызвать метод **Get** , обратившись к экземпляру. Дополнительные сведения см. в разделе [получение части экземпляра WMI](retrieving-part-of-an-instance.md).

Получите локальную копию экземпляра, вызвав метод VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) .

**Получение экземпляра класса WMI с помощью VBScript**

-   Вызовите GetObject с [**путем к объекту**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) экземпляра, как показано в следующем примере.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    Для получения конкретного экземпляра необходимо указать имя как часть пути к объекту.

В C++ вызовите [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Извлечение экземпляра класса WMI с помощью C++**

-   Получите локальную копию экземпляра с вызовом [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync). Необходимо добавить путь WMI к объекту.

    Как следует из названия, [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) получает экземпляр асинхронно, а [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) получает экземпляр синхронно. Если вы хотите использовать асинхронный выбор, необходимо реализовать интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .

## <a name="examples"></a>Примеры

Пример сценария VBScript, используемый в качестве шаблона для получения сведений о классе и экземпляре, см. в разделе пример [скрипта шаблона WMI](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) в коллекции TechNet. В этом конкретном примере для получения службы WMI используется GetObject.

 

 
