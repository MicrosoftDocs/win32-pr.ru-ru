---
description: Описывает, как сценарии, приложения и поставщики могут устанавливать подключения к инструментарию WMI на удаленных компьютерах для получения данных, управления оборудованием и программным обеспечением.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Подключение к инструментарию WMI на удаленном компьютере
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d581d1be73013e57ef2193102f6e8afc287b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674069"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a>Подключение к инструментарию WMI на удаленном компьютере

Инструментарий WMI можно использовать для управления и доступа к данным WMI на удаленных компьютерах. На удаленные подключения в WMI влияют параметры [брандмауэра Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) и DCOM. Для [контроля учетных записей (UAC)](/previous-versions/aa905108(v=msdn.10)) также могут потребоваться изменения некоторых параметров. Однако после настройки параметров вызов удаленной системы будет очень похож на локальный вызов WMI. Тем не менее, вы можете сделать его более сложным, используя разные учетные данные, альтернативные протоколы проверки подлинности и другие функции безопасности.

## <a name="configuring-a-computer-for-a-remote-connection"></a>Настройка компьютера для удаленного подключения

Прежде чем получить доступ к удаленной системе с помощью инструментария WMI, может потребоваться проверить некоторые параметры безопасности, чтобы убедиться, что у вас есть доступ. В частности, внесены следующие изменения.

-   Windows содержит ряд функций безопасности, которые могут блокировать доступ к сценариям в удаленных системах. Таким образом, может потребоваться изменить параметры системы Active Directory и брандмауэра Windows перед вызовом инструментария WMI. Дополнительные сведения см. в разделе [Настройка удаленного WMI-подключения](connecting-to-wmi-remotely-starting-with-vista.md) и [Устранение неполадок удаленного WMI-подключения](troubleshooting-a-remote-wmi-connection.md).

-   Чтобы удаленное подключение работало, необходимо включить правильные параметры DCOM. Изменение параметров DCOM позволяет пользователям с ограниченными правами получать доступ к компьютеру для удаленного подключения. Дополнительные сведения см. [в разделе Защита удаленного WMI-подключения](securing-a-remote-wmi-connection.md).

Кроме того, в некоторых случаях может потребоваться запустить Инструментарий WMI, хотя фиксированный порт. Для этого также потребуется изменить параметры. Дополнительные сведения см. [в разделе Настройка фиксированного порта для WMI](setting-up-a-fixed-port-for-wmi.md).

## <a name="connecting-to-a-remote-computer"></a>Подключение к удаленному компьютеру

По сути, подключение к удаленной системе с помощью инструментария WMI состоит в том, что у вас есть соответствующие разрешения на доступ к системе и правильно настроено подключение. После получения этих двух элементов соединение само по себе является сравнительно простым. Например, если вы используете учетные данные безопасности по умолчанию, вы можете получить доступ к инструментарию WMI в удаленной системе, используя следующий код:

<dl> <dt>

<span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Удаленное подключение к инструментарию WMI с помощью PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)
</dt> <dd>

Используйте параметр *-ComputerName* , общий для большинства командлетов WMI, например [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Удаленное подключение к инструментарию WMI с помощью VBScript](connecting-to-wmi-remotely-with-vbscript.md)
</dt> <dd>

Используйте моникер, содержащий имя удаленной системы в вызове [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Удаленное подключение к инструментарию WMI с помощью C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Для текущей версии управляемого интерфейса WMI ([Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))) используйте объект [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) для представления подключения к удаленному узлу.


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Удаленное подключение к инструментарию WMI с помощью C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Для версии v1 управляемого интерфейса WMI ([System. Management](/dotnet/api/system.management)) используйте объект [манажементскопе](/dotnet/api/system.management.managementscope) для представления подключения к удаленному узлу.


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Пример. получение данных WMI с удаленного компьютера (C++)](example--getting-wmi-data-from-a-remote-computer.md)
</dt> <dd>

Используйте метод [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) , чтобы указать имя удаленного компьютера в параметре *стрнетворкресаурце* .


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

Предыдущие примеры кода, вероятно, являются самым простым удаленным подключением, которое можно выполнять с помощью инструментария WMI. В частности, в примерах предполагается следующее:

-   Вы являетесь администратором на удаленном компьютере. Из-за [контроля учетных записей пользователя](/previous-versions/aa905108(v=msdn.10))учетная запись в удаленной системе должна быть учетной записью домена в группе администраторов. Дополнительные сведения см. в разделе Управление учетными записями пользователей и инструментарий WMI.
-   Пароль на текущем локальном компьютере не пуст. По сути, это требование безопасности Windows, которое необходимо войти в систему с паролем.
-   Как локальные, так и удаленные компьютеры находятся в одном домене. Если необходимо использовать междоменные границы, необходимо указать дополнительные сведения или воспользоваться немного другой моделью программирования.
-   Для доступа к удаленному компьютеру используется собственная учетная запись. Если вы пытались получить доступ к другой учетной записи, вам потребуется указать дополнительные учетные данные. (Обратите внимание, что попытка доступа к инструментарию WMI локально с учетными данными, отличными от текущей учетной записи, не разрешено)
-   Оба компьютера работают под управлением IPv6. WMI поддерживает подключения к компьютерам с IPv6. Однако на локальном компьютере и компьютере \_ B должен быть установлен протокол IPv6. На одном из компьютеров может также работать протокол IPv4. Дополнительные сведения см. [в разделе Поддержка IPv6 и IPv4 в WMI](ipv6-and-ipv4-support-in-wmi.md).
-   Ваш сценарий не обязан делегировать, т. е. ему не требуется доступ к дополнительным удаленным компьютерам через Целевой Удаленный компьютер. Дополнительные сведения см. в разделе [делегирование с помощью WMI](connecting-to-a-3rd-computer-delegation.md).
-   Вы пытаетесь выполнить конкретный вызов, а не создавать удаленный процесс. Дополнительные сведения см. в статье [Удаленное создание процессов с помощью WMI](creating-processes-remotely.md).

Учитывая эти ограничения, удаленный вызов WMI очень напоминает локальный вызов WMI. Единственное отличие заключается в том, что необходимо указать имя удаленной системы. Однако вы можете изменить многие из этих функций: использовать другие учетные данные или маршрутизацию вызова через другой компьютер или доступ к другому домену.

 

 
