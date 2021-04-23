---
description: 'Применяет результаты фоновой операции анализа рукописного ввода к дереву узлов контекста для частей дерева, которые не были изменены приложением с момента вызова метода Иинканализер:: Баккграунданализе.'
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'Метод Иинканализер:: Reconcile (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647183"
---
# <a name="iinkanalyzerreconcile-method"></a><span data-ttu-id="4824f-103">Метод Иинканализер:: Reconcile</span><span class="sxs-lookup"><span data-stu-id="4824f-103">IInkAnalyzer::Reconcile method</span></span>

<span data-ttu-id="4824f-104">Применяет результаты фоновой операции анализа рукописного ввода к дереву узлов контекста для частей дерева, которые не были изменены приложением с момента вызова [**метода иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="4824f-104">Applies the results of a background ink analysis operation to the context node tree for the portions of the tree that have not been modified by the application since the call to [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4824f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4824f-105">Syntax</span></span>


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a><span data-ttu-id="4824f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4824f-106">Parameters</span></span>

<span data-ttu-id="4824f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4824f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4824f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4824f-108">Return value</span></span>

<span data-ttu-id="4824f-109">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4824f-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4824f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4824f-110">Remarks</span></span>

<span data-ttu-id="4824f-111">По умолчанию [**иинканализер**](iinkanalyzer.md) выполняет этап автоматической сверки непосредственно перед вызовом событий [**\_ ианалисисевентс:: интермедиатересултс**](-ianalysisevents-intermediateresults.md) и [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="4824f-111">By default, the [**IInkAnalyzer**](iinkanalyzer.md) performs an automatic reconciliation phase immediately before raising the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) and [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) events.</span></span>

<span data-ttu-id="4824f-112">Чтобы отключить автоматическую выверку, снимите флажок **аналисисмодес \_ аутоматикреконЦилиатион** в режимах анализа анализатора рукописного ввода (см. [**метод иинканализер:: сетаналисисмодес**](iinkanalyzer-setanalysismodes.md) и [**аналисисмодес**](analysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="4824f-112">To disable automatic reconciliation, clear the **AnalysisModes\_AutomaticReconciliation** flag from the ink analyzer's analysis modes (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md) and [**AnalysisModes**](analysismodes.md)).</span></span> <span data-ttu-id="4824f-113">Метод [**метода иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md) возвращает ошибку, если Автоматическая выверка отключена и приложение не обрабатывает событие [**\_ ианалисисевентс:: реадитореконЦиле**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="4824f-113">The [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method returns an error when automatic reconciliation is disabled and your application does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="4824f-114">Приложение должно вызвать метод **метода иинканализер:: Reconcile** перед тем, как [**иинканализер**](iinkanalyzer.md) сможет продолжить обработку результатов или продолжить анализ соответствующего этапа анализа.</span><span class="sxs-lookup"><span data-stu-id="4824f-114">Your application must call the **IInkAnalyzer::Reconcile Method** method before the [**IInkAnalyzer**](iinkanalyzer.md) can continue to process the results or continue further analysis for the corresponding analysis stage.</span></span>

<span data-ttu-id="4824f-115">Приложение может вносить изменения, такие как добавление или удаление штрихов и изменение данных Stroke, в дереве узлов контекста объекта [**иинканализер**](iinkanalyzer.md) во время фонового анализа.</span><span class="sxs-lookup"><span data-stu-id="4824f-115">Your application can make changes, such as adding or removing strokes and changing stroke data, in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree during background analysis.</span></span> <span data-ttu-id="4824f-116">Такие изменения могут сделать недействительными части результатов фонового анализа.</span><span class="sxs-lookup"><span data-stu-id="4824f-116">Such changes can invalidate portions of the background analysis results.</span></span> <span data-ttu-id="4824f-117">Этот метод применяет результаты анализа только к дереву узлов контекста анализатора для частей дерева, которые приложение не изменило.</span><span class="sxs-lookup"><span data-stu-id="4824f-117">This method applies analysis results only to the analyzer's context node tree for the portions of the tree that your application has not changed.</span></span> <span data-ttu-id="4824f-118">Этот метод также добавляет регионы, содержащие аннулированные результаты анализа, в область "грязного" объекта **иинканализер** (см. [**метод Иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="4824f-118">This method also adds regions containing invalidated analysis results to the **IInkAnalyzer** object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="4824f-119">Дополнительные сведения об использовании для анализа рукописного ввода см. в разделе [Общие сведения о анализе рукописного ввода](ink-analysis-overview.md). [**Аналисисмодес**](analysismodes.md)</span><span class="sxs-lookup"><span data-stu-id="4824f-119">For more information about using the to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).[**AnalysisModes**](analysismodes.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="4824f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4824f-120">Requirements</span></span>



| <span data-ttu-id="4824f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4824f-121">Requirement</span></span> | <span data-ttu-id="4824f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4824f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4824f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4824f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4824f-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4824f-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4824f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4824f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4824f-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4824f-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4824f-127">Header</span><span class="sxs-lookup"><span data-stu-id="4824f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4824f-128"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4824f-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4824f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4824f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4824f-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4824f-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4824f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4824f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4824f-132">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="4824f-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4824f-133">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="4824f-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="4824f-134">**\_Ианалисисевентс:: РеадитореконЦиле**</span><span class="sxs-lookup"><span data-stu-id="4824f-134">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="4824f-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="4824f-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




