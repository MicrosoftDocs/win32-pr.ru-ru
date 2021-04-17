---
description: Содержит заголовок последовательности MPEG-1 или MPEG-2 для типа видеоматериала.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: Атрибут MF_MT_MPEG_SEQUENCE_HEADER (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693302"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a>\_ \_ \_ Атрибут заголовка последовательного сервера MF MT MPEG \_

Содержит заголовок последовательности MPEG-1 или MPEG-2 для типа видеоматериала.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Этот атрибут соответствует элементу **двсекуенцехеадер** структуры [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) или элементу **бсекуенцехеадер** структуры [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .

Для видео H264 Single bitrate и H265 BLOB-объект содержит Соединенные [NAL-единицы](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) в формате приложение б, а также их начальные коды. В частности, для H264 Single bitrate видео это SPS & PPS NAL Units. Для H265 это ВПС, SPS & PPS.

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

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 
