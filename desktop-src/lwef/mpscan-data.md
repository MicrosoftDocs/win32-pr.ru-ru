---
title: Структура MPSCAN_DATA (Мпклиент. h)
description: Просмотр данных, передаваемых в обратный вызов.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA структуры устаревшие функции среды Windows
- Функции PMPSCAN_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493059"
---
# <a name="mpscan_data-structure"></a><span data-ttu-id="97b11-105">\_Структура данных мпскан</span><span class="sxs-lookup"><span data-stu-id="97b11-105">MPSCAN\_DATA structure</span></span>

<span data-ttu-id="97b11-106">Просмотр данных, передаваемых в обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="97b11-106">Scan data passed to the callback.</span></span>

<span data-ttu-id="97b11-107">Эта структура содержит общую статистику угроз и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97b11-107">This structure contains cumulative threat and resource statistics.</span></span> <span data-ttu-id="97b11-108">Эти поля stat всегда являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="97b11-108">These stat fields are always valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="97b11-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97b11-109">Syntax</span></span>


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a><span data-ttu-id="97b11-110">Члены</span><span class="sxs-lookup"><span data-stu-id="97b11-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="97b11-111">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="97b11-111">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="97b11-112">Тип: **[ **мпскан \_ тип**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="97b11-112">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b11-113">Тип проверки.</span><span class="sxs-lookup"><span data-stu-id="97b11-113">Scan type.</span></span>

</dd> <dt>

<span data-ttu-id="97b11-114">**ресаурцеинфо**</span><span class="sxs-lookup"><span data-stu-id="97b11-114">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="97b11-115">Тип: **пмпресаурце \_ info** .</span><span class="sxs-lookup"><span data-stu-id="97b11-115">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="97b11-116">Информация о ресурсе.</span><span class="sxs-lookup"><span data-stu-id="97b11-116">Resource information.</span></span> <span data-ttu-id="97b11-117">См [**. \_ сведения о мпресаурце**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="97b11-117">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="97b11-118">**ресаурцестатс**</span><span class="sxs-lookup"><span data-stu-id="97b11-118">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="97b11-119">Тип: **[ **мпресаурце \_ stats**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="97b11-119">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b11-120">Накопительная статистика, связанная с ресурсами.</span><span class="sxs-lookup"><span data-stu-id="97b11-120">Resource-related cumulative statistics.</span></span>

</dd> <dt>

<span data-ttu-id="97b11-121">**среатстатс**</span><span class="sxs-lookup"><span data-stu-id="97b11-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="97b11-122">Тип: **[ **мпсреат \_ stats**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="97b11-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b11-123">Статистика угроз с успешным завершением сканирования.</span><span class="sxs-lookup"><span data-stu-id="97b11-123">Threat statistics with successful scan completions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97b11-124">Требования</span><span class="sxs-lookup"><span data-stu-id="97b11-124">Requirements</span></span>



| <span data-ttu-id="97b11-125">Требование</span><span class="sxs-lookup"><span data-stu-id="97b11-125">Requirement</span></span> | <span data-ttu-id="97b11-126">Значение</span><span class="sxs-lookup"><span data-stu-id="97b11-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97b11-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97b11-127">Minimum supported client</span></span><br/> | <span data-ttu-id="97b11-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="97b11-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="97b11-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97b11-129">Minimum supported server</span></span><br/> | <span data-ttu-id="97b11-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="97b11-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97b11-131">Header</span><span class="sxs-lookup"><span data-stu-id="97b11-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="97b11-132"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="97b11-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97b11-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97b11-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b11-134">**\_сведения о мпресаурце**</span><span class="sxs-lookup"><span data-stu-id="97b11-134">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="97b11-135">**\_Статистика мпресаурце**</span><span class="sxs-lookup"><span data-stu-id="97b11-135">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="97b11-136">**\_тип мпскан**</span><span class="sxs-lookup"><span data-stu-id="97b11-136">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="97b11-137">**\_Статистика мпсреат**</span><span class="sxs-lookup"><span data-stu-id="97b11-137">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





