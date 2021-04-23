---
title: Структура WMDRM_ANALOG_VIDEO_RESTRICTIONS (Вмдрмсдк. h)
description: '\_ \_ Структура ограничений аналогового видео WMDRM \_ содержит сведения об ограничении для воспроизведения содержимого в виде аналогового видео.'
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- Формат WMDRM_ANALOG_VIDEO_RESTRICTIONS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694864"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a><span data-ttu-id="9ca51-105">\_ \_ Структура ограничений аналогового видео WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="9ca51-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS structure</span></span>

<span data-ttu-id="9ca51-106">Структура **\_ \_ \_ ограничений аналогового видео WMDRM** содержит сведения об ограничении для воспроизведения содержимого в виде аналогового видео.</span><span class="sxs-lookup"><span data-stu-id="9ca51-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS** structure holds information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca51-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ca51-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="9ca51-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9ca51-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ca51-109">**гуидрестриктионид**</span><span class="sxs-lookup"><span data-stu-id="9ca51-109">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="9ca51-110">Идентификатор ограничения.</span><span class="sxs-lookup"><span data-stu-id="9ca51-110">Restriction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9ca51-111">**дврестриктиондата**</span><span class="sxs-lookup"><span data-stu-id="9ca51-111">**dwRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="9ca51-112">Данные ограничений.</span><span class="sxs-lookup"><span data-stu-id="9ca51-112">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ca51-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ca51-113">Remarks</span></span>

<span data-ttu-id="9ca51-114">Эта структура получается при вызове [**ивмдрмлиценсе:: жетаналогвидеорестриктионлевелс**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span><span class="sxs-lookup"><span data-stu-id="9ca51-114">This structure is received when you call [**IWMDRMLicense::GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca51-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9ca51-115">Requirements</span></span>



| <span data-ttu-id="9ca51-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9ca51-116">Requirement</span></span> | <span data-ttu-id="9ca51-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca51-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca51-118">Header</span><span class="sxs-lookup"><span data-stu-id="9ca51-118">Header</span></span><br/> | <dl> <span data-ttu-id="9ca51-119"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ca51-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ca51-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ca51-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca51-121">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="9ca51-121">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="9ca51-122">**\_ограничения аналогового видео WMDRM ( \_ \_ \_ пример)**</span><span class="sxs-lookup"><span data-stu-id="9ca51-122">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX**</span></span>](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





