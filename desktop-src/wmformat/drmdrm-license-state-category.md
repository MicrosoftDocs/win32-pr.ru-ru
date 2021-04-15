---
title: Перечисление DRM_LICENSE_STATE_CATEGORY (Вмдрмсдк. h)
description: '\_ \_ \_ Тип перечисления Категория состояния лицензии DRM определяет тип ограничения лицензии, описываемого \_ \_ \_ структурой данных состояния лицензии DRM.'
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- Формат Windows Media DRM_LICENSE_STATE_CATEGORY перечисления
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e928a95a71d9636f88bc3c79ac36168072527040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689156"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a><span data-ttu-id="3be7e-104">Перечисление DRM_LICENSE_STATE_CATEGORY (Вмдрмсдк. h)</span><span class="sxs-lookup"><span data-stu-id="3be7e-104">DRM_LICENSE_STATE_CATEGORY enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="3be7e-105">Тип **перечисления \_ \_ \_ Категория состояния лицензии DRM** определяет тип ограничения лицензии, описываемого структурой [**\_ \_ \_ данных состояния лицензии DRM**](drmdrm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="3be7e-105">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be7e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3be7e-106">Syntax</span></span>


```C++
typedef enum DRM_LICENSE_STATE_CATEGORY { 
  WM_DRM_LICENSE_STATE_NORIGHT                    = 0,
  WM_DRM_LICENSE_STATE_UNLIM,
  WM_DRM_LICENSE_STATE_COUNT,
  WM_DRM_LICENSE_STATE_FROM,
  WM_DRM_LICENSE_STATE_UNTIL,
  WM_DRM_LICENSE_STATE_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM,
  WM_DRM_LICENSE_STATE_COUNT_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE
} DRM_LICENSE_STATE_CATEGORY;
```



## <a name="constants"></a><span data-ttu-id="3be7e-107">Константы</span><span class="sxs-lookup"><span data-stu-id="3be7e-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3be7e-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**\_ \_ \_ неправильное состояние \_ лицензии WM DRM**</span><span class="sxs-lookup"><span data-stu-id="3be7e-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="3be7e-109">Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , запрещено.</span><span class="sxs-lookup"><span data-stu-id="3be7e-109">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="3be7e-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_ \_ \_ УНЛИМ состояния лицензии WM \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="3be7e-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="3be7e-111">Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено без ограничений.</span><span class="sxs-lookup"><span data-stu-id="3be7e-111">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="3be7e-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="3be7e-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="3be7e-113">Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено, но только заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="3be7e-113">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times.</span></span>

</dd> <dt>

<span data-ttu-id="3be7e-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ из**</span><span class="sxs-lookup"><span data-stu-id="3be7e-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="3be7e-115">Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено после даты установки.</span><span class="sxs-lookup"><span data-stu-id="3be7e-115">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="3be7e-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ до**</span><span class="sxs-lookup"><span data-stu-id="3be7e-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="3be7e-117">Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено до даты установки.</span><span class="sxs-lookup"><span data-stu-id="3be7e-117">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="3be7e-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ с \_ до**</span><span class="sxs-lookup"><span data-stu-id="3be7e-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="3be7e-119">Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено между двумя датами набора.</span><span class="sxs-lookup"><span data-stu-id="3be7e-119">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="3be7e-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM \_ из**</span><span class="sxs-lookup"><span data-stu-id="3be7e-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="3be7e-121">Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено, но только заданное число раз после даты установки.</span><span class="sxs-lookup"><span data-stu-id="3be7e-121">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="3be7e-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM \_ до**</span><span class="sxs-lookup"><span data-stu-id="3be7e-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="3be7e-123">Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено, но только заданное число раз до даты установки.</span><span class="sxs-lookup"><span data-stu-id="3be7e-123">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="3be7e-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ число состояний лицензий WM DRM \_ \_ \_ от \_ до**</span><span class="sxs-lookup"><span data-stu-id="3be7e-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="3be7e-125">Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено, но только заданное число раз между двумя датами набора.</span><span class="sxs-lookup"><span data-stu-id="3be7e-125">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="3be7e-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_ \_ срок действия лицензии WM DRM \_ \_ \_ после \_ фирстусе**</span><span class="sxs-lookup"><span data-stu-id="3be7e-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="3be7e-127">Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено в течение заданного интервала времени, начиная с первого использования действия.</span><span class="sxs-lookup"><span data-stu-id="3be7e-127">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed for a set amount of time beginning with the first use of the action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3be7e-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3be7e-128">Remarks</span></span>

<span data-ttu-id="3be7e-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="3be7e-129">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be7e-130">Требования</span><span class="sxs-lookup"><span data-stu-id="3be7e-130">Requirements</span></span>



| <span data-ttu-id="3be7e-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3be7e-131">Requirement</span></span> | <span data-ttu-id="3be7e-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3be7e-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3be7e-133">Header</span><span class="sxs-lookup"><span data-stu-id="3be7e-133">Header</span></span><br/> | <dl> <span data-ttu-id="3be7e-134"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="3be7e-134"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be7e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3be7e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be7e-136">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="3be7e-136">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





