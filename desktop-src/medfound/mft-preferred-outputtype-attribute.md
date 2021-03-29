---
description: Указывает предпочтительный выходной формат кодировщика.
ms.assetid: 36a09696-3fe7-41a0-93f1-712220f88b04
title: Атрибут MFT_PREFERRED_OUTPUTTYPE_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13cd079bee65f5324987d9b38dca845ec5b85f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898725"
---
# <a name="mft_preferred_outputtype_attribute-attribute"></a>\_ \_ Атрибут атрибута OUTPUTTYPE, предпочтительный для MFT \_

Указывает предпочтительный выходной формат кодировщика.

## <a name="data-type"></a>Тип данных

**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Имфаттрибутес \** _ хранится как _*IUnknown \**_

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Применяется к

[**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Комментарии

Этот атрибут может быть задан для объекта активации, возвращаемого функцией [**мфкреатетрансформактивате**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) . Атрибут применяется только в том случае, если объект активации настроен для создания кодировщика. Значением атрибута является тип мультимедиа. Объект активации задает этот тип выходных данных для кодировщика.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**мфкреатетрансформактивате**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




