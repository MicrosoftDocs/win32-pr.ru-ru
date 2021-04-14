---
description: Начат новый сегмент.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651647"
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

## <a name="remarks"></a>Комментарии

Если фильтр будет отправлять конец сегмента [**EC \_ \_ \_**](ec-end-of-segment.md) в конце сегмента, он отправляет это событие в начале сегмента. Диспетчер графов фильтров использует это уведомление о событии, чтобы вычислить, сколько \_ \_ уведомлений в виде конца сегмента EC \_ должно рассчитываться в конце сегмента.

По умолчанию фильтры не отправляют данные о [**\_ завершении событий \_ \_ сегмента EC**](ec-end-of-segment.md) в конце сегментов и поэтому не должны отсылать это событие. Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




