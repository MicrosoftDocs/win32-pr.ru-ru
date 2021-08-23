---
description: содержит идентификатор GUID формата DirectShow для типа мультимедиа.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Атрибут MF_MT_AM_FORMAT_TYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff59e148f7532cc07e47acf033de91b5eaeb8969f0c39376850738fd54e758e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973633"
---
# <a name="mf_mt_am_format_type-attribute"></a>MF \_ MT \_ , \_ Формат: \_ атрибут типа

содержит идентификатор GUID формата DirectShow для типа мультимедиа.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Remarks

этот атрибут может быть задан при преобразовании DirectShowного типа носителя в Media Foundationный тип мультимедиа. атрибут указывает исходный тип формата DirectShow. Значение соответствует элементу форматтипе структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

для звукового формата атрибут [**\_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) может содержать исходный блок формата, если тип формата DirectShow не распознан.

не устанавливайте этот атрибут для типа мультимедиа, если только не выполняется преобразование структуры формата DirectShow.

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

 

 
