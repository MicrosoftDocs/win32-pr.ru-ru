---
description: Идентификатор GUID подтипа для типа мультимедиа.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: Атрибут MF_MT_SUBTYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080865"
---
# <a name="mf_mt_subtype-attribute"></a>\_ \_ Атрибут подтипа MF MT

Идентификатор GUID подтипа для типа мультимедиа.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Комментарии

Идентификатор GUID подтипа определяет конкретный тип формата носителя в основном типе. Например, в видео подтипы включают RGB-24, RGB-32, UYVY, АЙУВ и т. д. В звуке подтипы включают в себя звук PCM, Windows Media Audio 9 и т. д.

Возможные значения см. в следующих разделах:

-   [Идентификаторы GUID для подтипов звука](audio-subtype-guids.md)
-   [Идентификаторы GUID для подтипов видео](video-subtype-guids.md)

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: a GUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Имфаттрибутес:: Сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




