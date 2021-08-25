---
description: Используйте свойство Count объекта SWbemObjectSet, чтобы определить, сколько элементов находится в коллекции SWbemObjectSet. Это свойство доступно только для чтения.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Свойство SWbemObjectSet. Count (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1305cc0119f002f8ac3229664227d5c21bea9d865eedb0a31fcb7eb77250424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857234"
---
# <a name="swbemobjectsetcount-property"></a>SWbemObjectSet. Count, свойство

Используйте свойство **Count** объекта [**SWbemObjectSet**](swbemobjectset.md) , чтобы определить, сколько элементов находится в коллекции **SWbemObjectSet** . Это свойство доступно только для чтения.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

При использовании параметра count необходимо соблюдать осторожность, так как инструментарий WMI не сохраняет непрерывное количество элементов в коллекции. Если вы запрашиваете счетчик для коллекции, Инструментарий WMI не может мгновенно ответить на число. Вместо этого он должен буквально подсчитать элементы, перечисляя всю коллекцию. Для коллекции, которая содержит относительно несколько элементов, таких как службы, это перечисление, скорее всего, занимает меньше секунды. Однако подсчет количества событий в коллекции журналов событий может занять значительно больше времени.

А затем Предположим, что необходимо отобразить значения свойств для каждого события в коллекции. В этом случае Инструментарий WMI должен перечислять всю коллекцию во второй раз.

> [!Note]  
> При попытке получить это свойство из объекта [**SWbemObjectSet**](swbemobjectset.md) , возвращаемого методом, в котором указанные флаги включены в флаг вбемфлагфорвардонли, возникнет ошибка вбемеррфаилед.

 

## <a name="examples"></a>Примеры

В большинстве случаев единственное, что вы будете делать с SWbemObjectSet, — перечисляет все объекты, содержащиеся в самой коллекции. Однако счетчик количества, который может быть полезен при создании сценариев системного администрирования. Как следует из названия, Count сообщает число элементов в коллекции. Например, этот скрипт извлекает коллекцию всех служб, установленных на компьютере, а затем отображает общее число найденных служб:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



То, что делает число полезным, заключается в том, что он может сообщить вам, доступен ли конкретный экземпляр на компьютере. Например, этот скрипт получает коллекцию всех служб на компьютере с именем W3SVC. Если значение счетчика равно 0 (и оно допустимо для коллекций, не имеющих экземпляров), это означает, что на компьютере не установлена служба W3SVC.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемобжектсет<br/>                                                         |



 

 




