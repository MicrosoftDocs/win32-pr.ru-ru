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
ms.openlocfilehash: 41e5cfcc65c54f882f10e87a0f2aaebad0e1a55c94b6581031b034799987bc6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956963"
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

## <a name="remarks"></a>Remarks

Можно выбрать один или несколько счетчиков из коллекции счетчиков. Выбор счетчика, выбор счетчика в условных обозначениях, делает счетчик видимым в условных обозначениях и создает событие [**онкаунтерселектед**](-systemmonitor-oncounterselected.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**каунтеритем**](counteritem.md)
</dt> </dl>

 

 





