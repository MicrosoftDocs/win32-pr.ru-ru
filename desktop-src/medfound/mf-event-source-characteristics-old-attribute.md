---
description: Задает предыдущие характеристики источника мультимедиа.
ms.assetid: 9779f350-60d5-4129-bada-0c4a58f93e6a
title: Атрибут MF_EVENT_SOURCE_CHARACTERISTICS_OLD (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb19505643de064e3aa54abc9e37649ecd97ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656578"
---
# <a name="mf_event_source_characteristics_old-attribute"></a>\_ \_ \_ Старый атрибут характеристик для источника события MF \_

Задает предыдущие характеристики источника мультимедиа. Данные атрибута являются **побитовыми флагами из перечисления** [**\_ характеристик мфмедиасаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут используется с событием [месаурцечарактеристиксчанжед](mesourcecharacteristicschanged.md) .

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
</dt> <dt>

[**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




