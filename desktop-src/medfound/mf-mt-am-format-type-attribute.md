---
description: Содержит идентификатор GUID формата DirectShow для типа мультимедиа.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Атрибут MF_MT_AM_FORMAT_TYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344572"
---
# <a name="mf_mt_am_format_type-attribute"></a>MF \_ MT \_ , \_ Формат: \_ атрибут типа

Содержит идентификатор GUID формата DirectShow для типа мультимедиа.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Комментарии

Этот атрибут может быть задан при преобразовании типа носителя DirectShow в Media Foundation тип носителя. Атрибут указывает исходный тип формата DirectShow. Значение соответствует элементу форматтипе структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

Для звукового формата атрибут [**\_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) может содержать исходный блок формата, если тип формата DirectShow не был распознан.

Не устанавливайте этот атрибут для типа мультимедиа, если только не выполняется преобразование структуры формата DirectShow.

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

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[Преобразования типов мультимедиа](media-type-conversions.md)
</dt> <dt>

[Типы носителей](media-types.md)
</dt> <dt>

[**Имфаттрибутес:: a GUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Имфаттрибутес:: Сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**мфкреатемедиатипефромрепресентатион**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
