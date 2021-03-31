---
title: Перечисление MPCOMPONENT_ID (Мпклиент. h)
description: Возможные компоненты для диспетчера защиты от вредоносных программ.
ms.assetid: 014B400A-880B-419D-9F50-F3354CE945D9
keywords:
- MPCOMPONENT_ID перечисления устаревшие функции среды Windows
- PMPCOMPONENT_ID указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_ID
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196eebc5a3bee4968878c376cd7358724c9c55cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135619"
---
# <a name="mpcomponent_id-enumeration"></a><span data-ttu-id="84b46-105">\_Перечисление идентификаторов мпкомпонент</span><span class="sxs-lookup"><span data-stu-id="84b46-105">MPCOMPONENT\_ID enumeration</span></span>

<span data-ttu-id="84b46-106">Возможные компоненты для диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="84b46-106">Possible components for the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="84b46-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84b46-107">Syntax</span></span>


```C++
typedef enum tagMPCOMPONENT_ID { 
  MPCOMPONENT_AS_SIGNATURE         = 0,
  MPCOMPONENT_AV_SIGNATURE         = 1,
  MPCOMPONENT_REALTIME_MONITOR     = 2,
  MPCOMPONENT_ONACCESS_PROTECTION  = 3,
  MPCOMPONENT_IOAV_PROTECTION      = 4,
  MPCOMPONENT_BEHAVIOR_MONITOR     = 5,
  MPCOMPONENT_AUTO_SCAN            = 6,
  MPCOMPONENT_AUTO_SIGUPDATE       = 7,
  MPCOMPONENT_IPC                  = 8,
  MPCOMPONENT_NIS                  = 9,
  MPCOMPONENT_ELAM                 = 10,
  MPCOMPONENT_MAXVALUE             = 10
} MPCOMPONENT_ID, *PMPCOMPONENT_ID;
```



## <a name="constants"></a><span data-ttu-id="84b46-108">Константы</span><span class="sxs-lookup"><span data-stu-id="84b46-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="84b46-109"><span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**МПКОМПОНЕНТ \_ как \_ подпись**</span><span class="sxs-lookup"><span data-stu-id="84b46-109"><span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**MPCOMPONENT\_AS\_SIGNATURE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-110"><span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**\_ \_ сигнатура мпкомпонент AV**</span><span class="sxs-lookup"><span data-stu-id="84b46-110"><span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**MPCOMPONENT\_AV\_SIGNATURE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-111"><span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**\_монитор мпкомпонент реального времени \_**</span><span class="sxs-lookup"><span data-stu-id="84b46-111"><span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**MPCOMPONENT\_REALTIME\_MONITOR**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-112"><span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**\_Защита мпкомпонент на \_ ЗАЩИЩЕНном доступе**</span><span class="sxs-lookup"><span data-stu-id="84b46-112"><span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**MPCOMPONENT\_ONACCESS\_PROTECTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-113"><span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**\_Защита мпкомпонент защиту ioav \_**</span><span class="sxs-lookup"><span data-stu-id="84b46-113"><span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**MPCOMPONENT\_IOAV\_PROTECTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-114"><span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**\_монитор поведения \_ мпкомпонент**</span><span class="sxs-lookup"><span data-stu-id="84b46-114"><span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**MPCOMPONENT\_BEHAVIOR\_MONITOR**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-115"><span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**\_Автоматическое \_ сканирование мпкомпонент**</span><span class="sxs-lookup"><span data-stu-id="84b46-115"><span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**MPCOMPONENT\_AUTO\_SCAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-116"><span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**МПКОМПОНЕНТ \_ Auto \_ сигупдате**</span><span class="sxs-lookup"><span data-stu-id="84b46-116"><span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**MPCOMPONENT\_AUTO\_SIGUPDATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-117"><span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**МПКОМПОНЕНТ \_ IPC**</span><span class="sxs-lookup"><span data-stu-id="84b46-117"><span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**MPCOMPONENT\_IPC**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-118"><span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**МПКОМПОНЕНТ \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="84b46-118"><span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**MPCOMPONENT\_NIS**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-119"><span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**МПКОМПОНЕНТ \_ ELAM**</span><span class="sxs-lookup"><span data-stu-id="84b46-119"><span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**MPCOMPONENT\_ELAM**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="84b46-120"><span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**МПКОМПОНЕНТ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="84b46-120"><span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**MPCOMPONENT\_MAXVALUE**</span></span>
<span data-ttu-id="84b46-121"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="84b46-121"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="84b46-122">Требования</span><span class="sxs-lookup"><span data-stu-id="84b46-122">Requirements</span></span>



| <span data-ttu-id="84b46-123">Требование</span><span class="sxs-lookup"><span data-stu-id="84b46-123">Requirement</span></span> | <span data-ttu-id="84b46-124">Значение</span><span class="sxs-lookup"><span data-stu-id="84b46-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84b46-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84b46-125">Minimum supported client</span></span><br/> | <span data-ttu-id="84b46-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="84b46-126">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="84b46-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84b46-127">Minimum supported server</span></span><br/> | <span data-ttu-id="84b46-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="84b46-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84b46-129">Header</span><span class="sxs-lookup"><span data-stu-id="84b46-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="84b46-130"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="84b46-130"><dt>MpClient.h</dt></span></span> </dl> |



 

 





