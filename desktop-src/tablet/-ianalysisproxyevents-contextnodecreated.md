---
description: Происходит после того, как Иинканализер создает объект Иконтекстноде.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: 'Событие _IAnalysisProxyEvents:: Контекстнодекреатед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104000001"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a><span data-ttu-id="86382-103">\_Событие Ианалисиспроксевентс:: Контекстнодекреатед</span><span class="sxs-lookup"><span data-stu-id="86382-103">\_IAnalysisProxyEvents::ContextNodeCreated event</span></span>

<span data-ttu-id="86382-104">Происходит после того, как [**иинканализер**](iinkanalyzer.md) создает объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="86382-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="86382-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86382-105">Syntax</span></span>


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="86382-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86382-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86382-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86382-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86382-108">[**Иинканализер**](iinkanalyzer.md) , создающий объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="86382-108">The [**IInkAnalyzer**](iinkanalyzer.md) creating the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="86382-109">*пконтекстнодекреатед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86382-109">*pContextNodeCreated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86382-110">Новый объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="86382-110">The new [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86382-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86382-111">Return value</span></span>

<span data-ttu-id="86382-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="86382-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="86382-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86382-113">Remarks</span></span>

<span data-ttu-id="86382-114">Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="86382-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="86382-115">Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод анализа рукописного ввода, создающий [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="86382-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that creates an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="86382-116">Когда [**иинканализер**](iinkanalyzer.md) создает [**Иконтекстноде**](icontextnode.md), новый **иконтекстноде** не содержит штрихов, не содержит ссылок на другие объекты **иконтекстноде** и может иметь не все заданные свойства.</span><span class="sxs-lookup"><span data-stu-id="86382-116">When the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md), the new **IContextNode** does not contain any strokes, does not contain links to other **IContextNode** objects, and may not have all of its properties set.</span></span> <span data-ttu-id="86382-117">Кроме того, новый **иконтекстноде** добавляется в конец коллекции подузлов его родительского узла (см. раздел [**Иконтекстноде:: жетпарентноде**](icontextnode-getparentnode.md) and [**иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="86382-117">Also, the new **IContextNode** is added to the end of its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="86382-118">После этого события **иинканализер** может вызвать следующие события.</span><span class="sxs-lookup"><span data-stu-id="86382-118">After this event, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="86382-119">Событие [**\_ ианалисиспроксевентс:: строкерепарентед**](-ianalysisproxyevents-strokereparented.md) при перемещении штриха из одного контекстного узла в другой.</span><span class="sxs-lookup"><span data-stu-id="86382-119">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from one context node to another.</span></span>
-   <span data-ttu-id="86382-120">Событие [**\_ ианалисиспроксевентс:: контекстноделинкаддинг**](-ianalysisproxyevents-contextnodelinkadding.md) при добавлении [**иконтекстлинк**](icontextlink.md) в [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="86382-120">The [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) event when it adds an [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="86382-121">Событие [**\_ ианалисиспроксевентс:: контекстнодемовингтопоситион**](-ianalysisproxyevents-contextnodemovingtoposition.md) при изменении порядка [**иконтекстноде**](icontextnode.md) в коллекции подузлов его родительского узла.</span><span class="sxs-lookup"><span data-stu-id="86382-121">The [**\_IAnalysisProxyEvents::ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) event when it changes the order of an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes.</span></span>
-   <span data-ttu-id="86382-122">[**Иинканализер**](iinkanalyzer.md) вызывает событие [**\_ ианалисиспроксевентс:: контекстнодепропертиесупдатед**](-ianalysisproxyevents-contextnodepropertiesupdated.md) после того, как оно разрешит состояние [**иконтекстноде**](icontextnode.md) для этого этапа анализа.</span><span class="sxs-lookup"><span data-stu-id="86382-122">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) event after it resolves the state of the [**IContextNode**](icontextnode.md) for this analysis phase.</span></span>

<span data-ttu-id="86382-123">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="86382-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86382-124">Требования</span><span class="sxs-lookup"><span data-stu-id="86382-124">Requirements</span></span>



| <span data-ttu-id="86382-125">Требование</span><span class="sxs-lookup"><span data-stu-id="86382-125">Requirement</span></span> | <span data-ttu-id="86382-126">Значение</span><span class="sxs-lookup"><span data-stu-id="86382-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86382-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86382-127">Minimum supported client</span></span><br/> | <span data-ttu-id="86382-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="86382-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="86382-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86382-129">Minimum supported server</span></span><br/> | <span data-ttu-id="86382-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="86382-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="86382-131">Header</span><span class="sxs-lookup"><span data-stu-id="86382-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="86382-132"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="86382-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="86382-133">DLL</span><span class="sxs-lookup"><span data-stu-id="86382-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86382-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86382-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="86382-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86382-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86382-136">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="86382-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="86382-137">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="86382-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="86382-138">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="86382-138">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="86382-139">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="86382-139">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="86382-140">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="86382-140">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="86382-141">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="86382-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




