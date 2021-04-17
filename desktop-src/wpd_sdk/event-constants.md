---
description: Портативные устройства Windows определяют следующие значения событий.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Константы событий (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EVENT_DEVICE_CAPABILITIES_UPDATED
- WPD_EVENT_DEVICE_REMOVED
- WPD_EVENT_DEVICE_RESET
- WPD_EVENT_OBJECT_ADDED
- WPD_EVENT_OBJECT_REMOVED
- WPD_EVENT_OBJECT_TRANSFER_REQUESTED
- WPD_EVENT_OBJECT_UPDATED
- WPD_EVENT_SERVICE_METHOD_COMPLETE
- WPD_EVENT_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e60c44cda2585655a86ca1cdb4653ad002a0225d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695092"
---
# <a name="event-constants-portabledeviceh"></a>Константы событий (Портабледевице. h)

Портативные устройства Windows определяют следующие значения событий.



| Константа                                                                                                                                                                                                                                 | Описание                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**\_ \_ \_ обновленные возможности устройства для событий WPD \_**</dt> </dl> | Это событие указывает, что возможности устройства изменились. Клиенты должны переделать запрос к устройству, если они внесли какие либо решения на основе возможностей устройства.<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**\_устройство событий \_ WPD \_ удалено**</dt> </dl>                                         | Это событие отправляется при выгрузке драйвера для устройства. Как правило, это результат отключения устройства.<br/> Клиенты должны освободить интерфейс **ипортабледевице** и все интерфейсы [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) , указанные в **\_ \_ параметре события \_ WPD \_ \_ идентификатор устройства PnP**.<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**\_Сброс устройства с событием WPD \_ \_**</dt> </dl>                                               | Это событие указывает, что устройство будет сброшено, и все подключенные клиенты должны закрыть свои подключения к устройству.<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**\_ \_ добавлен объект события \_ WPD**</dt> </dl>                                               | Это событие указывает на то, что на устройстве доступен новый объект.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**\_объект событий \_ WPD \_ удален**</dt> </dl>                                         | Это событие отправляется после удаления ранее существующего объекта с устройства.<br/> Объект может быть объектом содержимого, например, удален файл изображения; или это может быть функциональный объект, например, новое устройство хранения было отключено от устройства.<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**\_ \_ \_ запрошено перемещение объектов событий WPD \_**</dt> </dl>       | Это событие отправляется, чтобы запросить приложение для передачи определенного объекта с устройства.<br/> Объект обычно является объектом содержимого, например файлом изображения.<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**\_ \_ обновлен объект события \_ WPD**</dt> </dl>                                         | Это событие отправляется после обновления объекта, и любой подключенный клиент должен обновить его представление этого объекта.<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**\_ \_ метод службы событий \_ WPD \_ завершен**</dt> </dl>             | Это событие отправляется, когда драйвер завершил вызов метода службы. Это событие должно быть отправлено даже при сбое метода. Это внутреннее событие DDI для WPD, которое не будет доступно для приложений с помощью [**ипортабледевице:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) или [**Ипортабледевицесервице:: Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**\_ \_ Формат хранения событий \_ WPD**</dt> </dl>                                         | Это событие показывает ход выполнения операции форматирования в объекте хранилища.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы](constants.md)
</dt> </dl>

 

 




