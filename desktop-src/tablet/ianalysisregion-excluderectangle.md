---
description: Ограничивающий область Ианалисисрегион до части области, которая не пересекается с указанным прямоугольником.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'Метод Ианалисисрегион:: Ексклудеректангле (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711150"
---
# <a name="ianalysisregionexcluderectangle-method"></a><span data-ttu-id="7be05-103">Метод Ианалисисрегион:: Ексклудеректангле</span><span class="sxs-lookup"><span data-stu-id="7be05-103">IAnalysisRegion::ExcludeRectangle method</span></span>

<span data-ttu-id="7be05-104">Ограничивающий область [**ианалисисрегион**](ianalysisregion.md) до части области, которая не пересекается с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="7be05-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be05-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7be05-105">Syntax</span></span>


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="7be05-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7be05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be05-107">*пексклудингректангле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7be05-107">*pExcludingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be05-108">Прямоугольник, исключаемый из этого [**ианалисисрегион**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="7be05-108">The rectangle to exclude from this [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be05-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7be05-109">Return value</span></span>

<span data-ttu-id="7be05-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7be05-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7be05-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7be05-111">Remarks</span></span>

<span data-ttu-id="7be05-112">Координаты прямоугольника находятся в единицах HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="7be05-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="7be05-113">Если две области не пересекаются, [**ианалисисрегион**](ianalysisregion.md) не изменяется.</span><span class="sxs-lookup"><span data-stu-id="7be05-113">If the two areas do not intersect, the [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be05-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7be05-114">Requirements</span></span>



| <span data-ttu-id="7be05-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7be05-115">Requirement</span></span> | <span data-ttu-id="7be05-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7be05-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be05-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7be05-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7be05-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7be05-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7be05-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7be05-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7be05-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7be05-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7be05-121">Header</span><span class="sxs-lookup"><span data-stu-id="7be05-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7be05-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7be05-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7be05-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7be05-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7be05-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7be05-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7be05-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7be05-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be05-126">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="7be05-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="7be05-127">**Метод Ианалисисрегион:: Ексклудерегион**</span><span class="sxs-lookup"><span data-stu-id="7be05-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="7be05-128">**Метод Ианалисисрегион:: Интерсектректангле**</span><span class="sxs-lookup"><span data-stu-id="7be05-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="7be05-129">**Метод Ианалисисрегион:: Интерсектрегион**</span><span class="sxs-lookup"><span data-stu-id="7be05-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="7be05-130">**Метод Ианалисисрегион:: Унионректангле**</span><span class="sxs-lookup"><span data-stu-id="7be05-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="7be05-131">**Метод Ианалисисрегион:: Унионрегион**</span><span class="sxs-lookup"><span data-stu-id="7be05-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="7be05-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="7be05-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




