---
title: Структура DRM_VIDEO_OUTPUT_PROTECTION_IDS (Вмдрмсдк. h)
description: '\_ \_ \_ \_ Структура идентификаторов для защиты от видео DRM содержит массив \_ \_ структур защиты вывода видео DRM \_ .'
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- Формат DRM_VIDEO_OUTPUT_PROTECTION_IDS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704111"
---
# <a name="drm_video_output_protection_ids-structure"></a><span data-ttu-id="5a54e-105">\_ \_ \_ Структура идентификаторов защиты ВИДЕОпотока DRM \_</span><span class="sxs-lookup"><span data-stu-id="5a54e-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="5a54e-106">Структура **\_ \_ \_ \_ идентификаторов для защиты от видео DRM** содержит массив структур **\_ \_ \_ защиты вывода видео DRM** .</span><span class="sxs-lookup"><span data-stu-id="5a54e-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a54e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a54e-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="5a54e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5a54e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5a54e-109">**центриес**</span><span class="sxs-lookup"><span data-stu-id="5a54e-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="5a54e-110">Число элементов в массиве, на которые ссылается **ргвоп**.</span><span class="sxs-lookup"><span data-stu-id="5a54e-110">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="5a54e-111">**ргвоп**</span><span class="sxs-lookup"><span data-stu-id="5a54e-111">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="5a54e-112">Адрес массива структур **\_ \_ \_ защиты вывода видео DRM** .</span><span class="sxs-lookup"><span data-stu-id="5a54e-112">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="5a54e-113">**DRM \_ \_ \_ Защита вывода видео** — это тип, определенный [**как \_ \_ Защита выходных данных DRM**](drm-output-protection.md).</span><span class="sxs-lookup"><span data-stu-id="5a54e-113">**DRM\_VIDEO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a54e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a54e-114">Remarks</span></span>

<span data-ttu-id="5a54e-115">Эта структура используется в качестве члена структуры [**DRM \_ Play \_ ОПЛ**](drmdrm-play-opl.md) .</span><span class="sxs-lookup"><span data-stu-id="5a54e-115">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a54e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5a54e-116">Requirements</span></span>



| <span data-ttu-id="5a54e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5a54e-117">Requirement</span></span> | <span data-ttu-id="5a54e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5a54e-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a54e-119">Header</span><span class="sxs-lookup"><span data-stu-id="5a54e-119">Header</span></span><br/> | <dl> <span data-ttu-id="5a54e-120"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a54e-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a54e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a54e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a54e-122">**\_ \_ \_ идентификаторы защиты звука в DRM \_**</span><span class="sxs-lookup"><span data-stu-id="5a54e-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="5a54e-123">**\_ \_ \_ идентификаторы защиты вывода видео DRM \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="5a54e-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="5a54e-124">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="5a54e-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





