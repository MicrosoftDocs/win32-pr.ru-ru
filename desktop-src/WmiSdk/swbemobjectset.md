---
description: Объект SWbemObjectSet — это коллекция объектов SWbemObject. Дополнительные сведения см. в разделе доступ к коллекции. Не удается создать этот объект с помощью вызова функции VBScript.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Объект SWbemObjectSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272558"
---
# <a name="swbemobjectset-object"></a>Объект SWbemObjectSet

Объект **SWbemObjectSet** — это коллекция объектов [**SWbemObject**](swbemobject.md) . Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md). Не удается создать этот объект с **помощью вызова функции** VBScript.

Объект **SWbemObjectSet** можно получить, вызвав любой из следующих методов или их асинхронных эквивалентов:

-   [**SWbemObject. соединители\_**](swbemobject-associators-.md)
-   [**SWbemObject. Instances\_**](swbemobject-instances-.md)
-   [**SWbemObject. References\_**](swbemobject-references-.md)
-   [**SWbemObject. подклассы\_**](swbemobject-subclasses-.md)
-   [**SWbemServices. АссоЦиаторсоф**](swbemservices-associatorsof.md)
-   [**SWbemServices.ExeКкуери**](swbemservices-execquery.md)
-   [**SWbemServices. Инстанцесоф**](swbemservices-instancesof.md)
-   [**SWbemServices. Референцесто**](swbemservices-referencesto.md)
-   [**SWbemServices. Субклассесоф**](swbemservices-subclassesof.md)

> [!Note]  
> Объект **SWbemObjectSet** не поддерживает необязательные методы **добавления** и **удаления** коллекции.

 

> [!Note]  
> Поскольку обратный вызов к приемнику может быть не возвращен на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

 

## <a name="members"></a>Элементы

Объект **SWbemObjectSet** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **SWbemObjectSet** содержит эти методы.



| Метод                              | Описание                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**Item**](swbemobjectset-item.md) | Извлекает объект [**SWbemObject**](swbemobject.md) из коллекции. Это метод объекта по умолчанию.<br/> |



 

### <a name="properties"></a>Свойства

Объект **SWbemObjectSet** имеет следующие свойства.



| Свойство                                                  | Тип доступа          | Описание                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Расчета**](swbemobjectset-count.md)<br/>          | Только для чтения<br/> | Количество элементов в коллекции.<br/>        |
| [**Безопасность\_**](swbemobjectset-security-.md)<br/> | Только для чтения<br/> | Используется для чтения или изменения параметров безопасности.<br/> |



 

## <a name="remarks"></a>Комментарии

**SWbemObjectSet** — это коллекция из нуля или более объектов [**SWbemObject**](swbemobject.md) . Каждый **SWbemObject** в **SWbemObjectSet** может представлять одно из двух вещей:

-   Экземпляр управляемого WMI ресурса.
-   Экземпляр определения класса.

Чаще всего этот класс используется в WMI как возвращаемое значение для вызова [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) или [**инстанцесоф**](swbemservices-instancesof.md) , как описано в следующем примере кода:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



В большинстве случаев единственное, что вы будете делать с **SWbemObjectSet** , — перечисляет все объекты, содержащиеся в самой коллекции. Однако **SWbemObjectSet** включает число свойств, которое может быть полезно при создании сценариев системного администрирования. Как следует из названия, Count сообщает число элементов в коллекции. Например, этот скрипт извлекает коллекцию всех служб, установленных на компьютере, а затем отображает общее число найденных служб:

Дополнительные сведения об использовании этого класса см. в разделе [перечисление WMI](enumerating-wmi.md).

## <a name="examples"></a>Примеры

В следующем примере кода VBScript показано, как обрабатываются **SWbemObjectSet** коллекции.


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



В следующем образце кода Perl показано, как обрабатываются **SWbemObjectSet** коллекции.


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
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
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемобжектсет<br/>                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

 




