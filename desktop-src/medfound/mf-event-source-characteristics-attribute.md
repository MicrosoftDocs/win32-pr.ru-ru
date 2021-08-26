---
description: Задает текущие характеристики источника мультимедиа.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: Атрибут MF_EVENT_SOURCE_CHARACTERISTICS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a9b72adaa5869d806ab0a3c8afcddff7892f93872e86aa6dfe96bde1b8348b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956594"
---
# <a name="mf_event_source_characteristics-attribute"></a>\_ \_ Атрибут характеристик источника события MF \_

Задает текущие характеристики источника мультимедиа.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Значение этого атрибута является побитовым оператором **or** для флагов [**перечисления \_ мфмедиасаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .

Этот атрибут используется с событием [месаурцечарактеристиксчанжед](mesourcecharacteristicschanged.md) .

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

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




