---
description: Указывает время начала для топологии сегмента.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: Атрибут MF_EVENT_SOURCE_PROJECTSTART (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e3d386b90a45d1ba06d0d0c1641b97544ca1d2422dd1d2d6f7762f93cf4ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060704"
---
# <a name="mf_event_source_projectstart-attribute"></a>\_ \_ Атрибут прожектстарт источника события MF \_

Указывает время начала для топологии сегмента.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как значение **лонглонг** .

## <a name="remarks"></a>Remarks

Этот атрибут используется с событием [месаурцестартед](mesourcestarted.md) . Источник Sequencer задает этот атрибут, если топология текущего сегмента имеет атрибут [**MF \_ Topology \_ прожектстарт**](mf-topology-projectstart-attribute.md) . Два атрибута имеют одинаковое значение.

Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты событий](event-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




