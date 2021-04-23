---
description: Возвращает ограничивающий прямоугольник Ианалисисрегион.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: Метод Ианалисисрегион::-Bounds (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810055"
---
# <a name="ianalysisregiongetbounds-method"></a><span data-ttu-id="bce1f-103">Метод Ианалисисрегион:: DataBound</span><span class="sxs-lookup"><span data-stu-id="bce1f-103">IAnalysisRegion::GetBounds method</span></span>

<span data-ttu-id="bce1f-104">Возвращает ограничивающий прямоугольник [**ианалисисрегион**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="bce1f-104">Gets the bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bce1f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bce1f-105">Syntax</span></span>


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="bce1f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bce1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce1f-107">*пбаундингректангле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bce1f-107">*pBoundingRectangle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bce1f-108">Ограничивающий прямоугольник [**ианалисисрегион**](ianalysisregion.md) в координатах рукописного пространства.</span><span class="sxs-lookup"><span data-stu-id="bce1f-108">The bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md) in ink space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce1f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bce1f-109">Return value</span></span>

<span data-ttu-id="bce1f-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bce1f-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bce1f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bce1f-111">Remarks</span></span>

<span data-ttu-id="bce1f-112">Границы находятся в координатах для рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="bce1f-112">The bounds are in ink-space coordinates.</span></span>

<span data-ttu-id="bce1f-113">Если [**ианалисисрегион**](ianalysisregion.md) представляет бесконечную область, левая и верхняя границы имеют **тип int \_ min**, а правая и нижняя границы — **int \_ Max**.</span><span class="sxs-lookup"><span data-stu-id="bce1f-113">If the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite area, the left and top bounds are **INT\_MIN**; and the right and bottom bounds are **INT\_MAX**.</span></span>

<span data-ttu-id="bce1f-114">Если [**ианалисисрегион**](ianalysisregion.md) представляет пустую область, все границы прямоугольника равны 0.</span><span class="sxs-lookup"><span data-stu-id="bce1f-114">If the [**IAnalysisRegion**](ianalysisregion.md) represents an empty area, all the bounds of the rectangle are 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="bce1f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bce1f-115">Requirements</span></span>



| <span data-ttu-id="bce1f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bce1f-116">Requirement</span></span> | <span data-ttu-id="bce1f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bce1f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bce1f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bce1f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bce1f-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bce1f-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bce1f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bce1f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bce1f-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bce1f-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bce1f-122">Header</span><span class="sxs-lookup"><span data-stu-id="bce1f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bce1f-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bce1f-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bce1f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bce1f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bce1f-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bce1f-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bce1f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bce1f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce1f-127">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="bce1f-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="bce1f-128">**Метод Ианалисисрегион:: Жетрегионсканс**</span><span class="sxs-lookup"><span data-stu-id="bce1f-128">**IAnalysisRegion::GetRegionScans Method**</span></span>](ianalysisregion-getregionscans.md)
</dt> <dt>

[<span data-ttu-id="bce1f-129">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="bce1f-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




