---
description: Максимальное число кадров, которое кодировщик H. 264 принимает для ответа на команду.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: Атрибут MF_MT_H264_MAX_CODEC_CONFIG_DELAY (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc3610f9fce8201e3381b9684e3ea5b76578d8a22f751821dd16b0d9742ffff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035202"
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

## <a name="remarks"></a>Remarks

Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB. Значение соответствует полю **бмакскодекконфигделай** в дескрипторе формата видео УВК 1,2 H. 264.

Этот атрибут также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




