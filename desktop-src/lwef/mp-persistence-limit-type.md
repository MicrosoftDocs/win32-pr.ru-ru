---
title: Перечисление MP_PERSISTENCE_LIMIT_TYPE (Мпклиент. h)
description: Тип ограничения сохраняемости.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE перечисления устаревшие функции среды Windows
- PMP_PERSISTENCE_LIMIT_TYPE указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb52bc6ee630590ca189b88c1fdde5a30e17747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071936"
---
# <a name="mp_persistence_limit_type-enumeration"></a><span data-ttu-id="b45a1-105">\_ \_ Перечисление типов пределов СОХРАНЯЕМости MP \_</span><span class="sxs-lookup"><span data-stu-id="b45a1-105">MP\_PERSISTENCE\_LIMIT\_TYPE enumeration</span></span>

<span data-ttu-id="b45a1-106">Тип ограничения сохраняемости.</span><span class="sxs-lookup"><span data-stu-id="b45a1-106">Persistence limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b45a1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b45a1-107">Syntax</span></span>


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="b45a1-108">Константы</span><span class="sxs-lookup"><span data-stu-id="b45a1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b45a1-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**\_неизвестная сохраняемость пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="b45a1-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP\_PERSISTENCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="b45a1-110">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b45a1-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="b45a1-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**\_Сохранение пакета управления \_ без \_ ограничения**</span><span class="sxs-lookup"><span data-stu-id="b45a1-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP\_PERSISTENCE\_NO\_LIMIT**</span></span>
</dt> <dd>

<span data-ttu-id="b45a1-112">Без ограничений.</span><span class="sxs-lookup"><span data-stu-id="b45a1-112">No limit.</span></span>

</dd> <dt>

<span data-ttu-id="b45a1-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**\_Длительность сохраняемости пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="b45a1-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**MP\_PERSISTENCE\_DURATION**</span></span>
</dt> <dd>

<span data-ttu-id="b45a1-114">Длительность.</span><span class="sxs-lookup"><span data-stu-id="b45a1-114">Duration.</span></span>

</dd> <dt>

<span data-ttu-id="b45a1-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**\_версия VDM сохраняемости пакета управления \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b45a1-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP\_PERSISTENCE\_VDM\_VERSION**</span></span>
</dt> <dd>

<span data-ttu-id="b45a1-116">Версия VDM.</span><span class="sxs-lookup"><span data-stu-id="b45a1-116">VDM version.</span></span>

</dd> <dt>

<span data-ttu-id="b45a1-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**\_отметка времени сохраняемости MP \_**</span><span class="sxs-lookup"><span data-stu-id="b45a1-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP\_PERSISTENCE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="b45a1-118">Отметка времени.</span><span class="sxs-lookup"><span data-stu-id="b45a1-118">Timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="b45a1-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**\_Принудительное сохранение пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="b45a1-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**MP\_PERSISTENCE\_FORCED**</span></span>
</dt> <dd>

<span data-ttu-id="b45a1-120">Обязательна.</span><span class="sxs-lookup"><span data-stu-id="b45a1-120">Forced.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b45a1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b45a1-121">Requirements</span></span>



| <span data-ttu-id="b45a1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b45a1-122">Requirement</span></span> | <span data-ttu-id="b45a1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b45a1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b45a1-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b45a1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b45a1-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b45a1-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b45a1-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b45a1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b45a1-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b45a1-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b45a1-128">Header</span><span class="sxs-lookup"><span data-stu-id="b45a1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b45a1-129"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="b45a1-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





