---
description: Разворачивает область этого Ианалисисрегиона в область, созданную его объединением с указанным прямоугольником.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'Метод Ианалисисрегион:: Унионректангле (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692452"
---
# <a name="ianalysisregionunionrectangle-method"></a><span data-ttu-id="1b1f7-103">Метод Ианалисисрегион:: Унионректангле</span><span class="sxs-lookup"><span data-stu-id="1b1f7-103">IAnalysisRegion::UnionRectangle method</span></span>

<span data-ttu-id="1b1f7-104">Разворачивает область этого [**ианалисисрегиона**](ianalysisregion.md) в область, созданную его объединением с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="1b1f7-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b1f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b1f7-105">Syntax</span></span>


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="1b1f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b1f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b1f7-107">*пректангле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b1f7-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b1f7-108">Указатель на прямоугольник, с которым выполняется объединение, в координатах рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="1b1f7-108">A pointer to the rectangle with which to combine, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b1f7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b1f7-109">Return value</span></span>

<span data-ttu-id="1b1f7-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1b1f7-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1b1f7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b1f7-111">Remarks</span></span>

<span data-ttu-id="1b1f7-112">Координаты прямоугольника находятся в единицах HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="1b1f7-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="1b1f7-113">Если любая из этих областей бесконечно, Новая область также будет бесконечна.</span><span class="sxs-lookup"><span data-stu-id="1b1f7-113">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b1f7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1b1f7-114">Requirements</span></span>



| <span data-ttu-id="1b1f7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1b1f7-115">Requirement</span></span> | <span data-ttu-id="1b1f7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1b1f7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1f7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b1f7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1b1f7-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1b1f7-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1b1f7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b1f7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1b1f7-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1b1f7-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1b1f7-121">Header</span><span class="sxs-lookup"><span data-stu-id="1b1f7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b1f7-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1b1f7-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1b1f7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1b1f7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b1f7-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b1f7-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1b1f7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b1f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b1f7-126">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="1b1f7-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="1b1f7-127">**Ианалисисрегион:: Ексклудеректангле**</span><span class="sxs-lookup"><span data-stu-id="1b1f7-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="1b1f7-128">**Метод Ианалисисрегион:: Ексклудерегион**</span><span class="sxs-lookup"><span data-stu-id="1b1f7-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="1b1f7-129">**Метод Ианалисисрегион:: Интерсектректангле**</span><span class="sxs-lookup"><span data-stu-id="1b1f7-129">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="1b1f7-130">**Метод Ианалисисрегион:: Интерсектрегион**</span><span class="sxs-lookup"><span data-stu-id="1b1f7-130">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="1b1f7-131">**Метод Ианалисисрегион:: Унионрегион**</span><span class="sxs-lookup"><span data-stu-id="1b1f7-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="1b1f7-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="1b1f7-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




