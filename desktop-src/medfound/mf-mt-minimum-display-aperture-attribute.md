---
description: Определяет отображаемый Апертура, представляющий собой область видеокадра, которая содержит допустимые данные изображения.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: Атрибут MF_MT_MINIMUM_DISPLAY_APERTURE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711155"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a>\_ \_ Минимальный \_ отображаемый \_ атрибут апертуры MF

Определяет отображаемый Апертура, представляющий собой область видеокадра, которая содержит допустимые данные изображения.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Значение атрибута является структурой [**мфвидеоареа**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

Минимальный отображаемый Апертура — это область, которая содержит действительную часть сигнала. Пиксели за пределами апертуры содержат недопустимые данные и не должны отображаться.

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

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[Пропорции рисунка](picture-aspect-ratio.md)
</dt> <dt>

[Типы видеоклипов](video-media-types.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_ \_ геометрическое \_ Апертура MF**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**\_ \_ \_ Апертура для поиска MF MT \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




