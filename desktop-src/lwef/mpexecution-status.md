---
title: Перечисление MPEXECUTION_STATUS (Мпклиент. h)
description: Возможное состояние выполнения угрозы.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS перечисления устаревшие функции среды Windows
- PMPEXECUTION_STATUS указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891721"
---
# <a name="mpexecution_status-enumeration"></a><span data-ttu-id="52b4f-105">\_Перечисление состояния мпексекутион</span><span class="sxs-lookup"><span data-stu-id="52b4f-105">MPEXECUTION\_STATUS enumeration</span></span>

<span data-ttu-id="52b4f-106">Возможное состояние выполнения угрозы.</span><span class="sxs-lookup"><span data-stu-id="52b4f-106">Possible threat execution status.</span></span>

## <a name="syntax"></a><span data-ttu-id="52b4f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52b4f-107">Syntax</span></span>


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a><span data-ttu-id="52b4f-108">Константы</span><span class="sxs-lookup"><span data-stu-id="52b4f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="52b4f-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**\_состояние выполнения пакета управления \_ \_ неизвестно**</span><span class="sxs-lookup"><span data-stu-id="52b4f-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**MP\_EXECUTION\_STATUS\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="52b4f-110">Состояние выполнения неизвестно.</span><span class="sxs-lookup"><span data-stu-id="52b4f-110">Execution status is not known.</span></span>

</dd> <dt>

<span data-ttu-id="52b4f-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**\_состояние выполнения пакета управления \_ \_ заблокировано**</span><span class="sxs-lookup"><span data-stu-id="52b4f-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**MP\_EXECUTION\_STATUS\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="52b4f-112">Заблокировано выполнение с помощью мини-фильтра.</span><span class="sxs-lookup"><span data-stu-id="52b4f-112">Blocked from execution by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="52b4f-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**\_ \_ разрешено состояние выполнения пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="52b4f-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**MP\_EXECUTION\_STATUS\_ALLOWED**</span></span>
</dt> <dd>

<span data-ttu-id="52b4f-114">Разрешено выполнять с помощью мини-фильтра.</span><span class="sxs-lookup"><span data-stu-id="52b4f-114">Allowed to execute by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="52b4f-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**\_ \_ выполнение состояния выполнения пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="52b4f-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**MP\_EXECUTION\_STATUS\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="52b4f-116">Идет запуск угрозы.</span><span class="sxs-lookup"><span data-stu-id="52b4f-116">Threat is executing.</span></span>

</dd> <dt>

<span data-ttu-id="52b4f-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**\_состояние выполнения пакета управления \_ \_ не \_ выполняется**</span><span class="sxs-lookup"><span data-stu-id="52b4f-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**MP\_EXECUTION\_STATUS\_NOT\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="52b4f-118">Угроза не исполняется и доступна только из подсистемы во время исправления.</span><span class="sxs-lookup"><span data-stu-id="52b4f-118">Threat is not executing, and is only available from the engine during remediation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52b4f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="52b4f-119">Requirements</span></span>



| <span data-ttu-id="52b4f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="52b4f-120">Requirement</span></span> | <span data-ttu-id="52b4f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="52b4f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52b4f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52b4f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="52b4f-123">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="52b4f-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="52b4f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52b4f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="52b4f-125">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="52b4f-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52b4f-126">Header</span><span class="sxs-lookup"><span data-stu-id="52b4f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="52b4f-127"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="52b4f-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





