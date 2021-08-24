---
description: При работе с данными производительности используются следующие структуры.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Структуры счетчиков производительности
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 00e9a505a9fe74592f571f3db108af2247a6d44889bc3ddbc2e4dae0844600b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674754"
---
# <a name="performance-counters-structures"></a>Структуры счетчиков производительности

При работе с данными производительности используются следующие структуры.

Дополнительные сведения о функциях, доступных для работы со счетчиками производительности, см. в разделе [функции счетчиков производительности](performance-counters-functions.md).

## <a name="performance-data-helper-pdh-structures"></a>Вспомогательные структуры данных производительности (PDH)

Потребители, использующие функции [модуля поддержки данных производительности (PDH)](using-the-pdh-functions-to-consume-counter-data.md) , используют следующие структуры:

- [**\_Конфигурация PDH Browse \_ DLG \_**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [**\_ \_ \_ Конфигурация H для обозревателя \_ PDH**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [**\_сведения о счетчике PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [**\_ \_ элементы пути к СЧЕТЧИКу PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [**\_ \_ \_ элементы пути к ЭЛЕМЕНТу данных PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [**PDH \_ FMT \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [**\_ \_ элемент COUNTERVALUE PDH \_ FMT**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [**\_Счетчик PDH RAW \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [**\_необработанный \_ элемент СЧЕТЧИКа PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [**\_необработанная \_ запись журнала PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [**\_Статистика PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [**\_ \_ сведения о времени PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a>Пользовательские структуры PerfLib v2

Потребители, использующие функции-получатели [версии PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md) , используют следующие структуры:

- [**\_данные счетчика производительности \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [**\_заголовок счетчика производительности \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [**\_Идентификатор счетчика производительности \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [**\_ \_ сведения о reg СЧЕТЧИКа производительности \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [**\_ \_ сведения о наборе СЧЕТЧИКов производительности \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [**\_заголовок данных о производительности \_**](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [**\_Заголовок экземпляра \_ PERF**](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [**\_счетчики производительности с несколькими потоками \_**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [**\_несколько \_ экземпляров производительности**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [**\_ \_ заголовок буфера строк \_ производительности**](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [**\_ \_ заголовок счетчика строк производительности \_**](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a>Структуры поставщика PerfLib v2

[Поставщики данных производительности v2](providing-counter-data-using-version-2-0.md) используют следующие структуры:

- [**\_удостоверение счетчика производительности \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [**\_сведения о счетчике производительности \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [**\_сведения о наборе счетчиков производительности \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [**\_экземпляр COUNTERSET производительности \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [**\_контекст поставщика \_ производительности**](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a>Структуры DLL производительности

[Поставщики DLL расширения производительности](providing-counter-data-using-a-performance-dll.md) и [потребители, использующие функции реестра для использования данных счетчиков](using-the-registry-functions-to-consume-counter-data.md) , используют следующие структуры:

- [**\_блок счетчика производительности \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [**\_Определение счетчика производительности \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [**\_блок данных о производительности \_**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [**\_Определение экземпляра \_ производительности**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [**\_тип объекта \_ производительности**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
