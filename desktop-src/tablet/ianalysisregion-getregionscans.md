---
description: Извлекает массив прямоугольников, определяющих площадь Ианалисисрегион.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'Метод Ианалисисрегион:: Жетрегионсканс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673311"
---
# <a name="ianalysisregiongetregionscans-method"></a><span data-ttu-id="cc27c-103">Метод Ианалисисрегион:: Жетрегионсканс</span><span class="sxs-lookup"><span data-stu-id="cc27c-103">IAnalysisRegion::GetRegionScans method</span></span>

<span data-ttu-id="cc27c-104">Извлекает массив прямоугольников, определяющих площадь [**ианалисисрегион**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="cc27c-104">Retrieves an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc27c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc27c-105">Syntax</span></span>


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a><span data-ttu-id="cc27c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc27c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc27c-107">*пулкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cc27c-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc27c-108">Число прямоугольников, возвращаемых в *прегионсканс*.</span><span class="sxs-lookup"><span data-stu-id="cc27c-108">The number of rectangles returned in *pRegionScans*.</span></span>

</dd> <dt>

<span data-ttu-id="cc27c-109">*прегионсканс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cc27c-109">*pRegionScans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc27c-110">Указатель на массив прямоугольников, определяющий площадь [**ианалисисрегион**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="cc27c-110">A pointer to an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc27c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc27c-111">Return value</span></span>

<span data-ttu-id="cc27c-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cc27c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc27c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc27c-113">Remarks</span></span>

<span data-ttu-id="cc27c-114">Если *прегионсканс* передается как **null**, метод **жетрегионсканс** возвращает значение **S \_ ОК** , а число прямоугольников возвращается в *пулкаунт*.</span><span class="sxs-lookup"><span data-stu-id="cc27c-114">If *pRegionScans* is passed as **NULL**, the **GetRegionScans** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="cc27c-115">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *прегионсканс* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="cc27c-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pRegionScans* when you no longer need the information.</span></span>

 

<span data-ttu-id="cc27c-116">Границы прямоугольников находятся в координатах для рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="cc27c-116">The bounds of the rectangles are in ink-space coordinates.</span></span>

<span data-ttu-id="cc27c-117">Объединение возвращенных прямоугольников представляет область [**ианалисисрегион**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="cc27c-117">The union of the returned rectangles represents the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cc27c-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="cc27c-118">Examples</span></span>

<span data-ttu-id="cc27c-119">В следующем примере показано, как получить прямоугольники, определяющие область [**ианалисисрегион**](ianalysisregion.md), `region` и как получить только число прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="cc27c-119">The following example shows how to get the rectangles that define the area of the [**IAnalysisRegion**](ianalysisregion.md), `region` and how to get only the number of rectangles.</span></span>


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="cc27c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cc27c-120">Requirements</span></span>



| <span data-ttu-id="cc27c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cc27c-121">Requirement</span></span> | <span data-ttu-id="cc27c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cc27c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc27c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc27c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cc27c-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cc27c-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cc27c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc27c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cc27c-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cc27c-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cc27c-127">Header</span><span class="sxs-lookup"><span data-stu-id="cc27c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc27c-128"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cc27c-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cc27c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cc27c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc27c-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc27c-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cc27c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc27c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc27c-132">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="cc27c-132">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="cc27c-133">**Метод Ианалисисрегион:: DataBound**</span><span class="sxs-lookup"><span data-stu-id="cc27c-133">**IAnalysisRegion::GetBounds Method**</span></span>](ianalysisregion-getbounds.md)
</dt> <dt>

[<span data-ttu-id="cc27c-134">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="cc27c-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

