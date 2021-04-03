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
# <a name="creating-a-wmi-script"></a>Создание скрипта WMI

Вы можете просматривать любую информацию, доступную через инструментарий WMI, или управлять ею с помощью сценариев. Сценарии могут быть написаны на любом языке сценариев, поддерживающем размещение сценариев Microsoft ActiveX, включая Visual Basic Scripting Edition (VBScript), PowerShell и Perl. Сервер сценариев Windows (WSH), Active Server страницы и Internet Explorer могут выполнять все сценарии WMI.

> [!Note]
>
> Основным языком сценариев, который сейчас поддерживает WMI, является PowerShell. Однако Инструментарий WMI также содержит надежное тело поддержки сценариев для VBScript и других языков, которые обращаются к [API скриптов для инструментария WMI](scripting-api-for-wmi.md).

 

## <a name="wmi-scripting-languages"></a>Языки сценариев WMI

Инструментарий WMI поддерживает два основных языка: PowerShell и VBScript (с помощью сервера сценариев Windows или WSH).

-   **PowerShell** был разработан с учетом тесной интеграции с WMI. Таким образом, большая часть базовых элементов WMI встроена в командлеты WMI: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)и [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1). В следующей таблице описаны общие процессы, используемые для доступа к данным WMI. Обратите внимание, что хотя в большинстве этих примеров используется Get-WMIObject, многие командлеты PowerShell WMI имеют одинаковые параметры, такие как *-Class* или *-Credential*. Поэтому многие из этих процессов также работают и для других объектов. Более подробное обсуждение PowerShell и инструментария WMI см. в разделе [использование командлета Get-WMiObject](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) и [Windows PowerShell — WMI-подключения](/previous-versions/technet-magazine/cc162365(v=msdn.10)).

-   Язык **VBScript**, напротив, явно обращается к [API сценариев для WMI](scripting-api-for-wmi.md), как упоминалось выше. Другие языки, такие как Perl, также могут использовать API скриптов для WMI. Однако в рамках этой документации большинство примеров, демонстрирующих API сценариев для WMI, будут использовать VBScript. Однако если методика программирования относится только к VBScript, она будет называться.

    В языке VBScript есть два отдельных способа доступа к инструментарию WMI. Первый — использование объекта [**SWbemLocator**](swbemlocator.md) для подключения к инструментарию WMI. Кроме того, можно использовать [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) и моникер. Моникер — это строка, которая может описывать ряд элементов: учетные данные, параметры олицетворения, компьютер, к которому необходимо подключиться, [*пространство имен*](gloss-n.md) WMI (общее расположение, в котором Инструментарий WMI хранит группы объектов) и объект WMI, который требуется получить. Многие из приведенных ниже примеров описывают обе методики. Дополнительные сведения см. в разделе [Создание строки моникера](constructing-a-moniker-string.md) и [Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).

    Независимо от того, какой метод используется для подключения к WMI, скорее всего, вы получите один или несколько объектов из API скриптов. Наиболее распространенным является [**SWbemObject**](swbemobject.md), который WMI использует для описания объекта WMI. Кроме того, вы можете использовать объект [**SwbemServices**](swbemservices.md) для описания самой службы WMI или объект [**свбемобжектпас**](swbemobjectpath.md) для описания расположения объекта WMI. Дополнительные сведения см. в разделе [Создание скриптов с помощью](scripting-with-swbemobject.md) [вспомогательных объектов](scripting-helper-objects.md)SWbemObject и сценариев.

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a>Использование инструментария WMI и языка сценариев...

<dl> <dt>

<span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... подключиться к инструментарию WMI?
</dt> <dd>

Для VBScript и API скриптов для WMI извлеките объект [**SwbemServices**](swbemservices.md) с моникером и вызовом [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)). Кроме того, можно подключиться к серверу с помощью вызова [**SWbemLocator. коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Затем можно использовать объект для доступа к определенному пространству имен WMI или экземпляру класса WMI.

Для PowerShell соединение с WMI обычно выполняется непосредственно в вызове командлета. Поэтому никаких дополнительных действий не требуется.

Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md), [Создание строки моникера](constructing-a-moniker-string.md)и [Подключение к WMI с помощью VBScript](connecting-to-wmi-with-vbscript.md).


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

<span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... получить сведения из инструментария WMI?
</dt> <dd>

Для VBScript и API скриптов для WMI используйте функцию извлечения, например [**вбемсервицес. Get**](swbemservices-get.md) или [**вбемсервицес. инстанцесоф**](swbemservices-instancesof.md). Вы также можете поместить имя класса объекта для извлечения в моникер, что может быть более эффективным.

Для PowerShell используйте параметр *-Class* . Обратите внимание, что параметр-Class используется по умолчанию. Поэтому вам не нужно явно их задавать.

Дополнительные сведения см. в разделе [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md).


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

<span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... создаете запрос WMI?
</dt> <dd>

Для VBScript и API скриптов для WMI используйте метод [**SWbemServices.Exeккуери**](swbemservices-execquery.md) .

Для PowerShell используйте параметр *-Query* . Можно также выполнить фильтрацию с помощью параметра *-Filter* .

Дополнительные сведения см. в разделе [запрос WMI](querying-wmi.md).


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

<span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... перечислить список объектов WMI?
</dt> <dd>

Для VBScript и API скриптов для WMI используйте объект контейнера [**SWbemObjectSet**](swbemobjectset.md) , который рассматривается в скрипте как коллекция, которую можно перечислить. **SWbemObjectSet** можно извлечь из вызова из [**SwbemServices. Инстанцесоф**](swbemservices-instancesof.md) или [**SWbemServices.Exeккуери**](swbemservices-execquery.md).

PowerShell может извлекать и управлять перечислениями так же, как и любым другим объектом. в WMI нет ничего особенного.

Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).


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

<span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... доступ к другому пространству имен WMI?
</dt> <dd>

Для VBScript и API скриптов для инструментария WMI заполните пространство имен в моникере или, в противном случае, можно явно задать пространство имен в вызове [**SwbemLocator. коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

Для PowerShell используйте параметр *-Namespace* . Пространством имен по умолчанию является root \\ cimV2, однако многие старые классы хранятся в корневом каталоге \\ по умолчанию.

Чтобы найти расположение данного класса WMI, просмотрите страницу справки. Кроме того, можно вручную просмотреть пространство имен с помощью Get-WmiObject.


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

<span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... получить все дочерние экземпляры класса?
</dt> <dd>

Для языков, которые непосредственно используют API скриптов для WMI и PowerShell, WMI поддерживает получение дочерних классов базового класса. Таким образом, чтобы получить дочерние экземпляры, необходимо найти только родительский класс. В следующем примере выполняется поиск логического диска CIM, который является предварительно установленным классом WMI, представляющим логические диски в системе на основе Windows. [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldisk) Таким образом, при поиске этого родительского класса также возвращаются экземпляры [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), которые используются Windows для описания жестких дисков. Дополнительные сведения см. в разделе [модель CIM](common-information-model.md). Инструментарий WMI предоставляет всю схему таких предустановленных классов, которые позволяют получать доступ к управляемым объектам и управлять ими. Дополнительные сведения см. в разделе [Классы Win32](/windows/desktop/CIMWin32Prov/win32-provider) и [классы WMI](wmi-classes.md).


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... находите объект WMI?
</dt> <dd>

Для API скриптов для WMI и PowerShell в WMI используется сочетание пространства имен, имени класса и ключевых свойств для уникальной идентификации данного экземпляра WMI. Вместе это называется путем объекта WMI. Для VBScript свойство [**SWbemObject. Path \_**](swbemobject-path-.md) описывает путь для любого объекта, возвращаемого API скриптов. Для PowerShell каждый объект WMI будет иметь \_ \_ свойство Path. Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md) .

Помимо пространства имен и имени класса, объект WMI также имеет ключевое свойство, которое однозначно определяет этот экземпляр по сравнению с другими экземплярами на компьютере. Например, свойство **DeviceID** является ключевым свойством для класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) . Дополнительные сведения см. в разделе [MOF-файл (MOF)](managed-object-format--mof-.md).

Наконец, относительный путь представляет собой сокращенную форму пути и включает имя класса и значение ключа. В приведенных ниже примерах путь может иметь \\ \\ вид "имя_компьютера \\ root \\ CIMV2: Win32 \_ LogicalDisk. DeviceID =" D: ", а относительный путь —" "Win32LogicalDisk. DeviceID =" D "" ".


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

<span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... задать сведения в инструментарии WMI?
</dt> <dd>

Для VBScript и API скриптов для WMI используйте метод [**SWbemObject. поместил \_**](swbemobject-put-.md) .

Для PowerShell можно либо использовать метод размещения, либо [задать параметр-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

Дополнительные сведения см. в разделе [изменение свойства экземпляра](modifying-an-instance-property.md).


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

<span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... использовать другие учетные данные?
</dt> <dd>

Для VBScript и API скриптов для WMI используйте параметры *username* и *Password* в методе [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) .

Для PowerShell используйте параметр *-Credential* .

Обратите внимание, что на удаленной системе можно использовать только альтернативные учетные данные. Дополнительные сведения см. в разделе [Защита скриптов для клиентов](securing-scripting-clients.md).


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

<span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... доступ к удаленному компьютеру
</dt> <dd>

Для VBScript и API скриптов для WMI следует явно указать имя компьютера в моникере или в вызове [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md). Дополнительные сведения см. [в статье удаленное подключение к WMI с помощью VBScript](connecting-to-wmi-remotely-with-vbscript.md).

Для PowerShell используйте параметр *-ComputerName* . Дополнительные сведения см. [в статье удаленное подключение к WMI с помощью PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).


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

<span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... задать уровни проверки подлинности и олицетворения?
</dt> <dd>

Для VBScript и API скриптов для WMI используйте свойство [**SwbemServices. Security \_**](swbemlocator-security-.md) для возвращенного серверного объекта или задайте соответствующие значения в моникере.

Для PowerShell используйте параметры *-authentication* и *-Impersonation* соответственно. Дополнительные сведения см. в разделе [Защита скриптов для клиентов](securing-scripting-clients.md).

Дополнительные сведения см. в разделе [Защита скриптов для клиентов](securing-scripting-clients.md).


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

<span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... Обработайте ошибки в WMI?
</dt> <dd>

Для API скриптов для инструментария WMI поставщик может предоставить объект [**свбемластеррор**](swbemlasterror.md) , чтобы получить дополнительные сведения об ошибке.

В частности, в VBScript также поддерживается обработка ошибок с помощью собственного объекта **Err** . Вы также можете получить доступ к объекту [**свбемластеррор**](swbemlasterror.md), как описано выше. Дополнительные сведения см. в разделе [Получение кода ошибки](retrieving-an-error-code.md).

Для PowerShell можно использовать стандартные методы обработки ошибок PowerShell. Дополнительные сведения см. в статье [Введение в обработку ошибок в PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).


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

 

 
