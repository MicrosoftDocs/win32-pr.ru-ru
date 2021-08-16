---
description: Свойство производности \_ объекта SWbemObject содержит массив строк, описывающих производную иерархию класса для экземпляра, на который указывает ссылка.
ms.assetid: 8a4daab0-7d10-4a37-aacd-1f3f499b859a
ms.tgt_platform: multiple
title: Свойство SWbemObject.Derivation_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Derivation_
- ISWbemObject.Derivation_
- ISWbemObject.get_Derivation_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 35195a6e3067fa68db747f04df8ec2c70480d297e4780c48059a1ba7f031e453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313906"
---
# <a name="swbemobjectderivation_-property"></a>SWbemObject. производное \_ свойство

Свойство **производности \_** объекта [**SWbemObject**](swbemobject.md) содержит массив строк, описывающих производную иерархию класса для экземпляра, на который указывает ссылка. Первый элемент массива определяет родительский класс, а последний элемент определяет класс династию. Это свойство доступно только для чтения.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObject.Derivation_ As String
```



## <a name="property-value"></a>Значение свойства

## <a name="examples"></a>Примеры

Следующий пример сценария VBScript описывает, как получить иерархию классов для Win32 \_ LogicalDisk.


```VB
on Error resume next

Set c = GetObject("winmgmts://./root/cimv2:win32_logicaldisk")
d = c.Derivation_

for x = LBound(d) to UBound(d)
 WScript.Echo d(x)
Next

if err <> 0 then
 WScript.Echo Err.Description
end if
```



Следующий пример Perl описывает, как получить иерархию классов для Win32 \_ LogicalDisk.


```
use strict;
use Win32::OLE;

my ($C, $D, @collection);

eval {$C = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("win32_logicaldisk") };
unless ($@) 
{
 @collection = in $C;
 eval {$D = $collection[0]->Derivation_();};
 print "\n";
 unless ($@) 
 {
  print map{"$_\n"} @{$D};
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
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбемобжект<br/>                                                            |



 

 




