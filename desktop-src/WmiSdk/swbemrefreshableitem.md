---
description: Представляет отдельный элемент в объекте Свбемрефрешер.
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: Объект Свбемрефрешаблеитем (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem
- ISWbemRefreshableItem
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bc4f85145926aba2bd050052c33eb5669dfee8a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820237"
---
# <a name="swbemrefreshableitem-object"></a>Объект Свбемрефрешаблеитем

Объект **свбемрефрешаблеитем** представляет отдельный элемент в объекте [**свбемрефрешер**](swbemrefresher.md) . Объект **свбемрефрешаблеитем** получается с помощью методов [**Add**](swbemrefresher-add.md) и [**адденум**](swbemrefresher-addenum.md) объекта [**свбемрефрешер**](swbemrefresher.md). Не удается создать этот объект с [помощью вызова функции](creating-an-object-using-vbscript.md) VBScript.

## <a name="members"></a>Элементы

Объект **свбемрефрешаблеитем** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **свбемрефрешаблеитем** содержит эти методы.



| Метод                                        | Описание                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Отменит**](swbemrefreshableitem-remove.md) | Удаляет объект **свбемрефрешаблеитем** из родительского объекта [**свбемрефрешер**](swbemrefresher.md) .<br/> |



 

### <a name="properties"></a>Свойства

Объект **свбемрефрешаблеитем** имеет следующие свойства.



| Свойство                                                       | Тип доступа           | Описание                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [**Номер**](swbemrefreshableitem-index.md)<br/>         | Чтение/запись<br/> | Индекс элемента в родительском объекте [**свбемрефрешер**](swbemrefresher.md) .<br/>                                          |
| [**иссет**](swbemrefreshableitem-isset.md)<br/>         | Чтение/запись<br/> | Указывает, представляет ли объект **свбемрефрешаблеитем** один объект или набор объектов.<br/>                        |
| [**Объект**](swbemrefreshableitem-object.md)<br/>       | Чтение/запись<br/> | Представляет один объект [**SWbemObject**](swbemobject.md) , который обновляется.<br/>                                          |
| [**ObjectSet**](swbemrefreshableitem-objectset.md)<br/> | Чтение/запись<br/> | Представляет набор объектов для обновления.<br/>                                                                                |
| [**Модулю обновления**](swbemrefreshableitem-refresher.md)<br/> | Только для чтения<br/>  | Представляет родительский объект [**свбемрефрешер**](swbemrefresher.md) , содержащий объект **свбемрефрешаблеитем** .<br/> |



 

## <a name="remarks"></a>Комментарии

Метод [**VBScript не может**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) использоваться для непосредственного создания объектов **свбемрефрешаблеитем** .

## <a name="examples"></a>Примеры

Следующий скрипт иллюстрирует создание объекта [**свбемрефрешер**](swbemrefresher.md) и добавление одного объекта и перечислителя **свбемрефрешаблеитем** к нему.


```VB
' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " & I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " & process.Name & _
           " Page Faults " & process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    & refresher.Count
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМРЕФРЕШАБЛЕИТЕМ CLSID<br/>                                                  |
| IID<br/>                      | IID \_ исвбемрефрешаблеитем<br/>                                                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

 




