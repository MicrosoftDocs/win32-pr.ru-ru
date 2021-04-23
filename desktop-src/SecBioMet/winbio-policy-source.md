---
title: Перечисление WINBIO_POLICY_SOURCE (Винбио \_ types. h)
description: Список возможных источников сведений о политике для обнаружения подмены для биометрических факторов.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- API биометрическая платформа Windows перечисления WINBIO_POLICY_SOURCE
- API биометрическая платформа Windows указателя перечисления PWINBIO_POLICY_SOURCE
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341265"
---
# <a name="winbio_policy_source-enumeration"></a><span data-ttu-id="1be22-105">\_ \_ Перечисление источников политики винбио</span><span class="sxs-lookup"><span data-stu-id="1be22-105">WINBIO\_POLICY\_SOURCE enumeration</span></span>

<span data-ttu-id="1be22-106">Список возможных источников сведений о политике для обнаружения подмены для биометрических факторов.</span><span class="sxs-lookup"><span data-stu-id="1be22-106">Lists the possible sources of policy information for the detection of spoofing for biometric factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1be22-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1be22-107">Syntax</span></span>


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a><span data-ttu-id="1be22-108">Константы</span><span class="sxs-lookup"><span data-stu-id="1be22-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1be22-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**\_неизвестная политика винбио \_**</span><span class="sxs-lookup"><span data-stu-id="1be22-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**WINBIO\_POLICY\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="1be22-110">Неизвестный источник политики.</span><span class="sxs-lookup"><span data-stu-id="1be22-110">The source of the policy is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="1be22-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_Политика винбио \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="1be22-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**WINBIO\_POLICY\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="1be22-112">Политика является политикой по умолчанию, которую предоставляет биометрическая платформа Windows.</span><span class="sxs-lookup"><span data-stu-id="1be22-112">The policy is the default policy that the Windows Biometric Framework provides.</span></span>

</dd> <dt>

<span data-ttu-id="1be22-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**\_ \_ Локальная политика винбио**</span><span class="sxs-lookup"><span data-stu-id="1be22-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO\_POLICY\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="1be22-114">Политика, которую отдельный пользователь задает для своей учетной записи с помощью приложения " **Параметры** ".</span><span class="sxs-lookup"><span data-stu-id="1be22-114">The policy that the individual user set for their account by using the **Settings** app.</span></span> <span data-ttu-id="1be22-115">Эта политика переопределяет политику по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1be22-115">This policy overrides the default policy.</span></span>

</dd> <dt>

<span data-ttu-id="1be22-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_Администратор политики \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="1be22-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**WINBIO\_POLICY\_ADMIN**</span></span>
</dt> <dd>

<span data-ttu-id="1be22-117">Групповая политика, заданная ИТ-администратором для предприятия.</span><span class="sxs-lookup"><span data-stu-id="1be22-117">A group policy that the IT administrator set for the enterprise.</span></span> <span data-ttu-id="1be22-118">Отдельные пользователи не могут переопределить эту политику.</span><span class="sxs-lookup"><span data-stu-id="1be22-118">Individual users cannot override this policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1be22-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1be22-119">Requirements</span></span>



| <span data-ttu-id="1be22-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1be22-120">Requirement</span></span> | <span data-ttu-id="1be22-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1be22-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1be22-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1be22-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1be22-123">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1be22-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="1be22-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1be22-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1be22-125">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="1be22-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="1be22-126">Header</span><span class="sxs-lookup"><span data-stu-id="1be22-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1be22-127"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="1be22-127"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1be22-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1be22-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be22-129">**\_ \_ \_ действие политики АНТИфишинга винбио \_**</span><span class="sxs-lookup"><span data-stu-id="1be22-129">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





