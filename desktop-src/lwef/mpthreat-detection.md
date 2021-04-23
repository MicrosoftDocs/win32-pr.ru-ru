---
title: Перечисление MPTHREAT_DETECTION (Мпклиент. h)
description: Возможные известные неправильные типы обнаружения угроз.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION перечисления устаревшие функции среды Windows
- PMPTHREAT_DETECTION указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801906"
---
# <a name="mpthreat_detection-enumeration"></a><span data-ttu-id="0a857-105">\_Перечисление мпсреат обнаружения</span><span class="sxs-lookup"><span data-stu-id="0a857-105">MPTHREAT\_DETECTION enumeration</span></span>

<span data-ttu-id="0a857-106">Возможные известные неправильные типы обнаружения угроз.</span><span class="sxs-lookup"><span data-stu-id="0a857-106">Possible known bad threat detection types.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a857-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a857-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a><span data-ttu-id="0a857-108">Константы</span><span class="sxs-lookup"><span data-stu-id="0a857-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0a857-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**\_ \_ конкретное обнаружение угроз MP \_**</span><span class="sxs-lookup"><span data-stu-id="0a857-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP\_THREAT\_DETECTION\_CONCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="0a857-110">Обнаружена угроза через конкретные подписи.</span><span class="sxs-lookup"><span data-stu-id="0a857-110">Threat was detected via concrete signatures.</span></span>

</dd> <dt>

<span data-ttu-id="0a857-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_ \_ эвристика обнаружения угроз MP \_**</span><span class="sxs-lookup"><span data-stu-id="0a857-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP\_THREAT\_DETECTION\_HEURISTIC**</span></span>
</dt> <dd>

<span data-ttu-id="0a857-112">Обнаружена угроза с помощью эвристического алгоритма.</span><span class="sxs-lookup"><span data-stu-id="0a857-112">Threat was detected via heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="0a857-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**\_ \_ универсальное обнаружение угроз MP \_**</span><span class="sxs-lookup"><span data-stu-id="0a857-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP\_THREAT\_DETECTION\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="0a857-114">Обнаружена угроза через универсальные подписи.</span><span class="sxs-lookup"><span data-stu-id="0a857-114">Threat was detected via generic signatures.</span></span>

</dd> <dt>

<span data-ttu-id="0a857-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**\_обнаружение угроз с точки управления \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a857-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP\_THREAT\_DETECTION\_SUSPICIOUS**</span></span>
</dt> <dd>

<span data-ttu-id="0a857-116">Обнаружена угроза с помощью функции мониторинга поведения.</span><span class="sxs-lookup"><span data-stu-id="0a857-116">Threat was detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="0a857-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**\_ \_ фастпас обнаружения угроз \_ MP**</span><span class="sxs-lookup"><span data-stu-id="0a857-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP\_THREAT\_DETECTION\_FASTPATH**</span></span>
</dt> <dd>

<span data-ttu-id="0a857-118">Обнаружена угроза через фастпас.</span><span class="sxs-lookup"><span data-stu-id="0a857-118">Threat was detected via fastpath.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a857-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0a857-119">Requirements</span></span>



| <span data-ttu-id="0a857-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0a857-120">Requirement</span></span> | <span data-ttu-id="0a857-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0a857-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a857-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a857-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0a857-123">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0a857-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0a857-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a857-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0a857-125">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0a857-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a857-126">Header</span><span class="sxs-lookup"><span data-stu-id="0a857-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a857-127"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a857-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





