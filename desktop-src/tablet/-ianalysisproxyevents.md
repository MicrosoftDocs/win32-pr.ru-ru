---
description: Указывает события, связанные с шагами прокси-сервера данных для объекта Иинканализер.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: Интерфейс _IAnalysisProxyEvents (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105674567"
---
# <a name="_ianalysisproxyevents-interface"></a><span data-ttu-id="26f72-103">\_Интерфейс Ианалисиспроксевентс</span><span class="sxs-lookup"><span data-stu-id="26f72-103">\_IAnalysisProxyEvents interface</span></span>

<span data-ttu-id="26f72-104">Указывает события, связанные с шагами прокси-сервера данных для объекта [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="26f72-104">Specifies events associated with the data proxy steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="26f72-105">События</span><span class="sxs-lookup"><span data-stu-id="26f72-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="26f72-106">События</span><span class="sxs-lookup"><span data-stu-id="26f72-106">Events</span></span>

<span data-ttu-id="26f72-107">Интерфейс **\_ ианалисиспроксевентс** содержит следующие события.</span><span class="sxs-lookup"><span data-stu-id="26f72-107">The **\_IAnalysisProxyEvents** interface has these events.</span></span>



| <span data-ttu-id="26f72-108">Событие</span><span class="sxs-lookup"><span data-stu-id="26f72-108">Event</span></span>                                                                                      | <span data-ttu-id="26f72-109">Описание</span><span class="sxs-lookup"><span data-stu-id="26f72-109">Description</span></span>                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26f72-110">**контекстнодекреатед**</span><span class="sxs-lookup"><span data-stu-id="26f72-110">**ContextNodeCreated**</span></span>](-ianalysisproxyevents-contextnodecreated.md)                     | <span data-ttu-id="26f72-111">Происходит после того, как [**иинканализер**](iinkanalyzer.md) создает объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="26f72-111">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                  |
| [<span data-ttu-id="26f72-112">**контекстнодеделетинг**</span><span class="sxs-lookup"><span data-stu-id="26f72-112">**ContextNodeDeleting**</span></span>](-ianalysisproxyevents-contextnodedeleting.md)                   | <span data-ttu-id="26f72-113">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) удаляет объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="26f72-113">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                 |
| [<span data-ttu-id="26f72-114">**контекстноделинкаддинг**</span><span class="sxs-lookup"><span data-stu-id="26f72-114">**ContextNodeLinkAdding**</span></span>](-ianalysisproxyevents-contextnodelinkadding.md)               | <span data-ttu-id="26f72-115">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) добавляет объект [**иконтекстлинк**](icontextlink.md) между двумя объектами [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="26f72-115">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>           |
| [<span data-ttu-id="26f72-116">**контекстноделинкделетинг**</span><span class="sxs-lookup"><span data-stu-id="26f72-116">**ContextNodeLinkDeleting**</span></span>](-ianalysisproxyevents-contextnodelinkdeleting.md)           | <span data-ttu-id="26f72-117">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) удаляет объект [**иконтекстлинк**](icontextlink.md) между двумя объектами [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="26f72-117">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>         |
| [<span data-ttu-id="26f72-118">**контекстнодемовингтопоситион**</span><span class="sxs-lookup"><span data-stu-id="26f72-118">**ContextNodeMovingToPosition**</span></span>](-ianalysisproxyevents-contextnodemovingtoposition.md)   | <span data-ttu-id="26f72-119">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) перемещает объект [**иконтекстноде**](icontextnode.md) в новую точку в коллекции подузлов родительского узла.</span><span class="sxs-lookup"><span data-stu-id="26f72-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span><br/> |
| [<span data-ttu-id="26f72-120">**контекстнодепропертиесупдатед**</span><span class="sxs-lookup"><span data-stu-id="26f72-120">**ContextNodePropertiesUpdated**</span></span>](-ianalysisproxyevents-contextnodepropertiesupdated.md) | <span data-ttu-id="26f72-121">Происходит после того, как [**иинканализер**](iinkanalyzer.md) обновляет одно или несколько свойств объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="26f72-121">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                        |
| [<span data-ttu-id="26f72-122">**контекстнодерепарентинг**</span><span class="sxs-lookup"><span data-stu-id="26f72-122">**ContextNodeReparenting**</span></span>](-ianalysisproxyevents-contextnodereparenting.md)             | <span data-ttu-id="26f72-123">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) перемещает объект [**иконтекстноде**](icontextnode.md) , изменяя его родительский узел.</span><span class="sxs-lookup"><span data-stu-id="26f72-123">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span><br/>                                       |
| [<span data-ttu-id="26f72-124">**инканализерстатечангинг**</span><span class="sxs-lookup"><span data-stu-id="26f72-124">**InkAnalyzerStateChanging**</span></span>](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | <span data-ttu-id="26f72-125">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) согласовывает результаты анализа, чтобы приложение могла синхронизировать данные с **иинканализер**.</span><span class="sxs-lookup"><span data-stu-id="26f72-125">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span><br/>                      |
| [<span data-ttu-id="26f72-126">**популатеконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="26f72-126">**PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)                   | <span data-ttu-id="26f72-127">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) выполняет анализ внутри региона частично заполненного объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="26f72-127">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span><br/>               |
| [<span data-ttu-id="26f72-128">**строкерепарентед**</span><span class="sxs-lookup"><span data-stu-id="26f72-128">**StrokeReparented**</span></span>](-ianalysisproxyevents-strokereparented.md)                         | <span data-ttu-id="26f72-129">Происходит, когда [**иинканализер**](iinkanalyzer.md) перемещает штрих из одного объекта [**иконтекстноде**](icontextnode.md) в другой.</span><span class="sxs-lookup"><span data-stu-id="26f72-129">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span><br/>                                           |



 

## <a name="remarks"></a><span data-ttu-id="26f72-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26f72-130">Remarks</span></span>

<span data-ttu-id="26f72-131">Используйте эти события, если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="26f72-131">Use these events when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="26f72-132">Дополнительные сведения о синхронизации данных приложения с помощью **иинканализер** см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="26f72-132">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26f72-133">Требования</span><span class="sxs-lookup"><span data-stu-id="26f72-133">Requirements</span></span>



| <span data-ttu-id="26f72-134">Требование</span><span class="sxs-lookup"><span data-stu-id="26f72-134">Requirement</span></span> | <span data-ttu-id="26f72-135">Значение</span><span class="sxs-lookup"><span data-stu-id="26f72-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f72-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26f72-136">Minimum supported client</span></span><br/> | <span data-ttu-id="26f72-137">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="26f72-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="26f72-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26f72-138">Minimum supported server</span></span><br/> | <span data-ttu-id="26f72-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="26f72-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="26f72-140">Header</span><span class="sxs-lookup"><span data-stu-id="26f72-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="26f72-141"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="26f72-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="26f72-142">DLL</span><span class="sxs-lookup"><span data-stu-id="26f72-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26f72-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26f72-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="26f72-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26f72-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f72-145">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="26f72-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="26f72-146">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="26f72-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="26f72-147">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="26f72-147">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="26f72-148">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="26f72-148">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="26f72-149">\_ианалисисевентс</span><span class="sxs-lookup"><span data-stu-id="26f72-149">\_IAnalysisEvents</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="26f72-150">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="26f72-150">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

