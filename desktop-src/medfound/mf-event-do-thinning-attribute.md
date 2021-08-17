---
description: Когда источник мультимедиа запрашивает новый темп воспроизведения, этот атрибут указывает, запрашиваются ли в источнике тонкости. Определение тонкости см. в разделе сведения об управлении скоростью.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: Атрибут MF_EVENT_DO_THINNING (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9305df2b17e00b03bd9788ecd8caf26db82b8e331d1c72626374b63e7dcaf15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104940"
---
# <a name="mf_event_do_thinning-attribute"></a>\_Событие MF \_ — \_ тонкий атрибут

Когда источник мультимедиа запрашивает новый темп воспроизведения, этот атрибут указывает, запрашиваются ли в источнике тонкости. Определение тонкости см. в разделе [сведения об управлении скоростью](about-rate-control.md).

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Этот атрибут используется с событием [месаурцератечанжерекуестед](mesourceratechangerequested.md) . Если значение равно **true**, источник мультимедиа запрашивает переключение на тонкое воспроизведение.

Значение по умолчанию — **FALSE**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты событий](event-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




