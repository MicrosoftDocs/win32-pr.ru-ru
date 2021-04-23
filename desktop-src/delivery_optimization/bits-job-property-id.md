---
title: Перечисление BITS_JOB_PROPERTY_ID (Deliveryoptimization. h)
description: Перечисление BITS_JOB_PROPERTY_ID указывает идентификатор свойства для задания DO. Это перечисление используется в объединении BITS_JOB_PROPERTY_VALUE для определения типа значения, содержащегося в объединении.
ms.assetid: B0F3C6C2-474F-4FD8-990A-770FAA993550
keywords:
- Перечисление BITS_JOB_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1d00d4dc12b27c1c80b0e18bb095641a56e322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801390"
---
# <a name="bits_job_property_id-enumeration"></a><span data-ttu-id="162a7-105">Перечисление BITS_JOB_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="162a7-105">BITS_JOB_PROPERTY_ID enumeration</span></span>

<span data-ttu-id="162a7-106">Перечисление **BITS_JOB_PROPERTY_ID** указывает идентификатор свойства для задания Do.</span><span class="sxs-lookup"><span data-stu-id="162a7-106">The **BITS_JOB_PROPERTY_ID** enumeration specifies the ID of the property for the DO job.</span></span> <span data-ttu-id="162a7-107">Это перечисление используется в объединении [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) для определения типа значения, содержащегося в объединении.</span><span class="sxs-lookup"><span data-stu-id="162a7-107">This enumeration is used in the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union to determine the type of value contained in the union.</span></span>

## <a name="syntax"></a><span data-ttu-id="162a7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="162a7-108">Syntax</span></span>


```C++
typedef enum  { 
  BITS_JOB_PROPERTY_ID_COST_FLAGS                     = 1,
  BITS_JOB_PROPERTY_NOTIFICATION_CLSID                = 2,
  BITS_JOB_PROPERTY_DYNAMIC_CONTENT                   = 3,
  BITS_JOB_PROPERTY_HIGH_PERFORMANCE                  = 4,
  BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE                 = 5,
  BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS            = 7,
  BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS  = 9,
  BITS_JOB_PROPERTY_ON_DEMAND_MODE                    = 10
} BITS_JOB_PROPERTY_ID;
```



## <a name="constants"></a><span data-ttu-id="162a7-109">Константы</span><span class="sxs-lookup"><span data-stu-id="162a7-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="162a7-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="162a7-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="162a7-111">Идентификатор, используемый для [управления поведением передачи](https://www.bing.com/search?q=control+transfer+behavior) по сотовой или подобной сети.</span><span class="sxs-lookup"><span data-stu-id="162a7-111">The ID that is used to [control transfer behavior](https://www.bing.com/search?q=control+transfer+behavior) over cellular and/or similar networks.</span></span> <span data-ttu-id="162a7-112">Это свойство можно изменить, пока выполняется перемещение. новые флаги стоимости вступят в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="162a7-112">This property may be changed while a transfer is ongoing   the new cost flags will take effect immediately.</span></span>

<span data-ttu-id="162a7-113">Это свойство использует поле **Dword** **BITS_JOB_PROPERTY_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="162a7-113">This property uses the **BITS_JOB_PROPERTY_VALUE** s **Dword** field.</span></span>

</dd> <dt>

<span data-ttu-id="162a7-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span><span class="sxs-lookup"><span data-stu-id="162a7-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="162a7-115">Идентификатор, используемый для [регистрации обратного вызова com](https://www.bing.com/search?q=register+a+COM+callback) по CLSID для получения уведомлений о ходе выполнения и выполнении задания.</span><span class="sxs-lookup"><span data-stu-id="162a7-115">The ID that is used to [register a COM callback](https://www.bing.com/search?q=register+a+COM+callback) by CLSID to receive notifications about the progress and completion of a DO job.</span></span> <span data-ttu-id="162a7-116">CLSID должен ссылаться на класс, связанный с зарегистрированным серверным COM-сервером.</span><span class="sxs-lookup"><span data-stu-id="162a7-116">The CLSID must refer to a class associated with a registered out-of-process COM server.</span></span> <span data-ttu-id="162a7-117">Его также можно установить в **GUID_NULL** , чтобы очистить ранее установленный CLSID уведомления.</span><span class="sxs-lookup"><span data-stu-id="162a7-117">It may also be set to **GUID_NULL** to clear a previously set notification CLSID.</span></span>

<span data-ttu-id="162a7-118">Это свойство использует поле **CLsID** **BITS_JOB_PROPERTY_VALUE** s.</span><span class="sxs-lookup"><span data-stu-id="162a7-118">This property uses the **BITS_JOB_PROPERTY_VALUE** s **CLsID** field.</span></span>

</dd> <dt>

<span data-ttu-id="162a7-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="162a7-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="162a7-120">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="162a7-120">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="162a7-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span><span class="sxs-lookup"><span data-stu-id="162a7-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span></span>
</dt> <dd>

<span data-ttu-id="162a7-122">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="162a7-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="162a7-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span><span class="sxs-lookup"><span data-stu-id="162a7-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="162a7-124">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="162a7-124">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="162a7-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="162a7-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="162a7-126">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="162a7-126">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="162a7-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span><span class="sxs-lookup"><span data-stu-id="162a7-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span></span>
</dt> <dd>

<span data-ttu-id="162a7-128">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="162a7-128">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="162a7-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span><span class="sxs-lookup"><span data-stu-id="162a7-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="162a7-130">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="162a7-130">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="162a7-131">Требования</span><span class="sxs-lookup"><span data-stu-id="162a7-131">Requirements</span></span>



| <span data-ttu-id="162a7-132">Требование</span><span class="sxs-lookup"><span data-stu-id="162a7-132">Requirement</span></span> | <span data-ttu-id="162a7-133">Значение</span><span class="sxs-lookup"><span data-stu-id="162a7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="162a7-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="162a7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="162a7-135">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="162a7-135">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="162a7-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="162a7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="162a7-137">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="162a7-137">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="162a7-138">Header</span><span class="sxs-lookup"><span data-stu-id="162a7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="162a7-139"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="162a7-139"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="162a7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="162a7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="162a7-141">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="162a7-141">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="162a7-142">**BITS_JOB_PROPERTY_VALUE**</span><span class="sxs-lookup"><span data-stu-id="162a7-142">**BITS_JOB_PROPERTY_VALUE**</span></span>](bits-job-property-value-.md)
</dt> <dt>

[<span data-ttu-id="162a7-143">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="162a7-143">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> <dt>

[<span data-ttu-id="162a7-144">**IBackgroundCopyJob5:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="162a7-144">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[<span data-ttu-id="162a7-145">**IBackgroundCopyJob5:: Property**</span><span class="sxs-lookup"><span data-stu-id="162a7-145">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





