---
description: Методы и свойства объекта Свбемластеррор содержат объекты ошибок и управляют ими.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Объект Свбемластеррор (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692704"
---
# <a name="swbemlasterror-object"></a>Объект Свбемластеррор

Методы и свойства объекта **свбемластеррор** содержат объекты ошибок и управляют ими. Методы и свойства этого объекта точно совпадают с методами объекта [**SWbemObject**](swbemobject.md) , но используются для хранения сведений об ошибках вместо сведений о классах WMI. Этот объект может быть создан вызовом метода **CreateObject** VBScript.

Можно создать объект ошибки **свбемластеррор** для проверки расширенных сведений об ошибке, связанных с предыдущим вызовом метода. Если информация об ошибках недоступна, попытка создать объект ошибки завершится ошибкой. Если вызов завершается с ошибкой и возвращается объект Error, состояние объекта сбрасывается. Дальнейшие попытки получить объект ошибки будут завершаться ошибкой, пока не произойдет новая ошибка. В случае сбоя асинхронного вызова в параметре *обжвбемерроробжект* может возвращаться объект **свбемластеррор** , вызываемый событием [**свбемсинк. OnComplete**](swbemsink-oncompleted.md) .

## <a name="members"></a>Элементы

Объект **свбемластеррор** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **свбемластеррор** содержит эти методы.



| Метод                                                   | Описание                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| **ASSOCIATORS\_**                                        | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **ассоЦиаторсасинк\_**                                   | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| [**Клонировать\_**](swbemlasterror-clone-.md)                 | Создает копию текущего объекта.<br/>                                               |
| [**CompareTo\_**](swbemlasterror-compareto-.md)         | Проверяет два объекта на равенство.<br/>                                                   |
| **Удалить\_**                                             | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **DeleteAsync\_**                                        | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **ExecMethod\_**                                         | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **ексекмесодасинк\_**                                    | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| [**жетобжекттекст\_**](swbemlasterror-getobjecttext-.md) | Извлекает текстовое представление объекта, написанного с помощью синтаксиса MOF.<br/>       |
| **Экземпляры\_**                                          | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **инстанцесасинк\_**                                     | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **PUT\_**                                                | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **путасинк\_**                                           | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **Ссылки\_**                                         | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **референцесасинк\_**                                    | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **SpawnDerivedClass\_**                                  | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **SpawnInstance\_**                                      | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **Подклассы\_**                                         | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |
| **субклассесасинк\_**                                    | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/> |



 

### <a name="properties"></a>Свойства

Объект **свбемластеррор** имеет следующие свойства.



| Свойство                                                      | Тип доступа          | Описание                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Наследование\_**<br/>                                   | Только для чтения<br/> | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/>                                                                  |
| **Методы\_** <br/>                                     | Только для чтения<br/> | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/>                                                                  |
| [**Путь\_**](swbemlasterror-path-.md)<br/>             | Только для чтения<br/> | Содержит объект [**свбемобжектпас**](swbemobjectpath.md) , представляющий путь к объекту текущего класса или экземпляра.<br/>                    |
| [**Свойства\_**](swbemlasterror-properties-.md)<br/> | Только для чтения<br/> | Представляет коллекцию свойств объекта **свбемластеррор** . Это свойство является объектом [**SWbemPropertySet**](swbempropertyset.md) .<br/> |
| **Квалификаторы\_**<br/>                                   | Только для чтения<br/> | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/>                                                                  |
| **Безопасность\_**<br/>                                     | Только для чтения<br/> | Не используется. Объект [**SWbemObject**](swbemobject.md) предоставляет тот же метод.<br/>                                                                  |



 

## <a name="examples"></a>Примеры

В следующем примере сценария VBScript показано, как проверить сведения об объекте Error и Error.


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



В следующем образце Perl показано, как проверить сведения об объекте Error и Error.


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
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
| CLSID<br/>                    | \_СВБЕМЛАСТЕРРОР CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемластеррор<br/>                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

 




