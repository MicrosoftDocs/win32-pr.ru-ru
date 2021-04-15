---
description: Для трассировки событий в DirectShow используются следующие идентификаторы GUID.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: Идентификаторы GUID трассировки (Перфструкт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669103"
---
# <a name="trace-guids"></a>Идентификаторы GUID трассировки

Для трассировки событий в DirectShow используются следующие идентификаторы GUID.



| Идентификатор GUID                                                                                                                                                                   | Описание                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**GUID \_ аудиобреак**</dt> </dl>    | Событие разрыва звука. События этого типа используют структуру [**перфинфо \_ DSHOW \_ аудиобреак**](perfinfo-dshow-audiobreak.md) для данных событий.<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**CTL с GUID \_ DSHOW \_**</dt> </dl>      | Поставщик событий DirectShow.<br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <dt>**GUID \_ стреамтраце**</dt> </dl> | Общее событие потоковой передачи. События этого типа используют структуру [**перфинфо \_ DSHOW \_ стреамтраце**](perfinfo-dshow-streamtrace.md) для данных событий.<br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <dt>**GUID \_ видеоренд**</dt> </dl>       | Событие отрисовки видео. События этого типа используют структуру [**перфинфо \_ DSHOW \_ авренд**](perfinfo-dshow-avrend.md) для данных событий.<br/>             |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Перфструкт. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Трассировка событий в DirectShow](event-tracing-in-directshow.md)
</dt> </dl>

 

 




