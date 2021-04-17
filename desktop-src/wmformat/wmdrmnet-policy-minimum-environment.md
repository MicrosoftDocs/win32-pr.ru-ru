---
title: Структура WMDRMNET_POLICY_MINIMUM_ENVIRONMENT (Вмдрмсдк. h)
description: '\_ \_ Структура минимальной среды политики вмдрмнет \_ содержит минимальные требования к безопасности для Windows Media DRM для сетевых устройств.'
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- Формат WMDRMNET_POLICY_MINIMUM_ENVIRONMENT структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698840"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a><span data-ttu-id="84d98-105">\_ \_ Минимальная \_ Структура среды политики вмдрмнет</span><span class="sxs-lookup"><span data-stu-id="84d98-105">WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT structure</span></span>

<span data-ttu-id="84d98-106">Структура **\_ \_ минимальной \_ среды политики вмдрмнет** содержит минимальные требования к безопасности для Windows Media DRM для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="84d98-106">The **WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT** structure contains the minimum security requirements for Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="84d98-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84d98-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a><span data-ttu-id="84d98-108">Члены</span><span class="sxs-lookup"><span data-stu-id="84d98-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="84d98-109">**вминимумсекуритилевел**</span><span class="sxs-lookup"><span data-stu-id="84d98-109">**wMinimumSecurityLevel**</span></span>
</dt> <dd>

<span data-ttu-id="84d98-110">Требуется минимальный уровень безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="84d98-110">Minimum application security level required.</span></span>

</dd> <dt>

<span data-ttu-id="84d98-111">**двминимумаппревокатионлистверсион**</span><span class="sxs-lookup"><span data-stu-id="84d98-111">**dwMinimumAppRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="84d98-112">Требуется версия минимального списка отзыва сертификатов приложений.</span><span class="sxs-lookup"><span data-stu-id="84d98-112">Minimum application certificate revocation list version required.</span></span>

</dd> <dt>

<span data-ttu-id="84d98-113">**двминимумдевицеревокатионлистверсион**</span><span class="sxs-lookup"><span data-stu-id="84d98-113">**dwMinimumDeviceRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="84d98-114">Требуется минимальный список отзыва сертификатов устройства.</span><span class="sxs-lookup"><span data-stu-id="84d98-114">Minimum device certificate revocation list required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84d98-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84d98-115">Remarks</span></span>

<span data-ttu-id="84d98-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="84d98-116">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="84d98-117">Требования</span><span class="sxs-lookup"><span data-stu-id="84d98-117">Requirements</span></span>



| <span data-ttu-id="84d98-118">Требование</span><span class="sxs-lookup"><span data-stu-id="84d98-118">Requirement</span></span> | <span data-ttu-id="84d98-119">Значение</span><span class="sxs-lookup"><span data-stu-id="84d98-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84d98-120">Header</span><span class="sxs-lookup"><span data-stu-id="84d98-120">Header</span></span><br/> | <dl> <span data-ttu-id="84d98-121"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="84d98-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84d98-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84d98-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84d98-123">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="84d98-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="84d98-124">**\_Политика вмдрмнет**</span><span class="sxs-lookup"><span data-stu-id="84d98-124">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





