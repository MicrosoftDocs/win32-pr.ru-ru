---
description: Используйте следующие функции для использования и предоставления данных о производительности.
ms.assetid: a2c97b8b-b1b1-4dd8-8f23-edffaa74d028
title: Функции счетчиков производительности
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8ef01ac07ae8507f1005839ab838e2528e76d6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663191"
---
# <a name="performance-counters-functions"></a><span data-ttu-id="cb7f3-103">Функции счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="cb7f3-103">Performance Counters Functions</span></span>

<span data-ttu-id="cb7f3-104">Используйте следующие функции для использования и предоставления данных о производительности.</span><span class="sxs-lookup"><span data-stu-id="cb7f3-104">Use the following functions to consume and provide performance data.</span></span>

## <a name="consumer-functions"></a><span data-ttu-id="cb7f3-105">Пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="cb7f3-105">Consumer functions</span></span>

### <a name="performance-data-helper-pdh-functions"></a><span data-ttu-id="cb7f3-106">Функции поддержки данных производительности (PDH)</span><span class="sxs-lookup"><span data-stu-id="cb7f3-106">Performance Data Helper (PDH) functions</span></span>

<span data-ttu-id="cb7f3-107">Используйте функции модуля поддержки данных производительности (PDH) для использования данных производительности от поставщиков данных производительности v1 и v2.</span><span class="sxs-lookup"><span data-stu-id="cb7f3-107">Use the Performance Data Helper (PDH) functions to consume performance data from both V1 and V2 performance data providers.</span></span>

> [!Note]
> <span data-ttu-id="cb7f3-108">Приложения OneCore Windows не могут использовать функции PDH.</span><span class="sxs-lookup"><span data-stu-id="cb7f3-108">Windows OneCore apps cannot use the PDH functions.</span></span> <span data-ttu-id="cb7f3-109">При написании приложений OneCore Windows используйте [функции потребителя версии PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="cb7f3-109">If you are writing Windows OneCore apps, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

- [<span data-ttu-id="cb7f3-110">*каунтерпаскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="cb7f3-110">*CounterPathCallBack*</span></span>](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [<span data-ttu-id="cb7f3-111">**пдхаддкаунтер**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-111">**PdhAddCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [<span data-ttu-id="cb7f3-112">**пдхадденглишкаунтер**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-112">**PdhAddEnglishCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [<span data-ttu-id="cb7f3-113">**пдхбиндинпутдатасаурце**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-113">**PdhBindInputDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [<span data-ttu-id="cb7f3-114">**пдхбровсекаунтерс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-114">**PdhBrowseCounters**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [<span data-ttu-id="cb7f3-115">**пдхбровсекаунтерш**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-115">**PdhBrowseCountersH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [<span data-ttu-id="cb7f3-116">**пдхкалкулатекаунтерфромраввалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-116">**PdhCalculateCounterFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [<span data-ttu-id="cb7f3-117">**пдхклоселог**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-117">**PdhCloseLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [<span data-ttu-id="cb7f3-118">**пдхклосекуери**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-118">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="cb7f3-119">**пдхколлекткуеридата**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-119">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="cb7f3-120">**пдхколлекткуеридатаекс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-120">**PdhCollectQueryDataEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [<span data-ttu-id="cb7f3-121">**пдхколлекткуеридатавистиме**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-121">**PdhCollectQueryDataWithTime**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [<span data-ttu-id="cb7f3-122">**пдхкомпутекаунтерстатистикс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-122">**PdhComputeCounterStatistics**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [<span data-ttu-id="cb7f3-123">**пдхконнектмачине**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-123">**PdhConnectMachine**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [<span data-ttu-id="cb7f3-124">**пдхенумлогсетнамес**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-124">**PdhEnumLogSetNames**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [<span data-ttu-id="cb7f3-125">**пдхенуммачинес**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-125">**PdhEnumMachines**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [<span data-ttu-id="cb7f3-126">**пдхенуммачинеш**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-126">**PdhEnumMachinesH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [<span data-ttu-id="cb7f3-127">**пдхенумобжектитемс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-127">**PdhEnumObjectItems**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [<span data-ttu-id="cb7f3-128">**пдхенумобжектитемш**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-128">**PdhEnumObjectItemsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [<span data-ttu-id="cb7f3-129">**пдхенумобжектс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-129">**PdhEnumObjects**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [<span data-ttu-id="cb7f3-130">**пдхенумобжектш**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-130">**PdhEnumObjectsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [<span data-ttu-id="cb7f3-131">**пдхекспандкаунтерпас**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-131">**PdhExpandCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [<span data-ttu-id="cb7f3-132">**пдхекспандвилдкардпас**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-132">**PdhExpandWildCardPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [<span data-ttu-id="cb7f3-133">**пдхекспандвилдкардпасх**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-133">**PdhExpandWildCardPathH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [<span data-ttu-id="cb7f3-134">**пдхформатфромраввалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-134">**PdhFormatFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [<span data-ttu-id="cb7f3-135">**пдхжеткаунтеринфо**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-135">**PdhGetCounterInfo**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [<span data-ttu-id="cb7f3-136">**пдхжеткаунтертимебасе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-136">**PdhGetCounterTimeBase**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [<span data-ttu-id="cb7f3-137">**пдхжетдатасаурцетимеранже**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-137">**PdhGetDataSourceTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [<span data-ttu-id="cb7f3-138">**пдхжетдатасаурцетимеранжех**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-138">**PdhGetDataSourceTimeRangeH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [<span data-ttu-id="cb7f3-139">**пдхжетдефаултперфкаунтер**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-139">**PdhGetDefaultPerfCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [<span data-ttu-id="cb7f3-140">**пдхжетдефаултперфкаунтерх**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-140">**PdhGetDefaultPerfCounterH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [<span data-ttu-id="cb7f3-141">**пдхжетдефаултперфобжект**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-141">**PdhGetDefaultPerfObject**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [<span data-ttu-id="cb7f3-142">**пдхжетдефаултперфобжекс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-142">**PdhGetDefaultPerfObjectH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [<span data-ttu-id="cb7f3-143">**пдхжетдллверсион**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-143">**PdhGetDllVersion**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [<span data-ttu-id="cb7f3-144">**пдхжетформаттедкаунтераррай**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-144">**PdhGetFormattedCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [<span data-ttu-id="cb7f3-145">**пдхжетформаттедкаунтервалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-145">**PdhGetFormattedCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [<span data-ttu-id="cb7f3-146">**пдхжетлогфилесизе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-146">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [<span data-ttu-id="cb7f3-147">**пдхжетравкаунтераррай**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-147">**PdhGetRawCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [<span data-ttu-id="cb7f3-148">**пдхжетравкаунтервалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-148">**PdhGetRawCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [<span data-ttu-id="cb7f3-149">**пдхисреалтимекуери**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-149">**PdhIsRealTimeQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [<span data-ttu-id="cb7f3-150">**пдхлукупперфиндексбинаме**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-150">**PdhLookupPerfIndexByName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [<span data-ttu-id="cb7f3-151">**пдхлукупперфнамебиндекс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-151">**PdhLookupPerfNameByIndex**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [<span data-ttu-id="cb7f3-152">**пдхмакекаунтерпас**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-152">**PdhMakeCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [<span data-ttu-id="cb7f3-153">**пдхопенлог**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-153">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [<span data-ttu-id="cb7f3-154">**пдхопенкуери**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-154">**PdhOpenQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [<span data-ttu-id="cb7f3-155">**пдхопенкуерих**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-155">**PdhOpenQueryH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [<span data-ttu-id="cb7f3-156">**пдхпарсекаунтерпас**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-156">**PdhParseCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [<span data-ttu-id="cb7f3-157">**пдхпарсеинстанценаме**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-157">**PdhParseInstanceName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [<span data-ttu-id="cb7f3-158">**пдхреадравлогрекорд**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-158">**PdhReadRawLogRecord**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [<span data-ttu-id="cb7f3-159">**пдхремовекаунтер**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-159">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="cb7f3-160">**пдхселектдатасаурце**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-160">**PdhSelectDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [<span data-ttu-id="cb7f3-161">**пдхсеткаунтерскалефактор**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-161">**PdhSetCounterScaleFactor**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [<span data-ttu-id="cb7f3-162">**пдхсетдефаултреалтимедатасаурце**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-162">**PdhSetDefaultRealTimeDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [<span data-ttu-id="cb7f3-163">**пдхсеткуеритимеранже**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-163">**PdhSetQueryTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [<span data-ttu-id="cb7f3-164">**пдхупдателог**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-164">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [<span data-ttu-id="cb7f3-165">**пдхупдателогфилекаталог**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-165">**PdhUpdateLogFileCatalog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [<span data-ttu-id="cb7f3-166">**пдхвалидатепас**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-166">**PdhValidatePath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [<span data-ttu-id="cb7f3-167">**пдхвалидатепасекс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-167">**PdhValidatePathEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a><span data-ttu-id="cb7f3-168">Функции-потребители версии PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="cb7f3-168">PerfLib V2 Consumer functions</span></span>

<span data-ttu-id="cb7f3-169">Используйте функции-потребители версии PerfLib v2 для получения данных о производительности из поставщиков данных производительности v2, если нельзя использовать функции вспомогательных данных производительности (PDH).</span><span class="sxs-lookup"><span data-stu-id="cb7f3-169">Use the PerfLib V2 Consumer functions to consume performance data from V2 performance data providers if you cannot use the Performance Data Helper (PDH) functions.</span></span> <span data-ttu-id="cb7f3-170">Эти функции могут использоваться при написании приложений OneCore для сборки каунтерсетс v2 или при необходимости составлять отдельные каунтерсетс v2 с минимальными зависимостями и издержками.</span><span class="sxs-lookup"><span data-stu-id="cb7f3-170">These functions might be used when writing OneCore applications to collect V2 countersets or when you need to collect specific V2 countersets with minimal dependencies and overhead.</span></span>

> [!TIP]
> <span data-ttu-id="cb7f3-171">Функции-потребители версии PerfLib v2 сложнее использовать, чем функции модуля поддержки данных производительности (PDH) и поддерживают сбор данных только от поставщиков v2.</span><span class="sxs-lookup"><span data-stu-id="cb7f3-171">The PerfLib V2 Consumer functions are harder to use than the Performance Data Helper (PDH) functions and only support collecting data from V2 providers.</span></span> <span data-ttu-id="cb7f3-172">Для большинства приложений предпочтительнее использовать функции PDH.</span><span class="sxs-lookup"><span data-stu-id="cb7f3-172">The PDH functions should be preferred for most applications.</span></span>

- [<span data-ttu-id="cb7f3-173">**перфаддкаунтерс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-173">**PerfAddCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [<span data-ttu-id="cb7f3-174">**перфклосекуерихандле**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-174">**PerfCloseQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [<span data-ttu-id="cb7f3-175">**перфделетекаунтерс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-175">**PerfDeleteCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [<span data-ttu-id="cb7f3-176">**перфенумератекаунтерсет**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-176">**PerfEnumerateCounterSet**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [<span data-ttu-id="cb7f3-177">**перфенумератекаунтерсетинстанцес**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-177">**PerfEnumerateCounterSetInstances**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [<span data-ttu-id="cb7f3-178">**перфопенкуерихандле**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-178">**PerfOpenQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [<span data-ttu-id="cb7f3-179">**перфкуерикаунтердата**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-179">**PerfQueryCounterData**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [<span data-ttu-id="cb7f3-180">**перфкуерикаунтеринфо**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-180">**PerfQueryCounterInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [<span data-ttu-id="cb7f3-181">**перфкуерикаунтерсетрегистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-181">**PerfQueryCounterSetRegistrationInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a><span data-ttu-id="cb7f3-182">Функции поставщика</span><span class="sxs-lookup"><span data-stu-id="cb7f3-182">Provider functions</span></span>

### <a name="perflib-v2-provider-functions"></a><span data-ttu-id="cb7f3-183">Функции поставщика PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="cb7f3-183">PerfLib V2 Provider functions</span></span>

<span data-ttu-id="cb7f3-184">[Поставщики данных производительности v2](providing-counter-data-using-version-2-0.md) используют следующие функции:</span><span class="sxs-lookup"><span data-stu-id="cb7f3-184">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following functions:</span></span>

- [<span data-ttu-id="cb7f3-185">*аллокатемемори*</span><span class="sxs-lookup"><span data-stu-id="cb7f3-185">*AllocateMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [<span data-ttu-id="cb7f3-186">*контролкаллбакк*</span><span class="sxs-lookup"><span data-stu-id="cb7f3-186">*ControlCallback*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="cb7f3-187">**каунтерклеануп**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-187">**CounterCleanup**</span></span>](countercleanup.md)
- [<span data-ttu-id="cb7f3-188">**каунтеринитиализе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-188">**CounterInitialize**</span></span>](counterinitialize.md)
- [<span data-ttu-id="cb7f3-189">*FreeMemory*</span><span class="sxs-lookup"><span data-stu-id="cb7f3-189">*FreeMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [<span data-ttu-id="cb7f3-190">**перфкреатеинстанце**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-190">**PerfCreateInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="cb7f3-191">**перфдекрементулонгкаунтервалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-191">**PerfDecrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [<span data-ttu-id="cb7f3-192">**перфдекрементулонглонгкаунтервалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-192">**PerfDecrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [<span data-ttu-id="cb7f3-193">**перфделетеинстанце**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-193">**PerfDeleteInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="cb7f3-194">**перфинкрементулонгкаунтервалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-194">**PerfIncrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [<span data-ttu-id="cb7f3-195">**перфинкрементулонглонгкаунтервалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-195">**PerfIncrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [<span data-ttu-id="cb7f3-196">**перфкуеринстанце**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-196">**PerfQueryInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="cb7f3-197">**перфсеткаунтерсетинфо**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-197">**PerfSetCounterSetInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="cb7f3-198">**перфсетулонгкаунтервалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-198">**PerfSetULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="cb7f3-199">**перфсетулонглонгкаунтервалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-199">**PerfSetULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="cb7f3-200">**перфсеткаунтеррефвалуе**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-200">**PerfSetCounterRefValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="cb7f3-201">**перфстартпровидер**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-201">**PerfStartProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="cb7f3-202">**перфстартпровидерекс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-202">**PerfStartProviderEx**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [<span data-ttu-id="cb7f3-203">**перфстоппровидер**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-203">**PerfStopProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> <span data-ttu-id="cb7f3-204">Чтобы установить и удалить поставщики v2, используйте средства **lodctr** и **lodctr** .</span><span class="sxs-lookup"><span data-stu-id="cb7f3-204">To install and uninstall V2 providers, use the **lodctr** and **unlodctr** tools.</span></span> <span data-ttu-id="cb7f3-205">Функции **лоадперфкаунтертекстстрингс** и **унлоадперфкаунтертекстстрингс** нельзя использовать для установки и удаления поставщиков версии 2.</span><span class="sxs-lookup"><span data-stu-id="cb7f3-205">The **LoadPerfCounterTextStrings** and **UnloadPerfCounterTextStrings** functions cannot be used to install and uninstall V2 providers.</span></span>

### <a name="performance-dll-functions"></a><span data-ttu-id="cb7f3-206">Функции DLL производительности</span><span class="sxs-lookup"><span data-stu-id="cb7f3-206">Performance DLL functions</span></span>

<span data-ttu-id="cb7f3-207">[V1. поставщики данных производительности](providing-counter-data-using-a-performance-dll.md) РЕАЛИЗУЮТ библиотеку DLL, которая предоставляет следующие функции:</span><span class="sxs-lookup"><span data-stu-id="cb7f3-207">[V1 performance data providers](providing-counter-data-using-a-performance-dll.md) implement a DLL that provides the following functions:</span></span>

- [<span data-ttu-id="cb7f3-208">*ClosePerformanceData*</span><span class="sxs-lookup"><span data-stu-id="cb7f3-208">*ClosePerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [<span data-ttu-id="cb7f3-209">*CollectPerformanceData*</span><span class="sxs-lookup"><span data-stu-id="cb7f3-209">*CollectPerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- <span data-ttu-id="cb7f3-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb7f3-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span></span>

> [!Note]
> <span data-ttu-id="cb7f3-211">Из-за серьезных проблем с производительностью и надежностью поставщики данных производительности v1 являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="cb7f3-211">Due to significant performance and reliability issues, V1 performance data providers are deprecated.</span></span> <span data-ttu-id="cb7f3-212">Хотя вы по-прежнему можете использовать библиотеку DLL расширения производительности для предоставления данных счетчиков, вместо этого рекомендуется [создать поставщик v2](providing-counter-data-using-version-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="cb7f3-212">Although you still can use a performance extension DLL to provide counter data, you are encouraged to [create a V2 provider](providing-counter-data-using-version-2-0.md) instead.</span></span> <span data-ttu-id="cb7f3-213">Кроме того, рекомендуется заменить существующие поставщики v1 поставщиками v2.</span><span class="sxs-lookup"><span data-stu-id="cb7f3-213">You also are encouraged to replace existing V1 providers with V2 providers.</span></span>

<span data-ttu-id="cb7f3-214">Поставщики v1 можно устанавливать и удалять с помощью средств **lodctr** и **lodctr** или путем вызова следующих функций:</span><span class="sxs-lookup"><span data-stu-id="cb7f3-214">V1 providers can be installed and uninstalled using the **lodctr** and **unlodctr** tools or by calling the following functions:</span></span>

- [<span data-ttu-id="cb7f3-215">**лоадперфкаунтертекстстрингс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-215">**LoadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [<span data-ttu-id="cb7f3-216">**унлоадперфкаунтертекстстрингс**</span><span class="sxs-lookup"><span data-stu-id="cb7f3-216">**UnloadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)
