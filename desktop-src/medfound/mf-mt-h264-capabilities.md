---
description: Задает флаги возможностей для видеопотока H. 264.
ms.assetid: 59EF18D6-6063-4EF3-BBFB-51A966CFF09E
title: Атрибут MF_MT_H264_CAPABILITIES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138cfa32fc50ebb02ca4d399a178b338e58016c64ae3486d7f7b4a76f3e47afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741819"
---
# <a name="mf_mt_h264_capabilities-attribute"></a>\_ \_ Атрибут возможностей H264 Single bitrate MF MT \_

Задает флаги возможностей для видеопотока H. 264.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Remarks

Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB. Значение соответствует полю **бмкапабилитиес** в дескрипторе кадра видео УВК 1,5 H. 264.

Этот атрибут также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




