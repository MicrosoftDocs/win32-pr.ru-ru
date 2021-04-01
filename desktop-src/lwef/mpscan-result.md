---
title: Структура MPSCAN_RESULT (Мпклиент. h)
description: Результаты проверки.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT структуры устаревшие функции среды Windows
- Функции PMPSCAN_RESULT указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262225"
---
# <a name="mpscan_result-structure"></a><span data-ttu-id="60a72-105">\_Структура результата мпскан</span><span class="sxs-lookup"><span data-stu-id="60a72-105">MPSCAN\_RESULT structure</span></span>

<span data-ttu-id="60a72-106">Результаты проверки.</span><span class="sxs-lookup"><span data-stu-id="60a72-106">The results of a scan.</span></span>

## <a name="syntax"></a><span data-ttu-id="60a72-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60a72-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a><span data-ttu-id="60a72-108">Члены</span><span class="sxs-lookup"><span data-stu-id="60a72-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="60a72-109">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="60a72-109">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="60a72-110">Тип: **[ **мпскан \_ тип**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="60a72-110">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60a72-111">Тип проверки.</span><span class="sxs-lookup"><span data-stu-id="60a72-111">Scan type.</span></span> <span data-ttu-id="60a72-112">См. раздел [**\_ тип мпскан**](mpscan-type.md).</span><span class="sxs-lookup"><span data-stu-id="60a72-112">See [**MPSCAN\_TYPE**](mpscan-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="60a72-113">**Источник**</span><span class="sxs-lookup"><span data-stu-id="60a72-113">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="60a72-114">Тип: **[ **мпсаурце**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="60a72-114">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60a72-115">Источник сканирования, например инициированный пользователем или системой.</span><span class="sxs-lookup"><span data-stu-id="60a72-115">Scan source, such as user or system initiated.</span></span> <span data-ttu-id="60a72-116">См. [**мпсаурце**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="60a72-116">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="60a72-117">**скангуид**</span><span class="sxs-lookup"><span data-stu-id="60a72-117">**ScanGuid**</span></span>
</dt> <dd>

<span data-ttu-id="60a72-118">Тип: **GUID**</span><span class="sxs-lookup"><span data-stu-id="60a72-118">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="60a72-119">Идентификатор проверки.</span><span class="sxs-lookup"><span data-stu-id="60a72-119">Scan identifier.</span></span>

</dd> <dt>

<span data-ttu-id="60a72-120">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="60a72-120">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="60a72-121">Тип: **уларже \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="60a72-121">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="60a72-122">Время начала проверки.</span><span class="sxs-lookup"><span data-stu-id="60a72-122">Scan start time.</span></span>

</dd> <dt>

<span data-ttu-id="60a72-123">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="60a72-123">**EndTime**</span></span>
</dt> <dd>

<span data-ttu-id="60a72-124">Тип: **уларже \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="60a72-124">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="60a72-125">Время окончания проверки.</span><span class="sxs-lookup"><span data-stu-id="60a72-125">Scan end time.</span></span>

</dd> <dt>

<span data-ttu-id="60a72-126">**среатстатс**</span><span class="sxs-lookup"><span data-stu-id="60a72-126">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="60a72-127">Тип: **[ **мпсреат \_ stats**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="60a72-127">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60a72-128">Статистика, связанная с угрозами.</span><span class="sxs-lookup"><span data-stu-id="60a72-128">Threat-related statistics.</span></span> <span data-ttu-id="60a72-129">См. [**мпсреат \_ stats**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="60a72-129">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="60a72-130">**ресаурцестатс**</span><span class="sxs-lookup"><span data-stu-id="60a72-130">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="60a72-131">Тип: **[ **мпресаурце \_ stats**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="60a72-131">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60a72-132">Статистика, связанная с ресурсами.</span><span class="sxs-lookup"><span data-stu-id="60a72-132">Resource-related statistics.</span></span> <span data-ttu-id="60a72-133">См. [**мпресаурце \_ stats**](mpresource-stats.md).</span><span class="sxs-lookup"><span data-stu-id="60a72-133">See [**MPRESOURCE\_STATS**](mpresource-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="60a72-134">**Версия сигнатуры**</span><span class="sxs-lookup"><span data-stu-id="60a72-134">**SignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="60a72-135">Тип: **улонглонг**</span><span class="sxs-lookup"><span data-stu-id="60a72-135">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="60a72-136">Версия подписи, используемой для проверки.</span><span class="sxs-lookup"><span data-stu-id="60a72-136">Version of signature used for scan.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60a72-137">Требования</span><span class="sxs-lookup"><span data-stu-id="60a72-137">Requirements</span></span>



| <span data-ttu-id="60a72-138">Требование</span><span class="sxs-lookup"><span data-stu-id="60a72-138">Requirement</span></span> | <span data-ttu-id="60a72-139">Значение</span><span class="sxs-lookup"><span data-stu-id="60a72-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60a72-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60a72-140">Minimum supported client</span></span><br/> | <span data-ttu-id="60a72-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="60a72-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="60a72-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60a72-142">Minimum supported server</span></span><br/> | <span data-ttu-id="60a72-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="60a72-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60a72-144">Header</span><span class="sxs-lookup"><span data-stu-id="60a72-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="60a72-145"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="60a72-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60a72-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60a72-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a72-147">**\_Статистика мпресаурце**</span><span class="sxs-lookup"><span data-stu-id="60a72-147">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="60a72-148">**\_тип мпскан**</span><span class="sxs-lookup"><span data-stu-id="60a72-148">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="60a72-149">**мпсаурце**</span><span class="sxs-lookup"><span data-stu-id="60a72-149">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="60a72-150">**\_Статистика мпсреат**</span><span class="sxs-lookup"><span data-stu-id="60a72-150">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





