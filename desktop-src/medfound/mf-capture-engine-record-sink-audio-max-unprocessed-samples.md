---
description: Задает максимальное число необработанных выборок, которые могут быть помещены в буфер для обработки в звуковом пути приемника записи.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: Атрибут MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442e9b5eca3354e87b8e36b55a3c6cb92ec6f131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344582"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>\_ \_ \_ \_ \_ \_ \_ Необработанный \_ атрибут ВЫБОРки для звука записи подсистемы захвата MF

Задает максимальное число необработанных выборок, которые могут быть помещены в буфер для обработки в звуковом пути приемника записи.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Комментарии

Чтобы настроить этот атрибут в подсистеме записи, добавьте его в параметр *паттрибутес* при вызове [**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

Максимальное значение для этого атрибута — 100.

После того как запись помещается в буфер на максимальное количество необработанных образцов, заданное в \_ \_ стоке записи подсистемы захвата ( \_ \_ \_ \_ число \_ необработанных сбросов) \_ , это уменьшает частоту кадров, удаляя образцы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




