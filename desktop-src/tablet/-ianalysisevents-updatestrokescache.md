---
description: Происходит перед тем, как Иинканализер обращается к данным Stroke.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: 'Событие _IAnalysisEvents:: Упдатестрокескаче (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5d16011d8c5fe571d228b632fecb7a973bafcbf5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693902"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a><span data-ttu-id="f6429-103">\_Событие Ианалисисевентс:: Упдатестрокескаче</span><span class="sxs-lookup"><span data-stu-id="f6429-103">\_IAnalysisEvents::UpdateStrokesCache event</span></span>

<span data-ttu-id="f6429-104">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) обращается к данным Stroke.</span><span class="sxs-lookup"><span data-stu-id="f6429-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6429-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6429-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="f6429-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6429-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6429-107">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6429-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6429-108">Число идентификаторов Stroke в *плстрокеидс*.</span><span class="sxs-lookup"><span data-stu-id="f6429-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="f6429-109">*плстрокеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6429-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6429-110">Идентификаторы штрихов, данные пакетов которых были удалены.</span><span class="sxs-lookup"><span data-stu-id="f6429-110">The identifiers of the strokes whose packet data has been cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6429-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6429-111">Return value</span></span>

<span data-ttu-id="f6429-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f6429-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f6429-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6429-113">Remarks</span></span>

<span data-ttu-id="f6429-114">[**Иинканализер**](iinkanalyzer.md) вызывает это событие во время анализа рукописного ввода, когда он обращается к одному или нескольким штрихам, для которых данные пакета были удалены.</span><span class="sxs-lookup"><span data-stu-id="f6429-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during ink analysis when it accesses one or more strokes for which the packet data has been cleared.</span></span> <span data-ttu-id="f6429-115">Чтобы обновить данные пакета обводки, используйте метод [**метода иинканализер:: упдатестрокесдата**](iinkanalyzer-updatestrokesdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f6429-115">To update the stroke packet data, use the [**IInkAnalyzer::UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) method.</span></span>

<span data-ttu-id="f6429-116">[**Иинканализер**](iinkanalyzer.md) не вызывает это событие при доступе к частично заполненному конечному узлу рукописного ввода, если расположение узла не было задано параметром **иинканализер**.</span><span class="sxs-lookup"><span data-stu-id="f6429-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise this event when accessing a partially populated ink leaf node when the location of the node has not been set by the **IInkAnalyzer**.</span></span>

<span data-ttu-id="f6429-117">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f6429-117">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6429-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f6429-118">Requirements</span></span>



| <span data-ttu-id="f6429-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f6429-119">Requirement</span></span> | <span data-ttu-id="f6429-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f6429-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6429-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6429-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f6429-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f6429-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f6429-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6429-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f6429-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6429-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f6429-125">Header</span><span class="sxs-lookup"><span data-stu-id="f6429-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6429-126"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f6429-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f6429-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f6429-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6429-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6429-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f6429-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6429-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6429-130">**\_ианалисисевентс**</span><span class="sxs-lookup"><span data-stu-id="f6429-130">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="f6429-131">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="f6429-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="f6429-132">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="f6429-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f6429-133">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="f6429-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="f6429-134">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="f6429-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="f6429-135">**Метод Иинканализер:: Упдатестрокесдата**</span><span class="sxs-lookup"><span data-stu-id="f6429-135">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="f6429-136">**Иконтекстноде:: Креатепартиаллипопулатедсубноде**</span><span class="sxs-lookup"><span data-stu-id="f6429-136">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="f6429-137">**Иконтекстноде:: Жетпартиаллипопулатед**</span><span class="sxs-lookup"><span data-stu-id="f6429-137">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="f6429-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="f6429-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




