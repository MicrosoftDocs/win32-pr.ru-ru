---
title: Структура MPCALLBACK_DATA (Мпклиент. h)
description: Данные, передаваемые функции обратного вызова.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA структуры устаревшие функции среды Windows
- Функции PMPCALLBACK_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135802"
---
# <a name="mpcallback_data-structure"></a><span data-ttu-id="6b807-105">\_Структура данных мпкаллбакк</span><span class="sxs-lookup"><span data-stu-id="6b807-105">MPCALLBACK\_DATA structure</span></span>

<span data-ttu-id="6b807-106">Данные, передаваемые функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6b807-106">Data passed to the callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b807-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b807-107">Syntax</span></span>


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a><span data-ttu-id="6b807-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6b807-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b807-109">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="6b807-109">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-110">Тип: **[ **мпнотифи**](mpnotify.md)**</span><span class="sxs-lookup"><span data-stu-id="6b807-110">Type: **[**MPNOTIFY**](mpnotify.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-111">Изменить уведомление на отчет.</span><span class="sxs-lookup"><span data-stu-id="6b807-111">Change notification to report.</span></span>

</dd> <dt>

<span data-ttu-id="6b807-112">**Состав**</span><span class="sxs-lookup"><span data-stu-id="6b807-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-113">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6b807-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-114">Код ошибки в случае внутреннего сбоя.</span><span class="sxs-lookup"><span data-stu-id="6b807-114">Error code, in case of an internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="6b807-115">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="6b807-115">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-116">Тип: **уларже \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="6b807-116">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-117">Текущая отметка времени.</span><span class="sxs-lookup"><span data-stu-id="6b807-117">Current timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="6b807-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b807-118">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-119">Тип: **[ **мпкаллбакк \_ тип**](mpcallback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="6b807-119">Type: **[**MPCALLBACK\_TYPE**](mpcallback-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-120">Специальный тип данных обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6b807-120">Callback special data type.</span></span>

</dd> <dt>

<span data-ttu-id="6b807-121">**Data**</span><span class="sxs-lookup"><span data-stu-id="6b807-121">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-122">Специальные данные обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6b807-122">Callback special data.</span></span> <span data-ttu-id="6b807-123">Указатель на соответствующую структуру зависит от значения **типа**.</span><span class="sxs-lookup"><span data-stu-id="6b807-123">The pointer to the appropriate structure depends on the value of **Type**.</span></span>

<dl> <dt>

<span data-ttu-id="6b807-124">**пстатусдата**</span><span class="sxs-lookup"><span data-stu-id="6b807-124">**pStatusData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-125">Тип: **пмпстатус \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-125">Type: **PMPSTATUS\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-126">При **вводе**  ==  **\_ состояния мпкаллбакк**.</span><span class="sxs-lookup"><span data-stu-id="6b807-126">When **Type** == **MPCALLBACK\_STATUS**.</span></span> <span data-ttu-id="6b807-127">См. [**мпстатус \_ Data**](mpstatus-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-127">See [**MPSTATUS\_DATA**](mpstatus-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-128">**пскандата**</span><span class="sxs-lookup"><span data-stu-id="6b807-128">**pScanData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-129">Тип: **пмпскан \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-129">Type: **PMPSCAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-130">При   ==  **\_ проверке типа мпкаллбакк**.</span><span class="sxs-lookup"><span data-stu-id="6b807-130">When **Type** == **MPCALLBACK\_SCAN**.</span></span> <span data-ttu-id="6b807-131">См. [**мпскан \_ Data**](mpscan-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-131">See [**MPSCAN\_DATA**](mpscan-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-132">**пклеандата**</span><span class="sxs-lookup"><span data-stu-id="6b807-132">**pCleanData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-133">Тип: **пмпклеан \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-133">Type: **PMPCLEAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-134">При **вводе типа**  ==  **мпкаллбакк \_ Clean**.</span><span class="sxs-lookup"><span data-stu-id="6b807-134">When **Type** == **MPCALLBACK\_CLEAN**.</span></span> <span data-ttu-id="6b807-135">См. [**мпклеан \_ Data**](mpclean-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-135">See [**MPCLEAN\_DATA**](mpclean-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-136">**ппречеккдата**</span><span class="sxs-lookup"><span data-stu-id="6b807-136">**pPrecheckData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-137">Тип: **пмпклеан. \_ Проверка \_ данных**</span><span class="sxs-lookup"><span data-stu-id="6b807-137">Type: **PMPCLEAN\_PRECHECK\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-138">При   ==  **\_ проверке типа мпкаллбакк**.</span><span class="sxs-lookup"><span data-stu-id="6b807-138">When **Type** == **MPCALLBACK\_PRECHECK**.</span></span> <span data-ttu-id="6b807-139">См. раздел [**мпклеан \_ recheck \_ Data**](mpclean-precheck-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-139">See [**MPCLEAN\_PRECHECK\_DATA**](mpclean-precheck-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-140">**псреатдата**</span><span class="sxs-lookup"><span data-stu-id="6b807-140">**pThreatData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-141">Тип: **пмпсреат \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-141">Type: **PMPTHREAT\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-142">При **типе**  ==  **мпкаллбакк \_ THREAT**.</span><span class="sxs-lookup"><span data-stu-id="6b807-142">When **Type** == **MPCALLBACK\_THREAT**.</span></span> <span data-ttu-id="6b807-143">См. [**мпсреат \_ Data**](mpthreat-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-143">See [**MPTHREAT\_DATA**](mpthreat-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-144">**псигупдатедата**</span><span class="sxs-lookup"><span data-stu-id="6b807-144">**pSigUpdateData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-145">Тип: **пмпсигупдате \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-145">Type: **PMPSIGUPDATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-146">При **типе**  ==  **мпкаллбакк \_ сигупдате**.</span><span class="sxs-lookup"><span data-stu-id="6b807-146">When **Type** == **MPCALLBACK\_SIGUPDATE**.</span></span> <span data-ttu-id="6b807-147">См. [**мпсигупдате \_ Data**](mpsigupdate-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-147">See [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-148">**псампледата**</span><span class="sxs-lookup"><span data-stu-id="6b807-148">**pSampleData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-149">Тип: **пмпсампле \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-149">Type: **PMPSAMPLE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-150">При **вводе**  ==  **\_ образца Type мпкаллбакк**.</span><span class="sxs-lookup"><span data-stu-id="6b807-150">When **Type** == **MPCALLBACK\_SAMPLE**.</span></span> <span data-ttu-id="6b807-151">См. [**мпсампле \_ Data**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-151">See [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-152">**пресерведдата**</span><span class="sxs-lookup"><span data-stu-id="6b807-152">**pReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-153">Тип: **пмпресервед \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-153">Type: **PMPRESERVED\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-154">Если **тип**  ==  **мпкаллбакк \_ зарезервирован**.</span><span class="sxs-lookup"><span data-stu-id="6b807-154">When **Type** == **MPCALLBACK\_RESERVED**.</span></span> <span data-ttu-id="6b807-155">См. [**мпресервед \_ Data**](mpreserved-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-155">See [**MPRESERVED\_DATA**](mpreserved-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-156">**пконфигуратиондата**</span><span class="sxs-lookup"><span data-stu-id="6b807-156">**pConfigurationData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-157">Тип: **пмпконфигуратион \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-157">Type: **PMPCONFIGURATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-158">При   ==  **\_ \_ уведомлении о конфигурации типа мпкаллбакк**.</span><span class="sxs-lookup"><span data-stu-id="6b807-158">When **Type** == **MPCALLBACK\_CONFIGURATION\_NOTIFICATION**.</span></span> <span data-ttu-id="6b807-159">См. [**мпконфигуратион \_ Data**](mpconfiguration-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-159">See [**MPCONFIGURATION\_DATA**](mpconfiguration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-160">**пфастпасдата**</span><span class="sxs-lookup"><span data-stu-id="6b807-160">**pFastPathData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-161">Тип: **пмпфастпас \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-161">Type: **PMPFASTPATH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-162">При **типе**  ==  **мпкаллбакк \_ фастпас**.</span><span class="sxs-lookup"><span data-stu-id="6b807-162">When **Type** == **MPCALLBACK\_FASTPATH**.</span></span> <span data-ttu-id="6b807-163">См. [**мпфастпас \_ Data**](mpfastpath-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-163">See [**MPFASTPATH\_DATA**](mpfastpath-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-164">**пекспиратиондата**</span><span class="sxs-lookup"><span data-stu-id="6b807-164">**pExpirationData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-165">Тип: **пмпекспиратион \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-165">Type: **PMPEXPIRATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-166">При **вводе**  ==  **мпкаллбакк \_ \_ срока действия продукта**.</span><span class="sxs-lookup"><span data-stu-id="6b807-166">When **Type** == **MPCALLBACK\_PRODUCT\_EXPIRATION**.</span></span> <span data-ttu-id="6b807-167">См. [**мпекспиратион \_ Data**](mpexpiration-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-167">See [**MPEXPIRATION\_DATA**](mpexpiration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-168">**пнисприватедата**</span><span class="sxs-lookup"><span data-stu-id="6b807-168">**pNISPrivateData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-169">Тип: **пмпнис \_ Private \_ Data**</span><span class="sxs-lookup"><span data-stu-id="6b807-169">Type: **PMPNIS\_PRIVATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-170">Если **введите**  ==  **мпкаллбакк \_ NIS \_ Private**.</span><span class="sxs-lookup"><span data-stu-id="6b807-170">When **Type** == **MPCALLBACK\_NIS\_PRIVATE**.</span></span> <span data-ttu-id="6b807-171">См. раздел [**мпнис \_ Private \_ Data**](mpnis-private-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-171">See [**MPNIS\_PRIVATE\_DATA**](mpnis-private-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-172">**феалсдата**</span><span class="sxs-lookup"><span data-stu-id="6b807-172">**pHealthData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-173">Тип: **пмфеалс \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-173">Type: **PMPHEALTH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-174">При **типе**  ==  **\_ работоспособности мпкаллбакк**.</span><span class="sxs-lookup"><span data-stu-id="6b807-174">When **Type** == **MPCALLBACK\_HEALTH**.</span></span> <span data-ttu-id="6b807-175">См. [**мфеалс \_ Data**](mphealth-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-175">See [**MPHEALTH\_DATA**](mphealth-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-176">**пендофлифедата**</span><span class="sxs-lookup"><span data-stu-id="6b807-176">**pEndOfLifeData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-177">Тип: **пмпендофлифе \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-177">Type: **PMPENDOFLIFE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-178">При **типе**  ==  **мпкаллбакк \_ ендофлифе**.</span><span class="sxs-lookup"><span data-stu-id="6b807-178">When **Type** == **MPCALLBACK\_ENDOFLIFE**.</span></span> <span data-ttu-id="6b807-179">См. [**мпендофлифе \_ Data**](mpendoflife-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-179">See [**MPENDOFLIFE\_DATA**](mpendoflife-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b807-180">**пмалваретоастдата**</span><span class="sxs-lookup"><span data-stu-id="6b807-180">**pMalwareToastData**</span></span>
</dt> <dd>

<span data-ttu-id="6b807-181">Тип: **пмпмалваретоаст \_ Data** .</span><span class="sxs-lookup"><span data-stu-id="6b807-181">Type: **PMPMALWARETOAST\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="6b807-182">При **типе**  ==  **мпкаллбакк \_ малваретоаст**.</span><span class="sxs-lookup"><span data-stu-id="6b807-182">When **Type** == **MPCALLBACK\_MALWARETOAST**.</span></span> <span data-ttu-id="6b807-183">См. [**мпмалваретоаст \_ Data**](mpmalwaretoast-data.md).</span><span class="sxs-lookup"><span data-stu-id="6b807-183">See [**MPMALWARETOAST\_DATA**](mpmalwaretoast-data.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b807-184">Требования</span><span class="sxs-lookup"><span data-stu-id="6b807-184">Requirements</span></span>



| <span data-ttu-id="6b807-185">Требование</span><span class="sxs-lookup"><span data-stu-id="6b807-185">Requirement</span></span> | <span data-ttu-id="6b807-186">Значение</span><span class="sxs-lookup"><span data-stu-id="6b807-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b807-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b807-187">Minimum supported client</span></span><br/> | <span data-ttu-id="6b807-188">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6b807-188">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6b807-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b807-189">Minimum supported server</span></span><br/> | <span data-ttu-id="6b807-190">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6b807-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b807-191">Header</span><span class="sxs-lookup"><span data-stu-id="6b807-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b807-192"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b807-192"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b807-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b807-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b807-194">**\_тип мпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="6b807-194">**MPCALLBACK\_TYPE**</span></span>](mpcallback-type.md)
</dt> <dt>

[<span data-ttu-id="6b807-195">**\_данные мпклеан**</span><span class="sxs-lookup"><span data-stu-id="6b807-195">**MPCLEAN\_DATA**</span></span>](mpclean-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-196">**МПКЛЕАН \_ предпроверить \_ данные**</span><span class="sxs-lookup"><span data-stu-id="6b807-196">**MPCLEAN\_PRECHECK\_DATA**</span></span>](mpclean-precheck-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-197">**\_данные мпконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="6b807-197">**MPCONFIGURATION\_DATA**</span></span>](mpconfiguration-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-198">**\_данные мпендофлифе**</span><span class="sxs-lookup"><span data-stu-id="6b807-198">**MPENDOFLIFE\_DATA**</span></span>](mpendoflife-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-199">**\_данные мпекспиратион**</span><span class="sxs-lookup"><span data-stu-id="6b807-199">**MPEXPIRATION\_DATA**</span></span>](mpexpiration-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-200">**\_данные мпфастпас**</span><span class="sxs-lookup"><span data-stu-id="6b807-200">**MPFASTPATH\_DATA**</span></span>](mpfastpath-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-201">**\_данные мфеалс**</span><span class="sxs-lookup"><span data-stu-id="6b807-201">**MPHEALTH\_DATA**</span></span>](mphealth-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-202">**\_данные мпмалваретоаст**</span><span class="sxs-lookup"><span data-stu-id="6b807-202">**MPMALWARETOAST\_DATA**</span></span>](mpmalwaretoast-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-203">**МПНИС \_ закрытые \_ данные**</span><span class="sxs-lookup"><span data-stu-id="6b807-203">**MPNIS\_PRIVATE\_DATA**</span></span>](mpnis-private-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-204">**мпнотифи**</span><span class="sxs-lookup"><span data-stu-id="6b807-204">**MPNOTIFY**</span></span>](mpnotify.md)
</dt> <dt>

[<span data-ttu-id="6b807-205">**\_данные мпресервед**</span><span class="sxs-lookup"><span data-stu-id="6b807-205">**MPRESERVED\_DATA**</span></span>](mpreserved-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-206">**\_данные мпсампле**</span><span class="sxs-lookup"><span data-stu-id="6b807-206">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-207">**\_данные мпскан**</span><span class="sxs-lookup"><span data-stu-id="6b807-207">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-208">**\_данные мпсигупдате**</span><span class="sxs-lookup"><span data-stu-id="6b807-208">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-209">**\_данные мпстатус**</span><span class="sxs-lookup"><span data-stu-id="6b807-209">**MPSTATUS\_DATA**</span></span>](mpstatus-data.md)
</dt> <dt>

[<span data-ttu-id="6b807-210">**\_данные мпсреат**</span><span class="sxs-lookup"><span data-stu-id="6b807-210">**MPTHREAT\_DATA**</span></span>](mpthreat-data.md)
</dt> </dl>

 

 





