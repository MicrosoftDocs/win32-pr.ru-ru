---
description: Происходит перед тем, как анализатор рукописного ввода добавляет объект Иконтекстлинк между двумя объектами Иконтекстноде.
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: 'Событие _IAnalysisProxyEvents:: Контекстноделинкаддинг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 341c551064869532e8b51ddecdbe1d5a78878abd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703502"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a><span data-ttu-id="9c32a-103">\_Событие Ианалисиспроксевентс:: Контекстноделинкаддинг</span><span class="sxs-lookup"><span data-stu-id="9c32a-103">\_IAnalysisProxyEvents::ContextNodeLinkAdding event</span></span>

<span data-ttu-id="9c32a-104">Происходит перед тем, как анализатор рукописного ввода добавляет объект [**иконтекстлинк**](icontextlink.md) между двумя объектами [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="9c32a-104">Occurs before the ink analyzer adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c32a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c32a-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a><span data-ttu-id="9c32a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c32a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c32a-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c32a-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c32a-108">[**Иинканализер**](iinkanalyzer.md) , который добавляет ссылку.</span><span class="sxs-lookup"><span data-stu-id="9c32a-108">The [**IInkAnalyzer**](iinkanalyzer.md) adding the link.</span></span>

</dd> <dt>

<span data-ttu-id="9c32a-109">*пконтекстлинктобеаддед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c32a-109">*pContextLinkToBeAdded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c32a-110">Добавляемый объект [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="9c32a-110">The [**IContextLink**](icontextlink.md) object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c32a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c32a-111">Return value</span></span>

<span data-ttu-id="9c32a-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9c32a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c32a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c32a-113">Remarks</span></span>

<span data-ttu-id="9c32a-114">Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="9c32a-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="9c32a-115">Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод анализатора рукописного ввода, который добавляет новый [**иконтекстлинк**](icontextlink.md) в [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="9c32a-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that adds a new [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="9c32a-116">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9c32a-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c32a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9c32a-117">Requirements</span></span>



| <span data-ttu-id="9c32a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9c32a-118">Requirement</span></span> | <span data-ttu-id="9c32a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9c32a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c32a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c32a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9c32a-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9c32a-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9c32a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c32a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9c32a-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9c32a-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9c32a-124">Header</span><span class="sxs-lookup"><span data-stu-id="9c32a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c32a-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9c32a-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9c32a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9c32a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c32a-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c32a-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9c32a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c32a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c32a-129">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="9c32a-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="9c32a-130">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="9c32a-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9c32a-131">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="9c32a-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9c32a-132">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="9c32a-132">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="9c32a-133">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="9c32a-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="9c32a-134">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="9c32a-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="9c32a-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9c32a-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




