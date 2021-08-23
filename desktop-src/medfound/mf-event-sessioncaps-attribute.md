---
description: Содержит флаги, определяющие возможности сеанса мультимедиа на основе текущей презентации.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: Атрибут MF_EVENT_SESSIONCAPS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175c81d1cc231204060a63a90ffe9e2432b73bdec35c7885dea203416995ea92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973793"
---
# <a name="mf_event_sessioncaps-attribute"></a>\_ \_ Атрибут СЕССИОНКАПС события MF

Содержит флаги, определяющие возможности сеанса мультимедиа на основе текущей презентации.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут содержит побитовое **или** с нулевым или более флагами. Список возможных флагов см. в разделе [**имфмедиасессион:: жетсессионкапабилитиес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).

Этот атрибут используется с событием [месессионкапабилитиесчанжед](mesessioncapabilitieschanged.md) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



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

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




