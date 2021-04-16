---
description: Возвращает SWbemObject, связанный с указанным индексом в коллекцию.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: SWbemObjectSet. Итеминдекс, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702885"
---
# <a name="swbemobjectsetitemindex-method"></a>SWbemObjectSet. Итеминдекс, метод

Метод **итеминдекс** возвращает [**SWbemObject**](swbemobject.md) , связанный с указанным индексом, в коллекцию. Индекс указывает на расположение элемента в коллекции. Нумерация коллекций начинается с нуля.

## <a name="syntax"></a>Синтаксис


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*линдекс* 
</dt> <dd>

Индекс элемента в коллекции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения запрошенный объект [**SWbemObject**](swbemobject.md) возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода [**Item**](swbemobjectset-item.md) объект **Err** может содержать один из кодов ошибок, приведенных ниже.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр. Эта ошибка возвращается, если указан отрицательный номер индекса.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Запрошенный элемент не найден.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Метод **итеминдекс** позволяет клиентским сценариям WMI и приложениям, написанным на любом языке, единообразно управлять коллекцией, например массивом. Этот метод можно использовать с коллекциями [**SWbemObjectSet**](swbemobjectset.md) . Такие запросы, как [**SwbemServices. ассоЦиаторсоф**](swbemservices-associatorsof.md), [**SwbemServices. референцесто**](swbemservices-referencesto.md), [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md)или [**SWbemServices.Exeккуери**](swbemservices-execquery.md) , возвращают **SWbemObjectSet** коллекции. Метод **итеминдекс** не работает с коллекциями, которые не содержат [**Свбемобжектс**](swbemobject.md), например [**свбеммесодсет**](swbemmethodset.md), [**свбемнамедвалуесет**](swbemnamedvalueset.md), [**свбемпривилежесет**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md)и [**свбемкуалифиерсет**](swbemqualifierset.md).

**Итеминдекс** также можно использовать для получения единственного экземпляра одноэлементного класса.

## <a name="examples"></a>Примеры

В следующем примере кода VBScript выполняется запрос коллекции всех экземпляров [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , а затем отображаются имена первых трех процессов.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



Для каждой установки операционной системы существует только один экземпляр [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) . Создание пути к [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) для получения единственного экземпляра является неудобным, поэтому сценарии обычно перечисляют набор **Win32 \_ , даже** если доступен только один экземпляр. В следующем примере кода VBScript показано, как использовать метод **итеминдекс** для получения одной **\_ операционной системы Win32** без использования цикла **for each** .


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



Следующий пример кода VBScript получает экземпляры, связанные с [**Win32 \_ операционной**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)системы, например [**Win32 \_ системоператингсистем**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



В следующем примере кода показаны экземпляры, связанные с [**\_ операционной системы Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
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

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

