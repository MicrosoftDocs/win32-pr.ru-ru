---
title: Сообщение RB_PUSHCHEVRON (Коммктрл. h)
description: Посылается элементу управления главной панели для программной отправки шеврона.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- элементы управления Windows сообщений RB_PUSHCHEVRON
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d095cd824970b7ea90541420274b204a1e2f63ce6e1218e62221741f572feb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434974"
---
# <a name="rb_pushchevron-message"></a>\_Сообщение ПУШЧЕВРОН RB

Посылается элементу управления главной панели для программной отправки шеврона.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс полосы, Шеврон которого должен быть отправлен.

</dd> <dt>

*lParam* 
</dt> <dd>

Определенное приложением 32-разрядное значение. Он будет передан обратно в приложение в качестве элемента **лпарамнм** структуры [**нмребарчеврон**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) , который передается с уведомлением [РБН \_ чевронпушед](rbn-chevronpushed.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="remarks"></a>Remarks

При отправке этого сообщения элемент управления "Главная панель" отправит приложению код уведомления [РБН \_ чевронпушед](rbn-chevronpushed.md) , запросите его, чтобы отобразить угловое меню.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





