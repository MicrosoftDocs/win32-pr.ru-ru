---
description: В следующей таблице описаны основные типы носителей.
ms.assetid: 718a07f6-e2e4-4670-b9cf-982b53abffd2
title: Основные типы (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5722cbad713f2fb9ae876e58941bde44c2e110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685426"
---
# <a name="major-types"></a>Основные типы

В следующей таблице описаны основные типы носителей.



| Идентификатор GUID                                                                                                                                                                                                                                  | Описание                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="MEDIATYPE_AnalogAudio"></span><span id="mediatype_analogaudio"></span><span id="MEDIATYPE_ANALOGAUDIO"></span><dl> <dt>**MEDIATYPE \_ аналогаудио**</dt> </dl>         | Аналоговый звук.<br/>                                                                                  |
| <span id="MEDIATYPE_AnalogVideo"></span><span id="mediatype_analogvideo"></span><span id="MEDIATYPE_ANALOGVIDEO"></span><dl> <dt>**MEDIATYPE \_ аналогвидео**</dt> </dl>         | Аналоговый видеоролик.<br/>                                                                                  |
| <span id="MEDIATYPE_Audio"></span><span id="mediatype_audio"></span><span id="MEDIATYPE_AUDIO"></span><dl> <dt>**MEDIATYPE \_ Audio**</dt> </dl>                                 | Аудиосигнал. См. раздел [аудио подтипы](audio-subtypes.md).<br/>                                               |
| <span id="MEDIATYPE_AUXLine21Data"></span><span id="mediatype_auxline21data"></span><span id="MEDIATYPE_AUXLINE21DATA"></span><dl> <dt>**MEDIATYPE \_ AUXLine21Data**</dt> </dl> | Строка 21 данных. Используется закрытыми субтитрами. См. [**строку 21 типы носителей**](line-21-media-types.md).<br/> |
| <span id="MEDIATYPE_File"></span><span id="mediatype_file"></span><span id="MEDIATYPE_FILE"></span><dl> <dt>**\_Файл MEDIATYPE**</dt> </dl>                                     | File. (Устарело)<br/>                                                                               |
| <span id="MEDIATYPE_Interleaved"></span><span id="mediatype_interleaved"></span><span id="MEDIATYPE_INTERLEAVED"></span><dl> <dt>**\_Чередующийся MEDIATYPE**</dt> </dl>         | Звук и видео с чередованием. Используется для цифрового видео (DV).<br/>                                      |
| <span id="MEDIATYPE_LMRT"></span><span id="mediatype_lmrt"></span><dl> <dt>**MEDIATYPE \_ лмрт**</dt> </dl>                                                                      | Является устаревшей. Не используйте.<br/>                                                                          |
| <span id="MEDIATYPE_Midi"></span><span id="mediatype_midi"></span><span id="MEDIATYPE_MIDI"></span><dl> <dt>**MEDIATYPE \_ MIDI**</dt> </dl>                                     | Формат MIDI.<br/>                                                                                   |
| <span id="MEDIATYPE_MPEG2_PES"></span><span id="mediatype_mpeg2_pes"></span><dl> <dt>**MEDIATYPE \_ MPEG2 \_ PES**</dt> </dl>                                                      | Пакеты MPEG-2 PES. См. раздел [типы носителей MPEG-2](mpeg-2-media-types.md).<br/>                          |
| <span id="MEDIATYPE_MPEG2_SECTIONS"></span><span id="mediatype_mpeg2_sections"></span><dl> <dt>**\_Разделы MEDIATYPE MPEG2 \_**</dt> </dl>                                       | Данные раздела MPEG-2. См. раздел [типы носителей MPEG-2](mpeg-2-media-types.md).<br/>                         |
| <span id="MEDIATYPE_ScriptCommand"></span><span id="mediatype_scriptcommand"></span><span id="MEDIATYPE_SCRIPTCOMMAND"></span><dl> <dt>**MEDIATYPE \_ команду скрипта**</dt> </dl> | Данные — это команда сценария, используемая закрытыми заголовками.<br/>                                             |
| <span id="MEDIATYPE_Stream"></span><span id="mediatype_stream"></span><span id="MEDIATYPE_STREAM"></span><dl> <dt>**\_Поток MEDIATYPE**</dt> </dl>                             | Байтовый поток без отметок времени. См. раздел [**Stream подтипы**](stream-subtypes.md).<br/>               |
| <span id="MEDIATYPE_Text"></span><span id="mediatype_text"></span><span id="MEDIATYPE_TEXT"></span><dl> <dt>**MEDIATYPE, \_ текст**</dt> </dl>                                     | Текст.<br/>                                                                                          |
| <span id="MEDIATYPE_Timecode"></span><span id="mediatype_timecode"></span><span id="MEDIATYPE_TIMECODE"></span><dl> <dt>**Код \_ времени носителя**</dt> </dl>                     | Временные данные. Примечание. DirectShow не предоставляет фильтры, поддерживающие этот тип мультимедиа.<br/>     |
| <span id="MEDIATYPE_URL_STREAM"></span><span id="mediatype_url_stream"></span><dl> <dt>**\_поток URL-адресов MEDIATYPE \_**</dt> </dl>                                                   | Является устаревшей. Не используйте.<br/>                                                                          |
| <span id="MEDIATYPE_VBI"></span><span id="mediatype_vbi"></span><dl> <dt>**MEDIATYPE \_ ВБИ**</dt> </dl>                                                                         | Вертикальный интервал пустых значений (ВБИ) (для телевизора). То же, что и КСДАТАФОРМАТ \_ типа \_ ВБИ.<br/>       |
| <span id="MEDIATYPE_Video"></span><span id="mediatype_video"></span><span id="MEDIATYPE_VIDEO"></span><dl> <dt>**\_Видео MEDIATYPE**</dt> </dl>                                 | Видео. См. [подтипы видео](video-subtypes.md).<br/>                                               |



## <a name="remarks"></a>Комментарии

Идентификатор GUID подтипа дополнительно определяет формат. В некоторых форматах GUID подтипа может быть МЕДИАСУБТИПЕ \_ None, что означает, что формат не требует подтипа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Типы носителей](media-types.md)
</dt> </dl>

 

 




