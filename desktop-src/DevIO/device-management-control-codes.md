---
description: С устройствами сменщика используются следующие управляющие коды.
ms.assetid: b3a3ffa1-e710-4d96-aff8-5b6876ab032b
title: Управляющие коды управления устройствами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bd6aa147407618c6df82686f175cb92690ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072502"
---
# <a name="device-management-control-codes"></a>Управляющие коды управления устройствами

С устройствами сменщика используются следующие управляющие коды.



| Значение                                                                                          | Значение                                                                                                                                              |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_носитель для преобразователя подзапроса ioctl \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_exchange_medium)                      | Перемещает элемент мультимедиа из исходного элемента в одно место назначения и фрагмент мультимедиа, который изначально находится в первом месте назначения, во второе место назначения. |
| [**\_ \_ \_ состояние элемента получения преобразователя \_ ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_element_status)               | Получает состояние всех элементов или указанное число элементов определенного типа.                                                         |
| [**\_ \_ Получение параметров СМЕНЩИКа ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_parameters)                        | Извлекает параметры указанного устройства.                                                                                                    |
| [**\_СМЕНЩИК ioctl \_ Получение \_ данных о продуктах \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_product_data)                   | Извлекает данные о продукте для указанного устройства.                                                                                                 |
| [**\_ \_ состояние получения преобразователя \_ ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_status)                                | Извлекает текущее состояние указанного устройства.                                                                                                |
| [**\_преобразователь \_ ioctl \_ инициализировать \_ состояние элемента**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_initialize_element_status) | Инициализирует состояние всех элементов или указанных элементов определенного типа.                                                               |
| [**\_Перемещение сменщика ioctl — \_ \_ средний**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_move_medium)                              | Перемещает элемент мультимедиа в место назначения.                                                                                                             |
| [**\_ \_ \_ теги томов запросов сменщика ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_query_volume_tags)                 | Извлекает сведения о теге тома для указанных элементов.                                                                                     |
| [**\_ \_ транспорт повторной инициализации СМЕНЩИКа ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_reinitialize_transport)        | Физически перекалибрует транспортный элемент.                                                                                                         |
| [**преобразователь IOCTL \_ \_ задать \_ доступ**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_access)                                | Задает состояние порта вставки и извлечения устройства, дверцы или клавиатуры.                                                                                   |
| [**\_ \_ Задание расположения для СМЕНЩИКа ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_position)                            | Задает для механизма автоматической транспортировки сменщика указанный адрес элемента.                                                                     |



 

В управлении устройствами используются следующие управляющие коды.



| Контрольный код                                                                                      | Операция                                                                                                    |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Проверка службы \_ хранилища ioctl \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_check_verify)                               | Проверяет наличие изменений на съемном носителе.                                                               |
| [**\_ \_ Извлечение мультимедиа из хранилища ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_eject_media)                                 | Извлекает носитель с устройства SCSI.                                                                             |
| [**\_ \_ управление извлечением данных из службы "ioctl" \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_ejection_control)                       | Включает или отключает механизм, который извлекает носитель.                                                         |
| [**\_ \_ Получение \_ номера устройства в хранилище ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_device_number)                    | Извлекает тип устройства, номер устройства и, для секционированного устройства — номер раздела устройства. |
| [**запрос \_ на \_ Получение \_ \_ сведений о хотплуг в хранилище ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_hotplug_info)                      | Извлекает конфигурацию хотплуг указанного устройства.                                                 |
| [**IOCTL \_ хранилище \_ Получение \_ \_ серийного \_ номера носителя**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)       | Извлекает серийный номер USB-устройства.                                                                 |
| [**\_ \_ Получение \_ типов мультимедиа для \_ типа данных ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types)                        | Извлекает сведения об геометрии устройства.                                                            |
| [**для \_ хранилища ioctl \_ Get \_ Media \_ types \_ ex**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types_ex)                 | Извлекает сведения о типах носителей, поддерживаемых устройством.                                        |
| [**запрос \_ на \_ загрузку носителя для хранилища ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_load_media)                                   | Загружает носитель в устройство.                                                                                   |
| [**\_ \_ Управление \_ \_ атрибутами НАБОРОВ данных \_ в хранилище ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_manage_data_set_attributes) |                                                                                                              |
| [**\_ \_ элемент управления МКН хранилища ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_mcn_control)                                 | Включает или отключает уведомление об изменении носителя.                                                               |
| [**\_ \_ Удаление носителя хранилища \_ ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_media_removal)                             | Включает или отключает механизм извлечения мультимедиа.                                                               |
| [**\_Чтение данных \_ о \_ емкости хранилища ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)                             | Извлекает сведения об геометрии для устройства.                                                           |
| [**\_ \_ \_ сведения о хотплуг для набора хранения ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_set_hotplug_info)                      | Задает конфигурацию хотплуг указанного устройства.                                                      |



 

 

 



