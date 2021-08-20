---
description: Начат новый сегмент.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b33d9f75dc4fa8e86b13e61c78b98a19248c16f2f627e1c1b09e536b31a73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015922"
---
# <a name="ec_segment_started"></a>\_сегмент EC \_ запущен

Начат новый сегмент.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

( **\_ время ссылки на****константу** \* ) указатель на значение **\_ времени ссылки** , указывающее накопленное время потока с начала сегмента в 100-наносекундных единицах.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Номер сегмента (от нуля).

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Это событие не отправляется в приложение. Приложения не могут переопределять действие по умолчанию для этого события.

## <a name="remarks"></a>Remarks

Если фильтр будет отправлять конец сегмента [**EC \_ \_ \_**](ec-end-of-segment.md) в конце сегмента, он отправляет это событие в начале сегмента. Диспетчер графов фильтров использует это уведомление о событии, чтобы вычислить, сколько \_ \_ уведомлений в виде конца сегмента EC \_ должно рассчитываться в конце сегмента.

По умолчанию фильтры не отправляют данные о [**\_ завершении событий \_ \_ сегмента EC**](ec-end-of-segment.md) в конце сегментов и поэтому не должны отсылать это событие. Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




