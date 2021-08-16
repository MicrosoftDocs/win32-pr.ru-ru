---
description: Используйте методы и свойства объекта Свбемобжектпас для создания и проверки пути к объекту. Этот объект может быть создан вызовом метода CreateObject VBScript.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Объект Свбемобжектпас (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2d7273b39c5cdccea7e46a077c925247846cd9ca255fc1dba20a95aeb159b773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313553"
---
# <a name="swbemobjectpath-object"></a>Объект Свбемобжектпас

Используйте методы и свойства объекта **свбемобжектпас** для создания и проверки пути к объекту. Этот объект может быть создан вызовом метода **CreateObject** VBScript.

## <a name="members"></a>Элементы

Объект **свбемобжектпас** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **свбемобжектпас** содержит эти методы.



| Метод                                                   | Описание                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [**сетаскласс**](swbemobjectpath-setasclass.md)         | Заставляет путь обращаться к классу WMI.<br/>              |
| [**сетассинглетон**](swbemobjectpath-setassingleton.md) | Заставляет путь обращаться к экземпляру WMI Singleton.<br/> |



 

### <a name="properties"></a>Свойства

Объект **свбемобжектпас** имеет следующие свойства.



| Свойство                                                              | Тип доступа           | Описание                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Authority**](swbemobjectpath-authority.md)<br/>             | Чтение/запись<br/> | Строка, определяющая компонент центра пути к объекту.<br/>                                                                                                           |
| [**См**](swbemobjectpath-class.md)<br/>                     | Чтение/запись<br/> | Имя класса, который является частью пути к объекту.<br/>                                                                                                                        |
| [**DisplayName**](swbemobjectpath-displayname.md)<br/>         | Чтение/запись<br/> | Строка, содержащая путь в форме, которую можно использовать в качестве отображаемого имени моникера. См. раздел [Создание приложения WMI или скрипта](creating-a-wmi-application-or-script.md).<br/> |
| [**Класс класса**](swbemobjectpath-isclass.md)<br/>                 | Только для чтения<br/>  | Логическое значение, указывающее, представляет ли этот путь класс. Это аналогично свойству [ \_ \_ женус](wmi-system-properties.md) в COM API.<br/>                    |
| [**Singleton**](swbemobjectpath-issingleton.md)<br/>         | Только для чтения<br/>  | Логическое значение, указывающее, представляет ли этот путь одноэлементный экземпляр.<br/>                                                                                                |
| [**Ключи**](swbemobjectpath-keys.md)<br/>                       | Только для чтения<br/>  | Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , содержащий привязки значений ключа.<br/>                                                                          |
| [**Языкового стандарта**](swbemobjectpath-locale.md)<br/>                   | Чтение/запись<br/> | Строка, содержащая языковой стандарт для этого пути объекта.<br/>                                                                                                                     |
| [**Пространство имен**](swbemobjectpath-namespace.md)<br/>             | Чтение/запись<br/> | Имя пространства имен, которое является частью пути к объекту. Это то же самое, что и свойство [ \_ \_ Namespace](wmi-system-properties.md) в COM API.<br/>                        |
| [**парентнамеспаце**](swbemobjectpath-parentnamespace.md)<br/> | Только для чтения<br/>  | Имя родителя пространства имен, которое является частью пути к объекту.<br/>                                                                                                      |
| [**Путь**](swbemobjectpath-path.md)<br/>                       | Чтение/запись<br/> | Содержит абсолютный путь. Это то же самое, что и системное свойство [ \_ \_ path](wmi-system-properties.md) в COM API. Это свойство данного объекта по умолчанию.<br/>    |
| [**релпас**](swbemobjectpath-relpath.md)<br/>                 | Чтение/запись<br/> | Содержит относительный путь. Это то же самое, что и системное свойство [ \_ \_ релпас](wmi-system-properties.md) в COM API.<br/>                                              |
| [**Безопасность\_**](swbemobjectpath-security-.md)<br/>            | Только для чтения<br/>  | Используется для чтения или изменения параметров безопасности.<br/>                                                                                                                             |
| [**Сервер**](swbemobjectpath-server.md)<br/>                   | Чтение/запись<br/> | Имя сервера. Это то же самое, что и свойство System [ \_ \_ Server](wmi-system-properties.md) в интерфейсе API COM.<br/>                                                       |



 

## <a name="examples"></a>Примеры

В следующем примере кода VBScript показано, как создавать пути к объектам.


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



В следующем образце кода Perl показано, как создавать пути к объектам.


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
  }
  else
  {
   print STDERR Win32::OLE->LastError, "\n";
  }
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМОБЖЕКТПАС CLSID<br/>                                                       |
| IID<br/>                      | IID \_ исвбемобжектпас<br/>                                                        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

 




