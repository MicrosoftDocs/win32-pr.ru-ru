---
description: Происходит перед тем, как Иинканализер удаляет объект Иконтекстлинк между двумя объектами Иконтекстноде.
ms.assetid: bc9716b8-8793-4886-aff4-d880024129a6
title: 'Событие _IAnalysisProxyEvents:: Контекстноделинкделетинг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc4ba9586fc4c520b9ee44b039bd56f8ef2ade3c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273311"
---
# <a name="_ianalysisproxyeventscontextnodelinkdeleting-event"></a><span data-ttu-id="ca57e-103">\_Событие Ианалисиспроксевентс:: Контекстноделинкделетинг</span><span class="sxs-lookup"><span data-stu-id="ca57e-103">\_IAnalysisProxyEvents::ContextNodeLinkDeleting event</span></span>

<span data-ttu-id="ca57e-104">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) удаляет объект [**иконтекстлинк**](icontextlink.md) между двумя объектами [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ca57e-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca57e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca57e-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="ca57e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca57e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca57e-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca57e-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca57e-108">[**Иинканализер**](iinkanalyzer.md) удаляет ссылку.</span><span class="sxs-lookup"><span data-stu-id="ca57e-108">The [**IInkAnalyzer**](iinkanalyzer.md) deleting the link.</span></span>

</dd> <dt>

<span data-ttu-id="ca57e-109">*пконтекстлинктобеделетед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca57e-109">*pContextLinkToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca57e-110">Удаляемый объект [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="ca57e-110">The [**IContextLink**](icontextlink.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca57e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca57e-111">Return value</span></span>

<span data-ttu-id="ca57e-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ca57e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca57e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca57e-113">Remarks</span></span>

<span data-ttu-id="ca57e-114">Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ca57e-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="ca57e-115">Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод **иинканализер** , который удаляет [**иконтекстлинк**](icontextlink.md) из [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="ca57e-115">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that removes an [**IContextLink**](icontextlink.md) from an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="ca57e-116">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ca57e-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca57e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ca57e-117">Requirements</span></span>



| <span data-ttu-id="ca57e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ca57e-118">Requirement</span></span> | <span data-ttu-id="ca57e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ca57e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca57e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca57e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ca57e-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ca57e-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ca57e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca57e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ca57e-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ca57e-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ca57e-124">Header</span><span class="sxs-lookup"><span data-stu-id="ca57e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca57e-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ca57e-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ca57e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ca57e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca57e-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca57e-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ca57e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca57e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca57e-129">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="ca57e-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="ca57e-130">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="ca57e-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ca57e-131">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="ca57e-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="ca57e-132">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="ca57e-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ca57e-133">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="ca57e-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="ca57e-134">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="ca57e-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ca57e-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ca57e-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




