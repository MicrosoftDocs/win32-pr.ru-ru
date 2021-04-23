---
description: Происходит при завершении текущего промежуточного этапа анализа.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: 'Событие _IAnalysisEvents:: Интермедиатересултс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693900"
---
# <a name="_ianalysiseventsintermediateresults-event"></a><span data-ttu-id="19092-103">\_Событие Ианалисисевентс:: Интермедиатересултс</span><span class="sxs-lookup"><span data-stu-id="19092-103">\_IAnalysisEvents::IntermediateResults event</span></span>

<span data-ttu-id="19092-104">Происходит при завершении текущего промежуточного этапа анализа.</span><span class="sxs-lookup"><span data-stu-id="19092-104">Occurs when the current intermediate analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="19092-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19092-105">Syntax</span></span>


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="19092-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19092-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19092-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19092-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19092-108">[**Иинканализер**](iinkanalyzer.md) , выполняющий анализ.</span><span class="sxs-lookup"><span data-stu-id="19092-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is performing the analysis.</span></span>

</dd> <dt>

<span data-ttu-id="19092-109">*паналисисстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19092-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19092-110">Объект [**ианалисисстатус**](ianalysisstatus.md) , представляющий состояние промежуточных результатов.</span><span class="sxs-lookup"><span data-stu-id="19092-110">The [**IAnalysisStatus**](ianalysisstatus.md) object representing the status of the intermediate results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19092-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19092-111">Return value</span></span>

<span data-ttu-id="19092-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="19092-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="19092-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19092-113">Remarks</span></span>

<span data-ttu-id="19092-114">[**Иинканализер**](iinkanalyzer.md) создает это событие после того, как оно выверят промежуточные результаты для текущего этапа анализа.</span><span class="sxs-lookup"><span data-stu-id="19092-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the intermediate results for the current analysis stage.</span></span>

<span data-ttu-id="19092-115">Если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md), это событие указывает, что **иинканализер** завершил внесение изменений во внутренние данные для этого этапа анализа.</span><span class="sxs-lookup"><span data-stu-id="19092-115">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="19092-116">Заблокируйте структуру данных, когда [**иинканализер**](iinkanalyzer.md) вызывает событие [**\_ ианалисиспроксевентс:: инканализерстатечангинг**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="19092-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="19092-117">Внесение изменений в структуру данных на этом этапе анализа может привести к ошибкам при анализе и синхронизации рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="19092-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="19092-118">Вы можете разблокировать структуру данных, когда **иинканализер** вызывает событие **\_ ианалисисевентс:: интермедиатересултс** или [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="19092-118">You can unlock your data structure when the **IInkAnalyzer** raises the **\_IAnalysisEvents::IntermediateResults** or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="19092-119">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="19092-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="19092-120">[**Иинканализер**](iinkanalyzer.md) создает промежуточные результаты только в том случае, если в его режимах анализа установлен флаг **аналисисмодес \_ Интермедиатересултс** (см. [**метод иинканализер:: жетаналисисмодес**](iinkanalyzer-getanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="19092-120">The [**IInkAnalyzer**](iinkanalyzer.md) generates intermediate results only when its analysis modes has the **AnalysisModes\_IntermediateResults** flag set (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="19092-121">Требования</span><span class="sxs-lookup"><span data-stu-id="19092-121">Requirements</span></span>



| <span data-ttu-id="19092-122">Требование</span><span class="sxs-lookup"><span data-stu-id="19092-122">Requirement</span></span> | <span data-ttu-id="19092-123">Значение</span><span class="sxs-lookup"><span data-stu-id="19092-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19092-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19092-124">Minimum supported client</span></span><br/> | <span data-ttu-id="19092-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="19092-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="19092-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19092-126">Minimum supported server</span></span><br/> | <span data-ttu-id="19092-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="19092-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="19092-128">Header</span><span class="sxs-lookup"><span data-stu-id="19092-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="19092-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="19092-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="19092-130">DLL</span><span class="sxs-lookup"><span data-stu-id="19092-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19092-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19092-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="19092-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19092-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19092-133">**\_ианалисисевентс**</span><span class="sxs-lookup"><span data-stu-id="19092-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="19092-134">**аналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="19092-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="19092-135">**\_Ианалисисевентс:: Results**</span><span class="sxs-lookup"><span data-stu-id="19092-135">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="19092-136">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="19092-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="19092-137">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="19092-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="19092-138">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="19092-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="19092-139">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="19092-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="19092-140">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="19092-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>
