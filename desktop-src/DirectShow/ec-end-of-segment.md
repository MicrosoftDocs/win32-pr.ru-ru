---
description: Достигнут конец сегмента.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13bbc55ab316a56264c9c0b66196a53181d0abd72bfdddf3315523b8c387a1d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639754"
---
# <a name="ec_end_of_segment"></a>\_конец \_ \_ сегмента EC

Достигнут конец сегмента.

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

Диспетчер графов фильтров проверяет количество событий **\_ завершения \_ \_ сегмента EC** по числу событий [**\_ \_ начала сегмента EC**](ec-segment-started.md) . Если они совпадают, перенаправляет событие **\_ конца \_ \_ сегмента EC** в приложение. Приложения не могут переопределять действие по умолчанию для этого события.

## <a name="remarks"></a>Remarks

Этот код события поддерживает простой цикл. Когда вызов метода [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) включает \_ флаг «поиск \_ сегмента», фильтр источника отправляет этот код события вместо вызова [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).

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

 

 




