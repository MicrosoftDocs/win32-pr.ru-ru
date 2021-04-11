---
description: Происходит, когда Иинканализер готова к согласованию результатов своего фонового анализа с текущим состоянием.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: 'Событие _IAnalysisEvents:: РеадитореконЦиле (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273313"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a><span data-ttu-id="1fc17-103">\_Событие Ианалисисевентс:: РеадитореконЦиле</span><span class="sxs-lookup"><span data-stu-id="1fc17-103">\_IAnalysisEvents::ReadyToReconcile event</span></span>

<span data-ttu-id="1fc17-104">Происходит, когда [**иинканализер**](iinkanalyzer.md) готова к согласованию результатов своего фонового анализа с текущим состоянием.</span><span class="sxs-lookup"><span data-stu-id="1fc17-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc17-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fc17-105">Syntax</span></span>


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a><span data-ttu-id="1fc17-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1fc17-106">Parameters</span></span>

<span data-ttu-id="1fc17-107">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="1fc17-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1fc17-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1fc17-108">Return value</span></span>

<span data-ttu-id="1fc17-109">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1fc17-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc17-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1fc17-110">Remarks</span></span>

<span data-ttu-id="1fc17-111">[**Иинканализер**](iinkanalyzer.md) выполняет автоматическую выверку, если установлен флаг **аналисисмодес \_ аутоматикреконЦилиатион** анализатора рукописного ввода (см. [**метод иинканализер:: сетаналисисмодес**](iinkanalyzer-setanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="1fc17-111">The [**IInkAnalyzer**](iinkanalyzer.md) performs automatic reconciliation when the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag is set (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)).</span></span> <span data-ttu-id="1fc17-112">Если флаг **аналисисмодес \_ аутоматикреконЦилиатион** не установлен, приложение должно выполнить согласование результатов фонового анализа вручную.</span><span class="sxs-lookup"><span data-stu-id="1fc17-112">When the **AnalysisModes\_AutomaticReconciliation** flag is not set, your application needs to reconcile background analysis results manually.</span></span>

<span data-ttu-id="1fc17-113">Чтобы выполнить выверку вручную, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1fc17-113">To perform manual reconciliation, follow these steps.</span></span>

1.  <span data-ttu-id="1fc17-114">Снимите флаг **аналисисмодес \_ аутоматикреконЦилиатион** анализатора рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="1fc17-114">Clear the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag.</span></span>
2.  <span data-ttu-id="1fc17-115">Обработайте событие **\_ ианалисисевентс:: реадитореконЦиле** .</span><span class="sxs-lookup"><span data-stu-id="1fc17-115">Handle the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>
3.  <span data-ttu-id="1fc17-116">Чтобы согласовать результаты анализа, вызовите метод [**иинканализер:: Reconcile**](iinkanalyzer-reconcile.md) из обработчика событий для события **\_ ианалисисевентс:: реадитореконЦиле** .</span><span class="sxs-lookup"><span data-stu-id="1fc17-116">To reconcile the analysis results, call the [**IInkAnalyzer::Reconcile Method**](iinkanalyzer-reconcile.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span> <span data-ttu-id="1fc17-117">Чтобы отменить текущую операцию фонового анализа, вызовите метод [**метода иинканализер:: Abort**](iinkanalyzer-abort.md) из обработчика событий для события **\_ ианалисисевентс:: реадитореконЦиле** .</span><span class="sxs-lookup"><span data-stu-id="1fc17-117">To cancel the current background analysis operation, call the [**IInkAnalyzer::Abort Method**](iinkanalyzer-abort.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>

<span data-ttu-id="1fc17-118">[**Иинканализер**](iinkanalyzer.md) вызывает это событие до того, как оно вызовет событие [**\_ ианалисиспроксевентс:: инканализерстатечангинг**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc17-118">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event before it raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span>

<span data-ttu-id="1fc17-119">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1fc17-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="1fc17-120">[**Иинканализер**](iinkanalyzer.md) вызывает это событие во время фонового анализа.</span><span class="sxs-lookup"><span data-stu-id="1fc17-120">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during background analysis.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc17-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1fc17-121">Requirements</span></span>



| <span data-ttu-id="1fc17-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1fc17-122">Requirement</span></span> | <span data-ttu-id="1fc17-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1fc17-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc17-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fc17-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc17-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1fc17-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1fc17-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fc17-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc17-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1fc17-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1fc17-128">Header</span><span class="sxs-lookup"><span data-stu-id="1fc17-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fc17-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1fc17-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1fc17-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1fc17-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fc17-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fc17-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1fc17-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fc17-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc17-133">**\_ианалисисевентс**</span><span class="sxs-lookup"><span data-stu-id="1fc17-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="1fc17-134">**аналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="1fc17-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="1fc17-135">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="1fc17-135">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="1fc17-136">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="1fc17-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1fc17-137">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="1fc17-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="1fc17-138">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="1fc17-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="1fc17-139">**Метод Иинканализер:: Reconcile**</span><span class="sxs-lookup"><span data-stu-id="1fc17-139">**IInkAnalyzer::Reconcile Method**</span></span>](iinkanalyzer-reconcile.md)
</dt> <dt>

[<span data-ttu-id="1fc17-140">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="1fc17-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




