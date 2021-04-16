---
description: Ограничивающий область Ианалисисрегион до части области, которая не пересекается с заданным Ианалисисрегион.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'Метод Ианалисисрегион:: Ексклудерегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542103"
---
# <a name="ianalysisregionexcluderegion-method"></a><span data-ttu-id="caaae-103">Метод Ианалисисрегион:: Ексклудерегион</span><span class="sxs-lookup"><span data-stu-id="caaae-103">IAnalysisRegion::ExcludeRegion method</span></span>

<span data-ttu-id="caaae-104">Ограничивающий область [**ианалисисрегион**](ianalysisregion.md) до части области, которая не пересекается с заданным **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="caaae-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="caaae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="caaae-105">Syntax</span></span>


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a><span data-ttu-id="caaae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="caaae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caaae-107">*прегионтоексклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="caaae-107">*pRegionToExclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caaae-108">[**Ианалисисрегион**](ianalysisregion.md) , исключаемый из этого **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="caaae-108">The [**IAnalysisRegion**](ianalysisregion.md) to exclude from this **IAnalysisRegion**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caaae-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="caaae-109">Return value</span></span>

<span data-ttu-id="caaae-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="caaae-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="caaae-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="caaae-111">Remarks</span></span>

<span data-ttu-id="caaae-112">Если две области не пересекаются, это [**ианалисисрегион**](ianalysisregion.md) не изменяется.</span><span class="sxs-lookup"><span data-stu-id="caaae-112">If the two areas do not intersect, this [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="caaae-113">Требования</span><span class="sxs-lookup"><span data-stu-id="caaae-113">Requirements</span></span>



| <span data-ttu-id="caaae-114">Требование</span><span class="sxs-lookup"><span data-stu-id="caaae-114">Requirement</span></span> | <span data-ttu-id="caaae-115">Значение</span><span class="sxs-lookup"><span data-stu-id="caaae-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caaae-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="caaae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="caaae-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="caaae-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="caaae-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="caaae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="caaae-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="caaae-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="caaae-120">Header</span><span class="sxs-lookup"><span data-stu-id="caaae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="caaae-121"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="caaae-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="caaae-122">DLL</span><span class="sxs-lookup"><span data-stu-id="caaae-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caaae-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caaae-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="caaae-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="caaae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caaae-125">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="caaae-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="caaae-126">**Ианалисисрегион:: Ексклудеректангле**</span><span class="sxs-lookup"><span data-stu-id="caaae-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="caaae-127">**Метод Ианалисисрегион:: Интерсектректангле**</span><span class="sxs-lookup"><span data-stu-id="caaae-127">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="caaae-128">**Метод Ианалисисрегион:: Интерсектрегион**</span><span class="sxs-lookup"><span data-stu-id="caaae-128">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="caaae-129">**Метод Ианалисисрегион:: Унионректангле**</span><span class="sxs-lookup"><span data-stu-id="caaae-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="caaae-130">**Метод Ианалисисрегион:: Унионрегион**</span><span class="sxs-lookup"><span data-stu-id="caaae-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="caaae-131">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="caaae-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




