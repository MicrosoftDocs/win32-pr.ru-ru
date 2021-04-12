---
description: Изменяет область, которая изменилась со времени последнего выполнения операции анализа.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'Метод Иинканализер:: Сетдиртирегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 72278dd9fe1d772d4ef340d25694d42f9c48ed7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145436"
---
# <a name="iinkanalyzersetdirtyregion-method"></a><span data-ttu-id="3df27-103">Метод Иинканализер:: Сетдиртирегион</span><span class="sxs-lookup"><span data-stu-id="3df27-103">IInkAnalyzer::SetDirtyRegion method</span></span>

<span data-ttu-id="3df27-104">Изменяет область, которая изменилась со времени последнего выполнения операции анализа.</span><span class="sxs-lookup"><span data-stu-id="3df27-104">Modifies the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df27-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3df27-105">Syntax</span></span>


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="3df27-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3df27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df27-107">*пдиртирегион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3df27-107">*pDirtyRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df27-108">Объект [**ианалисисрегион**](ianalysisregion.md) , описывающий область, измененную с момента последнего выполнения операции анализа.</span><span class="sxs-lookup"><span data-stu-id="3df27-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df27-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3df27-109">Return value</span></span>

<span data-ttu-id="3df27-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3df27-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3df27-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3df27-111">Remarks</span></span>

<span data-ttu-id="3df27-112">Этот метод определяет области, которые необходимо проанализировать или повторно проанализировать.</span><span class="sxs-lookup"><span data-stu-id="3df27-112">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="3df27-113">Все методы [**иинканализер**](iinkanalyzer.md) , которые добавляют, обновляют или удаляют данные обводки, обновляют «грязную» область.</span><span class="sxs-lookup"><span data-stu-id="3df27-113">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="3df27-114">Чтобы вручную пометить область для переанализа:</span><span class="sxs-lookup"><span data-stu-id="3df27-114">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="3df27-115">Получите "грязную" область с помощью [**метода иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md).</span><span class="sxs-lookup"><span data-stu-id="3df27-115">Get the dirty region using [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md).</span></span>
2.  <span data-ttu-id="3df27-116">Используйте [**метод ианалисисрегион:: унионрегион**](ianalysisregion-unionregion.md) или [**метод Ианалисисрегион:: унионректангле**](ianalysisregion-unionrectangle.md) для добавления области в регион из шага 1.</span><span class="sxs-lookup"><span data-stu-id="3df27-116">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="3df27-117">Чтобы обновить "грязную" область, используйте **метод иинканализер:: сетдиртирегион** .</span><span class="sxs-lookup"><span data-stu-id="3df27-117">Use **IInkAnalyzer::SetDirtyRegion Method** to update the dirty region.</span></span>

<span data-ttu-id="3df27-118">[**Иинканализер**](iinkanalyzer.md) анализирует рукописный ввод в своей «грязной» области во время вызова метода [**Иинканализер:: Analyze**](iinkanalyzer-analyze.md) или [**иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="3df27-118">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="3df27-119">Однако **иинканализер** может расширить операцию анализа, включив в нее соседние регионы.</span><span class="sxs-lookup"><span data-stu-id="3df27-119">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3df27-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3df27-120">Requirements</span></span>



| <span data-ttu-id="3df27-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3df27-121">Requirement</span></span> | <span data-ttu-id="3df27-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3df27-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df27-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3df27-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3df27-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3df27-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3df27-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3df27-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3df27-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3df27-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3df27-127">Header</span><span class="sxs-lookup"><span data-stu-id="3df27-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3df27-128"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3df27-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3df27-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3df27-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3df27-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df27-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3df27-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3df27-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df27-132">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="3df27-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3df27-133">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="3df27-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="3df27-134">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="3df27-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="3df27-135">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="3df27-135">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="3df27-136">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="3df27-136">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="3df27-137">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="3df27-137">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="3df27-138">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="3df27-138">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="3df27-139">**Метод Иинканализер:: Ремовестроке**</span><span class="sxs-lookup"><span data-stu-id="3df27-139">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="3df27-140">**Метод Иинканализер:: Ремовестрокес**</span><span class="sxs-lookup"><span data-stu-id="3df27-140">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="3df27-141">**Метод Иинканализер:: Упдатестрокесдата**</span><span class="sxs-lookup"><span data-stu-id="3df27-141">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="3df27-142">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="3df27-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




