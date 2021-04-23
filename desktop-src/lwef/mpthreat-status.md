---
title: Перечисление MPTHREAT_STATUS (Мпклиент. h)
description: Возможное состояние угрозы.
ms.assetid: 64B57C8B-231B-4A2C-BF2E-45DB62B8350E
keywords:
- MPTHREAT_STATUS перечисления устаревшие функции среды Windows
- PMPTHREAT_STATUS указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978a152d6f14d7b3577ece0a2e8bd5a8ba741a3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661870"
---
# <a name="mpthreat_status-enumeration"></a><span data-ttu-id="0cdcc-105">\_Перечисление состояния мпсреат</span><span class="sxs-lookup"><span data-stu-id="0cdcc-105">MPTHREAT\_STATUS enumeration</span></span>

<span data-ttu-id="0cdcc-106">Возможное состояние угрозы.</span><span class="sxs-lookup"><span data-stu-id="0cdcc-106">Possible threat status.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cdcc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cdcc-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_STATUS { 
  MP_THREAT_STATUS_UNKNOWN            = 0,
  MP_THREAT_STATUS_DETECTED           = 1,
  MP_THREAT_STATUS_CLEANED            = 2,
  MP_THREAT_STATUS_QUARANTINED        = 3,
  MP_THREAT_STATUS_REMOVED            = 4,
  MP_THREAT_STATUS_ALLOWED            = 5,
  MP_THREAT_STATUS_BLOCKED            = 6,
  MP_THREAT_STATUS_CLEAN_FAILED       = 102,
  MP_THREAT_STATUS_QUARANTINE_FAILED  = 103,
  MP_THREAT_STATUS_REMOVE_FAILED      = 104,
  MP_THREAT_STATUS_ALLOW_FAILED       = 105,
  MP_THREAT_STATUS_ABANDONED          = 106,
  MP_THREAT_STATUS_BLOCK_FAILED       = 107
} MPTHREAT_STATUS, *PMPTHREAT_STATUS;
```



## <a name="constants"></a><span data-ttu-id="0cdcc-108">Константы</span><span class="sxs-lookup"><span data-stu-id="0cdcc-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0cdcc-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**\_ \_ Неизвестное состояние угрозы пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP\_THREAT\_STATUS\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**\_ \_ обнаружено состояние угрозы пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**MP\_THREAT\_STATUS\_DETECTED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**\_ \_ Очистка состояния угрозы пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**MP\_THREAT\_STATUS\_CLEANED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**\_состояние угроз пакета управления \_ \_ помещено в карантин**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**MP\_THREAT\_STATUS\_QUARANTINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**\_состояние угрозы пакета управления \_ \_ удалено**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**MP\_THREAT\_STATUS\_REMOVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**\_состояние угрозы пакета управления \_ \_ разрешено**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**MP\_THREAT\_STATUS\_ALLOWED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**\_состояние угрозы пакета управления \_ \_ заблокировано**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**MP\_THREAT\_STATUS\_BLOCKED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**\_ \_ \_ сбой очистки состояния угрозы \_ пакета управления**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**MP\_THREAT\_STATUS\_CLEAN\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**\_ \_ \_ сбой карантина состояния угрозы пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**MP\_THREAT\_STATUS\_QUARANTINE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**\_ \_ \_ не удалось удалить состояние угрозы пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**MP\_THREAT\_STATUS\_REMOVE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**\_ \_ \_ не удалось разрешить состояние угрозы пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**MP\_THREAT\_STATUS\_ALLOW\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**\_состояние угрозы пакета управления \_ \_ прервано**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**MP\_THREAT\_STATUS\_ABANDONED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0cdcc-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**\_ \_ \_ сбой блока состояния угрозы \_ для пакета управления**</span><span class="sxs-lookup"><span data-stu-id="0cdcc-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**MP\_THREAT\_STATUS\_BLOCK\_FAILED**</span></span>
<span data-ttu-id="0cdcc-122"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0cdcc-122"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0cdcc-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0cdcc-123">Requirements</span></span>



| <span data-ttu-id="0cdcc-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0cdcc-124">Requirement</span></span> | <span data-ttu-id="0cdcc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0cdcc-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cdcc-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0cdcc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0cdcc-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0cdcc-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0cdcc-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0cdcc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0cdcc-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0cdcc-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cdcc-130">Header</span><span class="sxs-lookup"><span data-stu-id="0cdcc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cdcc-131"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cdcc-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





