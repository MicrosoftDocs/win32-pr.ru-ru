---
description: Следующие глобальные уникальные идентификаторы (GUID) определяют типы узлов для фильтров режима ядра. Чтобы найти тип узла, запросите фильтр для интерфейса Икстопологинфо.
ms.assetid: 0e133ce3-8815-47d1-a5c3-577a98963912
title: Типы узлов KS (Ксмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSNODETYPE_DEV_SPECIFIC
- KSNODETYPE_VIDEO_CAMERA_TERMINAL
- KSNODETYPE_VIDEO_INPUT_MTT
- KSNODETYPE_VIDEO_INPUT_TERMINAL
- KSNODETYPE_VIDEO_OUTPUT_MTT
- KSNODETYPE_VIDEO_OUTPUT_TERMINAL
- KSNODETYPE_VIDEO_PROCESSING
- KSNODETYPE_VIDEO_SELECTOR
- KSNODETYPE_VIDEO_STREAMING
api_type:
- HeaderDef
api_location:
- Ksmedia.h
ms.openlocfilehash: eadae4fdd70fd80115ea4e8902ba1bb2aa7bf53b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685296"
---
# <a name="ks-node-types"></a>Типы узлов KS

Следующие глобальные уникальные идентификаторы (GUID) определяют типы узлов для фильтров режима ядра. Чтобы найти тип узла, запросите фильтр для интерфейса [**икстопологинфо**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) .



| Идентификатор GUID                                                                                                                                                                                                                     | Описание                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KSNODETYPE_DEV_SPECIFIC"></span><span id="ksnodetype_dev_specific"></span><dl> <dt>**КСНОДЕТИПЕ для \_ разработчиков \_**</dt> </dl>                             | Представляет одну или несколько функций обработки для конкретных устройств. Узел имеет одно входное соединение и одно выходное соединение.<br/> Узел может предоставлять пользовательский COM-интерфейс через подключаемый модуль Кспрокси, если он предоставляется производителем устройства.<br/>                                            |
| <span id="KSNODETYPE_VIDEO_CAMERA_TERMINAL"></span><span id="ksnodetype_video_camera_terminal"></span><dl> <dt>**\_ \_ терминал ВИДЕОкамеры \_ кснодетипе**</dt> </dl> | Представляет данные, перемещенные на устройство с датчика камеры, независимо от шины USB. Узел имеет одно выходное соединение.<br/> Узел предоставляет интерфейсы [**иамкамераконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) и [**икамераконтрол**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-icameracontrol) для управления камерой.<br/> |
| <span id="KSNODETYPE_VIDEO_INPUT_MTT"></span><span id="ksnodetype_video_input_mtt"></span><dl> <dt>**\_ \_ входное видео кснодетипе \_ МТТ**</dt> </dl>                   | Представляет данные, перемещенные на устройство из последовательного транспорта носителя, например Втр ленту, независимо от шины USB. Узел имеет одно выходное соединение.<br/> Узел предоставляет интерфейс [**иамексттранспорт**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) для управления транспортным механизмом.<br/>   |
| <span id="KSNODETYPE_VIDEO_INPUT_TERMINAL"></span><span id="ksnodetype_video_input_terminal"></span><dl> <dt>**\_ \_ терминал входного видео кснодетипе \_**</dt> </dl>    | Представляет данные, перемещаемые на устройство независимо от шины USB. Например, этот узел может представлять собой аналоговый звуковой разъем или разъем S/PDIF. Узел имеет одно выходное соединение.<br/>                                                                                                             |
| <span id="KSNODETYPE_VIDEO_OUTPUT_MTT"></span><span id="ksnodetype_video_output_mtt"></span><dl> <dt>**\_ \_ выходной МТТ кснодетипе \_ видео**</dt> </dl>                | Представляет данные, перемещающиеся с устройства в последовательный транспорт мультимедиа, например на ленту Втр, независимо от шины USB. Узел имеет одно входное соединение.<br/> Узел предоставляет интерфейс [**иамексттранспорт**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) для управления транспортным механизмом.<br/>      |
| <span id="KSNODETYPE_VIDEO_OUTPUT_TERMINAL"></span><span id="ksnodetype_video_output_terminal"></span><dl> <dt>**\_ \_ терминал вывода видео \_ кснодетипе**</dt> </dl> | Представляет данные, перемещающиеся с устройства независимо от шины USB. Например, этот узел может представлять собой аналоговый звуковой разъем или разъем S/PDIF. Узел имеет одно входное соединение.<br/>                                                                                                              |
| <span id="KSNODETYPE_VIDEO_PROCESSING"></span><span id="ksnodetype_video_processing"></span><dl> <dt>**\_Обработка видео \_ кснодетипе**</dt> </dl>                 | Представляет одну или несколько функций обработки видео. Узел имеет одно входное соединение и одно выходное соединение.<br/> Узел предоставляет интерфейсы [**иамвидеопрокамп**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) и [**ивидеопрокамп**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ivideoprocamp) для настройки качества видеосигнала.<br/> |
| <span id="KSNODETYPE_VIDEO_SELECTOR"></span><span id="ksnodetype_video_selector"></span><dl> <dt>**средство \_ выбора видео кснодетипе \_**</dt> </dl>                       | Представляет механизм для выбора входного пути из двух или более возможных источников. Узел имеет два или более входных соединения и одно выходное соединение.<br/> Узел [**предоставляет интерфейс для**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) выбора между входными данными.<br/>                               |
| <span id="KSNODETYPE_VIDEO_STREAMING"></span><span id="ksnodetype_video_streaming"></span><dl> <dt>**\_ \_ потоковая передача видео кснодетипе**</dt> </dl>                    | Представляет перемещение данных между узлом и устройством. Для устройств УВК этот узел представляет конечную точку USB. Входные конечные точки имеют одно входное соединение; выходные конечные точки имеют одно выходное соединение.<br/>                                                                                         |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ксмедиа. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы и идентификаторы GUID](constants-and-guids.md)
</dt> </dl>

 

 




