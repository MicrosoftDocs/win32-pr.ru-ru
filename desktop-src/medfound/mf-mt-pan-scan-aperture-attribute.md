---
description: Определяет апертуру и сканирование, т. е. 4&\# 215; 3 региона видео, который должен отображаться в режиме панорамирования и сканирования.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: Атрибут MF_MT_PAN_SCAN_APERTURE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692546"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a>\_ \_ \_ Атрибут апертуры развертки MF MT \_

Определяет апертуру и сканирование, то есть 4 × 3 региона видео, который должен отображаться в режиме панорамы и сканирования.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Значение атрибута является структурой [**мфвидеоареа**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

Этот атрибут используется для обрезки широкоэкранных видео до 4:3 пропорций. Апертура/развертка используется только в режиме панорамирования/развертки, который включается путем установки атрибута « [**\_ \_ \_ \_ Включить сканирование MF MT Pan**](mf-mt-pan-scan-enabled-attribute.md) » в **значение true**.

Если режим Pan/Scan не включен, используйте апертуру экрана, заданную атрибутом [**\_ \_ \_ \_ апертуры по крайней мере в MF MT**](mf-mt-minimum-display-aperture-attribute.md) .

Если этот атрибут не задан, то раскадровка панорамы и развертки считается кадром всего видео.

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

[**\_ \_ Минимальный \_ \_ Апертура экрана MF MT**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_ \_ включена проверка панорамы MF MT \_ \_**](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




