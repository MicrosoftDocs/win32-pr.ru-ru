---
description: Загружает сохраненные результаты анализа в Иинканализер.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'Метод Иинканализер:: Лоадресултс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497559"
---
# <a name="iinkanalyzerloadresults-method"></a><span data-ttu-id="27d8c-103">Метод Иинканализер:: Лоадресултс</span><span class="sxs-lookup"><span data-stu-id="27d8c-103">IInkAnalyzer::LoadResults method</span></span>

<span data-ttu-id="27d8c-104">Загружает сохраненные результаты анализа в [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="27d8c-104">Loads saved analysis results into the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="27d8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27d8c-105">Syntax</span></span>


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="27d8c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="27d8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27d8c-107">*улдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-107">*ulDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d8c-108">Число байтов в *пбсериализедресултс*.</span><span class="sxs-lookup"><span data-stu-id="27d8c-108">The number of bytes in *pbSerializedResults*.</span></span>

</dd> <dt>

<span data-ttu-id="27d8c-109">*пбсериализедресултс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-109">*pbSerializedResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d8c-110">Результаты сериализованного анализа.</span><span class="sxs-lookup"><span data-stu-id="27d8c-110">The serialized analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="27d8c-111">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-111">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d8c-112">Число идентификаторов Stroke.</span><span class="sxs-lookup"><span data-stu-id="27d8c-112">The number of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="27d8c-113">*плоригиналстрокеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-113">*plOriginalStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d8c-114">Массив исходных идентификаторов обводки.</span><span class="sxs-lookup"><span data-stu-id="27d8c-114">The array of original stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="27d8c-115">*плневстрокеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-115">*plNewStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d8c-116">Массив новых идентификаторов Stroke.</span><span class="sxs-lookup"><span data-stu-id="27d8c-116">The array of new stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="27d8c-117">*пфсукцессфул* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-117">*pfSuccessful* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="27d8c-118">**Вариант \_ Значение TRUE** , если загрузка прошла успешно; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="27d8c-118">**VARIANT\_TRUE** if loading was successful; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27d8c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27d8c-119">Return value</span></span>

<span data-ttu-id="27d8c-120">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="27d8c-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="27d8c-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27d8c-121">Remarks</span></span>

<span data-ttu-id="27d8c-122">Когда [**иинканализер**](iinkanalyzer.md) добавляет [**иконтекстноде**](icontextnode.md) из сохраненных результатов, он присваивает **иконтекстноде** новый глобальный уникальный идентификатор (GUID) (см. раздел [**иконтекстноде:: жетпропертидата**](icontextnode-getpropertydata.md) и [Свойства контекстного узла](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="27d8c-122">When the [**IInkAnalyzer**](iinkanalyzer.md) adds a [**IContextNode**](icontextnode.md) from the saved results, it assigns a new globally unique identifier (GUID) to the **IContextNode** (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md) and [Context Node Properties](context-node-properties.md)).</span></span>

<span data-ttu-id="27d8c-123">Этот метод добавляет сохраненные результаты анализа в существующее дерево [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="27d8c-123">This method adds the saved analysis results to the existing [**IContextNode**](icontextnode.md) tree.</span></span> <span data-ttu-id="27d8c-124">Чтобы обеспечить правильную сортировку Объединенных результатов, добавьте область, содержащую загруженные узлы контекста, в "грязную" область объекта [**иинканализер**](iinkanalyzer.md) (см. раздел [**метод Иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)) и повторно Проанализируйте рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="27d8c-124">To ensure that the combined results are ordered correctly, add the area containing the loaded context nodes to the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) and reanalyze the ink.</span></span>

<span data-ttu-id="27d8c-125">Метод [**иинканализер:: савересултс**](iinkanalyzer-saveresults.md), [**метод Иинканализер:: Савересултсфорнодес**](iinkanalyzer-saveresultsfornodes.md)и методы [**иинканализер:: савересултсфорстрокес**](iinkanalyzer-saveresultsforstrokes.md) не сохраняют данные пакета вместе с результатами анализа.</span><span class="sxs-lookup"><span data-stu-id="27d8c-125">The [**IInkAnalyzer::SaveResults Method**](iinkanalyzer-saveresults.md), [**IInkAnalyzer::SaveResultsForNodes Method**](iinkanalyzer-saveresultsfornodes.md), and [**IInkAnalyzer::SaveResultsForStrokes Method**](iinkanalyzer-saveresultsforstrokes.md) methods do not save the packet data along with the analysis results.</span></span>

<span data-ttu-id="27d8c-126">Каждый идентификатор в *плоригиналстрокеидс* — это идентификатор Stroke для росчерка в сохраненных результатах анализа.</span><span class="sxs-lookup"><span data-stu-id="27d8c-126">Each identifier in *plOriginalStrokeIds* is the stroke identifier for the stroke in the saved analysis results.</span></span> <span data-ttu-id="27d8c-127">Каждый идентификатор в *плневстрокеидс* — это новый идентификатор, используемый для замены исходного идентификатора в загруженных результатах анализа.</span><span class="sxs-lookup"><span data-stu-id="27d8c-127">Each identifier in *plNewStrokeIds* is the new identifier with which to replace the original identifier in the loaded analysis results.</span></span>

<span data-ttu-id="27d8c-128">Если сохраненное указание анализа конфликтует с имеющейся подсказкой анализа, [**иинканализер**](iinkanalyzer.md) не загружает сохраненную подсказку, но загружает остальные сохраненные результаты.</span><span class="sxs-lookup"><span data-stu-id="27d8c-128">If a saved analysis hint conflicts with an existing analysis hint, the [**IInkAnalyzer**](iinkanalyzer.md) does not load the saved hint but does load the rest of the saved results.</span></span> <span data-ttu-id="27d8c-129">Однако если **иинканализер** загружает результаты для росчерка, находящихся в области сохраненной подсказки анализа, которую **иинканализер** не загружает, **иинканализер** добавляет ограничивающий прямоугольник штриха в «грязную» область объекта **иинканализер** .</span><span class="sxs-lookup"><span data-stu-id="27d8c-129">However, if the **IInkAnalyzer** loads results for a stroke that is within the area of a saved analysis hint that the **IInkAnalyzer** does not load, the **IInkAnalyzer** adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="27d8c-130">Кроме того, если **иинканализер** загружает результаты для росчерка, находящихся в области подсказки для анализа, **иинканализер** также добавляет ограничивающий прямоугольник штриха в «грязную» область объекта **иинканализер** .</span><span class="sxs-lookup"><span data-stu-id="27d8c-130">Also, if the **IInkAnalyzer** loads results for a stroke that is within an existing analysis hint's area, the **IInkAnalyzer** also adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="27d8c-131">Дополнительные сведения о указаниях по анализу см. в разделе [Свойства подсказок по анализу](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="27d8c-131">For more information about analysis hints, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="27d8c-132">Этот метод может вызывать события [**\_ ианалисиспроксевентс:: контекстнодекреатед**](-ianalysisproxyevents-contextnodecreated.md), [**\_ ианалисиспроксевентс:: контекстноделинкаддинг**](-ianalysisproxyevents-contextnodelinkadding.md)и [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) при загрузке сохраненных результатов.</span><span class="sxs-lookup"><span data-stu-id="27d8c-132">This method may raise the [**\_IAnalysisProxyEvents::ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), and [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) events as it loads the saved results.</span></span>

## <a name="requirements"></a><span data-ttu-id="27d8c-133">Требования</span><span class="sxs-lookup"><span data-stu-id="27d8c-133">Requirements</span></span>



| <span data-ttu-id="27d8c-134">Требование</span><span class="sxs-lookup"><span data-stu-id="27d8c-134">Requirement</span></span> | <span data-ttu-id="27d8c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="27d8c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d8c-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27d8c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="27d8c-137">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="27d8c-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27d8c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="27d8c-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="27d8c-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="27d8c-140">Header</span><span class="sxs-lookup"><span data-stu-id="27d8c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="27d8c-141"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="27d8c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="27d8c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27d8c-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="27d8c-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27d8c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d8c-145">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="27d8c-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="27d8c-146">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="27d8c-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="27d8c-147">**Метод Иинканализер:: Жетдиртирегион**</span><span class="sxs-lookup"><span data-stu-id="27d8c-147">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="27d8c-148">**Метод Иинканализер:: Сетдиртирегион**</span><span class="sxs-lookup"><span data-stu-id="27d8c-148">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="27d8c-149">**Метод Иинканализер:: Савересултс**</span><span class="sxs-lookup"><span data-stu-id="27d8c-149">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="27d8c-150">**Метод Иинканализер:: Савересултсфорнодес**</span><span class="sxs-lookup"><span data-stu-id="27d8c-150">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="27d8c-151">**Метод Иинканализер:: Савересултсфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="27d8c-151">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="27d8c-152">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="27d8c-152">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




