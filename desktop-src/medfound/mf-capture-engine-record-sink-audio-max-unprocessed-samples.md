---
description: Задает максимальное число необработанных выборок, которые могут быть помещены в буфер для обработки в звуковом пути приемника записи.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: Атрибут MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5f6d2a2bcd592d5a6991028af90af008a827940903084054933558ed7088c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060834"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>\_ \_ \_ \_ \_ \_ \_ Необработанный \_ атрибут ВЫБОРки для звука записи подсистемы захвата MF

Задает максимальное число необработанных выборок, которые могут быть помещены в буфер для обработки в звуковом пути приемника записи.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Remarks

Чтобы настроить этот атрибут в подсистеме записи, добавьте его в параметр *паттрибутес* при вызове [**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

Максимальное значение для этого атрибута — 100.

После того как запись помещается в буфер на максимальное количество необработанных образцов, заданное в \_ \_ стоке записи подсистемы захвата ( \_ \_ \_ \_ число \_ необработанных сбросов) \_ , это уменьшает частоту кадров, удаляя образцы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                         |
| Заголовок<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




