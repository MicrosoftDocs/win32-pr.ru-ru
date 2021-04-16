---
description: Указывает события, связанные с шагами анализа объекта Иинканализер.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: Интерфейс _IAnalysisEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693285"
---
# <a name="_ianalysisevents-interface"></a><span data-ttu-id="bed68-103">\_Интерфейс Ианалисисевентс</span><span class="sxs-lookup"><span data-stu-id="bed68-103">\_IAnalysisEvents interface</span></span>

<span data-ttu-id="bed68-104">Указывает события, связанные с шагами анализа объекта [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="bed68-104">Specifies events associated with the analysis steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="bed68-105">События</span><span class="sxs-lookup"><span data-stu-id="bed68-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="bed68-106">События</span><span class="sxs-lookup"><span data-stu-id="bed68-106">Events</span></span>

<span data-ttu-id="bed68-107">Интерфейс **\_ ианалисисевентс** содержит следующие события.</span><span class="sxs-lookup"><span data-stu-id="bed68-107">The **\_IAnalysisEvents** interface has these events.</span></span>



| <span data-ttu-id="bed68-108">Событие</span><span class="sxs-lookup"><span data-stu-id="bed68-108">Event</span></span>                                                               | <span data-ttu-id="bed68-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bed68-109">Description</span></span>                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bed68-110">**Оборот**</span><span class="sxs-lookup"><span data-stu-id="bed68-110">**Activity**</span></span>](-ianalysisevents-activity.md)                       | <span data-ttu-id="bed68-111">Происходит при вызове метода [**иинканализер:: Analyze**](iinkanalyzer-analyze.md) или метода [**Иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md) .</span><span class="sxs-lookup"><span data-stu-id="bed68-111">Occurs during calls to the [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method.</span></span><br/> |
| [<span data-ttu-id="bed68-112">**интермедиатересултс**</span><span class="sxs-lookup"><span data-stu-id="bed68-112">**IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md) | <span data-ttu-id="bed68-113">Происходит при завершении текущего промежуточного этапа анализа.</span><span class="sxs-lookup"><span data-stu-id="bed68-113">Occurs when the current intermediate analysis stage is finished.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="bed68-114">**реадитореконЦиле**</span><span class="sxs-lookup"><span data-stu-id="bed68-114">**ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)       | <span data-ttu-id="bed68-115">Происходит, когда [**иинканализер**](iinkanalyzer.md) готова к согласованию результатов своего фонового анализа с текущим состоянием.</span><span class="sxs-lookup"><span data-stu-id="bed68-115">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span><br/>                                                  |
| [<span data-ttu-id="bed68-116">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="bed68-116">**Results**</span></span>](-ianalysisevents-results.md)                         | <span data-ttu-id="bed68-117">Происходит после завершения заключительного этапа анализа.</span><span class="sxs-lookup"><span data-stu-id="bed68-117">Occurs when the final analysis stage is finished.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="bed68-118">**упдатестрокескаче**</span><span class="sxs-lookup"><span data-stu-id="bed68-118">**UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)   | <span data-ttu-id="bed68-119">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) обращается к данным Stroke.</span><span class="sxs-lookup"><span data-stu-id="bed68-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span><br/>                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="bed68-120">Требования</span><span class="sxs-lookup"><span data-stu-id="bed68-120">Requirements</span></span>



| <span data-ttu-id="bed68-121">Требование</span><span class="sxs-lookup"><span data-stu-id="bed68-121">Requirement</span></span> | <span data-ttu-id="bed68-122">Значение</span><span class="sxs-lookup"><span data-stu-id="bed68-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="bed68-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bed68-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bed68-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bed68-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bed68-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bed68-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bed68-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bed68-126">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="bed68-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bed68-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed68-128">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="bed68-128">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="bed68-129">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="bed68-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="bed68-130">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="bed68-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="bed68-131">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="bed68-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="bed68-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="bed68-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

