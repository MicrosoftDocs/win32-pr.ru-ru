---
description: Содержит Имфмедиатипе, описывающий тип формата изображения, который содержится в \_ атрибуте Мфсампликстенсион thumbnail.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: Атрибут MFSampleExtension_PhotoThumbnailMediaType (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77496340d598c7caf1064df0d3fc7e1ae7f112309bf6fbba6a66f3d5516e3828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713604"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>Мфсампликстенсион \_ фотосумбнаилмедиатипе, атрибут

Содержит [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , описывающий тип формата изображения, который содержится в атрибуте [мфсампликстенсион \_ thumbnail](mfsampleextension-photothumbnail.md) .

## <a name="data-type"></a>Тип данных

**IUnknown** , хранимый как **имфмедиатипе**

## <a name="remarks"></a>Remarks

Если атрибут [мфсампликстенсион \_ фотоэскизов](mfsampleextension-photothumbnail.md) имеется в образце Photo, то мфсампликстенсион \_ фотосумбнаилмедиатипе является обязательным и должен содержать, по крайней мере, [ \_ \_ основной \_ тип MF MT, номер](mf-mt-major-type-attribute.md)MF- [ \_ \_ MT](mf-mt-subtype-attribute.md) и [ \_ \_ \_ Размер кадра MF MT](mf-mt-frame-size-attribute.md) , описывающие эскиз.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                     |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Мфсампликстенсион \_ ФотоЭскизы](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




