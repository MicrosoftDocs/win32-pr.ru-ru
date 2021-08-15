---
description: Следующие идентификаторы GUID используются для трассировки событий в DirectShow.
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
ms.openlocfilehash: 89465996c57e1f1f97f2c101c8dfee99a00219f992a4e68681f76465d21bef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951553"
---
# <a name="trace-guids"></a>Идентификаторы GUID трассировки

Следующие идентификаторы GUID используются для трассировки событий в DirectShow.



| Идентификатор GUID                                                                                                                                                                   | Описание                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**GUID \_ аудиобреак**</dt> </dl>    | Событие разрыва звука. События этого типа используют структуру [**перфинфо \_ DSHOW \_ аудиобреак**](perfinfo-dshow-audiobreak.md) для данных событий.<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**CTL с GUID \_ DSHOW \_**</dt> </dl>      | поставщик событий DirectShow.<br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <dt>**GUID \_ стреамтраце**</dt> </dl> | Общее событие потоковой передачи. События этого типа используют структуру [**перфинфо \_ DSHOW \_ стреамтраце**](perfinfo-dshow-streamtrace.md) для данных событий.<br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <dt>**GUID \_ видеоренд**</dt> </dl>       | Событие отрисовки видео. События этого типа используют структуру [**перфинфо \_ DSHOW \_ авренд**](perfinfo-dshow-avrend.md) для данных событий.<br/>             |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Перфструкт. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Трассировка событий в DirectShow](event-tracing-in-directshow.md)
</dt> </dl>

 

 




