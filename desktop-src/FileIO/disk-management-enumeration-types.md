---
description: Типы перечислений, используемые с управлением дисками.
ms.assetid: ed8fe5c1-dbdf-43bc-a0a7-17e541eba950
title: Типы перечислений управления дисками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e850e5161e4e8a6326d8014f67d6aad9373015e4354a01fa353087c6863a39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765914"
---
# <a name="disk-management-enumeration-types"></a>Типы перечислений управления дисками

В оснастке "Управление дисками" используются следующие типы перечислений.

## <a name="in-this-section"></a>Содержание раздела



| Перечисление                                                                              | Описание                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_тип носителя**](/windows/win32/api/winioctl/ne-winioctl-media_type)<br/>                                         | Представляет различные формы носителя устройства.<br/>                                                                                                                                                                                                                                                             |
| [**\_стиль раздела**](/windows/win32/api/winioctl/ne-winioctl-partition_style)<br/>                               | Представляет формат секции.<br/>                                                                                                                                                                                                                                                                     |
| [**\_Тип шины \_ хранилища**](/windows/win32/api/winioctl/ne-winioctl-storage_bus_type)<br/>                                | Предоставляет символьный способ представления типов шины хранилища.<br/>                                                                                                                                                                                                                                              |
| [**\_ \_ состояние работоспособности компонента хранилища \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_component_health_status)<br/> | Указывает состояние работоспособности компонента хранилища.<br/>                                                                                                                                                                                                                                                       |
| [**\_ \_ \_ конструктивный фактор устройства хранения**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_device_form_factor)<br/>           | Указывает форм-фактор устройства.<br/>                                                                                                                                                                                                                                                                    |
| [**\_ \_ \_ \_ единицы измерения мощности устройства хранения**](/windows/desktop/api/winioctl/ne-winioctl-storage_device_power_cap_units)<br/>  | Единицы максимального порога мощности.<br/>                                                                                                                                                                                                                                                                 |
| [**\_ \_ набор кодов портов \_ хранилища**](/windows/win32/api/winioctl/ne-winioctl-storage_port_code_set)<br/>                     | Зарезервировано для системного использования. <br/>                                                                                                                                                                                                                                                                                 |
| [**\_идентификатор свойства \_ хранилища**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)<br/>                          | Перечисляет возможные значения элемента **PropertyId** структуры [**\_ \_ запроса свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) , переданные в качестве входных данных в запрос [**\_ \_ \_ Свойства запроса на хранение ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) для получения свойств устройства или адаптера хранилища.<br/> |
| [**\_тип протокола \_ хранилища**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_type)<br/>                      | Указывает протокол устройства хранения.<br/>                                                                                                                                                                                                                                                               |
| [**\_тип запроса \_ хранилища**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_query_type)<br/>                            | Используется структурой [**\_ \_ запроса свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) , передаваемой в контрольный код [**\_ \_ \_ Свойства запроса на сохранение ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) , чтобы указать, какие сведения возвращаются для свойства устройства или адаптера хранилища.<br/>                             |
| [**\_изменение кэша \_ записи**](/windows/win32/api/winioctl/ne-winioctl-write_cache_change)<br/>                            | Указывает, могут ли быть изменены функции кэша записи устройства.<br/>                                                                                                                                                                                                                                    |
| [**\_включить кэш \_ записи**](/windows/win32/api/winioctl/ne-winioctl-write_cache_enable)<br/>                            | Указывает, включен ли кэш записи или отключен.<br/>                                                                                                                                                                                                                                                 |
| [**\_тип кэша \_ записи**](/windows/win32/api/winioctl/ne-winioctl-write_cache_type)<br/>                                | Указывает тип кэша.<br/>                                                                                                                                                                                                                                                                                 |
| [**ПИСАТЬ \_**](/windows/win32/api/winioctl/ne-winioctl-write_through)<br/>                                       | Указывает, поддерживает ли запоминающее устройство сквозное кэширование.<br/>                                                                                                                                                                                                                                        |



 

 

