---
title: Перечисление MPSTATUS_FLAG (Мпклиент. h)
description: Возможные общие битовые флаги состояния продукта.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG перечисления устаревшие функции среды Windows
- PMPSTATUS_FLAG указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPSTATUS_FLAG
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c7175980c09c63938be04626091c31b53335756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661885"
---
# <a name="mpstatus_flag-enumeration"></a><span data-ttu-id="6516b-105">\_Перечисление флагов мпстатус</span><span class="sxs-lookup"><span data-stu-id="6516b-105">MPSTATUS\_FLAG enumeration</span></span>

<span data-ttu-id="6516b-106">Возможные общие битовые флаги состояния продукта.</span><span class="sxs-lookup"><span data-stu-id="6516b-106">Possible overall product status bit flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="6516b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6516b-107">Syntax</span></span>


```C++
typedef enum tagMPSTATUS_FLAG { 
  MP_STATUS_FLAG_NONE                           = 0,
  MP_STATUS_FLAG_SERVICE_UNAVAILABLE            = 1 << 0,
  MP_STATUS_FLAG_MPENGINE_UNAVAILABLE           = 1 << 1,
  MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED       = 1 << 2,
  MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED         = 1 << 3,
  MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED   = 1 << 4,
  MP_STATUS_FLAG_DUE_AV_SIGNATURE               = 1 << 5,
  MP_STATUS_FLAG_DUE_AS_SIGNATURE               = 1 << 6,
  MP_STATUS_FLAG_DUE_QUICK_SCAN                 = 1 << 7,
  MP_STATUS_FLAG_DUE_FULL_SCAN                  = 1 << 8,
  MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN         = 1 << 9,
  MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING    = 1 << 10,
  MP_STATUS_FLAG_DUE_SAMPLES                    = 1 << 11,
  MP_STATUS_FLAG_EVALUATION_MODE                = 1 << 12,
  MP_STATUS_FLAG_NONGENUINE                     = 1 << 13,
  MP_STATUS_FLAG_PRODUCT_EXPIRED                = 1 << 14,
  MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED       = 1 << 15,
  MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN     = 1 << 16,
  MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE       = 1 << 17,
  MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE   = 1 << 18,
  MP_STATUS_FLAG_HEALTH_INITIALIZED             = 1 << 19,
  MP_STATUS_FLAG_DUE_PLATFORM_UPDATE            = 1 << 20,
  MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE     = 1 << 21,
  MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED  = 1 << 22,
  MP_STATUS_FLAG_END_OF_LIFE                    = 1 << 23,
  MP_STATUS_FLAG_MAX                            = 1 << 23,
  MP_STATUS_FLAG_ALL                            = (1 << 24)-1
} MPSTATUS_FLAG, *PMPSTATUS_FLAG;
```



## <a name="constants"></a><span data-ttu-id="6516b-108">Константы</span><span class="sxs-lookup"><span data-stu-id="6516b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6516b-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**\_флаг состояния точки управления \_ \_ нет**</span><span class="sxs-lookup"><span data-stu-id="6516b-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP\_STATUS\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-110">Флаги состояния не заданы (неинициализированное состояние).</span><span class="sxs-lookup"><span data-stu-id="6516b-110">No status flags set (non-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="6516b-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**\_ \_ Служба флагов состояния пакета управления \_ \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="6516b-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP\_STATUS\_FLAG\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-112">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="6516b-112">Service not running.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**\_флаг состояния пакета управления \_ \_ мпенгине \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="6516b-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP\_STATUS\_FLAG\_MPENGINE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-114">Служба запущена без механизма защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="6516b-114">Service started without any malware protection engine.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**\_требуется флаг состояния пакета управления для \_ \_ угрозы \_ FULLSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="6516b-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP\_STATUS\_FLAG\_THREAT\_FULLSCAN\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-116">Ожидание полной проверки из-за действия угрозы.</span><span class="sxs-lookup"><span data-stu-id="6516b-116">Pending full scan due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**\_ \_ \_ \_ требуется перезагрузка угрозы с флагом состояния пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="6516b-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**MP\_STATUS\_FLAG\_THREAT\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-118">Ожидается перезагрузка из-за действия угрозы.</span><span class="sxs-lookup"><span data-stu-id="6516b-118">Pending reboot due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**\_ \_ Пошаговое руководство по отметке состояния пакета управления — \_ \_ \_ \_ требуются действия**</span><span class="sxs-lookup"><span data-stu-id="6516b-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**MP\_STATUS\_FLAG\_THREAT\_MANUAL\_STEPS\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-120">Ожидаются ручные действия из-за действия угрозы.</span><span class="sxs-lookup"><span data-stu-id="6516b-120">Pending manual steps due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**флаг состояния пакета управления — \_ \_ \_ \_ \_ сигнатура AV**</span><span class="sxs-lookup"><span data-stu-id="6516b-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AV\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-122">Антивирусные сигнатуры устарели.</span><span class="sxs-lookup"><span data-stu-id="6516b-122">Antivirus signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**\_флаг состояния пакета управления \_ \_ из-за \_ \_ сигнатуры**</span><span class="sxs-lookup"><span data-stu-id="6516b-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AS\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-124">Устарели сигнатуры антишпионского по.</span><span class="sxs-lookup"><span data-stu-id="6516b-124">Antispyware signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**флаг состояния пакета управления — \_ \_ \_ \_ Быстрая \_ Проверка**</span><span class="sxs-lookup"><span data-stu-id="6516b-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP\_STATUS\_FLAG\_DUE\_QUICK\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-126">Быстрая проверка не выполнялась в течение указанного периода.</span><span class="sxs-lookup"><span data-stu-id="6516b-126">No quick scan has happened for a specified period.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**\_флаг состояния пакета управления \_ \_ из-за \_ полной \_ проверки**</span><span class="sxs-lookup"><span data-stu-id="6516b-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP\_STATUS\_FLAG\_DUE\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-128">Полная проверка не выполнялась в течение указанного периода</span><span class="sxs-lookup"><span data-stu-id="6516b-128">no full scan has happened for a specified period</span></span>

</dd> <dt>

<span data-ttu-id="6516b-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**\_флаг состояния пакета управления \_ \_ выполнение \_ \_ проверки системы**</span><span class="sxs-lookup"><span data-stu-id="6516b-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_SYSTEM\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-130">Выполняется проверка, инициированная системой.</span><span class="sxs-lookup"><span data-stu-id="6516b-130">System-initiated scan in progress.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**Установка \_ флага состояния пакета управления \_ \_ выполнение \_ очистки подпрограммы \_**</span><span class="sxs-lookup"><span data-stu-id="6516b-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_ROUTINE\_CLEANING**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-132">Выполняется очистка, инициированная системой.</span><span class="sxs-lookup"><span data-stu-id="6516b-132">System-initiated clean in progress.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**\_ \_ Примеры выполнения флагов состояния пакета \_ управления \_**</span><span class="sxs-lookup"><span data-stu-id="6516b-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**MP\_STATUS\_FLAG\_DUE\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-134">Имеются образцы, ожидающие отправки.</span><span class="sxs-lookup"><span data-stu-id="6516b-134">There are samples pending submission.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**\_ \_ режим вычисления флага состояния пакета \_ управления \_**</span><span class="sxs-lookup"><span data-stu-id="6516b-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MP\_STATUS\_FLAG\_EVALUATION\_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-136">Продукт работает в режиме оценки.</span><span class="sxs-lookup"><span data-stu-id="6516b-136">Product is running in evaluation mode.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**флаг состояния пакета управления — \_ \_ \_ неподлинная**</span><span class="sxs-lookup"><span data-stu-id="6516b-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP\_STATUS\_FLAG\_NONGENUINE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-138">Продукт работает в режиме Windows без подлинности.</span><span class="sxs-lookup"><span data-stu-id="6516b-138">Product is running in non-genuine Windows mode.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**\_ \_ \_ \_ истек срок действия продукта для флага состояния пакета управления**</span><span class="sxs-lookup"><span data-stu-id="6516b-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP\_STATUS\_FLAG\_PRODUCT\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-140">Срок действия продукта истек.</span><span class="sxs-lookup"><span data-stu-id="6516b-140">Product expired.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**\_требуется флаг состояния пакета управления \_ \_ THREAT \_ Каллисто \_**</span><span class="sxs-lookup"><span data-stu-id="6516b-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP\_STATUS\_FLAG\_THREAT\_CALLISTO\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-142">Каллисто требуется автономное сканирование.</span><span class="sxs-lookup"><span data-stu-id="6516b-142">Callisto off-line scan required.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ Служба флагов состояния пакета управления \_ \_ при \_ \_ завершении работы системы**</span><span class="sxs-lookup"><span data-stu-id="6516b-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**MP\_STATUS\_FLAG\_SERVICE\_ON\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-144">Служба завершает работу в процессе завершения работы системы.</span><span class="sxs-lookup"><span data-stu-id="6516b-144">Service is shutting down as part of system shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**\_ \_ \_ \_ критический сбой службы флагов состояния пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="6516b-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-146">Критическая ошибка при исправлении угроз.</span><span class="sxs-lookup"><span data-stu-id="6516b-146">Threat remediation failed critically.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**\_ \_ \_ \_ \_ некритический сбой службы флага состояния \_ пакета управления**</span><span class="sxs-lookup"><span data-stu-id="6516b-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_NON\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-148">Исправление угроз не было критическим.</span><span class="sxs-lookup"><span data-stu-id="6516b-148">Threat remediation failed non-critically.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**\_ \_ инициализировано состояние флага состояния пакета управления \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6516b-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**MP\_STATUS\_FLAG\_HEALTH\_INITIALIZED**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-150">Флаги состояния не заданы (правильно инициализированное состояние).</span><span class="sxs-lookup"><span data-stu-id="6516b-150">No status flags set (well-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="6516b-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**\_ \_ \_ обновление платформы из-за флага состояния пакета \_ управления \_**</span><span class="sxs-lookup"><span data-stu-id="6516b-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP\_STATUS\_FLAG\_DUE\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-152">Неактуальная версия платформы.</span><span class="sxs-lookup"><span data-stu-id="6516b-152">The platform is out of date.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**\_флаг состояния пакета управления \_ \_ \_ обновление платформы \_ выполняется**</span><span class="sxs-lookup"><span data-stu-id="6516b-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-154">Выполняется обновление платформы.</span><span class="sxs-lookup"><span data-stu-id="6516b-154">Platform update is in progress.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**\_ \_ платформа флага состояния пакета управления \_ \_ \_ , которая должна \_ быть \_ устаревшей**</span><span class="sxs-lookup"><span data-stu-id="6516b-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP\_STATUS\_FLAG\_PLATFORM\_ABOUT\_TO\_BE\_OUTDATED**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-156">Платформа скоро будет устаревшей</span><span class="sxs-lookup"><span data-stu-id="6516b-156">The platform is about to be outdated</span></span>

</dd> <dt>

<span data-ttu-id="6516b-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**\_ \_ \_ конец \_ \_ срока действия флага состояния пакета управления**</span><span class="sxs-lookup"><span data-stu-id="6516b-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP\_STATUS\_FLAG\_END\_OF\_LIFE**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-158">Подпись или окончание срока жизни платформы находится в прошлом или ожидает.</span><span class="sxs-lookup"><span data-stu-id="6516b-158">The signature or platform end of life is past or is pending.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**\_ \_ максимальный флаг состояния пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="6516b-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP\_STATUS\_FLAG\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-160">Максимальный допустимый флаг.</span><span class="sxs-lookup"><span data-stu-id="6516b-160">Maximum valid flag.</span></span>

</dd> <dt>

<span data-ttu-id="6516b-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**\_флаг состояния пакета управления \_ \_ все**</span><span class="sxs-lookup"><span data-stu-id="6516b-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP\_STATUS\_FLAG\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="6516b-162">Максимально возможное значение.</span><span class="sxs-lookup"><span data-stu-id="6516b-162">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6516b-163">Требования</span><span class="sxs-lookup"><span data-stu-id="6516b-163">Requirements</span></span>



| <span data-ttu-id="6516b-164">Требование</span><span class="sxs-lookup"><span data-stu-id="6516b-164">Requirement</span></span> | <span data-ttu-id="6516b-165">Значение</span><span class="sxs-lookup"><span data-stu-id="6516b-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6516b-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6516b-166">Minimum supported client</span></span><br/> | <span data-ttu-id="6516b-167">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6516b-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6516b-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6516b-168">Minimum supported server</span></span><br/> | <span data-ttu-id="6516b-169">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6516b-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6516b-170">Header</span><span class="sxs-lookup"><span data-stu-id="6516b-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="6516b-171"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="6516b-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





