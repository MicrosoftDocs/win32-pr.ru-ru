---
title: Оболочки адаптера датчика
description: Функции, которые можно использовать для вызова функций в адаптере датчика. Эти функции определены в Винбио \_ Adapter. h.
ms.assetid: 302a831c-38f7-4d32-8d9f-5ff58931224b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8887da38a7142c830f19a83b5950abea15791b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132986"
---
# <a name="sensor-adapter-wrappers"></a>Оболочки адаптера датчика

В Винбио Adapter. h определены следующие функции-оболочки \_ . Их можно использовать для вызова функций в адаптере датчика.



| Функция                                     | Описание                                                                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| вбиосенсоракцепткалибратиондата<br/>   | Вызывает функцию [**сенсорадаптеракцепткалибратиондата**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>     |
| вбиосенсорактивате<br/>                | Вызывает функцию [**сенсорадаптерактивате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                               |
| вбиосенсораттач<br/>                  | Вызывает функцию [**сенсорадаптераттач**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn) .<br/>                                                                                                         |
| вбиосенсорканцел<br/>                  | Вызывает функцию [**сенсорадаптерканцел**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn) .<br/>                                                                                                         |
| вбиосенсорклеарконтекст<br/>            | Вызывает функцию [**сенсорадаптерклеарконтекст**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn) .<br/>                                                                                             |
| вбиосенсорконтролунит<br/>             | Вызывает функцию [**сенсорадаптерконтролунит**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn) .<br/>                                                                                               |
| вбиосенсорконтролунитпривилежед<br/>   | Вызывает функцию [**сенсорадаптерконтролунитпривилежед**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn) .<br/>                                                                           |
| вбиосенсордеактивате<br/>              | Вызывает функцию [**сенсорадаптердеактивате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                           |
| вбиосенсордетач<br/>                  | Вызывает функцию [**сенсорадаптердетач**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn) .<br/>                                                                                                         |
| вбиосенсорекспортсенсордата<br/>        | Вызывает функцию [**сенсорадаптерекспортсенсордата**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn) .<br/>                                                                                     |
| вбиосенсорфинишкаптуре<br/>           | Вызывает функцию [**сенсорадаптерфинишкаптуре**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn) .<br/>                                                                                           |
| вбиосенсорнотифиповерчанже<br/>       | Вызывает функцию [**сенсорадаптернотифиповерчанже**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 8.<br/>              |
| вбиосенсорпипелинеклеануп<br/>         | Вызывает функцию [**сенсорадаптерпипелинеклеануп**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                 |
| вбиосенсорпипелинеинит<br/>            | Вызывает функцию [**сенсорадаптерпипелинеинит**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                       |
| вбиосенсорпушдататоенгине<br/>        | Вызывает функцию [**сенсорадаптерпушдататоенгине**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn) .<br/>                                                                                     |
| вбиосенсоркуерикалибратионформатс<br/> | Вызывает функцию [**сенсорадаптеркуерикалибратионформатс**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/> |
| вбиосенсоркуерекстендединфо<br/>       | Вызывает функцию [**сенсорадаптеркуерекстендединфо**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>             |
| вбиосенсоркуеристатус<br/>             | Вызывает функцию [**сенсорадаптеркуеристатус**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn) .<br/>                                                                                               |
| вбиосенсорресет<br/>                   | Вызывает функцию [**сенсорадаптерресет**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn) .<br/>                                                                                                           |
| вбиосенсорсеткалибратионформат<br/>    | Вызывает функцию [**сенсорадаптерсеткалибратионформат**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>       |
| вбиосенсорсетмоде<br/>                 | Вызывает функцию [**сенсорадаптерсетмоде**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) .<br/>                                                                                                       |
| вбиосенсорстарткаптуре<br/>            | Вызывает функцию [**сенсорадаптерстарткаптуре**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn) .<br/>                                                                                             |



 

Нет функций-оболочек для функций [**сенсорадаптержетиндикаторстатус**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn) и [**сенсорадаптерсетиндикаторстатус**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции адаптера датчика](sensor-adapter-functions.md)
</dt> <dt>

[Функции подключаемых модулей](plug-in-functions.md)
</dt> </dl>

 

 





