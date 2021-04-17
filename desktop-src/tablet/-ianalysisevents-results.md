---
description: Происходит после завершения заключительного этапа анализа.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: 'Событие _IAnalysisEvents:: Results (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693903"
---
# <a name="_ianalysiseventsresults-event"></a><span data-ttu-id="5cfc1-103">\_Событие Ианалисисевентс:: Results</span><span class="sxs-lookup"><span data-stu-id="5cfc1-103">\_IAnalysisEvents::Results event</span></span>

<span data-ttu-id="5cfc1-104">Происходит после завершения заключительного этапа анализа.</span><span class="sxs-lookup"><span data-stu-id="5cfc1-104">Occurs when the final analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cfc1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cfc1-105">Syntax</span></span>


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5cfc1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5cfc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cfc1-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5cfc1-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cfc1-108">[**Иинканализер**](iinkanalyzer.md) , создающая результаты анализа.</span><span class="sxs-lookup"><span data-stu-id="5cfc1-108">The [**IInkAnalyzer**](iinkanalyzer.md) that produces the analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="5cfc1-109">*паналисисстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5cfc1-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cfc1-110">Объект [**ианалисисстатус**](ianalysisstatus.md) , представляющий состояние анализа.</span><span class="sxs-lookup"><span data-stu-id="5cfc1-110">The [**IAnalysisStatus**](ianalysisstatus.md) object that represents the status of the analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cfc1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5cfc1-111">Return value</span></span>

<span data-ttu-id="5cfc1-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5cfc1-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5cfc1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5cfc1-113">Remarks</span></span>

<span data-ttu-id="5cfc1-114">[**Иинканализер**](iinkanalyzer.md) создает это событие после того, как оно выверят результаты для этапа окончательного анализа.</span><span class="sxs-lookup"><span data-stu-id="5cfc1-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the results for the final analysis stage.</span></span>

<span data-ttu-id="5cfc1-115">Если приложение вызывает [**метод иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md), это событие сигнализирует о готовности результатов анализа.</span><span class="sxs-lookup"><span data-stu-id="5cfc1-115">If your application calls [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), this event signals when analysis results are ready.</span></span>

<span data-ttu-id="5cfc1-116">Если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md), это событие указывает, что **иинканализер** завершил внесение изменений во внутренние данные для этого этапа анализа.</span><span class="sxs-lookup"><span data-stu-id="5cfc1-116">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="5cfc1-117">Заблокируйте структуру данных, когда [**иинканализер**](iinkanalyzer.md) вызывает событие [**\_ ианалисиспроксевентс:: инканализерстатечангинг**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="5cfc1-117">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="5cfc1-118">Внесение изменений в структуру данных на этом этапе анализа может привести к ошибкам при анализе и синхронизации рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="5cfc1-118">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="5cfc1-119">Разблокируйте структуру данных, когда **иинканализер** вызывает событие [**\_ ианалисисевентс:: интермедиатересултс**](-ianalysisevents-intermediateresults.md) или **\_ ианалисисевентс:: Results** .</span><span class="sxs-lookup"><span data-stu-id="5cfc1-119">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or **\_IAnalysisEvents::Results** event.</span></span>

<span data-ttu-id="5cfc1-120">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5cfc1-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cfc1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5cfc1-121">Requirements</span></span>



| <span data-ttu-id="5cfc1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5cfc1-122">Requirement</span></span> | <span data-ttu-id="5cfc1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5cfc1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cfc1-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5cfc1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5cfc1-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5cfc1-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5cfc1-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5cfc1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5cfc1-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5cfc1-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5cfc1-128">Header</span><span class="sxs-lookup"><span data-stu-id="5cfc1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cfc1-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5cfc1-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5cfc1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5cfc1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cfc1-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cfc1-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5cfc1-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cfc1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cfc1-133">**\_ианалисисевентс**</span><span class="sxs-lookup"><span data-stu-id="5cfc1-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="5cfc1-134">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="5cfc1-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="5cfc1-135">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="5cfc1-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5cfc1-136">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="5cfc1-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="5cfc1-137">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="5cfc1-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="5cfc1-138">**ианалисисстатус**</span><span class="sxs-lookup"><span data-stu-id="5cfc1-138">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="5cfc1-139">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="5cfc1-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




