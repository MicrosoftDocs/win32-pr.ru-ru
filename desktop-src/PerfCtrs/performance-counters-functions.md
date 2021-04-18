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
# <a name="performance-counters-functions"></a>Функции счетчиков производительности

Используйте следующие функции для использования и предоставления данных о производительности.

## <a name="consumer-functions"></a>Пользовательские функции

### <a name="performance-data-helper-pdh-functions"></a>Функции поддержки данных производительности (PDH)

Используйте функции модуля поддержки данных производительности (PDH) для использования данных производительности от поставщиков данных производительности v1 и v2.

> [!Note]
> Приложения OneCore Windows не могут использовать функции PDH. При написании приложений OneCore Windows используйте [функции потребителя версии PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md).

- [*каунтерпаскаллбакк*](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [**пдхаддкаунтер**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [**пдхадденглишкаунтер**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [**пдхбиндинпутдатасаурце**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [**пдхбровсекаунтерс**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [**пдхбровсекаунтерш**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [**пдхкалкулатекаунтерфромраввалуе**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [**пдхклоселог**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [**пдхклосекуери**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**пдхколлекткуеридата**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**пдхколлекткуеридатаекс**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [**пдхколлекткуеридатавистиме**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [**пдхкомпутекаунтерстатистикс**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [**пдхконнектмачине**](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [**пдхенумлогсетнамес**](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [**пдхенуммачинес**](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [**пдхенуммачинеш**](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [**пдхенумобжектитемс**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [**пдхенумобжектитемш**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [**пдхенумобжектс**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [**пдхенумобжектш**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [**пдхекспандкаунтерпас**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [**пдхекспандвилдкардпас**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [**пдхекспандвилдкардпасх**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [**пдхформатфромраввалуе**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [**пдхжеткаунтеринфо**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [**пдхжеткаунтертимебасе**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [**пдхжетдатасаурцетимеранже**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [**пдхжетдатасаурцетимеранжех**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [**пдхжетдефаултперфкаунтер**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [**пдхжетдефаултперфкаунтерх**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [**пдхжетдефаултперфобжект**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [**пдхжетдефаултперфобжекс**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [**пдхжетдллверсион**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [**пдхжетформаттедкаунтераррай**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [**пдхжетформаттедкаунтервалуе**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [**пдхжетлогфилесизе**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [**пдхжетравкаунтераррай**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [**пдхжетравкаунтервалуе**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [**пдхисреалтимекуери**](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [**пдхлукупперфиндексбинаме**](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [**пдхлукупперфнамебиндекс**](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [**пдхмакекаунтерпас**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [**пдхопенлог**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [**пдхопенкуери**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [**пдхопенкуерих**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [**пдхпарсекаунтерпас**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [**пдхпарсеинстанценаме**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [**пдхреадравлогрекорд**](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [**пдхремовекаунтер**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**пдхселектдатасаурце**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [**пдхсеткаунтерскалефактор**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [**пдхсетдефаултреалтимедатасаурце**](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [**пдхсеткуеритимеранже**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [**пдхупдателог**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [**пдхупдателогфилекаталог**](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [**пдхвалидатепас**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [**пдхвалидатепасекс**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a>Функции-потребители версии PerfLib v2

Используйте функции-потребители версии PerfLib v2 для получения данных о производительности из поставщиков данных производительности v2, если нельзя использовать функции вспомогательных данных производительности (PDH). Эти функции могут использоваться при написании приложений OneCore для сборки каунтерсетс v2 или при необходимости составлять отдельные каунтерсетс v2 с минимальными зависимостями и издержками.

> [!TIP]
> Функции-потребители версии PerfLib v2 сложнее использовать, чем функции модуля поддержки данных производительности (PDH) и поддерживают сбор данных только от поставщиков v2. Для большинства приложений предпочтительнее использовать функции PDH.

- [**перфаддкаунтерс**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [**перфклосекуерихандле**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [**перфделетекаунтерс**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [**перфенумератекаунтерсет**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [**перфенумератекаунтерсетинстанцес**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [**перфопенкуерихандле**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [**перфкуерикаунтердата**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [**перфкуерикаунтеринфо**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [**перфкуерикаунтерсетрегистратионинфо**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a>Функции поставщика

### <a name="perflib-v2-provider-functions"></a>Функции поставщика PerfLib v2

[Поставщики данных производительности v2](providing-counter-data-using-version-2-0.md) используют следующие функции:

- [*аллокатемемори*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [*контролкаллбакк*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [**каунтерклеануп**](countercleanup.md)
- [**каунтеринитиализе**](counterinitialize.md)
- [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [**перфкреатеинстанце**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [**перфдекрементулонгкаунтервалуе**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [**перфдекрементулонглонгкаунтервалуе**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [**перфделетеинстанце**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [**перфинкрементулонгкаунтервалуе**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [**перфинкрементулонглонгкаунтервалуе**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [**перфкуеринстанце**](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [**перфсеткаунтерсетинфо**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [**перфсетулонгкаунтервалуе**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [**перфсетулонглонгкаунтервалуе**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [**перфсеткаунтеррефвалуе**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [**перфстартпровидер**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [**перфстартпровидерекс**](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [**перфстоппровидер**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> Чтобы установить и удалить поставщики v2, используйте средства **lodctr** и **lodctr** . Функции **лоадперфкаунтертекстстрингс** и **унлоадперфкаунтертекстстрингс** нельзя использовать для установки и удаления поставщиков версии 2.

### <a name="performance-dll-functions"></a>Функции DLL производительности

[V1. поставщики данных производительности](providing-counter-data-using-a-performance-dll.md) РЕАЛИЗУЮТ библиотеку DLL, которая предоставляет следующие функции:

- [*ClosePerformanceData*](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [*CollectPerformanceData*](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- [*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))

> [!Note]
> Из-за серьезных проблем с производительностью и надежностью поставщики данных производительности v1 являются устаревшими. Хотя вы по-прежнему можете использовать библиотеку DLL расширения производительности для предоставления данных счетчиков, вместо этого рекомендуется [создать поставщик v2](providing-counter-data-using-version-2-0.md) . Кроме того, рекомендуется заменить существующие поставщики v1 поставщиками v2.

Поставщики v1 можно устанавливать и удалять с помощью средств **lodctr** и **lodctr** или путем вызова следующих функций:

- [**лоадперфкаунтертекстстрингс**](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [**унлоадперфкаунтертекстстрингс**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)
