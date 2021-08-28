---
title: Код уведомления HDN_ENDFILTEREDIT (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка о завершении редактирования фильтра. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d3832875-4cde-4d8a-b3a4-a8dae0742c56
keywords:
- HDN_ENDFILTEREDIT кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- HDN_ENDFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225ac41a875f6eadb17054c89e34451306cd78db66cc40cc3c26d15035f7c388
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435544"
---
# <a name="hdn_endfilteredit-notification-code"></a>\_Код уведомления ХДН ендфилтередит

Сообщает родительскому окну элемента управления заголовка о завершении редактирования фильтра. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_ENDFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую дополнительные сведения о редактируемом фильтре.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





