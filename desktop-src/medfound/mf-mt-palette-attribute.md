---
description: Содержит записи палитры для типа видеоматериала. Используйте этот атрибут для форматов видео палеттизед, например RGB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: Атрибут MF_MT_PALETTE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a20623262be0129cabf5675fd4cd1a37ec2fb61b6b9a0dd5e135fa9e48e1abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741659"
---
# <a name="mf_mt_palette-attribute"></a>\_ \_ Атрибут палитры MF MT

Содержит записи палитры для типа видеоматериала. Используйте этот атрибут для форматов видео палеттизед, например RGB 8.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Remarks

Данные атрибута являются массивом объединений [**мфпалеттинтри**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




