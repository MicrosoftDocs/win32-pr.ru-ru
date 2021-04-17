---
description: Квалификатор — это тег, предоставляющий дополнительные сведения об объекте WMI, методе или свойстве.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Доступ к квалификатору WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703008"
---
# <a name="accessing-a-wmi-qualifier"></a>Доступ к квалификатору WMI

Квалификатор — это тег, предоставляющий дополнительные сведения об объекте WMI, методе или свойстве. Иногда может потребоваться доступ к данным, хранящимся в квалификаторе. Например, Общая задача заключается в том, чтобы определить, реализует ли поставщик метод, выполнив попытку получить **реализованный** квалификатор для этого метода. Дополнительные сведения см. в разделе [квалификаторы WMI](wmi-qualifiers.md) и [Добавление квалификатора](adding-a-qualifier.md).

Чтобы получить квалификаторы для объекта WMI в PowerShell, сначала нужно получить объект, а затем проверить квалификаторы так же, как любое другое свойство.

**Извлечение квалификатора с помощью PowerShell**

-   Получите объект, квалификаторы которого необходимо просмотреть с помощью [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), а затем получите доступ к квалификаторам через свойство **Квалификаторы** :

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).

Чтобы получить квалификаторы на экземпляре WMI в C#, сначала нужно получить объект, а затем изучить квалификаторы как коллекцию.

**Извлечение квалификатора с помощью C# (Microsoft.SysTEM. MMC**

1.  Получите класс, квалификаторы которого нужно просмотреть, создав объект CimInstance с использованием указанного имени класса и пространства имен.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).

2.  Можно получить квалификаторы класса из [ciminstance. Цимкласс. Цимкласскуалифиерс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), квалификаторы свойств из [ciminstance. Цимкласс. Цимкласспропертиес](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))и квалификаторы методов из [ciminstance. Цимкласс. Цимклассмесодс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).

Чтобы получить квалификаторы для объекта WMI в C#, сначала нужно получить объект, а затем изучить квалификаторы как коллекцию.

> [!Note]  
> **System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .

 

**Извлечение квалификатора с помощью C# (System. Management)**

1.  Получите объект, квалификаторы которого необходимо просмотреть с помощью [ManagementObject](/dotnet/api/system.management.managementobject).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).

2.  Поместите квалификаторы в [куалифиердатаколлектион](/dotnet/api/system.management.qualifierdatacollection)и перечислите значения [куалифиердата](/dotnet/api/system.management.qualifierdata) .

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).

Следующая процедура описывает, как получить квалификатор с помощью VBScript.

**Извлечение квалификатора с помощью VBScript**

1.  Получите объект, квалификаторы которого необходимо просмотреть, как показано в следующем примере:

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    Наиболее распространенным способом извлечения объекта является использование метода [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) . Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).

2.  Доступ к квалификаторам объекта осуществляется через свойство [**SWbemObject. квалификаторы \_**](swbemobject-qualifiers-.md) , как показано в следующем примере:

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

В следующем примере кода показано, как получить доступ ко всем квалификаторам объекта [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) .


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



В следующей процедуре описывается извлечение квалификатора с помощью C++.

**Извлечение квалификатора с помощью C++**

1.  Получите объект, квалификаторы которого необходимо просмотреть.

    Наиболее распространенным способом извлечения объекта является использование вызова [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync). Дополнительные сведения см. в разделе [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md).

2.  Получение квалификатора, заданного для данного свойства, с вызовом методов [**ивбемклассобжект:: жетпропертикуалифиерсет**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) или [**Ивбемклассобжект:: жетмесодкуалифиерсет**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) .

3.  Доступ к квалификаторам объекта осуществляется через возвращенный интерфейс [**ивбемкуалифиерсет**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) .

## <a name="examples"></a>Примеры

Дополнительные сведения о получении квалификаторов см. в примере кода PowerShell [Get-вмиклассмесодсандвритаблевмипропертиес](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) в коллекции TechNet.

 

 
