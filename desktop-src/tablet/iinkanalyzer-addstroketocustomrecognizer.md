---
description: Добавляет данные Stroke для одного штриха в пользовательский узел распознавателя.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'Метод Иинканализер:: Аддстрокетокустомрекогнизер (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711120"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a><span data-ttu-id="d47e5-103">Метод Иинканализер:: Аддстрокетокустомрекогнизер</span><span class="sxs-lookup"><span data-stu-id="d47e5-103">IInkAnalyzer::AddStrokeToCustomRecognizer method</span></span>

<span data-ttu-id="d47e5-104">Добавляет данные Stroke для одного штриха в пользовательский узел распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d47e5-104">Adds stroke data for a single stroke to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47e5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d47e5-105">Syntax</span></span>


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="d47e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d47e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d47e5-107">*улстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d47e5-107">*ulStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47e5-108">Идентификатор добавляемого штриха.</span><span class="sxs-lookup"><span data-stu-id="d47e5-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="d47e5-109">*улстрокепаккетдатакаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d47e5-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47e5-110">Число пакетов в штрихе.</span><span class="sxs-lookup"><span data-stu-id="d47e5-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="d47e5-111">*плстрокепаккетдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d47e5-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47e5-112">Массив, содержащий данные пакета для штриха.</span><span class="sxs-lookup"><span data-stu-id="d47e5-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="d47e5-113">*улстрокепаккетдескриптионкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d47e5-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47e5-114">Число свойств пакетов в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="d47e5-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="d47e5-115">*пстрокепаккетдескриптионгуидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d47e5-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47e5-116">Массив, содержащий идентификаторы свойств пакета.</span><span class="sxs-lookup"><span data-stu-id="d47e5-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="d47e5-117">*пкустомрекогнизер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d47e5-117">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47e5-118">[**Иконтекстноде**](icontextnode.md) типа **кустомрекогнизер** , к которому добавляется росчерк.</span><span class="sxs-lookup"><span data-stu-id="d47e5-118">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="d47e5-119">*ппконтекстнодестрокеаддедто* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d47e5-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d47e5-120">[**Иконтекстноде**](icontextnode.md) , к которому анализатор рукописного ввода добавил штрих.</span><span class="sxs-lookup"><span data-stu-id="d47e5-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d47e5-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d47e5-121">Return value</span></span>

<span data-ttu-id="d47e5-122">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d47e5-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d47e5-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d47e5-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="d47e5-124">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодестрокеаддедто* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="d47e5-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="d47e5-125">Если *ппконтекстнодестрокеаддедто* имеет **значение NULL**, это означает, что вызывающий объект не заинтересован в возвращаемом значении метода.</span><span class="sxs-lookup"><span data-stu-id="d47e5-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="d47e5-126">[**Иинканализер**](iinkanalyzer.md) добавляет штрих в [**иконтекстноде**](icontextnode.md) типа **Кустомрекогнизер** (см. раздел [типы узлов контекста](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="d47e5-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="d47e5-127">Этот узел находится в коллекции подузлов корневого узла (см. методы [**иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md) и [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="d47e5-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="d47e5-128">[**Иинканализер**](iinkanalyzer.md) назначает идентификатор языка и региональных параметров активного входного потока штриху и добавляет штрих к первому узлу **Унклассифиединк** в узле **кустомрекогнизер** .</span><span class="sxs-lookup"><span data-stu-id="d47e5-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="d47e5-129">Если узел **унклассифиединк** не существует, он создается.</span><span class="sxs-lookup"><span data-stu-id="d47e5-129">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="d47e5-130">Если [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , связанный с узлом **кустомрекогнизер** , не поддерживает идентификатор языка и региональных параметров, **иинканализер** продолжит анализ и выдаст предупреждение [**ианалисисварнинг**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="d47e5-130">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="d47e5-131">Это предупреждение имеет значение [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode) , равное **аналисисварнингкоде \_ лангуажеиднотреспектед**.</span><span class="sxs-lookup"><span data-stu-id="d47e5-131">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="d47e5-132">*плстрокепаккетдата* содержит данные пакетов для всех точек в штрихе.</span><span class="sxs-lookup"><span data-stu-id="d47e5-132">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="d47e5-133">*пстрокепаккетдескриптионгуидс* содержит глобальные уникальные идентификаторы (GUID), которые описывают типы данных пакетов, включаемых для каждой точки в каждом штрихе.</span><span class="sxs-lookup"><span data-stu-id="d47e5-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="d47e5-134">Полный список доступных свойств пакетов см. в разделе [константы паккетпропертигуидс](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d47e5-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="d47e5-135">Этот метод расширяет «грязную» область до объединения текущего значения области и ограничивающего прямоугольника добавленного штриха.</span><span class="sxs-lookup"><span data-stu-id="d47e5-135">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="d47e5-136">[**Иинканализер**](iinkanalyzer.md) возвращает **значение HRESULT** для **E \_ INVALIDARG** при следующих обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="d47e5-136">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="d47e5-137">[**Иинканализер**](iinkanalyzer.md) уже содержит штрих с тем же идентификатором, что и добавляемый элемент Stroke.</span><span class="sxs-lookup"><span data-stu-id="d47e5-137">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as the stroke to be added.</span></span>
-   <span data-ttu-id="d47e5-138">Параметр *пкустомрекогнизер* содержит пользовательский узел распознавателя, связанный с другим объектом [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="d47e5-138">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="d47e5-139">Параметр *пкустомрекогнизер* содержит [**иконтекстноде**](icontextnode.md) , который не относится к типу **кустомрекогнизер**.</span><span class="sxs-lookup"><span data-stu-id="d47e5-139">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d47e5-140">Требования</span><span class="sxs-lookup"><span data-stu-id="d47e5-140">Requirements</span></span>



| <span data-ttu-id="d47e5-141">Требование</span><span class="sxs-lookup"><span data-stu-id="d47e5-141">Requirement</span></span> | <span data-ttu-id="d47e5-142">Значение</span><span class="sxs-lookup"><span data-stu-id="d47e5-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d47e5-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d47e5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d47e5-144">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d47e5-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d47e5-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d47e5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d47e5-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d47e5-146">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d47e5-147">Header</span><span class="sxs-lookup"><span data-stu-id="d47e5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d47e5-148"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d47e5-148"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d47e5-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d47e5-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d47e5-150"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d47e5-150"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d47e5-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d47e5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47e5-152">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="d47e5-152">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d47e5-153">Типы узлов контекста</span><span class="sxs-lookup"><span data-stu-id="d47e5-153">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="d47e5-154">**Метод Иинканализер:: Аддстрокестокустомрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="d47e5-154">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="d47e5-155">**Метод Иинканализер:: Креатекустомрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="d47e5-155">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="d47e5-156">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="d47e5-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

