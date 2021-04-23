---
title: Перечисление BITS_JOB_TRANSFER_POLICY (Deliveryoptimization. h)
description: Перечисление BITS_JOB_TRANSFER_POLICY определяет значения ИДЕНТИФИКАТОРов, соответствующие свойствам DO.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- Перечисление BITS_JOB_TRANSFER_POLICY
- Перечисление BITS_JOB_TRANSFER_POLICY
topic_type:
- apiref
api_name:
- BITS_JOB_TRANSFER_POLICY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 455752375b76e574923ccdd96d1d05fc9142c16c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135478"
---
# <a name="bits_job_transfer_policy-enumeration"></a><span data-ttu-id="da001-105">Перечисление BITS_JOB_TRANSFER_POLICY</span><span class="sxs-lookup"><span data-stu-id="da001-105">BITS_JOB_TRANSFER_POLICY enumeration</span></span>

<span data-ttu-id="da001-106">Перечисление **BITS_JOB_TRANSFER_POLICY** определяет значения идентификаторов, соответствующие свойствам Do.</span><span class="sxs-lookup"><span data-stu-id="da001-106">The **BITS_JOB_TRANSFER_POLICY** enumeration defines ID values corresponding to DO properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="da001-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da001-107">Syntax</span></span>


```C++
typedef enum _BITS_JOB_TRANSFER_POLICY { 
  BITS_JOB_TRANSFER_POLICY_ALWAYS        = 0x800000ff,
  BITS_JOB_TRANSFER_POLICY_NOT_ROAMING   = 0x8000007f,
  BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE  = 0x8000006f,
  BITS_JOB_TRANSFER_POLICY_STANDARD      = 0x80000067,
  BITS_JOB_TRANSFER_POLICY_UNRESTRICTED  = 0x80000021
} BITS_JOB_TRANSFER_POLICY;
```



## <a name="constants"></a><span data-ttu-id="da001-108">Константы</span><span class="sxs-lookup"><span data-stu-id="da001-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="da001-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span><span class="sxs-lookup"><span data-stu-id="da001-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="da001-110">Указывает, что задание будет передано при наличии подключения, независимо от стоимости.</span><span class="sxs-lookup"><span data-stu-id="da001-110">Specifies that the job will be transferred when connectivity is available, regardless of the cost.</span></span>

</dd> <dt>

<span data-ttu-id="da001-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span><span class="sxs-lookup"><span data-stu-id="da001-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span></span>
</dt> <dd>

<span data-ttu-id="da001-112">Указывает, что задание будет передано при наличии подключения, если это подключение не подлежит доплатам роуминга.</span><span class="sxs-lookup"><span data-stu-id="da001-112">Specifies that the job will be transferred when connectivity is available, unless that connectivity is subject to roaming surcharges.</span></span>

</dd> <dt>

<span data-ttu-id="da001-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span><span class="sxs-lookup"><span data-stu-id="da001-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span></span>
</dt> <dd>

<span data-ttu-id="da001-114">Указывает, что задание будет передано только при наличии подключения, которое не подлежит оплате.</span><span class="sxs-lookup"><span data-stu-id="da001-114">Specifies that the job will be transferred only when connectivity is available which is not subject to a surcharge.</span></span>

</dd> <dt>

<span data-ttu-id="da001-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span><span class="sxs-lookup"><span data-stu-id="da001-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="da001-116">Указывает, что задание будет передано только при наличии подключения, которое не подлежит оплате или приближается к исчерпанию.</span><span class="sxs-lookup"><span data-stu-id="da001-116">Specifies that the job will be transferred only when connectivity is available which is neither subject to a surcharge nor near exhaustion.</span></span>

</dd> <dt>

<span data-ttu-id="da001-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span><span class="sxs-lookup"><span data-stu-id="da001-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span></span>
</dt> <dd>

<span data-ttu-id="da001-118">Указывает, что задание будет передано только при наличии подключения, которое не накладывает затраты или лимиты трафика.</span><span class="sxs-lookup"><span data-stu-id="da001-118">Specifies that the job will be transferred only when connectivity is available which does not impose costs or traffic limits.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da001-119">Требования</span><span class="sxs-lookup"><span data-stu-id="da001-119">Requirements</span></span>



| <span data-ttu-id="da001-120">Требование</span><span class="sxs-lookup"><span data-stu-id="da001-120">Requirement</span></span> | <span data-ttu-id="da001-121">Значение</span><span class="sxs-lookup"><span data-stu-id="da001-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da001-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da001-122">Minimum supported client</span></span><br/> | <span data-ttu-id="da001-123">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="da001-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="da001-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da001-124">Minimum supported server</span></span><br/> | <span data-ttu-id="da001-125">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="da001-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="da001-126">Header</span><span class="sxs-lookup"><span data-stu-id="da001-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="da001-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="da001-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





