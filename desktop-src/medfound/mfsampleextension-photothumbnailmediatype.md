---
description: Содержит Имфмедиатипе, описывающий тип формата изображения, который содержится в \_ атрибуте Мфсампликстенсион thumbnail.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: Атрибут MFSampleExtension_PhotoThumbnailMediaType (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720037"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>Мфсампликстенсион \_ фотосумбнаилмедиатипе, атрибут

Содержит [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , описывающий тип формата изображения, который содержится в атрибуте [мфсампликстенсион \_ thumbnail](mfsampleextension-photothumbnail.md) .

## <a name="data-type"></a>Тип данных

**IUnknown** , хранимый как **имфмедиатипе**

## <a name="remarks"></a>Комментарии

Если атрибут [мфсампликстенсион \_ фотоэскизов](mfsampleextension-photothumbnail.md) имеется в образце Photo, то мфсампликстенсион \_ фотосумбнаилмедиатипе является обязательным и должен содержать, по крайней мере, [ \_ \_ основной \_ тип MF MT, номер](mf-mt-major-type-attribute.md)MF- [ \_ \_ MT](mf-mt-subtype-attribute.md) и [ \_ \_ \_ Размер кадра MF MT](mf-mt-frame-size-attribute.md) , описывающие эскиз.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>                                |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Мфсампликстенсион \_ ФотоЭскизы](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




