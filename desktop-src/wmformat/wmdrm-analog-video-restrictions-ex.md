---
title: Структура WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX (Вмдрмсдк. h)
description: '\_ \_ \_ Примерная структура ограничений аналогового видео WMDRM \_ содержит расширенные сведения об ограничении для воспроизведения содержимого в виде аналогового видео.'
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- Формат WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694865"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a><span data-ttu-id="9fbd8-105">\_Ограничения аналогового видео WMDRM — \_ \_ \_ Структура</span><span class="sxs-lookup"><span data-stu-id="9fbd8-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX structure</span></span>

<span data-ttu-id="9fbd8-106">**\_ \_ \_ \_ Примерная структура ограничений аналогового видео WMDRM** содержит расширенные сведения об ограничении для воспроизведения содержимого в виде аналогового видео.</span><span class="sxs-lookup"><span data-stu-id="9fbd8-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX** structure holds extended information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fbd8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fbd8-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="9fbd8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9fbd8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9fbd8-109">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="9fbd8-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9fbd8-110">Номер версии.</span><span class="sxs-lookup"><span data-stu-id="9fbd8-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="9fbd8-111">**гуидрестриктионид**</span><span class="sxs-lookup"><span data-stu-id="9fbd8-111">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="9fbd8-112">Идентификатор ограничения.</span><span class="sxs-lookup"><span data-stu-id="9fbd8-112">Restriction ID.</span></span>

</dd> <dt>

<span data-ttu-id="9fbd8-113">**кбрестриктиондата**</span><span class="sxs-lookup"><span data-stu-id="9fbd8-113">**cbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="9fbd8-114">Размер данных ограничения в байтах.</span><span class="sxs-lookup"><span data-stu-id="9fbd8-114">Size of restriction data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9fbd8-115">**пбрестриктиондата**</span><span class="sxs-lookup"><span data-stu-id="9fbd8-115">**pbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="9fbd8-116">Данные ограничений.</span><span class="sxs-lookup"><span data-stu-id="9fbd8-116">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fbd8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fbd8-117">Remarks</span></span>

<span data-ttu-id="9fbd8-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="9fbd8-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fbd8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9fbd8-119">Requirements</span></span>



| <span data-ttu-id="9fbd8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9fbd8-120">Requirement</span></span> | <span data-ttu-id="9fbd8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9fbd8-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fbd8-122">Header</span><span class="sxs-lookup"><span data-stu-id="9fbd8-122">Header</span></span><br/> | <dl> <span data-ttu-id="9fbd8-123"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fbd8-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fbd8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fbd8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fbd8-125">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="9fbd8-125">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="9fbd8-126">**\_ограничения аналогового \_ видео WMDRM \_**</span><span class="sxs-lookup"><span data-stu-id="9fbd8-126">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**</span></span>](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





