---
description: Дополнительные данные формата для двоичного потока в файле ASF.
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: Атрибут MF_MT_ARBITRARY_FORMAT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7629e92eea07059f562d553985628f2099df1da03bd371617f0eed5183dd69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973613"
---
# <a name="mf_mt_arbitrary_format-attribute"></a>\_ \_ Необязательный \_ атрибут формата MF MT

Дополнительные данные формата для двоичного потока в файле ASF.

## <a name="data-type"></a>Тип данных

**ДВУХБАЙТОВЫХ\[\]**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Remarks

Приложения могут использовать двоичные потоки для хранения пользовательских типов данных. Источник мультимедиа ASF считает значение этого атрибута непрозрачным BLOB-объектом. Элемент **форматтипе** в структуре [**\_ произвольного \_ заголовка MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) определяет макет данных формата.

Эта структура соответствует полю данных формата данных, характерных для конкретного типа, в объекте свойства потока в файлах, где тип потока является **\_ двоичным \_ носителем ASF**. Дополнительные сведения см. в спецификации ASF.

> [!Note]  
> в пакете SDK для Windows Media Format двоичные потоки называются *произвольными потоками* или *произвольными потоками данных*.

 

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[\_ \_ произвольный заголовок MF MT \_](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




