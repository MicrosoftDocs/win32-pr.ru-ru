---
description: Выполняет асинхронный анализ рукописного ввода.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'Метод Иинканализер:: Баккграунданализе (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542031"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a><span data-ttu-id="15dfb-103">Метод Иинканализер:: Баккграунданализе</span><span class="sxs-lookup"><span data-stu-id="15dfb-103">IInkAnalyzer::BackgroundAnalyze method</span></span>

<span data-ttu-id="15dfb-104">Выполняет асинхронный анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="15dfb-104">Performs asynchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="15dfb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15dfb-105">Syntax</span></span>


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a><span data-ttu-id="15dfb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15dfb-106">Parameters</span></span>

<span data-ttu-id="15dfb-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="15dfb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15dfb-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15dfb-108">Return value</span></span>

<span data-ttu-id="15dfb-109">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="15dfb-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="15dfb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15dfb-110">Remarks</span></span>

<span data-ttu-id="15dfb-111">При вызове этого метода [**иинканализер**](iinkanalyzer.md) выполняет анализ рукописного ввода в фоновом потоке.</span><span class="sxs-lookup"><span data-stu-id="15dfb-111">When this method is called, the [**IInkAnalyzer**](iinkanalyzer.md) performs the ink analysis on a background thread.</span></span>

<span data-ttu-id="15dfb-112">Этот метод возвращает **\_ значение false** и не запускает новую операцию фонового анализа в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="15dfb-112">This method returns **S\_FALSE** and does not start a new background analysis operation under the following circumstances.</span></span>

-   <span data-ttu-id="15dfb-113">[**Иинканализер**](iinkanalyzer.md) сейчас выполняет фоновый анализ.</span><span class="sxs-lookup"><span data-stu-id="15dfb-113">The [**IInkAnalyzer**](iinkanalyzer.md) is currently performing background analysis.</span></span>
-   <span data-ttu-id="15dfb-114">"грязный" регион (см. [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)) представляет собой пустую область.</span><span class="sxs-lookup"><span data-stu-id="15dfb-114">the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) represents an empty area.</span></span>

<span data-ttu-id="15dfb-115">[**Иинканализер**](iinkanalyzer.md) анализирует рукописный ввод в своей «грязной» области во время вызова метода [**Иинканализер:: Analyze**](iinkanalyzer-analyze.md) или **иинканализер:: баккграунданализе**.</span><span class="sxs-lookup"><span data-stu-id="15dfb-115">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or **IInkAnalyzer::BackgroundAnalyze Method**.</span></span> <span data-ttu-id="15dfb-116">Однако **иинканализер** может расширить операцию анализа, включив в нее соседние регионы.</span><span class="sxs-lookup"><span data-stu-id="15dfb-116">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="15dfb-117">Этот метод задает для "грязной" области пустой регион.</span><span class="sxs-lookup"><span data-stu-id="15dfb-117">This method sets the dirty region to an empty region.</span></span>

<span data-ttu-id="15dfb-118">Если данные Stroke были добавлены в [**иинканализер**](iinkanalyzer.md) после вызова **метода Иинканализер:: баккграунданализе**, **иинканализер** может обновить "грязную" область на этапе согласования анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="15dfb-118">If stroke data was added to the [**IInkAnalyzer**](iinkanalyzer.md) after the call to **IInkAnalyzer::BackgroundAnalyze Method**, the **IInkAnalyzer** may update the dirty region during the reconcile phase of ink analysis.</span></span>

<span data-ttu-id="15dfb-119">Настройка режимов анализа (см. [**метод иинканализер:: жетаналисисмодес**](iinkanalyzer-getanalysismodes.md)) указывает, как [**иинканализер**](iinkanalyzer.md) выполняет фоновый анализ.</span><span class="sxs-lookup"><span data-stu-id="15dfb-119">The analysis modes setting (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)) specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs background analysis.</span></span> <span data-ttu-id="15dfb-120">Дополнительные сведения о анализе рукописного ввода см. в разделе [Общие сведения об анализе рукописного текста](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="15dfb-120">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

<span data-ttu-id="15dfb-121">Этот метод возвращает код ошибки при следующих обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="15dfb-121">This method returns an error code under the following circumstances.</span></span>

-   <span data-ttu-id="15dfb-122">Приложение установило значение [**Аналисисмодес**](analysismodes.md) **Аналисисмодес \_ интермедиатересултс** в [**иинканализер**](iinkanalyzer.md) (см. [**метод иинканализер:: сетаналисисмодес**](iinkanalyzer-setanalysismodes.md)) и не обрабатывает событие [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) .</span><span class="sxs-lookup"><span data-stu-id="15dfb-122">Your application has set [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_IntermediateResults** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) event.</span></span>
-   <span data-ttu-id="15dfb-123">Приложение очистило значение [**Аналисисмодес**](analysismodes.md) **Аналисисмодес \_ аутоматикреконЦилиатион** в [**иинканализер**](iinkanalyzer.md) (см. [**метод иинканализер:: сетаналисисмодес**](iinkanalyzer-setanalysismodes.md)) и не обрабатывает событие [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="15dfb-123">Your application has cleared [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_AutomaticReconciliation** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>
-   <span data-ttu-id="15dfb-124">Приложение не обрабатывает событие [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="15dfb-124">Your application does not handle the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>
-   <span data-ttu-id="15dfb-125">Приложение не обрабатывает событие [**\_ ианалисисевентс:: упдатестрокескаче**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="15dfb-125">Your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

## <a name="examples"></a><span data-ttu-id="15dfb-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="15dfb-126">Examples</span></span>

<span data-ttu-id="15dfb-127">В следующем примере проверяется «грязный» регион анализатора рукописного ввода, а затем инициируется фоновый анализ рукописного ввода, если «грязная» область не пуста.</span><span class="sxs-lookup"><span data-stu-id="15dfb-127">The following example checks the ink analyzer's dirty region, and then initiates background ink analysis if the dirty region is not empty.</span></span>


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
}
```



## <a name="requirements"></a><span data-ttu-id="15dfb-128">Требования</span><span class="sxs-lookup"><span data-stu-id="15dfb-128">Requirements</span></span>



| <span data-ttu-id="15dfb-129">Требование</span><span class="sxs-lookup"><span data-stu-id="15dfb-129">Requirement</span></span> | <span data-ttu-id="15dfb-130">Значение</span><span class="sxs-lookup"><span data-stu-id="15dfb-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15dfb-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15dfb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="15dfb-132">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="15dfb-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="15dfb-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15dfb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="15dfb-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="15dfb-134">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="15dfb-135">Header</span><span class="sxs-lookup"><span data-stu-id="15dfb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="15dfb-136"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="15dfb-136"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="15dfb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="15dfb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15dfb-138"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15dfb-138"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="15dfb-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15dfb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15dfb-140">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="15dfb-140">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="15dfb-141">**аналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="15dfb-141">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="15dfb-142">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="15dfb-142">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="15dfb-143">**Метод Иинканализер:: Жетаналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="15dfb-143">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="15dfb-144">**Метод Иинканализер:: Сетаналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="15dfb-144">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="15dfb-145">**Метод Иинканализер:: Жетдиртирегион**</span><span class="sxs-lookup"><span data-stu-id="15dfb-145">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="15dfb-146">**Метод Иинканализер:: Сетдиртирегион**</span><span class="sxs-lookup"><span data-stu-id="15dfb-146">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="15dfb-147">**Метод Иинканализер:: Жетрутноде**</span><span class="sxs-lookup"><span data-stu-id="15dfb-147">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="15dfb-148">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="15dfb-148">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




