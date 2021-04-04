---
title: Константы состояния задания печати ADSI (Адсстс. h)
description: Для указания состояния задания печати используются следующие константы со свойством Иадспринтжобоператионс. status.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989101"
---
# <a name="adsi-print-job-status-constants"></a><span data-ttu-id="6ad10-103">Константы состояния задания печати ADSI</span><span class="sxs-lookup"><span data-stu-id="6ad10-103">ADSI Print Job Status Constants</span></span>

<span data-ttu-id="6ad10-104">Для указания состояния задания печати используются следующие константы со свойством [**иадспринтжобоператионс. status**](iadsprintjoboperations-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad10-104">The following constants are used with the [**IADsPrintJobOperations.Status**](iadsprintjoboperations-property-methods.md) property to indicate the status of a print job.</span></span>

<dl> <dt>

<span data-ttu-id="6ad10-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**\_Задание ADS \_ приостановлено**</span><span class="sxs-lookup"><span data-stu-id="6ad10-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**ADS\_JOB\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad10-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6ad10-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="6ad10-107">Задание печати приостановлено.</span><span class="sxs-lookup"><span data-stu-id="6ad10-107">The print job is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ad10-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**\_Ошибка задания \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="6ad10-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS\_JOB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad10-109">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="6ad10-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="6ad10-110">Произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="6ad10-110">An error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ad10-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**\_Удаление задания \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="6ad10-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**ADS\_JOB\_DELETING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad10-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="6ad10-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="6ad10-113">Удаляется задание печати.</span><span class="sxs-lookup"><span data-stu-id="6ad10-113">The print job is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ad10-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**\_очередь заданий \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="6ad10-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**ADS\_JOB\_SPOOLING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad10-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="6ad10-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="6ad10-116">Задание печати помещается в очередь.</span><span class="sxs-lookup"><span data-stu-id="6ad10-116">The print job is being spooled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ad10-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**\_печать задания \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="6ad10-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**ADS\_JOB\_PRINTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad10-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="6ad10-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="6ad10-119">Печатается задание печати.</span><span class="sxs-lookup"><span data-stu-id="6ad10-119">The print job is being printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ad10-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**\_ \_ автономное задание AD**</span><span class="sxs-lookup"><span data-stu-id="6ad10-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS\_JOB\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad10-121">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="6ad10-121">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="6ad10-122">Принтер отключен.</span><span class="sxs-lookup"><span data-stu-id="6ad10-122">The printer is offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ad10-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**\_Документация по заданию ADS \_**</span><span class="sxs-lookup"><span data-stu-id="6ad10-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**ADS\_JOB\_PAPEROUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad10-124">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="6ad10-124">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="6ad10-125">В принтере нет бумаги.</span><span class="sxs-lookup"><span data-stu-id="6ad10-125">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ad10-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**\_печать задания \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="6ad10-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**ADS\_JOB\_PRINTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad10-127">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="6ad10-127">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="6ad10-128">Задание печати напечатано.</span><span class="sxs-lookup"><span data-stu-id="6ad10-128">The print job has been printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ad10-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**\_Задание ADS \_ удалено**</span><span class="sxs-lookup"><span data-stu-id="6ad10-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**ADS\_JOB\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad10-130">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="6ad10-130">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="6ad10-131">Задание печати было удалено.</span><span class="sxs-lookup"><span data-stu-id="6ad10-131">The print job has been deleted.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ad10-132">Требования</span><span class="sxs-lookup"><span data-stu-id="6ad10-132">Requirements</span></span>



| <span data-ttu-id="6ad10-133">Требование</span><span class="sxs-lookup"><span data-stu-id="6ad10-133">Requirement</span></span> | <span data-ttu-id="6ad10-134">Значение</span><span class="sxs-lookup"><span data-stu-id="6ad10-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad10-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ad10-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad10-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ad10-136">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="6ad10-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ad10-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad10-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ad10-138">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="6ad10-139">Header</span><span class="sxs-lookup"><span data-stu-id="6ad10-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ad10-140"><dt>Адсстс. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ad10-140"><dt>Adssts.h</dt></span></span> </dl> |



 

 





