---
title: Перечисление MPCALLBACK_TYPE (Мпклиент. h)
description: Возможные типы обратного вызова.
ms.assetid: 8E4F50B7-0F02-434D-B91E-C9966C92CDC0
keywords:
- MPCALLBACK_TYPE перечисления устаревшие функции среды Windows
- PMPCALLBACK_TYPE указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPCALLBACK_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3fd310f3733d36dd92ace1c7a5286bcf73a75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490014"
---
# <a name="mpcallback_type-enumeration"></a><span data-ttu-id="7bf59-105">\_Перечисление типов мпкаллбакк</span><span class="sxs-lookup"><span data-stu-id="7bf59-105">MPCALLBACK\_TYPE enumeration</span></span>

<span data-ttu-id="7bf59-106">Возможные типы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7bf59-106">Possible callback types.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf59-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bf59-107">Syntax</span></span>


```C++
typedef enum tagMPCALLBACK_TYPE { 
  MPCALLBACK_UNKNOWN                     = 0,
  MPCALLBACK_STATUS                      = 1,
  MPCALLBACK_THREAT                      = 2,
  MPCALLBACK_SCAN                        = 3,
  MPCALLBACK_CLEAN                       = 4,
  MPCALLBACK_PRECHECK                    = 5,
  MPCALLBACK_SIGUPDATE                   = 6,
  MPCALLBACK_SAMPLE                      = 7,
  MPCALLBACK_RESERVED                    = 8,
  MPCALLBACK_CONFIGURATION_NOTIFICATION  = 9,
  MPCALLBACK_FASTPATH                    = 10,
  MPCALLBACK_PRODUCT_EXPIRATION          = 11,
  MPCALLBACK_NIS_PRIVATE                 = 12,
  MPCALLBACK_HEALTH                      = 13,
  MPCALLBACK_ENDOFLIFE                   = 14,
  MPCALLBACK_MALWARETOAST                = 15,
  MPCALLBACK_MAXVALUE                    = 15
} MPCALLBACK_TYPE, *PMPCALLBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="7bf59-108">Константы</span><span class="sxs-lookup"><span data-stu-id="7bf59-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7bf59-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**МПКАЛЛБАКК \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="7bf59-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**\_состояние мпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7bf59-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**MPCALLBACK\_STATUS**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**\_угроза мпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7bf59-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**MPCALLBACK\_THREAT**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**\_Проверка мпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7bf59-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**MPCALLBACK\_SCAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**МПКАЛЛБАКК \_ очистить**</span><span class="sxs-lookup"><span data-stu-id="7bf59-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**предпроверка МПКАЛЛБАКК \_**</span><span class="sxs-lookup"><span data-stu-id="7bf59-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**MPCALLBACK\_PRECHECK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**МПКАЛЛБАКК \_ сигупдате**</span><span class="sxs-lookup"><span data-stu-id="7bf59-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK\_SIGUPDATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**\_Пример мпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7bf59-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**MPCALLBACK\_SAMPLE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**МПКАЛЛБАКК \_ зарезервировано**</span><span class="sxs-lookup"><span data-stu-id="7bf59-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK\_RESERVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**\_ \_ уведомление о конфигурации мпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7bf59-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**MPCALLBACK\_CONFIGURATION\_NOTIFICATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**МПКАЛЛБАКК \_ фастпас**</span><span class="sxs-lookup"><span data-stu-id="7bf59-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK\_FASTPATH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**МПКАЛЛБАКК \_ \_ срок действия продукта**</span><span class="sxs-lookup"><span data-stu-id="7bf59-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**MPCALLBACK\_PRODUCT\_EXPIRATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**\_частный мпкаллбакк NIS \_**</span><span class="sxs-lookup"><span data-stu-id="7bf59-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK\_NIS\_PRIVATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**\_работоспособность мпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7bf59-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**MPCALLBACK\_HEALTH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**МПКАЛЛБАКК \_ ендофлифе**</span><span class="sxs-lookup"><span data-stu-id="7bf59-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK\_ENDOFLIFE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**МПКАЛЛБАКК \_ малваретоаст**</span><span class="sxs-lookup"><span data-stu-id="7bf59-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK\_MALWARETOAST**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bf59-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**МПКАЛЛБАКК \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="7bf59-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK\_MAXVALUE**</span></span>
<span data-ttu-id="7bf59-126"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7bf59-126"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7bf59-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7bf59-127">Requirements</span></span>



| <span data-ttu-id="7bf59-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7bf59-128">Requirement</span></span> | <span data-ttu-id="7bf59-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7bf59-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf59-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7bf59-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf59-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7bf59-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7bf59-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7bf59-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf59-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7bf59-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7bf59-134">Header</span><span class="sxs-lookup"><span data-stu-id="7bf59-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bf59-135"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bf59-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





