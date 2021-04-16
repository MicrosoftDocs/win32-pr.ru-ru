---
description: Указывает, требует ли тип видеоклипа принудительное применение защиты от копирования.
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: Атрибут MF_MT_DRM_FLAGS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ef771cb72050b2273d822ce799092ce51e64c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712407"
---
# <a name="mf_mt_drm_flags-attribute"></a>\_ \_ \_ Атрибут флагов DRM MF MT

Указывает, требует ли тип видеоклипа принудительное применение защиты от копирования.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Значение этого атрибута является членом перечисления [**мфвидеодрмфлагс**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) .

Этот атрибут обеспечивает указание для приложения. Он не используется для обеспечения защиты от копирования или для указания механизма защиты от копирования.

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

[MF \_ - \_ защищенный SD](mf-sd-protected-attribute.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




