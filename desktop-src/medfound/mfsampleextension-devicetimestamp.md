---
description: Содержит метку времени из драйвера устройства.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: Атрибут MFSampleExtension_DeviceTimestamp (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3322f295908ae2bbdc095a21ab57ee2e0f2ed10dd2267eaea227b9248ddc226b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241129"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a>Мфсампликстенсион \_ DeviceTimestamp, атрибут

Содержит метку времени из драйвера устройства.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarks

Этот атрибут задается в примерах носителей, созданных источником мультимедиа для устройства записи. Значение этого атрибута находится в домене [**мфтиме**](mftime.md) , которому предоставляется общий доступ к эпохе со счетчиком производительности запросов (QPC) и всегда выражается в единицах 100 нс. Этот атрибут доступен для МФТС, вставленного в конвейер захвата.

Чтобы получить отметку времени относительно начала потоковой передачи, вызовите метод [**имфсампле:: жетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Видеозапись Аудио/видео в Media Foundation](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> </dl>

 

 




