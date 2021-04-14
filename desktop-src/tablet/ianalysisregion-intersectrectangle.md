---
description: Область этого Ианалисисрегиона ограничена областью, созданной ее пересечением с указанным прямоугольником.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'Метод Ианалисисрегион:: Интерсектректангле (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4ce0e514b24aba0331d9ea604333680db1c67c8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542098"
---
# <a name="ianalysisregionintersectrectangle-method"></a><span data-ttu-id="48a41-103">Метод Ианалисисрегион:: Интерсектректангле</span><span class="sxs-lookup"><span data-stu-id="48a41-103">IAnalysisRegion::IntersectRectangle method</span></span>

<span data-ttu-id="48a41-104">Область этого [**ианалисисрегиона**](ianalysisregion.md) ограничена областью, созданной ее пересечением с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="48a41-104">Restricts the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a41-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48a41-105">Syntax</span></span>


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="48a41-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48a41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a41-107">*пинтерсектингректангле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48a41-107">*pIntersectingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48a41-108">Указатель на прямоугольник, с которым производится пересечение, в координатах рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="48a41-108">A pointer to the rectangle with which to intersect, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a41-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48a41-109">Return value</span></span>

<span data-ttu-id="48a41-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="48a41-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="48a41-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48a41-111">Remarks</span></span>

<span data-ttu-id="48a41-112">Координаты прямоугольника находятся в единицах HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="48a41-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="48a41-113">Если две области не пересекаются, Новая область будет пустой.</span><span class="sxs-lookup"><span data-stu-id="48a41-113">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="48a41-114">Требования</span><span class="sxs-lookup"><span data-stu-id="48a41-114">Requirements</span></span>



| <span data-ttu-id="48a41-115">Требование</span><span class="sxs-lookup"><span data-stu-id="48a41-115">Requirement</span></span> | <span data-ttu-id="48a41-116">Значение</span><span class="sxs-lookup"><span data-stu-id="48a41-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a41-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48a41-117">Minimum supported client</span></span><br/> | <span data-ttu-id="48a41-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="48a41-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="48a41-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48a41-119">Minimum supported server</span></span><br/> | <span data-ttu-id="48a41-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="48a41-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="48a41-121">Header</span><span class="sxs-lookup"><span data-stu-id="48a41-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="48a41-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="48a41-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="48a41-123">DLL</span><span class="sxs-lookup"><span data-stu-id="48a41-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48a41-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48a41-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="48a41-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48a41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a41-126">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="48a41-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="48a41-127">**Ианалисисрегион:: Ексклудеректангле**</span><span class="sxs-lookup"><span data-stu-id="48a41-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="48a41-128">**Метод Ианалисисрегион:: Ексклудерегион**</span><span class="sxs-lookup"><span data-stu-id="48a41-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="48a41-129">**Метод Ианалисисрегион:: Интерсектрегион**</span><span class="sxs-lookup"><span data-stu-id="48a41-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="48a41-130">**Метод Ианалисисрегион:: Унионректангле**</span><span class="sxs-lookup"><span data-stu-id="48a41-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="48a41-131">**Метод Ианалисисрегион:: Унионрегион**</span><span class="sxs-lookup"><span data-stu-id="48a41-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="48a41-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="48a41-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




