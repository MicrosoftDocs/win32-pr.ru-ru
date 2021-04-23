---
description: При работе с данными производительности используются следующие структуры.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Структуры счетчиков производительности
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0629aa1763f08dfce9e2cc646bd1b5744d6591cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998509"
---
# <a name="performance-counters-structures"></a><span data-ttu-id="de516-103">Структуры счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="de516-103">Performance Counters Structures</span></span>

<span data-ttu-id="de516-104">При работе с данными производительности используются следующие структуры.</span><span class="sxs-lookup"><span data-stu-id="de516-104">You use the following structures when working with performance data.</span></span>

<span data-ttu-id="de516-105">Дополнительные сведения о функциях, доступных для работы со счетчиками производительности, см. в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="de516-105">For information about the functions that are available for working with performance counters, see [Performance Counters Functions](performance-counters-functions.md).</span></span>

## <a name="performance-data-helper-pdh-structures"></a><span data-ttu-id="de516-106">Вспомогательные структуры данных производительности (PDH)</span><span class="sxs-lookup"><span data-stu-id="de516-106">Performance Data Helper (PDH) structures</span></span>

<span data-ttu-id="de516-107">Потребители, использующие функции [модуля поддержки данных производительности (PDH)](using-the-pdh-functions-to-consume-counter-data.md) , используют следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="de516-107">Consumers that use the [Performance Data Helper (PDH)](using-the-pdh-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="de516-108">**\_Конфигурация PDH Browse \_ DLG \_**</span><span class="sxs-lookup"><span data-stu-id="de516-108">**PDH\_BROWSE\_DLG\_CONFIG**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [<span data-ttu-id="de516-109">**\_ \_ \_ Конфигурация H для обозревателя \_ PDH**</span><span class="sxs-lookup"><span data-stu-id="de516-109">**PDH\_BROWSE\_DLG\_CONFIG\_H**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [<span data-ttu-id="de516-110">**\_сведения о счетчике PDH \_**</span><span class="sxs-lookup"><span data-stu-id="de516-110">**PDH\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [<span data-ttu-id="de516-111">**\_ \_ элементы пути к СЧЕТЧИКу PDH \_**</span><span class="sxs-lookup"><span data-stu-id="de516-111">**PDH\_COUNTER\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [<span data-ttu-id="de516-112">**\_ \_ \_ элементы пути к ЭЛЕМЕНТу данных PDH \_**</span><span class="sxs-lookup"><span data-stu-id="de516-112">**PDH\_DATA\_ITEM\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [<span data-ttu-id="de516-113">**PDH \_ FMT \_ COUNTERVALUE**</span><span class="sxs-lookup"><span data-stu-id="de516-113">**PDH\_FMT\_COUNTERVALUE**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [<span data-ttu-id="de516-114">**\_ \_ элемент COUNTERVALUE PDH \_ FMT**</span><span class="sxs-lookup"><span data-stu-id="de516-114">**PDH\_FMT\_COUNTERVALUE\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [<span data-ttu-id="de516-115">**\_Счетчик PDH RAW \_**</span><span class="sxs-lookup"><span data-stu-id="de516-115">**PDH\_RAW\_COUNTER**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [<span data-ttu-id="de516-116">**\_необработанный \_ элемент СЧЕТЧИКа PDH \_**</span><span class="sxs-lookup"><span data-stu-id="de516-116">**PDH\_RAW\_COUNTER\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [<span data-ttu-id="de516-117">**\_необработанная \_ запись журнала PDH \_**</span><span class="sxs-lookup"><span data-stu-id="de516-117">**PDH\_RAW\_LOG\_RECORD**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [<span data-ttu-id="de516-118">**\_Статистика PDH**</span><span class="sxs-lookup"><span data-stu-id="de516-118">**PDH\_STATISTICS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [<span data-ttu-id="de516-119">**\_ \_ сведения о времени PDH**</span><span class="sxs-lookup"><span data-stu-id="de516-119">**PDH\_TIME\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a><span data-ttu-id="de516-120">Пользовательские структуры PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="de516-120">PerfLib V2 Consumer structures</span></span>

<span data-ttu-id="de516-121">Потребители, использующие функции-получатели [версии PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md) , используют следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="de516-121">Consumers that use the [PerfLib V2 Consumer](using-the-perflib-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="de516-122">**\_данные счетчика производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-122">**PERF\_COUNTER\_DATA**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [<span data-ttu-id="de516-123">**\_заголовок счетчика производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-123">**PERF\_COUNTER\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [<span data-ttu-id="de516-124">**\_Идентификатор счетчика производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-124">**PERF\_COUNTER\_IDENTIFIER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [<span data-ttu-id="de516-125">**\_ \_ сведения о reg СЧЕТЧИКа производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-125">**PERF\_COUNTER\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [<span data-ttu-id="de516-126">**\_ \_ сведения о наборе СЧЕТЧИКов производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-126">**PERF\_COUNTERSET\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [<span data-ttu-id="de516-127">**\_заголовок данных о производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-127">**PERF\_DATA\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [<span data-ttu-id="de516-128">**\_Заголовок экземпляра \_ PERF**</span><span class="sxs-lookup"><span data-stu-id="de516-128">**PERF\_INSTANCE\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [<span data-ttu-id="de516-129">**\_счетчики производительности с несколькими потоками \_**</span><span class="sxs-lookup"><span data-stu-id="de516-129">**PERF\_MULTI\_COUNTERS**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [<span data-ttu-id="de516-130">**\_несколько \_ экземпляров производительности**</span><span class="sxs-lookup"><span data-stu-id="de516-130">**PERF\_MULTI\_INSTANCES**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [<span data-ttu-id="de516-131">**\_ \_ заголовок буфера строк \_ производительности**</span><span class="sxs-lookup"><span data-stu-id="de516-131">**PERF\_STRING\_BUFFER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [<span data-ttu-id="de516-132">**\_ \_ заголовок счетчика строк производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-132">**PERF\_STRING\_COUNTER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a><span data-ttu-id="de516-133">Структуры поставщика PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="de516-133">PerfLib V2 Provider structures</span></span>

<span data-ttu-id="de516-134">[Поставщики данных производительности v2](providing-counter-data-using-version-2-0.md) используют следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="de516-134">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following structures:</span></span>

- [<span data-ttu-id="de516-135">**\_удостоверение счетчика производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-135">**PERF\_COUNTER\_IDENTITY**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="de516-136">**\_сведения о счетчике производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-136">**PERF\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="de516-137">**\_сведения о наборе счетчиков производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-137">**PERF\_COUNTERSET\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="de516-138">**\_экземпляр COUNTERSET производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-138">**PERF\_COUNTERSET\_INSTANCE**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [<span data-ttu-id="de516-139">**\_контекст поставщика \_ производительности**</span><span class="sxs-lookup"><span data-stu-id="de516-139">**PERF\_PROVIDER\_CONTEXT**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a><span data-ttu-id="de516-140">Структуры DLL производительности</span><span class="sxs-lookup"><span data-stu-id="de516-140">Performance DLL structures</span></span>

<span data-ttu-id="de516-141">[Поставщики DLL расширения производительности](providing-counter-data-using-a-performance-dll.md) и [потребители, использующие функции реестра для использования данных счетчиков](using-the-registry-functions-to-consume-counter-data.md) , используют следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="de516-141">[Performance extension DLL providers](providing-counter-data-using-a-performance-dll.md) and [consumers that use the registry functions to consume counter data](using-the-registry-functions-to-consume-counter-data.md) use the following structures:</span></span>

- [<span data-ttu-id="de516-142">**\_блок счетчика производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-142">**PERF\_COUNTER\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [<span data-ttu-id="de516-143">**\_Определение счетчика производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-143">**PERF\_COUNTER\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [<span data-ttu-id="de516-144">**\_блок данных о производительности \_**</span><span class="sxs-lookup"><span data-stu-id="de516-144">**PERF\_DATA\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [<span data-ttu-id="de516-145">**\_Определение экземпляра \_ производительности**</span><span class="sxs-lookup"><span data-stu-id="de516-145">**PERF\_INSTANCE\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [<span data-ttu-id="de516-146">**\_тип объекта \_ производительности**</span><span class="sxs-lookup"><span data-stu-id="de516-146">**PERF\_OBJECT\_TYPE**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
