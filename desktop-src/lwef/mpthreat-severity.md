---
title: Перечисление MPTHREAT_SEVERITY (Мпклиент. h)
description: Возможные угрозы угроз.
ms.assetid: 7C50AC74-16CB-4198-ABB2-D6999429F2EA
keywords:
- MPTHREAT_SEVERITY перечисления устаревшие функции среды Windows
- PMPTHREAT_SEVERITY указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPTHREAT_SEVERITY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eec7bff3b23a89ce8187798d8a69a9968cbc2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691818"
---
# <a name="mpthreat_severity-enumeration"></a><span data-ttu-id="1dfb8-105">\_Перечисление серьезности мпсреат</span><span class="sxs-lookup"><span data-stu-id="1dfb8-105">MPTHREAT\_SEVERITY enumeration</span></span>

<span data-ttu-id="1dfb8-106">Возможные угрозы угроз.</span><span class="sxs-lookup"><span data-stu-id="1dfb8-106">Possible threat severities.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dfb8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dfb8-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_SEVERITY { 
  MP_THREAT_SEVERITY_UNKNOWN   = 0,
  MP_THREAT_SEVERITY_LOW       = 1,
  MP_THREAT_SEVERITY_MODERATE  = 2,
  MP_THREAT_SEVERITY_HIGH      = 4,
  MP_THREAT_SEVERITY_SEVERE    = 5,
  MP_THREAT_SEVERITY_MAXVALUE  = 5
} MPTHREAT_SEVERITY, *PMPTHREAT_SEVERITY;
```



## <a name="constants"></a><span data-ttu-id="1dfb8-108">Константы</span><span class="sxs-lookup"><span data-stu-id="1dfb8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1dfb8-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**\_ \_ степень серьезности угрозы пакета управления \_ неизвестна**</span><span class="sxs-lookup"><span data-stu-id="1dfb8-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**MP\_THREAT\_SEVERITY\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1dfb8-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**\_ \_ низкий уровень серьезности угрозы пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="1dfb8-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**MP\_THREAT\_SEVERITY\_LOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1dfb8-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**\_серьезность угрозы пакета управления — \_ \_ умеренный**</span><span class="sxs-lookup"><span data-stu-id="1dfb8-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**MP\_THREAT\_SEVERITY\_MODERATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1dfb8-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**\_ \_ высокий уровень серьезности угрозы пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="1dfb8-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**MP\_THREAT\_SEVERITY\_HIGH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1dfb8-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**\_серьезность угрозы пакета управления — \_ \_ серьезная**</span><span class="sxs-lookup"><span data-stu-id="1dfb8-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**MP\_THREAT\_SEVERITY\_SEVERE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1dfb8-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**\_ \_ степень серьезности угрозы пакета управления \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="1dfb8-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**MP\_THREAT\_SEVERITY\_MAXVALUE**</span></span>
<span data-ttu-id="1dfb8-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1dfb8-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1dfb8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1dfb8-116">Requirements</span></span>



| <span data-ttu-id="1dfb8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1dfb8-117">Requirement</span></span> | <span data-ttu-id="1dfb8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1dfb8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfb8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1dfb8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfb8-120">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1dfb8-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1dfb8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1dfb8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfb8-122">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1dfb8-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1dfb8-123">Header</span><span class="sxs-lookup"><span data-stu-id="1dfb8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dfb8-124"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dfb8-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





