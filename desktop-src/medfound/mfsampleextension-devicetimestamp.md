---
description: Содержит метку времени из драйвера устройства.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: Атрибут MFSampleExtension_DeviceTimestamp (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b354ecd0e399fc297d3677d29b88847f9eba8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898741"
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

## <a name="remarks"></a>Комментарии

Этот атрибут задается в примерах носителей, созданных источником мультимедиа для устройства записи. Значение этого атрибута находится в домене [**мфтиме**](mftime.md) , которому предоставляется общий доступ к эпохе со счетчиком производительности запросов (QPC) и всегда выражается в единицах 100 нс. Этот атрибут доступен для МФТС, вставленного в конвейер захвата.

Чтобы получить отметку времени относительно начала потоковой передачи, вызовите метод [**имфсампле:: жетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Видеозапись Аудио/видео в Media Foundation](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> </dl>

 

 




