---
description: Указывает, включен ли режим панорамирования/развертки.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: Атрибут MF_MT_PAN_SCAN_ENABLED (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e78c38cd15f5d735d49b5689905a40d74614b46817a8621ce1dabcdc5a1b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955494"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>\_Атрибут с \_ поддержкой MF Pan \_ Scan \_

Указывает, включен ли режим панорамирования/развертки.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Если этот атрибут имеет **значение true**, должен отображаться только регион сдвига и сканирования видео. Регион сдвига и сканирования задается атрибутом [**\_ \_ \_ \_ апертуры панорамного просмотра в MF-MT**](mf-mt-pan-scan-aperture-attribute.md) .

Если этот атрибут имеет **значение false** или не задан, отображается весь отображаемый Апертура видео. Отображаемый Апертура определяется с помощью атрибута « [**\_ \_ Минимальный \_ отображаемый \_ Апертура MF MT**](mf-mt-minimum-display-aperture-attribute.md) ».

Если для этого атрибута задано значение **true**, также следует задать для атрибута [**« \_ \_ \_ \_ Апертура панорамного сдвига MF**](mf-mt-pan-scan-aperture-attribute.md) ».

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[Пропорции рисунка](picture-aspect-ratio.md)
</dt> </dl>

 

 




