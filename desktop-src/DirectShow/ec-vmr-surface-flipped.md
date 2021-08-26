---
description: Посылается, когда на представляемой поверхности вызывается метод отражения VMR-7's распределителя. Таким образом, VMR должен синхронизировать свою таблицу Директксва поверхностей с цепочкой зеркального отображения DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c352af01ee31728b41aa276d14ca64b7c3fa6770bb4c9328a8c4ee5e91bb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043354"
---
# <a name="ec_vmr_surface_flipped"></a>\_перевернутая поверхность с фильтром EC \_ \_

Посылается, когда на представляемой поверхности вызывается метод отражения VMR-7's распределителя. Таким образом, VMR должен синхронизировать свою таблицу Директксва поверхностей с цепочкой зеркального отображения DirectDraw.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Код состояния, возвращенный методом отражения DirectDraw.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Пользовательский распределитель — выступающие для VMR-7 должны отправить это событие. Это событие не пересылается в приложения и не используется с распределителя-Presenters для VMR-9.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




