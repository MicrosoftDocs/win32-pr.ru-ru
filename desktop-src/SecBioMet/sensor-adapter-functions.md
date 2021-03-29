---
title: Функции адаптера датчика
description: Адаптер датчика создает оболочку для биометрического устройства и предоставляет стандартный интерфейс, который позволяет биометрической службе Windows настраивать датчик, собирать образцы и управлять передачей биометрических данных механизму обработки.
ms.assetid: 32cf28d3-cb78-442d-81db-7827f55b0ba8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cefc5e9221a56a7766e6af6a47449db4405b369
ms.sourcegitcommit: 8a30948ba97ab969fcaa7f7ff05b853f59d8bd5c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/14/2020
ms.locfileid: "103789391"
---
# <a name="sensor-adapter-functions"></a>Функции адаптера датчика

Адаптер датчика создает оболочку для биометрического устройства и предоставляет стандартный интерфейс, который позволяет биометрической службе Windows настраивать датчик, собирать образцы и управлять передачей биометрических данных механизму обработки. Разработчик адаптера должен реализовать следующие функции. Они вызываются биометрической службой Windows.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                           | Описание                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**сенсорадаптеракцепткалибратиондата**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn)<br/>     | Передает данные калибровки из адаптера модуля в адаптер датчика.<br/>                                                                                            |
| [**сенсорадаптерактивате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn)<br/>                               | Предоставляет адаптеру датчика возможность выполнять любую работу, необходимую для перевода компонента датчика в состояние простоя.<br/>                                                |
| [**сенсорадаптераттач**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn)<br/>                                   | Добавляет адаптер датчика в конвейер обработки биометрического блока.<br/>                                                                                           |
| [**сенсорадаптерканцел**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn)<br/>                                   | Отменяет все ожидающие операции датчика.<br/>                                                                                                                            |
| [**сенсорадаптерклеарконтекст**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn)<br/>                       | Подготавливает конвейер обработки биометрического блока для новой операции.<br/>                                                                                       |
| [**сенсорадаптерконтролунит**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn)<br/>                         | Выполняет определяемую поставщиком операцию элемента управления, которая не требует повышенных привилегий.<br/>                                                                             |
| [**сенсорадаптерконтролунитпривилежед**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn)<br/>     | Выполняет определяемую поставщиком операцию элемента управления, для которой требуются повышенные привилегии.<br/>                                                                                     |
| [**сенсорадаптердеактивате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn)<br/>                           | Предоставляет адаптеру датчика возможность выполнять любую работу, необходимую для перевода компонента датчика в состояние простоя.<br/>                                                    |
| [**сенсорадаптердетач**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn)<br/>                                   | Освобождает ресурсы адаптера, подключенные к конвейеру.<br/>                                                                                                     |
| [**сенсорадаптерекспортсенсордата**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn)<br/>               | Извлекает недавно записанный образец биометрической метрики в виде стандартной структуры [**\_ Бир винбио**](winbio-bir.md) .<br/>                                        |
| [**сенсорадаптерфинишкаптуре**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn)<br/>                     | Вызывается биометрическая платформа Windows для ожидания завершения операции записи, инициированной функцией Сенсорадаптерстарткаптуре.<br/>                                                                                       |
| [**сенсорадаптержетиндикаторстатус**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)<br/>           | Получает значение, указывающее, включен ли индикатор датчика.<br/>                                                                                       |
| [*сенсорадаптернотифиповерчанже*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn)<br/>               | Получает уведомление об изменении состояния электропитания компьютера и соответствующим образом подготавливает адаптер датчика.<br/>                                                     |
| [**сенсорадаптерпипелинеклеануп**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn)<br/>                 | Предоставляет адаптеру датчика возможность выполнять любые очистки в, для которых требуется помощь из компонентов ядра или адаптера хранилища.<br/>                                   |
| [**сенсорадаптерпипелинеинит**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn)<br/>                       | Предоставляет адаптеру датчика возможность выполнить любую инициализацию, которая остается незавершенной и которой требуется помощь из компонентов ядра или адаптера хранилища.<br/> |
| [**сенсорадаптерпушдататоенгине**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn)<br/>               | Делает текущее содержимое образца буфера доступным для адаптера ядра.<br/>                                                                                  |
| [**сенсорадаптеркуерикалибратионформатс**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn)<br/> | Определяет набор форматов калибровки, поддерживаемых адаптером датчика.<br/>                                                                                        |
| [**сенсорадаптеркуерекстендединфо**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn)<br/>             | Определяет возможности и ограничения для компонента биометрического датчика.<br/>                                                                                    |
| [**сенсорадаптеркуеристатус**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)<br/>                         | Извлекает сведения о текущем состоянии устройства датчика.<br/>                                                                                              |
| [**сенсорадаптерресет**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn)<br/>                                     | Повторно инициализирует датчик.<br/>                                                                                                                                         |
| [**сенсорадаптерсеткалибратионформат**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn)<br/>       | Уведомляет адаптер датчика о том, что в адаптере подсистемы выбран определенный формат данных калибровки.<br/>                                                    |
| [**сенсорадаптерсетиндикаторстатус**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)<br/>           | Включает или выключает индикатор датчика.<br/>                                                                                                                           |
| [**сенсорадаптерсетмоде**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn)<br/>                                 | Задает режим адаптера датчика.<br/>                                                                                                                                     |
| [**сенсорадаптерстарткаптуре**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn)<br/>                       | Начинает асинхронную биометрическую запись.<br/>                                                                                                                         |
| [**вбиокуерисенсоринтерфаце**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)<br/>                         | Получает указатель на структуру [**\_ \_ интерфейса датчика винбио**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface) для адаптера датчика.<br/>                                         |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции подключаемых модулей](plug-in-functions.md)
</dt> </dl>

 

 





