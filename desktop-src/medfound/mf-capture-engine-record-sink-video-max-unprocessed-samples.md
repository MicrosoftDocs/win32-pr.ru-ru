---
description: Задает максимальное число необработанных выборок, которые могут быть помещены в буфер для обработки в пути к видео приемника записи.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: Атрибут MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f776dd795103fccf81da4c739b767131a03bf83245c3c79e724274dcb52dc0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956824"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a>\_ \_ \_ \_ \_ \_ \_ Необработанный \_ атрибут выборки данных для приемника записей подсистемы захвата MF

Задает максимальное число необработанных выборок, которые могут быть помещены в буфер для обработки в пути к видео приемника записи.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Remarks

Чтобы настроить этот атрибут в подсистеме записи, добавьте его в параметр *паттрибутес* при вызове [**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

Максимальное значение для этого атрибута — 17.

После того как запись помещается в буфер на максимальное количество необработанных образцов, заданное с помощью \_ \_ приемника записей подсистемы записи MF, \_ \_ Максимальное число \_ \_ \_ необработанных \_ образцов, это снижает частоту кадров, удаляя образцы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                         |
| Заголовок<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




