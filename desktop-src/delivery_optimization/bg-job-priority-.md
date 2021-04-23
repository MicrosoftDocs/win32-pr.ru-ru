---
title: Перечисление BG_JOB_PRIORITY (Deliveryoptimization. h)
description: Перечисление BG_JOB_PRIORITY определяет постоянные значения, указывающие уровень приоритета задания.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- Перечисление BG_JOB_PRIORITY
- Перечисление BG_JOB_PRIORITY
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071489"
---
# <a name="bg_job_priority-enumeration"></a><span data-ttu-id="115c2-105">Перечисление BG_JOB_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="115c2-105">BG_JOB_PRIORITY enumeration</span></span>

<span data-ttu-id="115c2-106">Перечисление **BG_JOB_PRIORITY** определяет постоянные значения, указывающие уровень приоритета задания.</span><span class="sxs-lookup"><span data-stu-id="115c2-106">The **BG_JOB_PRIORITY** enumeration defines the constant values that specify the priority level of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="115c2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="115c2-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a><span data-ttu-id="115c2-108">Константы</span><span class="sxs-lookup"><span data-stu-id="115c2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="115c2-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span><span class="sxs-lookup"><span data-stu-id="115c2-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span></span>
</dt> <dd>

<span data-ttu-id="115c2-110">Передает задание на передний план.</span><span class="sxs-lookup"><span data-stu-id="115c2-110">Transfers the job in the foreground.</span></span> <span data-ttu-id="115c2-111">Переносы переднего плана приводят к пропускной способности сети с другими приложениями, что может помешать работе пользователя в сети.</span><span class="sxs-lookup"><span data-stu-id="115c2-111">Foreground transfers compete for network bandwidth with other applications, which can impede the user's network experience.</span></span> <span data-ttu-id="115c2-112">Это уровень наивысшего приоритета.</span><span class="sxs-lookup"><span data-stu-id="115c2-112">This is the highest priority level.</span></span>

</dd> <dt>

<span data-ttu-id="115c2-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span><span class="sxs-lookup"><span data-stu-id="115c2-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="115c2-114">Передает задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="115c2-114">Transfers the job in the background.</span></span> <span data-ttu-id="115c2-115">Фоновая передача использует небольшой процент пропускной способности сети.</span><span class="sxs-lookup"><span data-stu-id="115c2-115">Background transfers use a small percentage of network bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="115c2-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span><span class="sxs-lookup"><span data-stu-id="115c2-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="115c2-117">Поведение выполняется для всех заданий, не являющихся основными.</span><span class="sxs-lookup"><span data-stu-id="115c2-117">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="115c2-118">Дополнительные сведения см. в комментариях в BG_JOB_PRIORITY_HIGH.</span><span class="sxs-lookup"><span data-stu-id="115c2-118">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> <dt>

<span data-ttu-id="115c2-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span><span class="sxs-lookup"><span data-stu-id="115c2-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="115c2-120">Поведение выполняется для всех заданий, не являющихся основными.</span><span class="sxs-lookup"><span data-stu-id="115c2-120">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="115c2-121">Дополнительные сведения см. в комментариях в BG_JOB_PRIORITY_HIGH.</span><span class="sxs-lookup"><span data-stu-id="115c2-121">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="115c2-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="115c2-122">Remarks</span></span>

<span data-ttu-id="115c2-123">Несколько переносов переднего плана и фоновых передач могут выполняться одновременно.</span><span class="sxs-lookup"><span data-stu-id="115c2-123">Multiple foreground and background transfers can take place simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="115c2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="115c2-124">Requirements</span></span>



| <span data-ttu-id="115c2-125">Требование</span><span class="sxs-lookup"><span data-stu-id="115c2-125">Requirement</span></span> | <span data-ttu-id="115c2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="115c2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="115c2-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="115c2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="115c2-128">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="115c2-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="115c2-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="115c2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="115c2-130">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="115c2-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="115c2-131">Header</span><span class="sxs-lookup"><span data-stu-id="115c2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="115c2-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="115c2-132"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="115c2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="115c2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="115c2-134">**Использованием метода ibackgroundcopyjob:: предшествовал**</span><span class="sxs-lookup"><span data-stu-id="115c2-134">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[<span data-ttu-id="115c2-135">**Использованием метода ibackgroundcopyjob:: SetPriority**</span><span class="sxs-lookup"><span data-stu-id="115c2-135">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





