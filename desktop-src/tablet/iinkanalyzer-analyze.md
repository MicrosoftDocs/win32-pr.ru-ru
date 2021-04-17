---
description: Выполняет синхронный анализ рукописного ввода.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'Метод Иинканализер:: Analyze (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711118"
---
# <a name="iinkanalyzeranalyze-method"></a><span data-ttu-id="e09b3-103">Метод Иинканализер:: Analyze</span><span class="sxs-lookup"><span data-stu-id="e09b3-103">IInkAnalyzer::Analyze method</span></span>

<span data-ttu-id="e09b3-104">Выполняет синхронный анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="e09b3-104">Performs synchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="e09b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e09b3-105">Syntax</span></span>


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a><span data-ttu-id="e09b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e09b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e09b3-107">*ппстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e09b3-107">*ppStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e09b3-108">Указатель на [**ианалисисстатус**](ianalysisstatus.md) , описывающий состояние операции анализа.</span><span class="sxs-lookup"><span data-stu-id="e09b3-108">A pointer to an [**IAnalysisStatus**](ianalysisstatus.md) that describes the status of the analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e09b3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e09b3-109">Return value</span></span>

<span data-ttu-id="e09b3-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e09b3-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e09b3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e09b3-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e09b3-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппстатус* , когда больше не нужно использовать состояние анализа.</span><span class="sxs-lookup"><span data-stu-id="e09b3-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppStatus* when you no longer need to use the analysis status.</span></span>

 

<span data-ttu-id="e09b3-113">Этот метод запускает синхронную операцию анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="e09b3-113">This method starts a synchronous ink analysis operation.</span></span> <span data-ttu-id="e09b3-114">Анализ рукописного ввода включает в себя анализ макета, классификацию записи и рисования, а также распознавание рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="e09b3-114">Ink analysis includes layout analysis, writing and drawing classification, and handwriting recognition.</span></span> <span data-ttu-id="e09b3-115">Этот метод возвращает значение после завершения операции анализа.</span><span class="sxs-lookup"><span data-stu-id="e09b3-115">This method returns after the analysis operation is complete.</span></span>

<span data-ttu-id="e09b3-116">Этот метод возвращает **\_ указатель E** , если *ппстатус* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e09b3-116">This method returns **E\_POINTER** if *ppStatus* is **NULL**.</span></span>

<span data-ttu-id="e09b3-117">При вызове метода **иинканализер:: Analyze** или [**Иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md) [**иинканализер**](iinkanalyzer.md) анализирует рукописный ввод в пределах его «грязной» области (см. [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="e09b3-117">During a call to **IInkAnalyzer::Analyze Method** or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), the [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span> <span data-ttu-id="e09b3-118">Однако **иинканализер** может расширить операцию анализа, включив в нее соседние регионы.</span><span class="sxs-lookup"><span data-stu-id="e09b3-118">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="e09b3-119">Этот метод задает для "грязной" области объекта [**иинканализер**](iinkanalyzer.md) пустую область.</span><span class="sxs-lookup"><span data-stu-id="e09b3-119">This method sets the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region to an empty region.</span></span> <span data-ttu-id="e09b3-120">Если другой поток добавил данные Stroke, которые не были проанализированы, **иинканализер** добавляет ограничивающий прямоугольник необработанных штрихов в свою «грязную» область на этапе согласования анализа.</span><span class="sxs-lookup"><span data-stu-id="e09b3-120">If another thread has added stroke data that has not been analyzed, the **IInkAnalyzer** adds the bounding box of the unanalyzed strokes to its dirty region during the reconcile phase of the analysis.</span></span>

<span data-ttu-id="e09b3-121">Этот метод возвращает ошибку, если приложение не обрабатывает событие [**\_ ианалисисевентс:: упдатестрокескаче**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="e09b3-121">This method returns an error if your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

<span data-ttu-id="e09b3-122">[**Иинканализер**](iinkanalyzer.md) не вызывает события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) и [**\_ ианалисисевентс:: интермедиатересултс**](-ianalysisevents-intermediateresults.md) в ответ на этот метод.</span><span class="sxs-lookup"><span data-stu-id="e09b3-122">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) events in response to this method.</span></span>

<span data-ttu-id="e09b3-123">Чтобы изменить способ выполнения анализа рукописного ввода, используйте [**метод иинканализер:: сетаналисисмодес**](iinkanalyzer-setanalysismodes.md).</span><span class="sxs-lookup"><span data-stu-id="e09b3-123">To modify the way ink analysis is performed, use [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md).</span></span>

<span data-ttu-id="e09b3-124">Дополнительные сведения о анализе рукописного ввода см. в разделе [Общие сведения об анализе рукописного текста](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e09b3-124">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e09b3-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="e09b3-125">Examples</span></span>

<span data-ttu-id="e09b3-126">В следующем примере выполняется фоновый анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="e09b3-126">The following example performs foreground ink analysis.</span></span>


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="e09b3-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e09b3-127">Requirements</span></span>



| <span data-ttu-id="e09b3-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e09b3-128">Requirement</span></span> | <span data-ttu-id="e09b3-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e09b3-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e09b3-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e09b3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e09b3-131">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e09b3-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e09b3-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e09b3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e09b3-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e09b3-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e09b3-134">Header</span><span class="sxs-lookup"><span data-stu-id="e09b3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e09b3-135"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e09b3-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e09b3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e09b3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e09b3-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e09b3-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e09b3-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e09b3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e09b3-139">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="e09b3-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e09b3-140">**аналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="e09b3-140">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="e09b3-141">**Метод Иинканализер:: Жетдиртирегион**</span><span class="sxs-lookup"><span data-stu-id="e09b3-141">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="e09b3-142">**Метод Иинканализер:: Сетдиртирегион**</span><span class="sxs-lookup"><span data-stu-id="e09b3-142">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="e09b3-143">**Метод Иинканализер:: Жетрутноде**</span><span class="sxs-lookup"><span data-stu-id="e09b3-143">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="e09b3-144">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="e09b3-144">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

