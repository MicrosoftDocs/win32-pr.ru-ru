---
title: Структура MPSTATUS_INFO (Мпклиент. h)
description: Сведения о состоянии для диспетчера защиты от вредоносных программ.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO структуры устаревшие функции среды Windows
- Функции PMPSTATUS_INFO указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801247"
---
# <a name="mpstatus_info-structure"></a><span data-ttu-id="fac41-105">\_Структура сведений о мпстатус</span><span class="sxs-lookup"><span data-stu-id="fac41-105">MPSTATUS\_INFO structure</span></span>

<span data-ttu-id="fac41-106">Сведения о состоянии для диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="fac41-106">Status information for the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac41-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fac41-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a><span data-ttu-id="fac41-108">Члены</span><span class="sxs-lookup"><span data-stu-id="fac41-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fac41-109">**продуктстатус**</span><span class="sxs-lookup"><span data-stu-id="fac41-109">**ProductStatus**</span></span>
</dt> <dd>

<span data-ttu-id="fac41-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="fac41-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="fac41-111">Общее состояние продукта.</span><span class="sxs-lookup"><span data-stu-id="fac41-111">Overall product status.</span></span> <span data-ttu-id="fac41-112">Это сочетание битовых флагов из [**\_ флага мпстатус**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="fac41-112">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac41-113">**ласткуиккскан**</span><span class="sxs-lookup"><span data-stu-id="fac41-113">**LastQuickScan**</span></span>
</dt> <dd>

<span data-ttu-id="fac41-114">Тип: **[ **мпскан \_ результат**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="fac41-114">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fac41-115">Результаты последней проверки с помощью диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="fac41-115">Results of the last scan by the malware protection manager.</span></span> <span data-ttu-id="fac41-116">См. [**мпскан \_ result**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="fac41-116">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac41-117">**ластфуллскан**</span><span class="sxs-lookup"><span data-stu-id="fac41-117">**LastFullScan**</span></span>
</dt> <dd>

<span data-ttu-id="fac41-118">Тип: **[ **мпскан \_ результат**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="fac41-118">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fac41-119">Результаты последней полной проверки с помощью диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="fac41-119">Results of the last full scan by the malware protection manager.</span></span> <span data-ttu-id="fac41-120">См. [**мпскан \_ result**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="fac41-120">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac41-121">**среатстатс**</span><span class="sxs-lookup"><span data-stu-id="fac41-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="fac41-122">Тип: **[ **мпсреат \_ stats**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="fac41-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fac41-123">Статистика активных угроз.</span><span class="sxs-lookup"><span data-stu-id="fac41-123">Active threat statistics.</span></span> <span data-ttu-id="fac41-124">См. [**мпсреат \_ stats**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="fac41-124">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac41-125">**среатстате**</span><span class="sxs-lookup"><span data-stu-id="fac41-125">**ThreatState**</span></span>
</dt> <dd>

<span data-ttu-id="fac41-126">Тип: **[**мпсреат \_ stats \_ Data**](mpthreat-stats-data.md) \[ MP \_ угроза \_ stat \_ Max \_ Value + 1\]**</span><span class="sxs-lookup"><span data-stu-id="fac41-126">Type: **[**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md)\[MP\_THREAT\_STAT\_MAX\_VALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="fac41-127">Дополнительные данные статистики угроз, например число угроз.</span><span class="sxs-lookup"><span data-stu-id="fac41-127">Additional threat statistics data, such as the number of threats.</span></span> <span data-ttu-id="fac41-128">См. [**мпсреат \_ stats \_ Data**](mpthreat-stats-data.md).</span><span class="sxs-lookup"><span data-stu-id="fac41-128">See [**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac41-129">**Компонент**</span><span class="sxs-lookup"><span data-stu-id="fac41-129">**Component**</span></span>
</dt> <dd>

<span data-ttu-id="fac41-130">Тип: **[**мпкомпонент \_ Status**](mpcomponent-status.md) \[ мпкомпонент \_ MaxValue + 1\]**</span><span class="sxs-lookup"><span data-stu-id="fac41-130">Type: **[**MPCOMPONENT\_STATUS**](mpcomponent-status.md)\[MPCOMPONENT\_MAXVALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="fac41-131">Массив состояний для нескольких компонентов.</span><span class="sxs-lookup"><span data-stu-id="fac41-131">An array of statuses for multiple components.</span></span> <span data-ttu-id="fac41-132">Используйте значение из перечисления [**мпкомпонент \_ ID**](mpcomponent-id.md) в качестве индекса в массиве.</span><span class="sxs-lookup"><span data-stu-id="fac41-132">Use a value from the [**MPCOMPONENT\_ID**](mpcomponent-id.md) enumeration as an index into the array.</span></span>

</dd> <dt>

<span data-ttu-id="fac41-133">**продуктекспиратионтиме**</span><span class="sxs-lookup"><span data-stu-id="fac41-133">**ProductExpirationTime**</span></span>
</dt> <dd>

<span data-ttu-id="fac41-134">Тип: **уларже \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="fac41-134">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="fac41-135">Метка времени истечения срока действия продукта в формате UNC.</span><span class="sxs-lookup"><span data-stu-id="fac41-135">Product expiration timestamp in UNC.</span></span> <span data-ttu-id="fac41-136">Это допустимо, только если задано состояние истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="fac41-136">This is valid only if the expiration status is set.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fac41-137">Требования</span><span class="sxs-lookup"><span data-stu-id="fac41-137">Requirements</span></span>



| <span data-ttu-id="fac41-138">Требование</span><span class="sxs-lookup"><span data-stu-id="fac41-138">Requirement</span></span> | <span data-ttu-id="fac41-139">Значение</span><span class="sxs-lookup"><span data-stu-id="fac41-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fac41-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fac41-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fac41-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fac41-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fac41-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fac41-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fac41-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fac41-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fac41-144">Header</span><span class="sxs-lookup"><span data-stu-id="fac41-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fac41-145"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="fac41-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac41-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fac41-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac41-147">**\_идентификатор мпкомпонент**</span><span class="sxs-lookup"><span data-stu-id="fac41-147">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="fac41-148">**\_состояние мпкомпонент**</span><span class="sxs-lookup"><span data-stu-id="fac41-148">**MPCOMPONENT\_STATUS**</span></span>](mpcomponent-status.md)
</dt> <dt>

[<span data-ttu-id="fac41-149">**МПСКАН \_ результат**</span><span class="sxs-lookup"><span data-stu-id="fac41-149">**MPSCAN\_RESULT**</span></span>](mpscan-result.md)
</dt> <dt>

[<span data-ttu-id="fac41-150">**\_флаг мпстатус**</span><span class="sxs-lookup"><span data-stu-id="fac41-150">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="fac41-151">**\_Статистика мпсреат**</span><span class="sxs-lookup"><span data-stu-id="fac41-151">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> <dt>

[<span data-ttu-id="fac41-152">**\_данные статистики \_ мпсреат**</span><span class="sxs-lookup"><span data-stu-id="fac41-152">**MPTHREAT\_STATS\_DATA**</span></span>](mpthreat-stats-data.md)
</dt> </dl>

 

 





