---
description: Указывает поддерживаемые режимы управления частотой для видеопотока H. 264.
ms.assetid: DAA62ECD-AFA2-40C2-9B52-F2D581F4D894
title: Атрибут MF_MT_H264_SUPPORTED_RATE_CONTROL_MODES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b315bf41d662dd5abb283c346710f485789ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692462"
---
# <a name="mf_mt_h264_supported_rate_control_modes-attribute"></a>\_ \_ \_ \_ \_ Атрибут режимов управления скоростью H264 Single bitrate \_ MF MT

Указывает поддерживаемые режимы управления частотой для видеопотока H. 264.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB. Значение соответствует полю **бмсуппортедратеконтролмодес** в дескрипторе формата видео УВК 1,5 H. 264.

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

 

 




