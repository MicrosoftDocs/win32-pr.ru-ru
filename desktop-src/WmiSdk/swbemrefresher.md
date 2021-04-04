---
description: Объект Свбемрефрешер — это объект контейнера, который может обновлять данные для всех добавленных в него объектов. Набор добавленных объектов, каждый элемент, представленный экземпляром Свбемрефрешаблеитем, может рассматриваться как коллекция и перечисляться.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Объект Свбемрефрешер (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999937"
---
# <a name="swbemrefresher-object"></a>Объект Свбемрефрешер

Объект **свбемрефрешер** — это объект контейнера, который может обновлять данные для всех добавленных в него объектов. Отдельные экземпляры и перечислители экземпляров можно добавлять в контейнер или удалять из него. Набор добавленных объектов, каждый элемент которого представлен экземпляром [**свбемрефрешаблеитем**](swbemrefreshableitem.md) , можно рассматривать как коллекцию и перечислить. Экземпляры WMI из любого класса можно добавить в объект **свбемрефрешер** . Даже если поставщик данных экземпляра не является поставщиком высокой производительности, объект обновления по-прежнему может обновить данные в вызове [**обновления**](swbemrefresher-refresh.md) . Если данные передаются через высокопроизводительный поставщик, а свойство [**аутореконнект**](swbemrefresher-autoreconnect.md) имеет **значение true**, объект **свбемрефрешер** пытается восстановить разорванное соединение с поставщиком данных. Этот объект может быть создан вызовом метода **CreateObject** VBScript.

Операция обновления может быть выполнена путем вызова метода [**свбемрефрешер. Refresh**](swbemrefresher-refresh.md) или метода [**\_ свбемобжектекс. Refresh**](swbemobjectex-refresh-.md) .

## <a name="members"></a>Элементы

Объект **свбемрефрешер** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **свбемрефрешер** содержит эти методы.



| Метод                                        | Описание                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Включить**](swbemrefresher-add.md)             | Добавляет новый обновляемый объект в коллекцию в объекте обновления.<br/>                   |
| [**адденум**](swbemrefresher-addenum.md)     | Добавляет новый перечислитель в объект обновления.<br/>                                             |
| [**DeleteAll**](swbemrefresher-deleteall.md) | Удаляет все элементы из коллекции в объекте обновления.<br/>                             |
| [**Элемент**](swbemrefresher-item.md)           | Возвращает указанный элемент обновления из коллекции.<br/>                                    |
| [**Обновить**](swbemrefresher-refresh.md)     | Обновляет все элементы, содержащиеся в объекте обновления.<br/>                          |
| [**Отменит**](swbemrefresher-remove.md)       | Удаляет из Обновитель объект элемента обновления или набор объектов с указанным индексом.<br/> |



 

### <a name="properties"></a>Свойства

Объект **свбемрефрешер** имеет следующие свойства.



| Свойство                                                         | Тип доступа          | Описание                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**аутореконнект**](swbemrefresher-autoreconnect.md)<br/> | Только для чтения<br/> | Указывает, будет ли Обновитель автоматически повторно подключаться к удаленному поставщику, если соединение разорвано.<br/> |
| [**Расчета**](swbemrefresher-count.md)<br/>                 | Только для чтения<br/> | Содержит число элементов в объекте обновления.<br/>                                                      |



 

## <a name="examples"></a>Примеры

В следующем примере показано создание объекта **свбемрефрешер** с помощью методов [**Add**](swbemrefresher-add.md) и [**адденум**](swbemrefresher-addenum.md) для хранения одного экземпляра и экземпляра перечисления, обновления данных и использования свойства Item для получения объектов [**свбемрефрешаблеитем**](swbemrefreshableitem.md) .


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМРЕФРЕШЕР CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемрефрешер<br/>                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемрефрешаблеитем**](swbemrefreshableitem.md)
</dt> <dt>

[**свбемобжектекс**](swbemobjectex.md)
</dt> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

 




