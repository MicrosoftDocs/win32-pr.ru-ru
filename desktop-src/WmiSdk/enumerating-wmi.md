---
description: Перечисление — это процесс перемещения по набору объектов и, возможно, изменения каждого объекта.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Перечисление WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417e5ea2ae1a1216c567a1ddf257c34796b4344a807d323ad4ad7165f1707098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924700"
---
# <a name="enumerating-wmi"></a>Перечисление WMI

Перечисление — это процесс перемещения по набору объектов и, возможно, изменения каждого объекта. Например, можно перечислить набор объектов [**Win32 \_ дискдриве**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , чтобы найти конкретный серийный номер. Обратите внимание, что хотя можно перечислить любой объект, Инструментарий WMI возвращает только те объекты, к которым у вас есть доступ.

Перечисления больших наборов данных могут потребовать большого количества ресурсов и снизить производительность. Дополнительные сведения см. в разделе [повышение производительности перечисления](improving-enumeration-performance.md). Вы также можете запросить данные с более конкретным запросом. Дополнительные сведения см. в разделе [запрос WMI](querying-wmi.md).

В этом разделе обсуждаются следующие разделы:

-   [Перечисление WMI с помощью PowerShell](#enumerating-wmi-using-powershell)
-   [Перечисление WMI с помощью C# (Microsoft. Management. Infrastructure)](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [Перечисление WMI с помощью C# (System. Management)](#enumerating-wmi-using-c-systemmanagement)
-   [Перечисление WMI с помощью VBScript](#enumerating-wmi-using-vbscript)
-   [Перечисление WMI с помощью C++](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a>Перечисление WMI с помощью PowerShell

Если вы не узнаете путь к объекту для конкретного экземпляра или хотите получить все экземпляры для конкретного класса, используйте [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx)с именем класса в параметре *-Class* . Если вы хотите использовать запрос, можно использовать параметр *-Query* .

Следующая процедура описывает, как перечислить экземпляры класса с помощью PowerShell.

**Перечисление экземпляров класса с помощью PowerShell**

1.  Перечислите экземпляры с помощью вызова командлета [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) .

    Командлет [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) Возвращает коллекцию из одного или нескольких объектов WMI, с помощью которых можно выполнить перечисление. Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).

    Если вы хотите получить экземпляр класса WMI в другом пространстве имен или на другом компьютере, укажите компьютер и пространство имен в параметрах *-Computer* и *-Namespace* соответственно. Дополнительные сведения см. [в разделе Создание скрипта WMI](creating-a-wmi-script.md). Это работает только при наличии соответствующих прав доступа. Дополнительные сведения см. в разделе [поддержание безопасности WMI](maintaining-wmi-security.md) и [выполнение привилегированных операций](executing-privileged-operations.md).

2.  Получите отдельные экземпляры, в которых вы хотите использовать элементы коллекции.

В следующем примере кода извлекается коллекция PowerShell, а затем отображается свойство Size для всех экземпляров логических дисков на локальном компьютере.


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



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a>Перечисление WMI с помощью C# (Microsoft. Management. Infrastructure)

1.  Добавьте ссылку на сборку ссылки на **Microsoft. Management. Infrastructure** . (эта сборка поставляется в Windows составе [пакета средств разработки программного обеспечения (SDK) для Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)
2.  Добавьте инструкцию **using** для пространства имен **Microsoft. Management. Infrastructure** .

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  Создайте экземпляр объекта [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) . В следующем фрагменте используется стандартное значение localhost для метода [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  Вызовите метод [**CimSession. куеринстанцес**](https://www.bing.com/search?q=**CimSession.QueryInstances**) , передав требуемое пространство имен CIM и WQL для использования. следующий фрагмент кода возвратит два экземпляра, представляющие два стандартных процесса Windows, в которых свойство handle (представляющее идентификатор процесса или PID) имеет значение 0 или 4.

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  Перебрать возвращенные объекты [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) .

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

В следующем образце кода перечисляются все экземпляры класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) (который представляет активные процессы) на локальном компьютере и выводится имя каждого процесса.

> [!Note]  
> В реальном приложении вы определите в качестве параметров имя компьютера ("localhost") и пространство имен CIM ("root \\ CIMV2"). В этом примере в целях простоты они были жестко закодированы.

 


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





## <a name="enumerating-wmi-using-c-systemmanagement"></a>Перечисление WMI с помощью C# (System. Management)

Если вы не узнаете путь к объекту для конкретного экземпляра или хотите получить все экземпляры для конкретного класса, используйте объект [манажементкласс](/dotnet/api/system.management.managementclass) для получения [манажементобжектколлектион](/dotnet/api/system.management.managementobjectcollection) , содержащего все экземпляры данного класса в пространстве имен WMI. Кроме того, можно запросить WMI с помощью [манажементобжектсеарчер](/dotnet/api/system.management.managementobjectsearcher) , чтобы получить один и тот же набор объектов.

> [!Note]  
> **System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .

 

В следующей процедуре описывается перечисление экземпляров класса с помощью C#.

**Перечисление экземпляров класса с помощью C #**

1.  Перечислите экземпляры с помощью вызова [манажементкласс.](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances)GetEnumerator.

    Метод [WebMethod](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) Возвращает коллекцию или набор объектов, с помощью которых можно выполнить перечисление. Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md). Возвращаемая коллекция фактически является объектом [манажементобжектколлектион](/dotnet/api/system.management.managementobjectcollection) , поэтому можно вызывать любой из методов этого объекта.

    Если вы хотите получить экземпляр класса WMI в другом пространстве имен или на другом компьютере, укажите компьютер и пространство имен в параметре *path* . Дополнительные сведения см. [в разделе Создание скрипта WMI](creating-a-wmi-script.md). Это работает только при наличии соответствующих прав доступа. Дополнительные сведения см. в разделе [поддержание безопасности WMI](maintaining-wmi-security.md) и [выполнение привилегированных операций](executing-privileged-operations.md).

2.  Получите отдельные экземпляры, в которых вы хотите использовать элементы коллекции.

В следующем примере кода извлекается коллекция C#, а затем отображается свойство Size для всех экземпляров логических дисков на локальном компьютере.


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



## <a name="enumerating-wmi-using-vbscript"></a>Перечисление WMI с помощью VBScript

Если вы не узнаете путь к объекту для конкретного экземпляра или хотите получить все экземпляры для конкретного класса, используйте метод [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md) , чтобы вернуть перечисление [**SWbemObjectSet**](swbemobjectset.md) для всех экземпляров класса. Кроме того, можно запросить WMI с помощью [**SWbemServices.Exeккуери**](swbemservices-execquery.md) , чтобы получить тот же набор объектов.

Следующая процедура описывает, как перечислить экземпляры класса с помощью VBScript.

**Перечисление экземпляров класса с помощью VBScript**

1.  Перечислите экземпляры с помощью вызова метода [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md) .

    Метод [**инстанцесоф**](swbemservices-instancesof.md) Возвращает коллекцию или набор объектов, с помощью которых можно выполнить перечисление. Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md). Возвращаемая коллекция фактически является объектом [**SWbemObjectSet**](swbemobjectset.md) , поэтому можно вызывать любой из методов этого объекта.

    Если вы хотите получить экземпляр класса WMI в другом пространстве имен или на другом компьютере, укажите компьютер и пространство имен в моникере. Дополнительные сведения см. [в разделе Создание скрипта WMI](creating-a-wmi-script.md). Это работает только при наличии соответствующих прав доступа. Дополнительные сведения см. в разделе [поддержание безопасности WMI](maintaining-wmi-security.md) и [выполнение привилегированных операций](executing-privileged-operations.md).

2.  Получите отдельные экземпляры, которые вы хотите использовать с помощью методов коллекций.

В следующем примере кода извлекается объект [**SwbemServices**](swbemservices.md) , а затем выполняется метод [**инстанцесоф**](swbemservices-instancesof.md) для вывода свойства Size для всех экземпляров логических дисков на локальном компьютере.


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



## <a name="enumerating-wmi-using-c"></a>Перечисление WMI с помощью C++

Помимо выполнения базового перечисления, можно задать несколько флагов и свойств, чтобы повысить производительность перечисления. Дополнительные сведения см. в разделе [повышение производительности перечисления](improving-enumeration-performance.md).

**Перечисление набора объектов в WMI**

1.  Создайте интерфейс [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) , описывающий набор объектов, которые требуется перечислить.

    Объект [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) содержит список, описывающий набор объектов WMI. Можно использовать методы **иенумвбемклассобжект** для перечисления пересылаемых объектов, пропустить объекты, начать с начала и скопировать перечислитель. В следующей таблице перечислены методы, используемые для создания перечислителей для различных типов объектов WMI.

    

    <table>
    <thead>
    <tr class="header">
    <th>Объект</th>
    <th>Метод</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Класс</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices:: Креатеклассенум</strong></a><br />
[<strong>IWbemServices:: креатеклассенумасинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-креатеклассенумасинк)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Экземпляр</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices:: CreateInstanceEnum</strong></a><br />
[<strong>IWbemServices:: креатеинстанцеенумасинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-креатеинстанцеенумасинк)<br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td>Результат запроса</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices:: ExecQuery</strong></a><br />
[<strong>IWbemServices:: ексеккуерясинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-ексеккуерясинк)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Уведомление о событии</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices:: Ексекнотификатионкуери</strong></a><br />
[<strong>IWbemServices:: ExecNotificationQueryAsync</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-ексекнотификатионкуерясинк)<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Пройдите по возвращенному перечислению, используя несколько вызовов [**иенумвбемклассобжект:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) или [**Иенумвбемклассобжект:: некстасинк**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).

Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).

 

 
