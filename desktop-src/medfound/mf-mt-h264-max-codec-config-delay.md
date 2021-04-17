---
description: Максимальное число кадров, которое кодировщик H. 264 принимает для ответа на команду.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: Атрибут MF_MT_H264_MAX_CODEC_CONFIG_DELAY (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a835d5b5a37be0c722f313aaf4fe8ed8aa55f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656593"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a>\_ \_ \_ \_ \_ Атрибут задержки конфигурации кодека MF MT H264 Single bitrate \_

Максимальное число кадров, которое кодировщик H. 264 принимает для ответа на команду.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB. Значение соответствует полю **бмакскодекконфигделай** в дескрипторе формата видео УВК 1,2 H. 264.

Этот атрибут также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




