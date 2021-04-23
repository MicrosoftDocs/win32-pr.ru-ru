---
title: Структура DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX (Вмдрмсдк. h)
description: В \_ \_ \_ \_ структуре идентификаторов защиты видео DRM \_ содержится массив \_ \_ структур защиты вывода видео DRM \_ .
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- Формат DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704048"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a><span data-ttu-id="715af-105">\_ \_ Идентификатор защиты вывода видео DRM — \_ \_ \_ Структура ex</span><span class="sxs-lookup"><span data-stu-id="715af-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="715af-106">В **структуре \_ \_ \_ \_ \_ идентификаторов защиты видео DRM** содержится массив структур **\_ \_ \_ защиты вывода видео DRM** .</span><span class="sxs-lookup"><span data-stu-id="715af-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="715af-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="715af-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="715af-108">Члены</span><span class="sxs-lookup"><span data-stu-id="715af-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="715af-109">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="715af-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="715af-110">Номер версии.</span><span class="sxs-lookup"><span data-stu-id="715af-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="715af-111">**центриес**</span><span class="sxs-lookup"><span data-stu-id="715af-111">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="715af-112">Число элементов в массиве, на которые ссылается **ргвоп**.</span><span class="sxs-lookup"><span data-stu-id="715af-112">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="715af-113">**ргвоп**</span><span class="sxs-lookup"><span data-stu-id="715af-113">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="715af-114">Адрес массива структур для **\_ \_ \_ \_ защиты вывода видео DRM** .</span><span class="sxs-lookup"><span data-stu-id="715af-114">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="715af-115">**DRM \_ \_ \_ Защита от вывода видео \_ ex** — это тип, определенный как [**\_ \_ Защита \_ выходных данных DRM**](drm-output-protection-ex.md), например.</span><span class="sxs-lookup"><span data-stu-id="715af-115">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="715af-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="715af-116">Remarks</span></span>

<span data-ttu-id="715af-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="715af-117">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="715af-118">Требования</span><span class="sxs-lookup"><span data-stu-id="715af-118">Requirements</span></span>



| <span data-ttu-id="715af-119">Требование</span><span class="sxs-lookup"><span data-stu-id="715af-119">Requirement</span></span> | <span data-ttu-id="715af-120">Значение</span><span class="sxs-lookup"><span data-stu-id="715af-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="715af-121">Header</span><span class="sxs-lookup"><span data-stu-id="715af-121">Header</span></span><br/> | <dl> <span data-ttu-id="715af-122"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="715af-122"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="715af-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="715af-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="715af-124">**\_ \_ \_ идентификаторы защиты аудио вывода DRM \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="715af-124">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="715af-125">**\_ \_ \_ идентификаторы защиты вывода видео DRM \_**</span><span class="sxs-lookup"><span data-stu-id="715af-125">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="715af-126">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="715af-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





