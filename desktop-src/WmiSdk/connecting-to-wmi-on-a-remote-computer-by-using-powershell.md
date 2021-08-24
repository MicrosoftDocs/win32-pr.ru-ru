---
description: Удаленное подключение к инструментарию WMI с помощью PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Удаленное подключение к инструментарию WMI с помощью PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d499c59ee6774b1e972e192dfc2c0d1228469196c66e8f3feb80d1c9d6339c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679875"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a>Удаленное подключение к инструментарию WMI с помощью PowerShell

Windows PowerShell предоставляет простой механизм подключения к инструментарий управления Windows (WMI) (WMI) на удаленном компьютере. на удаленные подключения в WMI влияют [Windows брандмауэр](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), параметры DCOM и [управление учетными записями пользователей (UAC)](/previous-versions/aa905108(v=msdn.10)). дополнительные сведения о настройке удаленных соединений см. [в разделе подключение к инструментарию WMI удаленно с помощью Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).

Примеры в этом разделе основаны на сценариях VBScript при [подключении к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md). Во всех примерах в этом разделе используется командлет [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) . Дополнительные сведения см. в разделе [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

## <a name="windows-powershell-examples"></a>примеры Windows PowerShell

При создании подключения к удаленному компьютеру пользователь может указать такие сведения о соединении, как имя удаленного компьютера, учетные данные и уровень проверки подлинности для подключения. В следующих примерах показано, как подключиться к удаленному компьютеру с помощью различных наборов учетных данных и как получить доступ к сведениям WMI.

в следующем примере Windows PowerShell показана настройка уровня олицетворения.


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



В предыдущем примере пользователь подключается к удаленному компьютеру, используя те же учетные данные (домен и имя пользователя), в которых они вошли. Пользователь также запросил использовать олицетворение. В отличие от исходного примера VBScript, строка моникера не требуется, так как уровень олицетворения задается свойством "Impersonation". По умолчанию уровень олицетворения устанавливается равным 3 (IMPERSONATE).

В примере перечисляются все экземпляры класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , которые выполняются на удаленном компьютере.

> [!Note]  
> Необходимо указать пространство имен WMI для подключения к удаленному компьютеру, так как пространство имен по умолчанию не совпадает на разных компьютерах.

 

в следующем Windows PowerShell примере показано, как подключиться к удаленному компьютеру с другими учетными данными и установить уровень олицетворения равным 3, что является олицетворением.


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



В предыдущем примере имя компьютера было назначено переменной $Computer. Пользователь подключается к удаленному компьютеру, используя определенные учетные данные (имя домена и пользователя) и запрашивает олицетворение для уровня проверки подлинности.

> [!Note]  
> Знак ударения-ударения ( \` ) используется для обозначения разрыва строки. Он эквивалентен символу подчеркивания ( \_ ) в VBScript.

 

следующий Windows PowerShell пример подключается к группе удаленных компьютеров в том же домене, создавая массив имен удаленных компьютеров, а затем отображая имена самонастраивающийся устройств (экземпляры [**Win32 \_ пнпентити**](/windows/desktop/CIMWin32Prov/win32-pnpentity)) на каждом компьютере:


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> чтобы запустить предыдущий сценарий Windows PowerShell, необходимо быть администратором на удаленных компьютерах. Кроме того, в отношении предыдущего примера обратите внимание на следующее:

 

-   Имена компьютеров в массиве должны быть заключены в кавычки, так как они являются строками.
-   Объекты, возвращаемые [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) , присваиваются переменной $ColItems.
-   Оператор Range \[ \] ограничивает список самонастраивающийсяных устройств до 48 экземпляров. Дополнительные сведения см. в разделе [About \_ Operators](/previous-versions//dd347588(v=technet.10)).
-   " \| " — Это символ конвейера. Объект, возвращаемый функцией Колитемс, отправляется в командлет [Format-List]( /previous-versions//dd347700(v=technet.10)) .

следующий пример Windows PowerShell позволяет подключиться к удаленному компьютеру в другом домене. В этом примере также отображаются имена процессов для экземпляров [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) на удаленном компьютере.


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> чтобы запустить предыдущий сценарий Windows PowerShell, необходимо быть администратором на удаленном компьютере.

 

В предыдущем примере пользователь подключается к удаленному компьютеру в другом домене и указывает предпочтительный языковой стандарт. Команда [Get-Credential](/previous-versions//dd315327(v=technet.10)) запрашивает учетные данные пользователя и назначает учетные данные объекту. В примере также перечислены имена экземпляров класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , которые выполняются на компьютере.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Подключение к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
