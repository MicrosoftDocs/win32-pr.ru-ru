---
title: Структура DRM_OPL_OUTPUT_IDS (Вмдрмсдк. h)
description: '\_ \_ \_ Структура выходных идентификаторов DRM ОПЛ содержит ряд выходных идентификаторов уровня защиты выходных данных (ОПЛ).'
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- Формат DRM_OPL_OUTPUT_IDS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708364"
---
# <a name="drm_opl_output_ids-structure"></a><span data-ttu-id="d8183-105">\_ \_ Структура идентификаторов выходных данных ОПЛ DRM \_</span><span class="sxs-lookup"><span data-stu-id="d8183-105">DRM\_OPL\_OUTPUT\_IDS structure</span></span>

<span data-ttu-id="d8183-106">Структура **\_ \_ выходных \_ идентификаторов DRM ОПЛ** содержит ряд выходных идентификаторов уровня защиты выходных данных (ОПЛ).</span><span class="sxs-lookup"><span data-stu-id="d8183-106">The **DRM\_OPL\_OUTPUT\_IDS** structure holds a number of output protection level (OPL) output identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8183-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8183-107">Syntax</span></span>


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a><span data-ttu-id="d8183-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d8183-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8183-109">**Идентификаторы CID**</span><span class="sxs-lookup"><span data-stu-id="d8183-109">**cIds**</span></span>
</dt> <dd>

<span data-ttu-id="d8183-110">Количество идентификаторов в массиве, на которые ссылается **ргидс**.</span><span class="sxs-lookup"><span data-stu-id="d8183-110">Number of identifiers in the array referenced by **rgIds**.</span></span>

</dd> <dt>

<span data-ttu-id="d8183-111">**ргидс**</span><span class="sxs-lookup"><span data-stu-id="d8183-111">**rgIds**</span></span>
</dt> <dd>

<span data-ttu-id="d8183-112">Адрес массива идентификаторов GUID.</span><span class="sxs-lookup"><span data-stu-id="d8183-112">Address of an array of GUIDs.</span></span> <span data-ttu-id="d8183-113">Каждый элемент массива содержит идентификатор выхода ОПЛ.</span><span class="sxs-lookup"><span data-stu-id="d8183-113">Each member of the array contains an OPL output identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8183-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8183-114">Remarks</span></span>

<span data-ttu-id="d8183-115">Эта структура используется в качестве члена структур [**DRM \_ Copy \_ ОПЛ**](drmdrm-copy-opl.md) и [**DRM \_ Play \_ ОПЛ**](drmdrm-play-opl.md) для идентификации групп идентификаторов выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d8183-115">This structure is used as a member of the [**DRM\_COPY\_OPL**](drmdrm-copy-opl.md) and [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structures to identify groups of output identifiers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8183-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d8183-116">Requirements</span></span>



| <span data-ttu-id="d8183-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d8183-117">Requirement</span></span> | <span data-ttu-id="d8183-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d8183-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8183-119">Header</span><span class="sxs-lookup"><span data-stu-id="d8183-119">Header</span></span><br/> | <dl> <span data-ttu-id="d8183-120"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8183-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8183-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8183-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8183-122">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="d8183-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





