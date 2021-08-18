---
description: Содержит свойства конфигурации кодировщика.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: Атрибут MFT_PREFERRED_ENCODER_PROFILE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85acf742e518d91c6512b2b887cca910c3b19d21180500bd1180e6972255e54f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722509"
---
# <a name="mft_preferred_encoder_profile-attribute"></a>\_Атрибут предпочтительного \_ профиля КОДИРОВЩИКа MFT \_

Содержит свойства конфигурации кодировщика.

## <a name="data-type"></a>Тип данных

**[**Имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \* *_ хранится как _* IUnknown\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Применяется к

[**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Remarks

Этот атрибут может быть задан для объекта активации, возвращаемого функцией [**мфкреатетрансформактивате**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) . Атрибут применяется только в том случае, если объект активации настроен для создания кодировщика. Значение атрибута является указателем на хранилище атрибутов, которое само содержит свойства, заданные для кодировщика.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**мфкреатетрансформактивате**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




