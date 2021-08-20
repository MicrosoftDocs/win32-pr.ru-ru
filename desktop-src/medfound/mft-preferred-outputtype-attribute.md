---
description: Указывает предпочтительный выходной формат кодировщика.
ms.assetid: 36a09696-3fe7-41a0-93f1-712220f88b04
title: Атрибут MFT_PREFERRED_OUTPUTTYPE_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec39f95182b9070aa442c20719d88801ea944e77d1d49ea67d8320c130610fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688907"
---
# <a name="mft_preferred_outputtype_attribute-attribute"></a>\_ \_ Атрибут атрибута OUTPUTTYPE, предпочтительный для MFT \_

Указывает предпочтительный выходной формат кодировщика.

## <a name="data-type"></a>Тип данных

**[**Имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \* *_ хранится как _* IUnknown\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Применяется к

[**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Remarks

Этот атрибут может быть задан для объекта активации, возвращаемого функцией [**мфкреатетрансформактивате**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) . Атрибут применяется только в том случае, если объект активации настроен для создания кодировщика. Значением атрибута является тип мультимедиа. Объект активации задает этот тип выходных данных для кодировщика.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**мфкреатетрансформактивате**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




