---
description: Данные конкретного типа для двоичного потока в файле ASF.
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: Атрибут MF_MT_ARBITRARY_HEADER (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080483"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>\_ \_ Необязательный \_ атрибут заголовка MF MT

Данные конкретного типа для двоичного потока в файле ASF.

## <a name="data-type"></a>Тип данных

**[**MT \_ ПРОИЗВОЛЬНЫй \_ заголовок**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** хранится в виде **\[ \] байта**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Комментарии

Файлы ASF могут содержать потоки с двоичными данными. Атрибут MF \_ \_ Header с произвольным \_ заголовком в типе мультимедиа [**содержит \_ произвольную структуру \_ заголовков MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) , описывающую поток.

В дополнение к \_ \_ атрибуту заголовка MF MT произвольный \_ заголовок Тип мультимедиа для двоичного потока ASF содержит следующие атрибуты:



| attribute                                                 | Описание                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md) | Значение атрибута — **мфмедиатипе \_ binary**. |
| [\_ \_ необязательный \_ формат MF MT](mf-mt-arbitrary-format.md)   | Содержит дополнительные данные формата.                       |



 

> [!Note]  
> В пакете SDK для формата Windows Media двоичные потоки называются *произвольными потоками* или *произвольными потоками данных*.

 

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




