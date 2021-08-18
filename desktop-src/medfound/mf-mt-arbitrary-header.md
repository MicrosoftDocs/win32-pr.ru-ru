---
description: Данные конкретного типа для двоичного потока в файле ASF.
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: Атрибут MF_MT_ARBITRARY_HEADER (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d824aad4f76947786f991807d2f7b301703e3e356d2d1cfb416aa634d49f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826524"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>\_ \_ Необязательный \_ атрибут заголовка MF MT

Данные конкретного типа для двоичного потока в файле ASF.

## <a name="data-type"></a>Тип данных

**[**MT \_ ПРОИЗВОЛЬНЫй \_ заголовок**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** хранится в виде **\[ \] байта**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Remarks

Файлы ASF могут содержать потоки с двоичными данными. Атрибут MF \_ \_ Header с произвольным \_ заголовком в типе мультимедиа [**содержит \_ произвольную структуру \_ заголовков MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) , описывающую поток.

В дополнение к \_ \_ атрибуту заголовка MF MT произвольный \_ заголовок Тип мультимедиа для двоичного потока ASF содержит следующие атрибуты:



| attribute                                                 | Описание                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md) | Значение атрибута — **мфмедиатипе \_ binary**. |
| [\_ \_ необязательный \_ формат MF MT](mf-mt-arbitrary-format.md)   | Содержит дополнительные данные формата.                       |



 

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
</dt> </dl>

 

 




