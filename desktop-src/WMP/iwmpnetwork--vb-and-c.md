---
title: Интерфейс Ивмпнетворк (VB и C) (WMP. h)
description: Предоставляет свойства и методы для доступа к статистике, связанной с качеством сетевого подключения, а также для указания и получения параметров прокси-сервера сети. Интерфейс Ивмпнетворк предоставляет следующие свойства.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- проигрыватель Windows Media интерфейса ивмпнетворк (VB и C)
- проигрыватель Windows Media интерфейса ивмпнетворк (VB и C), описание
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93110b25bd7d194c4f1d7c213228512fd8bc6000df15b726e3f32a6e6e79a62a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572454"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a>Интерфейс Ивмпнетворк (VB и C#)

Предоставляет свойства и методы для доступа к статистике, связанной с качеством сетевого подключения, а также для указания и получения параметров прокси-сервера сети.

Интерфейс **ивмпнетворк** предоставляет следующие свойства.

## <a name="members"></a>Элементы

Интерфейс **ивмпнетворк (VB и C#)** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **ивмпнетворк (VB и C#)** содержит следующие методы.



| Метод                                                                                           | Описание                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**жетпроксибипассфорлокал**](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | Возвращает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.<br/> |
| [**жетпроксексцептионлист**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | Возвращает список исключений прокси-сервера.<br/>                                                                           |
| [**жетпроксинаме**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | Возвращает имя используемого прокси-сервера.<br/>                                                            |
| [**жетпроксипорт**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | Возвращает используемый порт прокси-сервера.<br/>                                                                          |
| [**жетпроксисеттингс**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | Возвращает сведения о параметрах прокси-сервера для протокола.<br/>                                                |
| [**сетпроксибипассфорлокал**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | Указывает, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.<br/>                  |
| [**сетпроксексцептионлист**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | Указывает список исключений прокси-сервера.<br/>                                                                         |
| [**сетпроксинаме**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | Указывает имя используемого прокси-сервера.<br/>                                                              |
| [**сетпроксипорт**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | Указывает используемый порт прокси-сервера.<br/>                                                                            |
| [**setProxySettings**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | Задает параметры прокси-сервера для протокола.<br/>                                                                |



 

### <a name="properties"></a>Свойства

Интерфейс **ивмпнетворк (VB и C#)** имеет следующие свойства.



| Свойство                                                                                          | Тип доступа           | Описание                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [**Связи**](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | Только для чтения<br/>  | Возвращает текущую пропускную способность элемента мультимедиа.<br/>                                     |
| [**Скорость**](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | Только для чтения<br/>  | Возвращает скорость получения текущей скорости.<br/>                                         |
| [**буфферингкаунт**](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | Только для чтения<br/>  | Возвращает количество попыток буферизации во время воспроизведения.<br/>                      |
| [**буфферингпрогресс**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | Только для чтения<br/>  | Возвращает процент завершенной буферизации.<br/>                                       |
| [**буфферингтиме**](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | Чтение/запись<br/> | Возвращает или задает количество времени буферизации в миллисекундах перед началом воспроизведения.<br/> |
| [**довнлоадпрогресс**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | Только для чтения<br/>  | Возвращает процент завершенной загрузки.<br/>                                     |
| [**енкодедфрамерате**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | Только для чтения<br/>  | Возвращает частоту кадров видео, указанную автором содержимого.<br/>                        |
| [**Частота**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | Только для чтения<br/>  | Возвращает текущую частоту кадров видео.<br/>                                                |
| [**фрамесскиппед**](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | Только для чтения<br/>  | Возвращает общее число кадров, пропущенных во время воспроизведения.<br/>                          |
| [**лостпаккетс**](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | Только для чтения<br/>  | Возвращает число потерянных пакетов.<br/>                                                  |
| [**maxBandwidth**](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | Чтение/запись<br/> | Возвращает или задает максимально допустимую пропускную способность.<br/>                                       |
| [**максбитрате**](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | Только для чтения<br/>  | Возвращает максимальную возможную скорость видео.<br/>                                         |
| [**рецеиведпаккетс**](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | Только для чтения<br/>  | Возвращает число полученных пакетов.<br/>                                              |
| [**рецептионкуалити**](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | Только для чтения<br/>  | Возвращает процент пакетов, которые не были потеряны за последние 30 секунд.<br/>                   |
| [**рековередпаккетс**](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | Только для чтения<br/>  | Возвращает число восстановленных пакетов.<br/>                                             |
| [**саурцепротокол**](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | Только для чтения<br/>  | Возвращает исходный протокол, используемый для получения данных.<br/>                                    |



 

Получите интерфейс **ивмпнетворк** с помощью следующего свойства.



| Объект                                                                   | Свойство                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Объект Аксвиндовсмедиаплайер](axwindowsmediaplayer-object--vb-and-c.md) | [**сети**](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**интерфейсы для Visual Basic .net и C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





