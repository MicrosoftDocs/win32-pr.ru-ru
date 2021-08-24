---
description: Время презентации, с которой приемники мультимедиа выводит первый образец новой топологии.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: Атрибут MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd5949a73244eec26fb0390805c11f630291a470b2016b5a3575311261b72a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723184"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a>\_Событие MF \_ Начало \_ презентации \_ время показа \_ с \_ выходным атрибутом

Время презентации, с которой приемники мультимедиа выводит первый образец новой топологии.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как значение **лонглонг** .

## <a name="remarks"></a>Remarks

Если какие-либо объекты конвейера в предыдущей топологии буферизованных данных, это значение будет немного меньше значения атрибута [**\_ \_ \_ \_ смещения времени представления событий MF**](mf-event-presentation-time-offset-attribute.md) , так как приемники должны визуализировать буферизованные данные.

Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты событий](event-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




