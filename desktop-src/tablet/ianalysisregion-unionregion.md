---
description: Разворачивает область этого Ианалисисрегиона в область, созданную с помощью объединения, с указанным Ианалисисрегион.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'Метод Ианалисисрегион:: Унионрегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 587986973c4ae4bebaeed3c031c746bc4f842c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711145"
---
# <a name="ianalysisregionunionregion-method"></a><span data-ttu-id="9e5ea-103">Метод Ианалисисрегион:: Унионрегион</span><span class="sxs-lookup"><span data-stu-id="9e5ea-103">IAnalysisRegion::UnionRegion method</span></span>

<span data-ttu-id="9e5ea-104">Разворачивает область этого [**ианалисисрегиона**](ianalysisregion.md) в область, созданную с помощью объединения, с указанным **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="9e5ea-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e5ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e5ea-105">Syntax</span></span>


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a><span data-ttu-id="9e5ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e5ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e5ea-107">*прегионтаунион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e5ea-107">*pRegionToUnion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5ea-108">[**Ианалисисрегион**](ianalysisregion.md) , с которым необходимо выполнить объединение.</span><span class="sxs-lookup"><span data-stu-id="9e5ea-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to combine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e5ea-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e5ea-109">Return value</span></span>

<span data-ttu-id="9e5ea-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9e5ea-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5ea-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e5ea-111">Remarks</span></span>

<span data-ttu-id="9e5ea-112">Если любая из этих областей бесконечно, Новая область также будет бесконечна.</span><span class="sxs-lookup"><span data-stu-id="9e5ea-112">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e5ea-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9e5ea-113">Requirements</span></span>



| <span data-ttu-id="9e5ea-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9e5ea-114">Requirement</span></span> | <span data-ttu-id="9e5ea-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9e5ea-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5ea-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e5ea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9e5ea-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9e5ea-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9e5ea-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e5ea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9e5ea-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9e5ea-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9e5ea-120">Header</span><span class="sxs-lookup"><span data-stu-id="9e5ea-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e5ea-121"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9e5ea-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9e5ea-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9e5ea-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e5ea-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e5ea-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9e5ea-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e5ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e5ea-125">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="9e5ea-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="9e5ea-126">**Ианалисисрегион:: Ексклудеректангле**</span><span class="sxs-lookup"><span data-stu-id="9e5ea-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="9e5ea-127">**Метод Ианалисисрегион:: Ексклудерегион**</span><span class="sxs-lookup"><span data-stu-id="9e5ea-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="9e5ea-128">**Метод Ианалисисрегион:: Интерсектректангле**</span><span class="sxs-lookup"><span data-stu-id="9e5ea-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="9e5ea-129">**Метод Ианалисисрегион:: Интерсектрегион**</span><span class="sxs-lookup"><span data-stu-id="9e5ea-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="9e5ea-130">**Метод Ианалисисрегион:: Унионректангле**</span><span class="sxs-lookup"><span data-stu-id="9e5ea-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="9e5ea-131">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9e5ea-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




