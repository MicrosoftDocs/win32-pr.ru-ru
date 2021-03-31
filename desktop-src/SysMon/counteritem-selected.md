---
title: Каунтеритем. Selected, свойство
description: Возвращает или задает значение, указывающее, выбран ли счетчик.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Выбранное свойство Сисмон
- Выбранное свойство Сисмон, объект Каунтеритем
- Объект Сисмон, выбранное свойство Каунтеритем
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988758"
---
# <a name="counteritemselected-property"></a>Каунтеритем. Selected, свойство

Возвращает или задает значение, указывающее, выбран ли счетчик.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Значение свойства

Значение true, если счетчик выбран. в противном случае — значение false.

## <a name="remarks"></a>Комментарии

Можно выбрать один или несколько счетчиков из коллекции счетчиков. Выбор счетчика, выбор счетчика в условных обозначениях, делает счетчик видимым в условных обозначениях и создает событие [**онкаунтерселектед**](-systemmonitor-oncounterselected.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**каунтеритем**](counteritem.md)
</dt> </dl>

 

 





