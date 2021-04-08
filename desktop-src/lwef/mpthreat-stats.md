---
title: Структура MPTHREAT_STATS (Мпклиент. h)
description: Статистика, связанная с угрозами.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS структуры устаревшие функции среды Windows
- Функции PMPTHREAT_STATS указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891853"
---
# <a name="mpthreat_stats-structure"></a><span data-ttu-id="fe4e1-105">\_Структура статистики мпсреат</span><span class="sxs-lookup"><span data-stu-id="fe4e1-105">MPTHREAT\_STATS structure</span></span>

<span data-ttu-id="fe4e1-106">Статистика, связанная с угрозами.</span><span class="sxs-lookup"><span data-stu-id="fe4e1-106">Threat-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4e1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe4e1-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a><span data-ttu-id="fe4e1-108">Члены</span><span class="sxs-lookup"><span data-stu-id="fe4e1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe4e1-109">**среаткаунт**</span><span class="sxs-lookup"><span data-stu-id="fe4e1-109">**ThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="fe4e1-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="fe4e1-110">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="fe4e1-111">Число обнаруженных угроз.</span><span class="sxs-lookup"><span data-stu-id="fe4e1-111">Number of threats detected.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e1-112">**суспиЦиауссреаткаунт**</span><span class="sxs-lookup"><span data-stu-id="fe4e1-112">**SuspiciousThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="fe4e1-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="fe4e1-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="fe4e1-114">Число обнаруженных угроз с мониторингом поведения.</span><span class="sxs-lookup"><span data-stu-id="fe4e1-114">Number of threats detected with behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="fe4e1-115">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="fe4e1-115">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="fe4e1-116">Тип: **uint \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="fe4e1-116">Type: **UINT\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="fe4e1-117">Поля, зарезервированные для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="fe4e1-117">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe4e1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fe4e1-118">Requirements</span></span>



| <span data-ttu-id="fe4e1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fe4e1-119">Requirement</span></span> | <span data-ttu-id="fe4e1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fe4e1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4e1-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe4e1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fe4e1-122">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fe4e1-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fe4e1-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe4e1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fe4e1-124">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fe4e1-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe4e1-125">Header</span><span class="sxs-lookup"><span data-stu-id="fe4e1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe4e1-126"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe4e1-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





