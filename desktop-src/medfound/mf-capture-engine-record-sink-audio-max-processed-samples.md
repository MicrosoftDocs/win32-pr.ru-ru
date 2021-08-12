---
description: Задает максимальное число обработанных выборок, которые могут быть помещены в буфер звукового пути приемника записи.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: Атрибут MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b4478ebecfc873c612e8deb0106cba5462e77cd56d5d818b03d74e88679c8b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245042"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a>\_Атрибут сбора данных о \_ \_ \_ приемнике для записи \_ \_ \_ обработчика MF \_

Задает максимальное число обработанных выборок, которые могут быть помещены в буфер звукового пути приемника записи.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Чтобы настроить этот атрибут в подсистеме записи, добавьте его в параметр *паттрибутес* при вызове [**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

Максимальное значение для этого атрибута — 100.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




