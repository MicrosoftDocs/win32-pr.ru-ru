---
title: Структура WINBIO_ANTI_SPOOF_POLICY (Винбио \_ types. h)
description: Представляет политику антиподмены для пользователя.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- API структуры WINBIO_ANTI_SPOOF_POLICY биометрическая платформа Windows
- PWINBIO_ANTI_SPOOF_POLICY API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491391"
---
# <a name="winbio_anti_spoof_policy-structure"></a><span data-ttu-id="6891d-105">\_ \_ Структура политики антифишинга винбио \_</span><span class="sxs-lookup"><span data-stu-id="6891d-105">WINBIO\_ANTI\_SPOOF\_POLICY structure</span></span>

<span data-ttu-id="6891d-106">Представляет политику антиподмены для пользователя.</span><span class="sxs-lookup"><span data-stu-id="6891d-106">Represents the antispoofing policy for a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="6891d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6891d-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a><span data-ttu-id="6891d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6891d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6891d-109">**Действие**</span><span class="sxs-lookup"><span data-stu-id="6891d-109">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="6891d-110">Тип действия, выполняемого для политики антиподмены.</span><span class="sxs-lookup"><span data-stu-id="6891d-110">The type of action to take for the antispoofing policy.</span></span>

</dd> <dt>

<span data-ttu-id="6891d-111">**Источник**</span><span class="sxs-lookup"><span data-stu-id="6891d-111">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="6891d-112">Источник политики антиподмены.</span><span class="sxs-lookup"><span data-stu-id="6891d-112">The source for the antispoofing policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6891d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6891d-113">Requirements</span></span>



| <span data-ttu-id="6891d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6891d-114">Requirement</span></span> | <span data-ttu-id="6891d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6891d-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6891d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6891d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6891d-117">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6891d-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="6891d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6891d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6891d-119">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="6891d-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="6891d-120">Header</span><span class="sxs-lookup"><span data-stu-id="6891d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6891d-121"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="6891d-121"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6891d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6891d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6891d-123">**\_ \_ \_ действие политики АНТИфишинга винбио \_**</span><span class="sxs-lookup"><span data-stu-id="6891d-123">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="6891d-124">**\_источник политики \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="6891d-124">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> <dt>

[<span data-ttu-id="6891d-125">**\_асинхронный \_ результат винбио**</span><span class="sxs-lookup"><span data-stu-id="6891d-125">**WINBIO\_ASYNC\_RESULT**</span></span>](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[<span data-ttu-id="6891d-126">**винбиожетпроперти**</span><span class="sxs-lookup"><span data-stu-id="6891d-126">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[<span data-ttu-id="6891d-127">**винбиосетпроперти**</span><span class="sxs-lookup"><span data-stu-id="6891d-127">**WinBioSetProperty**</span></span>](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





