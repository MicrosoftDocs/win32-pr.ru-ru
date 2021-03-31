---
description: Извлекает область, которая изменилась со времени последнего выполнения операции анализа.
ms.assetid: 0cd62775-59c6-41f5-957e-709a53a8c257
title: 'Метод Иинканализер:: Жетдиртирегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 56f980189e22f50bb832be904933ef0b26d9b54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263140"
---
# <a name="iinkanalyzergetdirtyregion-method"></a><span data-ttu-id="23f9a-103">Метод Иинканализер:: Жетдиртирегион</span><span class="sxs-lookup"><span data-stu-id="23f9a-103">IInkAnalyzer::GetDirtyRegion method</span></span>

<span data-ttu-id="23f9a-104">Извлекает область, которая изменилась со времени последнего выполнения операции анализа.</span><span class="sxs-lookup"><span data-stu-id="23f9a-104">Retrieves the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23f9a-105">Syntax</span></span>


```C++
HRESULT GetDirtyRegion(
  [out] IAnalysisRegion **ppDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="23f9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="23f9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f9a-107">*ппдиртирегион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="23f9a-107">*ppDirtyRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23f9a-108">Объект [**ианалисисрегион**](ianalysisregion.md) , описывающий область, измененную с момента последнего выполнения операции анализа.</span><span class="sxs-lookup"><span data-stu-id="23f9a-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f9a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23f9a-109">Return value</span></span>

<span data-ttu-id="23f9a-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="23f9a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23f9a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23f9a-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="23f9a-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппдиртирегион* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="23f9a-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppDirtyRegion* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="23f9a-113">Этот метод определяет области, которые необходимо проанализировать или повторно проанализировать.</span><span class="sxs-lookup"><span data-stu-id="23f9a-113">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="23f9a-114">Все методы [**иинканализер**](iinkanalyzer.md) , которые добавляют, обновляют или удаляют данные обводки, обновляют «грязную» область.</span><span class="sxs-lookup"><span data-stu-id="23f9a-114">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="23f9a-115">Чтобы вручную пометить область для переанализа:</span><span class="sxs-lookup"><span data-stu-id="23f9a-115">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="23f9a-116">Получите "грязную" область с помощью **метода иинканализер:: жетдиртирегион**.</span><span class="sxs-lookup"><span data-stu-id="23f9a-116">Get the dirty region using **IInkAnalyzer::GetDirtyRegion Method**.</span></span>
2.  <span data-ttu-id="23f9a-117">Используйте [**метод ианалисисрегион:: унионрегион**](ianalysisregion-unionregion.md) или [**метод Ианалисисрегион:: унионректангле**](ianalysisregion-unionrectangle.md) для добавления области в регион из шага 1.</span><span class="sxs-lookup"><span data-stu-id="23f9a-117">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="23f9a-118">Чтобы обновить "грязную" область, используйте [**метод иинканализер:: сетдиртирегион**](iinkanalyzer-setdirtyregion.md) .</span><span class="sxs-lookup"><span data-stu-id="23f9a-118">Use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to update the dirty region.</span></span>

<span data-ttu-id="23f9a-119">[**Иинканализер**](iinkanalyzer.md) анализирует рукописный ввод в своей «грязной» области во время вызова метода [**Иинканализер:: Analyze**](iinkanalyzer-analyze.md) или [**иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="23f9a-119">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="23f9a-120">Однако **иинканализер** может расширить операцию анализа, включив в нее соседние регионы.</span><span class="sxs-lookup"><span data-stu-id="23f9a-120">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="23f9a-121">Это свойство может содержать несмежные области.</span><span class="sxs-lookup"><span data-stu-id="23f9a-121">This property may contain nonadjacent areas.</span></span>

<span data-ttu-id="23f9a-122">Используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память из массива *ппдиртирегион* по завершении работы с ним.</span><span class="sxs-lookup"><span data-stu-id="23f9a-122">Use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory from the *ppDirtyRegion* array when you are finished with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="23f9a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="23f9a-123">Requirements</span></span>



| <span data-ttu-id="23f9a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="23f9a-124">Requirement</span></span> | <span data-ttu-id="23f9a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="23f9a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23f9a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23f9a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="23f9a-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="23f9a-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="23f9a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23f9a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="23f9a-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="23f9a-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="23f9a-130">Header</span><span class="sxs-lookup"><span data-stu-id="23f9a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="23f9a-131"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="23f9a-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="23f9a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="23f9a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23f9a-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23f9a-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="23f9a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23f9a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f9a-135">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="23f9a-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="23f9a-136">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="23f9a-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="23f9a-137">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="23f9a-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="23f9a-138">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="23f9a-138">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="23f9a-139">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="23f9a-139">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="23f9a-140">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="23f9a-140">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="23f9a-141">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="23f9a-141">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="23f9a-142">**Метод Иинканализер:: Ремовестроке**</span><span class="sxs-lookup"><span data-stu-id="23f9a-142">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="23f9a-143">**Метод Иинканализер:: Ремовестрокес**</span><span class="sxs-lookup"><span data-stu-id="23f9a-143">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="23f9a-144">**Метод Иинканализер:: Упдатестрокесдата**</span><span class="sxs-lookup"><span data-stu-id="23f9a-144">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="23f9a-145">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="23f9a-145">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

