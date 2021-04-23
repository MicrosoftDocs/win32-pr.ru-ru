---
title: Перечисление МПНОТИФИ (Мпклиент. h)
description: Возможные уведомления обратного вызова.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- Перечисление МПНОТИФИ. устаревшие функции среды Windows
- Устаревшие компоненты среды Windows в указателе перечисления ПМПНОТИФИ
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afa0eeb6cb1d610f28cc82f578617f7bd71cf886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701059"
---
# <a name="mpnotify-enumeration"></a><span data-ttu-id="e8df4-105">Перечисление МПНОТИФИ</span><span class="sxs-lookup"><span data-stu-id="e8df4-105">MPNOTIFY enumeration</span></span>

<span data-ttu-id="e8df4-106">Возможные уведомления обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e8df4-106">Possible callback notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8df4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8df4-107">Syntax</span></span>


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a><span data-ttu-id="e8df4-108">Константы</span><span class="sxs-lookup"><span data-stu-id="e8df4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e8df4-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**МПНОТИФИ \_ None**</span><span class="sxs-lookup"><span data-stu-id="e8df4-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY\_NONE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e8df4-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**\_Начало вызова \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY\_CALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-111">Начало вызова уведомления.</span><span class="sxs-lookup"><span data-stu-id="e8df4-111">Notification call start.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**\_вызов мпнотифи \_ завершен**</span><span class="sxs-lookup"><span data-stu-id="e8df4-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY\_CALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-113">Вызов уведомления завершен.</span><span class="sxs-lookup"><span data-stu-id="e8df4-113">Notification call completed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**\_внутренний \_ сбой мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**MPNOTIFY\_INTERNAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-115">Общий внутренний сбой.</span><span class="sxs-lookup"><span data-stu-id="e8df4-115">Generic internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**\_ \_ Запуск службы состояния \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY\_STATUS\_SERVICE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-117">Служба защиты от вредоносных программ запущена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-117">Malware protection service has started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**\_Служба состояния \_ мпнотифи \_ запущена**</span><span class="sxs-lookup"><span data-stu-id="e8df4-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY\_STATUS\_SERVICE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-119">Служба защиты от вредоносных программ запущена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-119">Malware protection service is running.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**\_ \_ Завершение службы состояния \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY\_STATUS\_SERVICE\_STOP**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-121">Служба защиты от вредоносных программ остановлена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-121">Malware protection service has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_компонент состояния \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**MPNOTIFY\_STATUS\_COMPONENT**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-123">Состояние конкретного компонента: включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="e8df4-123">Particular component enable/disable status.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**\_изменение состояния \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**MPNOTIFY\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-125">Изменено общее состояние продукта.</span><span class="sxs-lookup"><span data-stu-id="e8df4-125">Overall product status has changed.</span></span> <span data-ttu-id="e8df4-126">Вызовите [**мпманажерстатускуерекс**](mpmanagerstatusqueryex.md) , чтобы получить текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="e8df4-126">Call [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) to obtain the current status.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**\_ \_ Конфигурация компонента состояния \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**MPNOTIFY\_STATUS\_COMPONENT\_CONFIGURATION**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-128">Конфигурация определенного компонента изменилась.</span><span class="sxs-lookup"><span data-stu-id="e8df4-128">A particular component has changed configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**\_ \_ изменение срока действия состояния \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MPNOTIFY\_STATUS\_EXPIRATION\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-130">Состояние срока действия продукта изменилось.</span><span class="sxs-lookup"><span data-stu-id="e8df4-130">Product expiration status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**\_ \_ Изменение автономной \_ проверки \_ состояния мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**MPNOTIFY\_STATUS\_OFFLINE\_SCAN\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-132">Состояние "требуется Автономная проверка" изменилось.</span><span class="sxs-lookup"><span data-stu-id="e8df4-132">Offline scan required state changed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**\_Начало СКАНИРОВАНИЯ \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY\_SCAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-134">Сканирование начато.</span><span class="sxs-lookup"><span data-stu-id="e8df4-134">Scan started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**МПНОТИФИ \_ сканирование \_ приостановлено**</span><span class="sxs-lookup"><span data-stu-id="e8df4-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**MPNOTIFY\_SCAN\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-136">Сканирование приостановлено.</span><span class="sxs-lookup"><span data-stu-id="e8df4-136">Scan paused.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**\_сканирование мпнотифи \_ возобновлено**</span><span class="sxs-lookup"><span data-stu-id="e8df4-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**MPNOTIFY\_SCAN\_RESUMED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-138">Сканирование возобновлено.</span><span class="sxs-lookup"><span data-stu-id="e8df4-138">scan resumed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**\_Отмена СКАНИРОВАНИЯ \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY\_SCAN\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-140">Сканирование отменено.</span><span class="sxs-lookup"><span data-stu-id="e8df4-140">Scan cancelled.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**\_сканирование мпнотифи \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="e8df4-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY\_SCAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-142">Сканирование завершено.</span><span class="sxs-lookup"><span data-stu-id="e8df4-142">Scan completed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**\_ \_ ход выполнения сканирования мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**MPNOTIFY\_SCAN\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-144">Уведомление о ходе выполнения для конкретного проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8df4-144">Progress notification for the specific resource being scanned.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_Ошибка СКАНИРОВАНИЯ \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**MPNOTIFY\_SCAN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-146">Не удалось проверить конкретный ресурс.</span><span class="sxs-lookup"><span data-stu-id="e8df4-146">Failure to scan a particular resource.</span></span> <span data-ttu-id="e8df4-147">Сканирование по-прежнему будет продолжаться.</span><span class="sxs-lookup"><span data-stu-id="e8df4-147">Scan will still continue.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**МПНОТИФИ \_ сканирование с \_ заражением**</span><span class="sxs-lookup"><span data-stu-id="e8df4-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**MPNOTIFY\_SCAN\_INFECTED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-149">Проверка обнаружила зараженный ресурс.</span><span class="sxs-lookup"><span data-stu-id="e8df4-149">Scan found an infected resource.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**МПНОТИФИ \_ Scan \_ мемористарт**</span><span class="sxs-lookup"><span data-stu-id="e8df4-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY\_SCAN\_MEMORYSTART**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-151">Ход проверки для уведомления части сканирования памяти, запущенной при проверке системы.</span><span class="sxs-lookup"><span data-stu-id="e8df4-151">Scan progress to notify memory scan portion of the system scan has started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**МПНОТИФИ \_ Scan \_ меморикомплете**</span><span class="sxs-lookup"><span data-stu-id="e8df4-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-153">Ход сканирования для уведомления части сканирования памяти, выполненной в ходе проверки системы.</span><span class="sxs-lookup"><span data-stu-id="e8df4-153">Scan progress to notify memory scan portion of the system scan has completed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**\_ \_ \_ Начало сборки SFC мпнотифи \_ Scan**</span><span class="sxs-lookup"><span data-stu-id="e8df4-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-155">Ход выполнения проверки для уведомления о запуске сборки SFC.</span><span class="sxs-lookup"><span data-stu-id="e8df4-155">Scan progress to notify sfc build portion has started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**\_ \_ Сборка SFC мпнотифи \_ Scan \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="e8df4-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-157">Ход выполнения проверки для уведомления о завершении сборки SFC.</span><span class="sxs-lookup"><span data-stu-id="e8df4-157">Scan progress to notify sfc build portion has completed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**\_Запуск мпнотифи Scan \_ фастпас \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY\_SCAN\_FASTPATH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-159">Начато сканирование фастпас SpyNet.</span><span class="sxs-lookup"><span data-stu-id="e8df4-159">Scan fastpath spynet has begun.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**МПНОТИФИ \_ сканирование \_ фастпас \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="e8df4-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY\_SCAN\_FASTPATH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-161">Проверка фастпас SpyNet завершена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-161">Scan fastpath spynet has ended.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**\_ \_ ход выполнения мпнотифи сканирования фастпас \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY\_SCAN\_FASTPATH\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-163">Уведомление о ходе повторного сканирования фастпас, которое используется внутренне и преобразуется в **\_ \_ ход выполнения сканирования мпнотифи** для внешних.</span><span class="sxs-lookup"><span data-stu-id="e8df4-163">Progress notification for fastpath rescans, used internally and converted to **MPNOTIFY\_SCAN\_PROGRESS** for external.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**\_Начало очистки \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY\_CLEAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-165">Очистка запущена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-165">Cleaning started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**\_Очистка мпнотифи \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="e8df4-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY\_CLEAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-167">Очистка завершена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-167">Cleaning completed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**\_Начало очистки \_ ресторепоинт \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-169">Запущено создание точки восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="e8df4-169">Started to create a system restore point.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**МПНОТИФИ \_ Clean \_ ресторепоинт \_ выполнен**</span><span class="sxs-lookup"><span data-stu-id="e8df4-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-171">Точка восстановления системы успешно создана.</span><span class="sxs-lookup"><span data-stu-id="e8df4-171">System restore point successfully created.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**\_сбой мпнотифи Clean \_ ресторепоинт \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-173">Не удалось создать точку восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="e8df4-173">System restore point creation failed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**\_Запуск мпнотифи очистки \_ угрозы \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY\_CLEAN\_THREAT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-175">Для определенной угрозы запускается очистка.</span><span class="sxs-lookup"><span data-stu-id="e8df4-175">Cleaning is started for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**МПНОТИФИ \_ чистая \_ угроза \_ успешной**</span><span class="sxs-lookup"><span data-stu-id="e8df4-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-177">Очистка для определенной угрозы прошла.</span><span class="sxs-lookup"><span data-stu-id="e8df4-177">Cleaning is succeeded for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**\_сбой чистой \_ угрозы \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**MPNOTIFY\_CLEAN\_THREAT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-179">Произошел сбой при очистке определенной угрозы.</span><span class="sxs-lookup"><span data-stu-id="e8df4-179">Cleaning has failed for a particular threat.</span></span> <span data-ttu-id="e8df4-180">**Ошибка при \_ Код ошибки пакета управления " \_ \_ не \_ найден** " указывает на то, что угроза не найдена (и не была неудачной).</span><span class="sxs-lookup"><span data-stu-id="e8df4-180">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**Очистка МПНОТИФИного \_ \_ ресурса \_ прошла**</span><span class="sxs-lookup"><span data-stu-id="e8df4-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-182">Очистка для определенного ресурса прошла.</span><span class="sxs-lookup"><span data-stu-id="e8df4-182">Cleaning is succeeded for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**\_сбой очистки \_ ресурса \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-184">Произошел сбой при очистке определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8df4-184">Cleaning has failed for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**МПНОТИФИ \_ Чистка \_ угрозы \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="e8df4-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY\_CLEAN\_THREAT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-186">Очистка для определенной угрозы завершена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-186">Cleaning has completed for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**\_Начало ПРЕДПРОВЕРКИ \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY\_PRECHECK\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-188">Запущена чистая предпроверка.</span><span class="sxs-lookup"><span data-stu-id="e8df4-188">Clean precheck started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**\_ПРЕДПРОВЕРКА мпнотифи \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="e8df4-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY\_PRECHECK\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-190">Чистая проверка завершена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-190">Clean precheck completed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**\_ресурс ПРЕДПРОВЕРКИ \_ мпнотифи \_ заблокирован**</span><span class="sxs-lookup"><span data-stu-id="e8df4-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-192">Очистка предпроверки обнаружила заблокированный ресурс.</span><span class="sxs-lookup"><span data-stu-id="e8df4-192">Clean precheck detected blocked resource.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**\_ \_ обнаружена угроза мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**MPNOTIFY\_THREAT\_DETECTED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-194">В системе обнаружена новая угроза.</span><span class="sxs-lookup"><span data-stu-id="e8df4-194">New threat detected in system.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**\_ \_ изменена угроза мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY\_THREAT\_MODIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-196">Сведения об угрозе изменены.</span><span class="sxs-lookup"><span data-stu-id="e8df4-196">Threat information modified.</span></span> <span data-ttu-id="e8df4-197">Например, добавлен новый ресурс.</span><span class="sxs-lookup"><span data-stu-id="e8df4-197">For example, a new resource was added.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**\_Очистка угрозы \_ мпнотифи \_ прошла**</span><span class="sxs-lookup"><span data-stu-id="e8df4-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-199">Действие очистки для угрозы установлено.</span><span class="sxs-lookup"><span data-stu-id="e8df4-199">Cleaning action succeeded for a threat.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**\_ \_ сбой очистки угрозы \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**MPNOTIFY\_THREAT\_CLEAN\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-201">Сбой действия очистки для угрозы.</span><span class="sxs-lookup"><span data-stu-id="e8df4-201">Cleaning action failed for a threat.</span></span> <span data-ttu-id="e8df4-202">**Ошибка при \_ Код ошибки пакета управления " \_ \_ не \_ найден** " указывает на то, что угроза не найдена (и не была неудачной).</span><span class="sxs-lookup"><span data-stu-id="e8df4-202">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**\_ \_ прекращение угрозы мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY\_THREAT\_ABANDONED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-204">Не выполнено исправление до остановки службы.</span><span class="sxs-lookup"><span data-stu-id="e8df4-204">No remediation occurred before the service was stopped.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**\_ \_ \_ Начало события очистки мпнотифи \_ THREAT**</span><span class="sxs-lookup"><span data-stu-id="e8df4-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-206">Начато действие очистки.</span><span class="sxs-lookup"><span data-stu-id="e8df4-206">A cleaning action has been started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**\_ \_ событие очистки угрозы \_ мпнотифи \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="e8df4-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-208">Действие очистки завершено.</span><span class="sxs-lookup"><span data-stu-id="e8df4-208">A cleaning action has ended.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**\_Начало СИГУПДАТЕ \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY\_SIGUPDATE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-210">Обновление сигнатуры запущено.</span><span class="sxs-lookup"><span data-stu-id="e8df4-210">Signature update started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**\_ \_ Начало поиска мпнотифи \_ сигупдате**</span><span class="sxs-lookup"><span data-stu-id="e8df4-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-212">Поиск обновлений начат.</span><span class="sxs-lookup"><span data-stu-id="e8df4-212">Search for updates started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**\_Поиск мпнотифи \_ сигупдате \_ завершен**</span><span class="sxs-lookup"><span data-stu-id="e8df4-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-214">Поиск обновлений завершен.</span><span class="sxs-lookup"><span data-stu-id="e8df4-214">Search for updates completed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**\_ \_ Доступно обновление программного обеспечения мпнотифи сигупдате \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY\_SIGUPDATE\_SOFTWARE\_UPDATE\_AVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-216">Доступно обновление программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e8df4-216">Software update available.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**\_ \_ Начало загрузки сигупдате \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-218">Загрузка начата.</span><span class="sxs-lookup"><span data-stu-id="e8df4-218">Download started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**\_ \_ ход загрузки сигупдате \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-220">Идет скачивание.</span><span class="sxs-lookup"><span data-stu-id="e8df4-220">Download in progress.</span></span> <span data-ttu-id="e8df4-221">Данные обратного вызова содержат сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="e8df4-221">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**\_скачивание СИГУПДАТЕ \_ мпнотифи \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="e8df4-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-223">Скачивание завершено.</span><span class="sxs-lookup"><span data-stu-id="e8df4-223">Download completed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**\_ \_ Запуск установки мпнотифи \_ сигупдате**</span><span class="sxs-lookup"><span data-stu-id="e8df4-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-225">Установка запущена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-225">Installation started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**\_ \_ Ход установки мпнотифи \_ сигупдате**</span><span class="sxs-lookup"><span data-stu-id="e8df4-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-227">Выполняется установка.</span><span class="sxs-lookup"><span data-stu-id="e8df4-227">Installation in progress.</span></span> <span data-ttu-id="e8df4-228">Данные обратного вызова содержат сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="e8df4-228">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**\_Установка СИГУПДАТЕ \_ мпнотифи \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="e8df4-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-230">Установка завершена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-230">Installation complete.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**\_ \_ требуется перезагрузка сигупдате мпнотифи \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-232">Для обновления требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="e8df4-232">Update requires reboot.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**\_запрос СИГУПДАТЕ \_ мпнотифи \_ обработан**</span><span class="sxs-lookup"><span data-stu-id="e8df4-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-234">Служба обработала запрос на обновление сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="e8df4-234">Service processed a signature update request.</span></span> <span data-ttu-id="e8df4-235">В данных обратного вызова параметру HRESULT присвоено **значение** "сбой" или "успешно".</span><span class="sxs-lookup"><span data-stu-id="e8df4-235">Failure or success is indicated by **hResult** in the callback data.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**МПНОТИФИ \_ сигупдате \_ завершен**</span><span class="sxs-lookup"><span data-stu-id="e8df4-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-237">Обновление завершено.</span><span class="sxs-lookup"><span data-stu-id="e8df4-237">Update complete.</span></span> <span data-ttu-id="e8df4-238">**С \_ FALSE** — состояние означает, что обновления не были нужны.</span><span class="sxs-lookup"><span data-stu-id="e8df4-238">**S\_FALSE** status indicates that no updates were needed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**\_Начало образца \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY\_SAMPLE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-240">Начало отправки образца.</span><span class="sxs-lookup"><span data-stu-id="e8df4-240">Sample submission started.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**\_Пример мпнотифи \_ завершен**</span><span class="sxs-lookup"><span data-stu-id="e8df4-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**MPNOTIFY\_SAMPLE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-242">Отправка образца завершена.</span><span class="sxs-lookup"><span data-stu-id="e8df4-242">Sample submission completed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**\_Начало образца \_ элемента \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**MPNOTIFY\_SAMPLE\_ITEM\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-244">Начато отправку указанного примера элемента.</span><span class="sxs-lookup"><span data-stu-id="e8df4-244">Specific sample item submission started.</span></span> <span data-ttu-id="e8df4-245">Индекс образца элемента доступен в [**\_ данных мпсампле**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="e8df4-245">Sample item index is available in [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**\_образец \_ элемента мпнотифи \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**MPNOTIFY\_SAMPLE\_ITEM\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-247">Отправка указанного примера элемента прошла.</span><span class="sxs-lookup"><span data-stu-id="e8df4-247">Specific sample item submission succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**\_сбой образца \_ элемента \_ мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="e8df4-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**MPNOTIFY\_SAMPLE\_ITEM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-249">Не удалось отправить конкретный образец элемента.</span><span class="sxs-lookup"><span data-stu-id="e8df4-249">Specific sample item submission failed.</span></span> <span data-ttu-id="e8df4-250">Код ошибки доступен в [**\_ данных мпкаллбакк**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="e8df4-250">Error code is available in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**МПНОТИФИ \_ зарезервированные \_ данные**</span><span class="sxs-lookup"><span data-stu-id="e8df4-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY\_RESERVED\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-252">Внутренние зарезервированные данные.</span><span class="sxs-lookup"><span data-stu-id="e8df4-252">Internal reserved data.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**\_ \_ ДОБАВЛЕНА подпись мпнотифи \_ фастпас**</span><span class="sxs-lookup"><span data-stu-id="e8df4-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY\_FASTPATH\_SIG\_ADDED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-254">Сигнатура Фастпас либо добавила, либо отключила подпись.</span><span class="sxs-lookup"><span data-stu-id="e8df4-254">A Fastpath signature has either added or disabled a signature.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**\_удален мпнотифи фастпас \_ SIG \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY\_FASTPATH\_SIG\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-256">Удалена подпись Фастпас.</span><span class="sxs-lookup"><span data-stu-id="e8df4-256">A FastPath signature has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**\_частный мпнотифи NIS \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY\_NIS\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-258">Частный нотифкатионс NIS.</span><span class="sxs-lookup"><span data-stu-id="e8df4-258">NIS private notifcations.</span></span> <span data-ttu-id="e8df4-259">Ни один партнер не должен зарегистрироваться для этого.</span><span class="sxs-lookup"><span data-stu-id="e8df4-259">No partners should register for this.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**\_изменение работоспособности мпнотифи \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY\_HEALTH\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-261">Служба AM перешла в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="e8df4-261">The AM service has entered a new state.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**\_восстановление работоспособности мпнотифи \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY\_HEALTH\_RECOVERY**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-263">Служба AM восстановлена из состояния.</span><span class="sxs-lookup"><span data-stu-id="e8df4-263">The AM service has recovered from a state.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**\_Начало работоспособности мпнотифи \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY\_HEALTH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-265">Служба AM инициализировала работоспособность системы.</span><span class="sxs-lookup"><span data-stu-id="e8df4-265">The AM service has initialized the health of the system.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**\_изменение мпнотифи ендофлифе \_**</span><span class="sxs-lookup"><span data-stu-id="e8df4-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY\_ENDOFLIFE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-267">Изменились даты окончания срока действия для службы AM.</span><span class="sxs-lookup"><span data-stu-id="e8df4-267">The "End Of Life" expiry dates for the AM service have changed.</span></span>

</dd> <dt>

<span data-ttu-id="e8df4-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**МПНОТИФИ \_ малваретоаст \_ данные**</span><span class="sxs-lookup"><span data-stu-id="e8df4-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY\_MALWARETOAST\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="e8df4-269">В службе AM обнаружены вредоносные программы, которые могли привести к изменению критических параметров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e8df4-269">The AM service has encountered malware that might have caused critical settings change in the machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8df4-270">Требования</span><span class="sxs-lookup"><span data-stu-id="e8df4-270">Requirements</span></span>



| <span data-ttu-id="e8df4-271">Требование</span><span class="sxs-lookup"><span data-stu-id="e8df4-271">Requirement</span></span> | <span data-ttu-id="e8df4-272">Значение</span><span class="sxs-lookup"><span data-stu-id="e8df4-272">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8df4-273">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8df4-273">Minimum supported client</span></span><br/> | <span data-ttu-id="e8df4-274">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e8df4-274">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e8df4-275">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8df4-275">Minimum supported server</span></span><br/> | <span data-ttu-id="e8df4-276">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e8df4-276">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8df4-277">Header</span><span class="sxs-lookup"><span data-stu-id="e8df4-277">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8df4-278"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8df4-278"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8df4-279">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8df4-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8df4-280">**мпманажерстатускуерекс**</span><span class="sxs-lookup"><span data-stu-id="e8df4-280">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="e8df4-281">**\_данные мпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e8df4-281">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="e8df4-282">**\_данные мпсампле**</span><span class="sxs-lookup"><span data-stu-id="e8df4-282">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> </dl>

 

 





