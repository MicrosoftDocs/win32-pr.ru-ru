---
title: Перечисление МПСАУРЦЕ (Мпклиент. h)
description: Возможная Категория источника.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- Перечисление МПСАУРЦЕ. устаревшие функции среды Windows
- Устаревшие компоненты среды Windows в указателе перечисления ПМПСАУРЦЕ
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9255029512499a0e2948a44701ef4482aff4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988921"
---
# <a name="mpsource-enumeration"></a><span data-ttu-id="e9b72-105">Перечисление МПСАУРЦЕ</span><span class="sxs-lookup"><span data-stu-id="e9b72-105">MPSOURCE enumeration</span></span>

<span data-ttu-id="e9b72-106">Возможная Категория источника.</span><span class="sxs-lookup"><span data-stu-id="e9b72-106">Possible category of source.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b72-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9b72-107">Syntax</span></span>


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a><span data-ttu-id="e9b72-108">Константы</span><span class="sxs-lookup"><span data-stu-id="e9b72-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e9b72-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**МПСАУРЦЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="e9b72-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-110">Источник неизвестен.</span><span class="sxs-lookup"><span data-stu-id="e9b72-110">Source unknown.</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**\_пользователь мпсаурце**</span><span class="sxs-lookup"><span data-stu-id="e9b72-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**MPSOURCE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-112">Инициировано пользователем.</span><span class="sxs-lookup"><span data-stu-id="e9b72-112">User initiated.</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**МПСАУРЦЕ \_ система**</span><span class="sxs-lookup"><span data-stu-id="e9b72-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**MPSOURCE\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-114">инициировано системой.</span><span class="sxs-lookup"><span data-stu-id="e9b72-114">system initiated.</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**МПСАУРЦЕ в \_ реальном времени**</span><span class="sxs-lookup"><span data-stu-id="e9b72-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE\_REALTIME**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-116">Запущен компонент реального времени.</span><span class="sxs-lookup"><span data-stu-id="e9b72-116">Realtime component initiated.</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**МПСАУРЦЕ \_ защиту ioav**</span><span class="sxs-lookup"><span data-stu-id="e9b72-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE\_IOAV**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-118">Загрузки IE и инициированные вложения Outlook Express.</span><span class="sxs-lookup"><span data-stu-id="e9b72-118">IE Downloads and Outlook Express Attachments initiated.</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**МПСАУРЦЕ \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="e9b72-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-120">Система проверки сети.</span><span class="sxs-lookup"><span data-stu-id="e9b72-120">Network inspection system.</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**\_объект BHO мпсаурце**</span><span class="sxs-lookup"><span data-stu-id="e9b72-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**MPSOURCE\_BHO**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-122">Объект BHO — веб-скрипт (не рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="e9b72-122">BHO - web script (deprecated).</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**МПСАУРЦЕ \_ иепротект**</span><span class="sxs-lookup"><span data-stu-id="e9b72-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE\_IEPROTECT**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-124">IE — Иекстенсионвалидатион.</span><span class="sxs-lookup"><span data-stu-id="e9b72-124">IE - IExtensionValidation.</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**МПСАУРЦЕ \_ ELAM**</span><span class="sxs-lookup"><span data-stu-id="e9b72-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE\_ELAM**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-126">ELAM</span><span class="sxs-lookup"><span data-stu-id="e9b72-126">ELAM</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**МПСАУРЦЕ \_ локальную \_ аттестацию**</span><span class="sxs-lookup"><span data-stu-id="e9b72-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**MPSOURCE\_LOCAL\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-128">Локальная аттестация.</span><span class="sxs-lookup"><span data-stu-id="e9b72-128">Local attestation.</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**МПСАУРЦЕ \_ Удаленная \_ аттестация**</span><span class="sxs-lookup"><span data-stu-id="e9b72-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**MPSOURCE\_REMOTE\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-130">Удаленная аттестация.</span><span class="sxs-lookup"><span data-stu-id="e9b72-130">Remote attestation.</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**МПСАУРЦЕ \_ AMSI**</span><span class="sxs-lookup"><span data-stu-id="e9b72-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE\_AMSI**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-132">AMSI</span><span class="sxs-lookup"><span data-stu-id="e9b72-132">AMSI</span></span>

</dd> <dt>

<span data-ttu-id="e9b72-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**Источник пакета управления \_ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="e9b72-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**MP\_SOURCE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="e9b72-134">Максимально возможное значение.</span><span class="sxs-lookup"><span data-stu-id="e9b72-134">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9b72-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e9b72-135">Requirements</span></span>



| <span data-ttu-id="e9b72-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e9b72-136">Requirement</span></span> | <span data-ttu-id="e9b72-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e9b72-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b72-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9b72-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e9b72-139">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e9b72-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e9b72-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9b72-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e9b72-141">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e9b72-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9b72-142">Header</span><span class="sxs-lookup"><span data-stu-id="e9b72-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9b72-143"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9b72-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





