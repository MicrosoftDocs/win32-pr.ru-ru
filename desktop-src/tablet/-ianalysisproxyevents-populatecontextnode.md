---
description: Происходит перед тем, как Иинканализер выполняет анализ внутри региона частично заполненного объекта Иконтекстноде.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P событие Опулатеконтекстноде (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e8aebe4ba777d62f90aa00c45ea0f1644e2b8183
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273320"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a><span data-ttu-id="c14a8-103">\_Ианалисиспроксевентс: событие Опулатеконтекстноде:P</span><span class="sxs-lookup"><span data-stu-id="c14a8-103">\_IAnalysisProxyEvents::PopulateContextNode event</span></span>

<span data-ttu-id="c14a8-104">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) выполняет анализ внутри региона частично заполненного объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c14a8-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c14a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c14a8-105">Syntax</span></span>


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a><span data-ttu-id="c14a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c14a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c14a8-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c14a8-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c14a8-108">Объект [**иинканализер**](iinkanalyzer.md) , о котором необходимо выполнить анализ.</span><span class="sxs-lookup"><span data-stu-id="c14a8-108">The [**IInkAnalyzer**](iinkanalyzer.md) object about to perform analysis.</span></span>

</dd> <dt>

<span data-ttu-id="c14a8-109">*пконтекстнодетопопулате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c14a8-109">*pContextNodeToPopulate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c14a8-110">Частично заполненный объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c14a8-110">The partially populated [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c14a8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c14a8-111">Return value</span></span>

<span data-ttu-id="c14a8-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c14a8-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c14a8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c14a8-113">Remarks</span></span>

<span data-ttu-id="c14a8-114">Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="c14a8-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="c14a8-115">Когда **иинканализер** вызывает это событие, приложение должно заполнить *пконтекстнодетопопулате*.</span><span class="sxs-lookup"><span data-stu-id="c14a8-115">When the **IInkAnalyzer** raises this event, your application should populate the *pContextNodeToPopulate*.</span></span> <span data-ttu-id="c14a8-116">На этапе анализа **иинканализер** создает это событие для получения сведений о областях, в которых он анализирует рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="c14a8-116">During the analysis phase, the **IInkAnalyzer** raises this event to get information for areas in which it is analyzing ink.</span></span>

<span data-ttu-id="c14a8-117">Если документ содержит ссылки для *пконтекстнодетопопулате*, приложение должно создать и добавить эти ссылки.</span><span class="sxs-lookup"><span data-stu-id="c14a8-117">If the document contains links for the *pContextNodeToPopulate*, your application should create and add these links.</span></span> <span data-ttu-id="c14a8-118">Для этого процесса требуется, чтобы исходный и конечный узлы, включая их предки, были полностью заполнены до того, как обработчик событий для этого события выходит из системы (см. раздел [**иконтекстлинк:: жетсаурценоде**](icontextlink-getsourcenode.md) and [**Иконтекстлинк:: жетдестинатионноде**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="c14a8-118">This process requires that both the source and destination nodes, including their ancestors, are fully populated before the event handler for this event exits (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span>

<span data-ttu-id="c14a8-119">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c14a8-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="c14a8-120">Во время фонового анализа [**иинканализер**](iinkanalyzer.md) создает это событие после того, как оно вызывает событие [**\_ ианалисисевентс:: реадитореконЦиле**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="c14a8-120">During background analysis, the [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="c14a8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c14a8-121">Requirements</span></span>



| <span data-ttu-id="c14a8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c14a8-122">Requirement</span></span> | <span data-ttu-id="c14a8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c14a8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c14a8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c14a8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c14a8-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c14a8-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c14a8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c14a8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c14a8-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c14a8-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c14a8-128">Header</span><span class="sxs-lookup"><span data-stu-id="c14a8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c14a8-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c14a8-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c14a8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c14a8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c14a8-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c14a8-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c14a8-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c14a8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c14a8-133">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="c14a8-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="c14a8-134">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="c14a8-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c14a8-135">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="c14a8-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c14a8-136">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="c14a8-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="c14a8-137">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="c14a8-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="c14a8-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="c14a8-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




