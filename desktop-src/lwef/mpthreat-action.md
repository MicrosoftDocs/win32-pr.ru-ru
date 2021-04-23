---
title: Перечисление MPTHREAT_ACTION (Мпклиент. h)
description: Возможные действия по угрозе.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- MPTHREAT_ACTION перечисления устаревшие функции среды Windows
- PMPTHREAT_ACTION указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0377517af590072b797a57c051ad062842ea9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135795"
---
# <a name="mpthreat_action-enumeration"></a><span data-ttu-id="88313-105">\_Перечисление действий мпсреат</span><span class="sxs-lookup"><span data-stu-id="88313-105">MPTHREAT\_ACTION enumeration</span></span>

<span data-ttu-id="88313-106">Возможные действия по угрозе.</span><span class="sxs-lookup"><span data-stu-id="88313-106">Possible threat actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="88313-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88313-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a><span data-ttu-id="88313-108">Константы</span><span class="sxs-lookup"><span data-stu-id="88313-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="88313-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**\_действие управления угрозами \_ \_ неизвестно**</span><span class="sxs-lookup"><span data-stu-id="88313-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**MP\_THREAT\_ACTION\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="88313-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**\_ \_ Очистка действия угрозы пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="88313-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**MP\_THREAT\_ACTION\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="88313-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**\_ \_ Карантин действий пакета \_ управления**</span><span class="sxs-lookup"><span data-stu-id="88313-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**MP\_THREAT\_ACTION\_QUARANTINE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="88313-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**\_ \_ действие удаления угроз \_ пакета управления**</span><span class="sxs-lookup"><span data-stu-id="88313-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP\_THREAT\_ACTION\_REMOVE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="88313-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**\_действие для \_ действия \_ угроз пакета управления**</span><span class="sxs-lookup"><span data-stu-id="88313-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**MP\_THREAT\_ACTION\_ALLOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="88313-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**\_ \_ пользователяопределенные действия для пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="88313-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**MP\_THREAT\_ACTION\_USERDEFINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="88313-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**действие при действии угрозы пакета управления — \_ \_ \_ действие**</span><span class="sxs-lookup"><span data-stu-id="88313-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP\_THREAT\_ACTION\_NOACTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="88313-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**\_ \_ блок действий угроз для пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="88313-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP\_THREAT\_ACTION\_BLOCK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="88313-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**\_ \_ \_ Максимальное \_ значение действия угрозы пакета управления**</span><span class="sxs-lookup"><span data-stu-id="88313-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**MP\_THREAT\_ACTION\_MAX\_VALUE**</span></span>
<span data-ttu-id="88313-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="88313-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="88313-119">Требования</span><span class="sxs-lookup"><span data-stu-id="88313-119">Requirements</span></span>



| <span data-ttu-id="88313-120">Требование</span><span class="sxs-lookup"><span data-stu-id="88313-120">Requirement</span></span> | <span data-ttu-id="88313-121">Значение</span><span class="sxs-lookup"><span data-stu-id="88313-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88313-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88313-122">Minimum supported client</span></span><br/> | <span data-ttu-id="88313-123">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="88313-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="88313-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88313-124">Minimum supported server</span></span><br/> | <span data-ttu-id="88313-125">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="88313-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88313-126">Header</span><span class="sxs-lookup"><span data-stu-id="88313-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="88313-127"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="88313-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





