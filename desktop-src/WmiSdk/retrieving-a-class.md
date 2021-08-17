---
description: Первый тип объекта, который можно извлечь, — это класс WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Получение класса WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e2695a934436e6e53fe84ee11c6008615b3d6f5d1807039d76b72fa704a2cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739883"
---
# <a name="retrieving-a-wmi-class"></a>Получение класса WMI

Первый тип объекта, который можно извлечь, — это класс WMI. При извлечении класса WMI фактически извлекается определение класса, которое представляет собой список свойств, квалификаторов и методов, которые полностью описывают класс. Однако определение класса по сути является самим классом.

PowerShell использует стандартный запрос для получения определений классов с помощью класса **мета- \_ класса** .

**Извлечение определения класса в PowerShell**

-   Используйте [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) с запросом к **\_ классу meta** с предложением WHERE, содержащим имя класса, который вы хотите получить.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) — это стандартный командлет, используемый PowerShell для получения сведений о классах и экземплярах из WMI. Класс **мета- \_ класса** определяет запрос в виде запроса схемы. Без класса **\_ класса meta** этот запрос возвратит все экземпляры Win32 \_ LogicalDisk. Дополнительные сведения о запросах WMI см. в разделе [инструкция SELECT для запросов схемы](select-statement-for-schema-queries.md).

Текущим процессом получения определения WMI в C# является использование класса **CIMInstance** .

**Извлечение определения класса в C# (Microsoft. Management. Infrastructure)**

1.  С помощью пространства имен **Microsoft. Management. Infrastructure** создайте класс **CIMInstance** с указанным пространством имен и именем класса.

    Созданный класс будет содержать все сведения о классе, но не данные экземпляра.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  Кроме того, как и в случае с PowerShell, можно также выполнить запрос, используя тег **мета- \_ класса** в составе запроса.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

Как и в PowerShell, в C# для получения определений классов используется запрос **мета- \_ класса** . Кроме того, можно создать объект **манажементкласс** для непосредственного доступа к определению класса.

> [!Note]  
> **System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .

 

**Извлечение определения класса в C# (System. Management)**

1.  Можно использовать [манажементобжектсерарчер](/dotnet/api/system.management.managementobjectsearcher) с запросом к **\_ классу meta** с предложением WHERE, содержащим имя класса, который вы хотите получить.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [Манажементобжектсерарчер](/dotnet/api/system.management.managementobjectsearcher) — это стандартный класс, используемый .NET для получения сведений о классе и экземпляре из WMI. [Манажементобжектсерарчер. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) возвращает [манажементобжектколлектион](/dotnet/api/system.management.managementobjectcollection) , содержащий класс определения схемы. Класс **мета- \_ класса** определяет запрос в виде запроса схемы. Без класса **\_ класса meta** этот запрос возвратит все экземпляры [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). Дополнительные сведения о запросах WMI см. в разделе [инструкция SELECT для запросов схемы](select-statement-for-schema-queries.md).

2.  Кроме того, можно создать новый объект [манажементкласс](/dotnet/api/system.management.managementclass) с именем в качестве пути, чтобы получить класс.

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

Вы можете получить определение класса в VBScript аналогичным образом, чтобы извлечь конкретный экземпляр.

**Извлечение определения класса в VBScript**

1.  Вызовите [**SwbemServices. Get**](swbemservices-get.md) , но не вызывайте конкретный экземпляр в пути объекта для класса.
2.  В следующем примере кода извлекается определение класса, описывающего логические диски на компьютере.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    Windows Сервер сценариев (WSH) также поддерживает следующее.

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    На Active Server страницах (ASP) используйте [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) или [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) в скрипте на стороне сервера. Дополнительные сведения см. в разделе [Создание страниц Active Server для инструментария WMI](creating-active-server-pages-for-wmi.md).

3.  Можно также указать класс или экземпляр, в этом случае возвращаемый объект является объектом WMI, например, экземпляром [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), а не объектом служб. Обратите внимание, что функции языка VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) нельзя использовать для создания экземпляра универсального объекта [**SWbemObject**](swbemobject.md).
4.  в HTML-страницах, выполняющихся в Microsoft Internet Explorer (IE), [**getobject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) и [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) могут завершиться ошибкой, так как объекты сценариев WMI, такие как ActiveX элементы управления, не помечаются как надежные для создания скриптов. Единственным исключением является объект [**SWbemDateTime**](swbemdatetime.md) . Единственный способ, которым эти вызовы могут быть выполнены, — это понизить параметры безопасности ОБОЗРЕВАТЕЛЯ, что не рекомендуется.

При извлечении класса в C++ вызывайте версию [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) [**объекта GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Извлечение определения класса в C++**

1.  Вызовите методы [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) , чтобы получить определение класса.
2.  Один класс может иметь несколько определений классов, что обычно происходит при загрузке нескольких поставщиков классов в одно пространство имен. Если класс имеет несколько определений классов, Инструментарий WMI возвращает первое обнаруженное определение и код состояния для **\_ \_ дублирования \_ объектов WBEM** .

Поскольку [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) Возвращает определение класса, он обычно используется в качестве первого шага при создании экземпляра. Дополнительные сведения об использовании **GetObject** см. в разделе [Создание и объявление экземпляра с помощью C++](creating-and-declaring-an-instance-using-c-.md).

 

 
