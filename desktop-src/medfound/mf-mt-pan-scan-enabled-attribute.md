---
description: Указывает, включен ли режим панорамирования/развертки.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: Атрибут MF_MT_PAN_SCAN_ENABLED (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545031"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>\_Атрибут с \_ поддержкой MF Pan \_ Scan \_

Указывает, включен ли режим панорамирования/развертки.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Если этот атрибут имеет **значение true**, должен отображаться только регион сдвига и сканирования видео. Регион сдвига и сканирования задается атрибутом [**\_ \_ \_ \_ апертуры панорамного просмотра в MF-MT**](mf-mt-pan-scan-aperture-attribute.md) .

Если этот атрибут имеет **значение false** или не задан, отображается весь отображаемый Апертура видео. Отображаемый Апертура определяется с помощью атрибута « [**\_ \_ Минимальный \_ отображаемый \_ Апертура MF MT**](mf-mt-minimum-display-aperture-attribute.md) ».

Если для этого атрибута задано значение **true**, также следует задать для атрибута [**« \_ \_ \_ \_ Апертура панорамного сдвига MF**](mf-mt-pan-scan-aperture-attribute.md) ».

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

 

 




