---
title: Структура DRM_COPY_OPL (Вмдрмсдк. h)
description: '\_ \_ Структура копирования ОПЛ DRM содержит сведения об уровнях защиты выходных данных (оплс), указанных в лицензии для действий копирования.'
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- Формат DRM_COPY_OPL структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708396"
---
# <a name="drm_copy_opl-structure"></a><span data-ttu-id="5a31b-105">\_Структура копирования \_ ОПЛ DRM</span><span class="sxs-lookup"><span data-stu-id="5a31b-105">DRM\_COPY\_OPL structure</span></span>

<span data-ttu-id="5a31b-106">Структура **\_ копирования \_ ОПЛ DRM** содержит сведения об уровнях защиты выходных данных (оплс), указанных в лицензии для действий копирования.</span><span class="sxs-lookup"><span data-stu-id="5a31b-106">The **DRM\_COPY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for copy actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a31b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a31b-107">Syntax</span></span>


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a><span data-ttu-id="5a31b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5a31b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5a31b-109">**вминимумкопилевел**</span><span class="sxs-lookup"><span data-stu-id="5a31b-109">**wMinimumCopyLevel**</span></span>
</dt> <dd>

<span data-ttu-id="5a31b-110">Минимальный ОПЛ для действий копирования.</span><span class="sxs-lookup"><span data-stu-id="5a31b-110">Minimum OPL for copy actions.</span></span>

</dd> <dt>

<span data-ttu-id="5a31b-111">**оплидинклудес**</span><span class="sxs-lookup"><span data-stu-id="5a31b-111">**oplIdIncludes**</span></span>
</dt> <dd>

<span data-ttu-id="5a31b-112">[**DRM \_ Структура \_ \_ идентификаторов выходных данных ОПЛ**](drmdrm-opl-output-ids.md) , содержащая идентификаторы технологий, которые должны быть разрешены.</span><span class="sxs-lookup"><span data-stu-id="5a31b-112">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the identifiers of technologies to allow.</span></span> <span data-ttu-id="5a31b-113">Этот элемент используется для вывода технологий, которые назначаются Оплс ниже минимального уровня копирования, но для которого может быть скопировано содержимое.</span><span class="sxs-lookup"><span data-stu-id="5a31b-113">This member is used for output technologies that are assigned OPLs lower than the minimum copy level, but to which the content may be copied.</span></span>

</dd> <dt>

<span data-ttu-id="5a31b-114">**оплидексклудес**</span><span class="sxs-lookup"><span data-stu-id="5a31b-114">**oplIdExcludes**</span></span>
</dt> <dd>

<span data-ttu-id="5a31b-115">[**DRM \_ Структура \_ \_ идентификаторов выходных данных ОПЛ**](drmdrm-opl-output-ids.md) , содержащая идентификаторы выходных данных технологий для ограничения.</span><span class="sxs-lookup"><span data-stu-id="5a31b-115">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the output identifiers of technologies to restrict.</span></span> <span data-ttu-id="5a31b-116">Этот элемент используется для технологий вывода, которым назначены Оплс, превышающие минимальный уровень копирования, но поставщик лицензий не предоставляет права на копирование в.</span><span class="sxs-lookup"><span data-stu-id="5a31b-116">This member is used for output technologies that are assigned OPLs that exceed the minimum copy level, but that the license issuer does not grant rights for copying to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a31b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5a31b-117">Requirements</span></span>



| <span data-ttu-id="5a31b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5a31b-118">Requirement</span></span> | <span data-ttu-id="5a31b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5a31b-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a31b-120">Header</span><span class="sxs-lookup"><span data-stu-id="5a31b-120">Header</span></span><br/> | <dl> <span data-ttu-id="5a31b-121"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a31b-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a31b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a31b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a31b-123">**DRM \_ Play \_ ОПЛ**</span><span class="sxs-lookup"><span data-stu-id="5a31b-123">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="5a31b-124">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="5a31b-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





