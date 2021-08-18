---
description: объект свбемпривилежесет — это коллекция объектов свбемпривилеже в объекте свбемсекурити, которая запрашивает определенные привилегии для объекта инструментарий управления Windows (WMI) (WMI).
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Объект Свбемпривилежесет (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2117aec6fada67bddce9f07a6c985c73a3dcd93ef217ed7fe77dc46cc5659d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991954"
---
# <a name="swbemprivilegeset-object"></a>Объект Свбемпривилежесет

объект **свбемпривилежесет** — это коллекция объектов [**свбемпривилеже**](swbemprivilege.md) в объекте [**свбемсекурити**](swbemsecurity.md) , которая запрашивает определенные привилегии для объекта инструментарий управления Windows (WMI) (WMI). Список привилегий см. в разделе [**константы прав доступа**](privilege-constants.md). Элементы добавляются в коллекцию с помощью методов [**Add**](swbemprivilegeset-add.md) и [**аддасстринг**](swbemprivilegeset-addasstring.md) . Элементы извлекаются из коллекции с помощью метода [**Item**](swbemprivilegeset-item.md) и удаляются с помощью метода [**Remove**](swbemprivilegeset-remove.md) . Этот объект не может быть создан вызовом метода [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) для VBScript. Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).

Объект **свбемпривилежесет** — это набор запросов переопределения привилегий для определенного объекта. При вызове API с помощью этого объекта предпринимается попытка выполнить запросы на переопределение привилегий. Объект **свбемпривилежесет** не определяет привилегии, доступные текущему пользователю или процессу. Другими словами, получение привилегий для любого объекта WMI не определяет параметры привилегий, которые выполняются при подключении к WMI, или привилегии, действующие при доставке объекта в приемник.

## <a name="members"></a>Элементы

Объект **свбемпривилежесет** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **свбемпривилежесет** содержит эти методы.



| Метод                                               | Описание                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Включить**](swbemprivilegeset-add.md)                 | Добавляет объект [**свбемпривилеже**](swbemprivilege.md) в коллекцию **свбемпривилежесет** с помощью константы [вбемпривилежеенум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .<br/> |
| [**аддасстринг**](swbemprivilegeset-addasstring.md) | Добавляет объект [**свбемпривилеже**](swbemprivilege.md) в коллекцию **свбемпривилежесет** с помощью строки привилегий.<br/>                                    |
| [**DeleteAll**](swbemprivilegeset-deleteall.md)     | Удаляет все привилегии из коллекции.<br/>                                                                                                              |
| [**Компонент**](swbemprivilegeset-item.md)               | Извлекает объект [**свбемпривилеже**](swbemprivilege.md) из коллекции. Это метод по умолчанию для этого объекта.<br/>                                 |
| [**Отменит**](swbemprivilegeset-remove.md)           | Удаляет объект [**свбемпривилеже**](swbemprivilege.md) из коллекции.<br/>                                                                              |



 

### <a name="properties"></a>Свойства

Объект **свбемпривилежесет** имеет следующие свойства.



| Свойство                                            | Тип доступа          | Описание                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Count**](swbemprivilegeset-count.md)<br/> | Только для чтения<br/> | Количество элементов в коллекции.<br/> |



 

## <a name="examples"></a>Примеры

Следующий пример кода VBScript получает объект Свбемпривилежес и добавляет все доступные привилегии в коллекцию по значению привилегии, как определено в [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



В следующем примере кода VBScript показано, как добавить привилегии с помощью объекта **свбемпривилежесет** .


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



В следующем примере кода Perl показано, как добавить привилегии с помощью объекта **свбемпривилежесет** .


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМПРИВИЛЕЖЕСЕТ CLSID<br/>                                                     |
| IID<br/>                      | IID \_ исвбемпривилежесет<br/>                                                      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Выполнение привилегированных операций](executing-privileged-operations.md)
</dt> <dt>

[Выполнение привилегированных операций с помощью VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[вбемпривилежеенум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> <dt>

[**Константы прав доступа**](privilege-constants.md)
</dt> </dl>

 

