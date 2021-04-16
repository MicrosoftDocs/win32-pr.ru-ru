---
description: Содержит флаги, определяющие возможности сеанса мультимедиа на основе текущей презентации.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: Атрибут MF_EVENT_SESSIONCAPS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af38d61f07bf038d1906d6f11e46fea63e800efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656577"
---
# <a name="mf_event_sessioncaps-attribute"></a>\_ \_ Атрибут СЕССИОНКАПС события MF

Содержит флаги, определяющие возможности сеанса мультимедиа на основе текущей презентации.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут содержит побитовое **или** с нулевым или более флагами. Список возможных флагов см. в разделе [**имфмедиасессион:: жетсессионкапабилитиес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).

Этот атрибут используется с событием [месессионкапабилитиесчанжед](mesessioncapabilitieschanged.md) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
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

 

 




