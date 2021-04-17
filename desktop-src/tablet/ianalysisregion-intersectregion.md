---
description: Область Ианалисисрегион ограничена областью, созданной ее пересечением, с указанным Ианалисисрегион.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'Метод Ианалисисрегион:: Интерсектрегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7ff3caad382e54f41685f6102edafdeb86b813c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711149"
---
# <a name="ianalysisregionintersectregion-method"></a><span data-ttu-id="2e761-103">Метод Ианалисисрегион:: Интерсектрегион</span><span class="sxs-lookup"><span data-stu-id="2e761-103">IAnalysisRegion::IntersectRegion method</span></span>

<span data-ttu-id="2e761-104">Область [**ианалисисрегион**](ianalysisregion.md) ограничена областью, созданной ее пересечением, с указанным **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="2e761-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e761-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e761-105">Syntax</span></span>


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a><span data-ttu-id="2e761-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e761-107">*прегионтоинтерсект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e761-107">*pRegionToIntersect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e761-108">[**Ианалисисрегион**](ianalysisregion.md) , с которым производится пересечение.</span><span class="sxs-lookup"><span data-stu-id="2e761-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to intersect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e761-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e761-109">Return value</span></span>

<span data-ttu-id="2e761-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2e761-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e761-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e761-111">Remarks</span></span>

<span data-ttu-id="2e761-112">Если две области не пересекаются, Новая область будет пустой.</span><span class="sxs-lookup"><span data-stu-id="2e761-112">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e761-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2e761-113">Requirements</span></span>



| <span data-ttu-id="2e761-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2e761-114">Requirement</span></span> | <span data-ttu-id="2e761-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2e761-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e761-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e761-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e761-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2e761-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2e761-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e761-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e761-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2e761-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2e761-120">Header</span><span class="sxs-lookup"><span data-stu-id="2e761-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e761-121"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2e761-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2e761-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2e761-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e761-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e761-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2e761-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e761-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e761-125">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="2e761-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="2e761-126">**Ианалисисрегион:: Ексклудеректангле**</span><span class="sxs-lookup"><span data-stu-id="2e761-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="2e761-127">**Метод Ианалисисрегион:: Ексклудерегион**</span><span class="sxs-lookup"><span data-stu-id="2e761-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="2e761-128">**Метод Ианалисисрегион:: Интерсектректангле**</span><span class="sxs-lookup"><span data-stu-id="2e761-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="2e761-129">**Метод Ианалисисрегион:: Унионректангле**</span><span class="sxs-lookup"><span data-stu-id="2e761-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="2e761-130">**Метод Ианалисисрегион:: Унионрегион**</span><span class="sxs-lookup"><span data-stu-id="2e761-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="2e761-131">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="2e761-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




