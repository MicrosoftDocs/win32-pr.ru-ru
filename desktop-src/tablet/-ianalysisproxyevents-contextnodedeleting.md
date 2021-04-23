---
description: Происходит перед тем, как Иинканализер удаляет объект Иконтекстноде.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: 'Событие _IAnalysisProxyEvents:: Контекстнодеделетинг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703501"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a><span data-ttu-id="1c159-103">\_Событие Ианалисиспроксевентс:: Контекстнодеделетинг</span><span class="sxs-lookup"><span data-stu-id="1c159-103">\_IAnalysisProxyEvents::ContextNodeDeleting event</span></span>

<span data-ttu-id="1c159-104">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) удаляет объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1c159-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c159-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c159-105">Syntax</span></span>


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="1c159-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c159-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c159-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c159-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c159-108">Объект [**иинканализер**](iinkanalyzer.md) , удаляющий объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1c159-108">The [**IInkAnalyzer**](iinkanalyzer.md) object deleting the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="1c159-109">*пконтекстнодетобеделетед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c159-109">*pContextNodeToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c159-110">Удаляемый объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1c159-110">The [**IContextNode**](icontextnode.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c159-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c159-111">Return value</span></span>

<span data-ttu-id="1c159-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1c159-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c159-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c159-113">Remarks</span></span>

<span data-ttu-id="1c159-114">Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="1c159-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="1c159-115">Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод анализа рукописного ввода, который удаляет [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="1c159-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that deletes an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="1c159-116">Перед тем как [**иинканализер**](iinkanalyzer.md) удалит [**иконтекстноде**](icontextnode.md), **иинканализер** удаляет все штрихи из контекстного узла и удаляет все ссылки на другие контекстные узлы.</span><span class="sxs-lookup"><span data-stu-id="1c159-116">Before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md), the **IInkAnalyzer** removes all of the strokes from the context node and removes all of the links to other context nodes.</span></span> <span data-ttu-id="1c159-117">Перед удалением узла контекста **иинканализер** может вызвать следующие события.</span><span class="sxs-lookup"><span data-stu-id="1c159-117">Before the context node is removed, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="1c159-118">Событие [**\_ ианалисиспроксевентс:: строкерепарентед**](-ianalysisproxyevents-strokereparented.md) при перемещении штриха из [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="1c159-118">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="1c159-119">Событие [**\_ ианалисиспроксевентс:: контекстноделинкделетинг**](-ianalysisproxyevents-contextnodelinkdeleting.md) перед удалением [**иконтекстлинк**](icontextlink.md) из [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="1c159-119">The [**\_IAnalysisProxyEvents::ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) event before it removes a [**IContextLink**](icontextlink.md) from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="1c159-120">Событие **\_ ианалисиспроксевентс:: контекстнодеделетинг** перед удалением родительского узла контекста, у которого больше нет дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="1c159-120">The **\_IAnalysisProxyEvents::ContextNodeDeleting** event before it removes a parent context node that no longer has child nodes.</span></span>

<span data-ttu-id="1c159-121">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1c159-121">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c159-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1c159-122">Requirements</span></span>



| <span data-ttu-id="1c159-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1c159-123">Requirement</span></span> | <span data-ttu-id="1c159-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1c159-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c159-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c159-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1c159-126">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1c159-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1c159-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c159-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1c159-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c159-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1c159-129">Header</span><span class="sxs-lookup"><span data-stu-id="1c159-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c159-130"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1c159-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1c159-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1c159-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c159-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c159-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1c159-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c159-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c159-134">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="1c159-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="1c159-135">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="1c159-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1c159-136">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="1c159-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1c159-137">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="1c159-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="1c159-138">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="1c159-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="1c159-139">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="1c159-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




