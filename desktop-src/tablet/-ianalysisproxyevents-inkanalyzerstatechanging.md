---
description: Происходит перед тем, как Иинканализер согласовывает результаты анализа, чтобы приложение могла синхронизировать данные с Иинканализер.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: 'Событие _IAnalysisProxyEvents:: Инканализерстатечангинг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703496"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a><span data-ttu-id="f6db3-103">\_Событие Ианалисиспроксевентс:: Инканализерстатечангинг</span><span class="sxs-lookup"><span data-stu-id="f6db3-103">\_IAnalysisProxyEvents::InkAnalyzerStateChanging event</span></span>

<span data-ttu-id="f6db3-104">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) согласовывает результаты анализа, чтобы приложение могла синхронизировать данные с **иинканализер**.</span><span class="sxs-lookup"><span data-stu-id="f6db3-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6db3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6db3-105">Syntax</span></span>


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a><span data-ttu-id="f6db3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6db3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6db3-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6db3-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6db3-108">[**Иинканализер**](iinkanalyzer.md) , который собирается согласовать результаты анализа.</span><span class="sxs-lookup"><span data-stu-id="f6db3-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is about to reconcile its analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6db3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6db3-109">Return value</span></span>

<span data-ttu-id="f6db3-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f6db3-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f6db3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6db3-111">Remarks</span></span>

<span data-ttu-id="f6db3-112">Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="f6db3-112">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="f6db3-113">Когда **иинканализер** вызывает это событие, приложение должно заполнить подузлы корневого узла анализатора красок (см. раздел [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) and [**иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="f6db3-113">When the **IInkAnalyzer** raises this event, your application should populate the subnodes of the ink analyzer's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="f6db3-114">[**Иинканализер**](iinkanalyzer.md) вызывает это событие после того, как оно вызывает событие [**\_ ианалисисевентс:: реадитореконЦиле**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="f6db3-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="f6db3-115">Он вызывает это событие только при выполнении фонового анализа.</span><span class="sxs-lookup"><span data-stu-id="f6db3-115">It raises this event only while performing background analysis.</span></span>

<span data-ttu-id="f6db3-116">Заблокируйте структуру данных, когда [**иинканализер**](iinkanalyzer.md) вызывает событие **\_ ианалисиспроксевентс:: инканализерстатечангинг** .</span><span class="sxs-lookup"><span data-stu-id="f6db3-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the **\_IAnalysisProxyEvents::InkAnalyzerStateChanging** event.</span></span> <span data-ttu-id="f6db3-117">Внесение изменений в структуру данных на этом этапе анализа может привести к ошибкам при анализе и синхронизации рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="f6db3-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="f6db3-118">Разблокируйте структуру данных, когда **иинканализер** вызывает событие [**\_ ианалисисевентс:: интермедиатересултс**](-ianalysisevents-intermediateresults.md) или [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="f6db3-118">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="f6db3-119">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f6db3-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6db3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f6db3-120">Requirements</span></span>



| <span data-ttu-id="f6db3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f6db3-121">Requirement</span></span> | <span data-ttu-id="f6db3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f6db3-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6db3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6db3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f6db3-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f6db3-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f6db3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6db3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f6db3-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6db3-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f6db3-127">Header</span><span class="sxs-lookup"><span data-stu-id="f6db3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6db3-128"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f6db3-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f6db3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f6db3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6db3-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6db3-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f6db3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6db3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6db3-132">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="f6db3-132">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="f6db3-133">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="f6db3-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f6db3-134">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="f6db3-134">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f6db3-135">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="f6db3-135">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="f6db3-136">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="f6db3-136">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="f6db3-137">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="f6db3-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




