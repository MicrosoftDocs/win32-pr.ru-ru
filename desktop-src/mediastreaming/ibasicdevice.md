---
title: Интерфейс Ибасикдевице
description: Инкапсулирует методы и события, необходимые для моделирования устройства DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- API потоковой передачи мультимедиа интерфейса Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, описание
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25a60a3f722faac473b6f779de2d609cbdfc4ecb257d671136a8ef80535fdf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060364"
---
# <a name="ibasicdevice-interface"></a>Интерфейс Ибасикдевице

Инкапсулирует методы и события, необходимые для моделирования устройства DLNA.

## <a name="members"></a>Элементы

Интерфейс **ибасикдевице** наследует от [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable). **Ибасикдевице** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ибасикдевице** содержит следующие методы.



| Метод                                                                                 | Описание                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**добавить \_ коннектионстатусчанжед**](ibasicdevice-add-connectionstatuschanged.md)       | Регистрирует обработчик событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .<br/>                |
| [**канвакедевицес**](ibasicdevice-canwakedevices.md)                                  | Возвращает значение, указывающее, может ли устройство пробудиться.<br/>                                                            |
| [**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))                              | Возвращает значение перечисления, указывающее, находится ли устройство в данный момент в режиме «вне линии», в состоянии «в наличии», а также через режим пробуждения.<br/> |
| [**Описание**](ibasicdevice-description.md)                                        | Извлекает описание устройства.<br/>                                                                              |
| [**дисковередонкуррентнетворк**](ibasicdevice-discoveredoncurrentnetwork.md)          | Возвращает значение, указывающее, находится ли устройство в текущей сети.<br/>                                           |
| [**FriendlyName**](ibasicdevice-friendlyname.md)                                      | Получает понятное имя устройства s.<br/>                                                                               |
| [**Значки**](ibasicdevice-icons.md)                                                    | Возвращает вектор интерфейсов [**идевицеикон**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .<br/>                                                  |
| [**IpAddresses**](ibasicdevice-ipaddresses.md)                                        | Возвращает вектор IP-адресов.<br/>                                                                                   |
| [**ManufacturerName**](ibasicdevice-manufacturername.md)                              | Получает имя изготовителя устройства.<br/>                                                                           |
| [**мануфактурерурл**](ibasicdevice-manufacturerurl.md)                                | Получает URL-адрес изготовителя устройства.<br/>                                                                            |
| [**ModelName**](ibasicdevice-modelname.md)                                            | Извлекает имя модели устройства s.<br/>                                                                                  |
| [**ModelNumber**](ibasicdevice-modelnumber.md)                                        | Извлекает номер модели устройства s.<br/>                                                                                |
| [**моделурл**](ibasicdevice-modelurl.md)                                              | Извлекает URL-адрес модели устройства s.<br/>                                                                                   |
| [**фисикаладдрессес**](ibasicdevice-physicaladdresses.md)                            | Возвращает вектор физических адресов.<br/>                                                                             |
| [**пресентатионурл**](ibasicdevice-presentationurl.md)                                | Извлекает URL-адрес презентации устройства с.<br/>                                                                            |
| [**ремотестреамингурлс**](ibasicdevice-remotestreamingurls.md)                        | Возвращает вектор URL-адресов удаленной потоковой передачи.<br/>                                                                          |
| [**удалить \_ коннектионстатусчанжед**](ibasicdevice-remove-connectionstatuschanged.md) | Отменяет регистрацию обработчика событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .<br/>              |
| [**Номер**](ibasicdevice-serialnumber.md)                                      | Извлекает серийный номер устройства s.<br/>                                                                               |
| [**Тип**](ibasicdevice-type.md)                                                      | Возвращает значение перечисления, указывающее тип устройства DLNA.<br/>                                       |
| [**уникуедевиценаме**](ibasicdevice-uniquedevicename.md)                              | Извлекает уникальное имя устройства (УДН) устройства.<br/>                                                                    |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

