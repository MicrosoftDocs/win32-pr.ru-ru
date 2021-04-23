---
title: Перечисление MPDETECTION_STATE (Мпклиент. h)
description: Состояние обнаруженной в настоящее время угрозы.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE перечисления устаревшие функции среды Windows
- PMPDETECTION_STATE указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490005"
---
# <a name="mpdetection_state-enumeration"></a><span data-ttu-id="14450-105">\_Перечисление состояний мпдетектион</span><span class="sxs-lookup"><span data-stu-id="14450-105">MPDETECTION\_STATE enumeration</span></span>

<span data-ttu-id="14450-106">Состояние обнаруженной в настоящее время угрозы.</span><span class="sxs-lookup"><span data-stu-id="14450-106">The state of the currently detected threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="14450-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14450-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a><span data-ttu-id="14450-108">Константы</span><span class="sxs-lookup"><span data-stu-id="14450-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="14450-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**\_Неизвестное состояние мпдетектион \_**</span><span class="sxs-lookup"><span data-stu-id="14450-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**MPDETECTION\_STATE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="14450-110">В состоянии ошибки.</span><span class="sxs-lookup"><span data-stu-id="14450-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="14450-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**\_активное состояние \_ мпдетектион**</span><span class="sxs-lookup"><span data-stu-id="14450-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION\_STATE\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="14450-112">Активная угроза.</span><span class="sxs-lookup"><span data-stu-id="14450-112">Active threat.</span></span>

</dd> <dt>

<span data-ttu-id="14450-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**\_состояние мпдетектион \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="14450-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="14450-114">Перемещение в незавершенное время в течение 24 часов.</span><span class="sxs-lookup"><span data-stu-id="14450-114">Pending 24 hours to a move to cleared.</span></span>

</dd> <dt>

<span data-ttu-id="14450-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**\_ \_ Дополнительные действия для состояния мпдетектион \_**</span><span class="sxs-lookup"><span data-stu-id="14450-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**MPDETECTION\_STATE\_ADDITIONAL\_ACTIONS**</span></span>
</dt> <dd>

<span data-ttu-id="14450-116">Требуются дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="14450-116">Additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="14450-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**\_Сбой состояния \_ мпдетектион**</span><span class="sxs-lookup"><span data-stu-id="14450-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**MPDETECTION\_STATE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="14450-118">Некритическая ошибка исправления.</span><span class="sxs-lookup"><span data-stu-id="14450-118">Non-critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="14450-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**\_ \_ критический сбой состояния \_ мпдетектион**</span><span class="sxs-lookup"><span data-stu-id="14450-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION\_STATE\_CRITICALLY\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="14450-120">Критическая ошибка исправления.</span><span class="sxs-lookup"><span data-stu-id="14450-120">Critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="14450-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**МПДЕТЕКТИОН \_ состояние \_ очистки**</span><span class="sxs-lookup"><span data-stu-id="14450-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**MPDETECTION\_STATE\_CLEARED**</span></span>
</dt> <dd>

<span data-ttu-id="14450-122">Угроза не отображается в запросе состояния, только в журнале.</span><span class="sxs-lookup"><span data-stu-id="14450-122">Threat does not show up in the state query, only in history.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14450-123">Требования</span><span class="sxs-lookup"><span data-stu-id="14450-123">Requirements</span></span>



| <span data-ttu-id="14450-124">Требование</span><span class="sxs-lookup"><span data-stu-id="14450-124">Requirement</span></span> | <span data-ttu-id="14450-125">Значение</span><span class="sxs-lookup"><span data-stu-id="14450-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14450-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14450-126">Minimum supported client</span></span><br/> | <span data-ttu-id="14450-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="14450-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="14450-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14450-128">Minimum supported server</span></span><br/> | <span data-ttu-id="14450-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="14450-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14450-130">Header</span><span class="sxs-lookup"><span data-stu-id="14450-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="14450-131"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="14450-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





