---
description: Добавляет данные Stroke для нескольких штрихов в пользовательский узел распознавателя.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'Метод Иинканализер:: Аддстрокестокустомрекогнизер (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df1b31957f3b4087b51fbad0e7b527c2ede799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711121"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a><span data-ttu-id="ef4b8-103">Метод Иинканализер:: Аддстрокестокустомрекогнизер</span><span class="sxs-lookup"><span data-stu-id="ef4b8-103">IInkAnalyzer::AddStrokesToCustomRecognizer method</span></span>

<span data-ttu-id="ef4b8-104">Добавляет данные Stroke для нескольких штрихов в пользовательский узел распознавателя.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-104">Adds stroke data for multiple strokes to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef4b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef4b8-105">Syntax</span></span>


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="ef4b8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef4b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef4b8-107">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef4b8-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4b8-108">Число добавляемых штрихов.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="ef4b8-109">*плстрокеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef4b8-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4b8-110">Массив, содержащий идентификаторы штрихов.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="ef4b8-111">*улстрокепаккетдескриптионкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef4b8-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4b8-112">Число свойств в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="ef4b8-113">*пстрокепаккетдескриптионгуидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef4b8-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4b8-114">Массив, содержащий идентификаторы свойств пакета.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="ef4b8-115">*пулпаккетдатакаунтперстроке* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef4b8-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4b8-116">Массив, содержащий количество пакетов в каждом штрихе.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="ef4b8-117">*плстрокепаккетдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef4b8-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4b8-118">Массив, содержащий данные пакета для штрихов.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="ef4b8-119">*пкустомрекогнизер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef4b8-119">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4b8-120">[**Иконтекстноде**](icontextnode.md) типа **кустомрекогнизер** , к которому добавляются штрихи.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-120">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="ef4b8-121">*ппконтекстнодестрокеаддедто* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ef4b8-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4b8-122">[**Иконтекстноде**](icontextnode.md) , к которому анализатор рукописного ввода добавил штрихи.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef4b8-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef4b8-123">Return value</span></span>

<span data-ttu-id="ef4b8-124">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ef4b8-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef4b8-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef4b8-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ef4b8-126">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодестрокеаддедто* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="ef4b8-127">Если *ппконтекстнодестрокеаддедто* имеет **значение NULL**, это означает, что вызывающий объект не заинтересован в возвращаемом значении метода.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="ef4b8-128">[**Иинканализер**](iinkanalyzer.md) добавляет штрихи к [**иконтекстноде**](icontextnode.md) типа **Кустомрекогнизер** (см. раздел [типы узлов контекста](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="ef4b8-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="ef4b8-129">Этот узел находится в коллекции подузлов корневого узла (см. методы [**иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md) и [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="ef4b8-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="ef4b8-130">[**Иинканализер**](iinkanalyzer.md) назначает идентификатор языка и региональных параметров активного входного потока штрихам и добавляет штрихи к первому узлу **Унклассифиединк** в узле **кустомрекогнизер** .</span><span class="sxs-lookup"><span data-stu-id="ef4b8-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="ef4b8-131">Если узел **унклассифиединк** не существует, он создается.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-131">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="ef4b8-132">Если [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , связанный с узлом **кустомрекогнизер** , не поддерживает идентификатор языка и региональных параметров, **иинканализер** продолжит анализ и выдаст предупреждение [**ианалисисварнинг**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="ef4b8-132">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="ef4b8-133">Это предупреждение имеет значение [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode) , равное **аналисисварнингкоде \_ лангуажеиднотреспектед**.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-133">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="ef4b8-134">*плстрокепаккетдата* содержит данные пакетов для всех штрихов.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-134">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="ef4b8-135">*пстрокепаккетдескриптионгуидс* содержит глобальные уникальные идентификаторы (GUID), которые описывают типы данных пакетов, включаемых для каждой точки в каждом штрихе.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-135">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="ef4b8-136">Полный список доступных свойств пакетов см. в разделе [константы паккетпропертигуидс](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ef4b8-136">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="ef4b8-137">В одном вызове **метода иинканализер:: аддстрокестокустомрекогнизер** можно добавлять только штрихи с теми же описаниями пакетов.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-137">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokesToCustomRecognizer Method**.</span></span>

 

<span data-ttu-id="ef4b8-138">Этот метод расширяет «грязную» область до объединения текущего значения области и ограничивающего прямоугольника добавленных штрихов.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-138">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="ef4b8-139">[**Иинканализер**](iinkanalyzer.md) возвращает **значение HRESULT** для **E \_ INVALIDARG** при следующих обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-139">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="ef4b8-140">[**Иинканализер**](iinkanalyzer.md) уже содержит штрих с тем же идентификатором, что и один из добавляемых штрихов.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-140">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added.</span></span>
-   <span data-ttu-id="ef4b8-141">Параметр *пкустомрекогнизер* содержит пользовательский узел распознавателя, связанный с другим объектом [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="ef4b8-141">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="ef4b8-142">Параметр *пкустомрекогнизер* содержит [**иконтекстноде**](icontextnode.md) , который не относится к типу **кустомрекогнизер**.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-142">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef4b8-143">Требования</span><span class="sxs-lookup"><span data-stu-id="ef4b8-143">Requirements</span></span>



| <span data-ttu-id="ef4b8-144">Требование</span><span class="sxs-lookup"><span data-stu-id="ef4b8-144">Requirement</span></span> | <span data-ttu-id="ef4b8-145">Значение</span><span class="sxs-lookup"><span data-stu-id="ef4b8-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4b8-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef4b8-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ef4b8-147">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ef4b8-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ef4b8-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef4b8-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ef4b8-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ef4b8-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ef4b8-150">Header</span><span class="sxs-lookup"><span data-stu-id="ef4b8-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef4b8-151"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ef4b8-151"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ef4b8-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ef4b8-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef4b8-153"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef4b8-153"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ef4b8-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef4b8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef4b8-155">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="ef4b8-155">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ef4b8-156">Типы узлов контекста</span><span class="sxs-lookup"><span data-stu-id="ef4b8-156">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="ef4b8-157">**Метод Иинканализер:: Аддстрокетокустомрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="ef4b8-157">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="ef4b8-158">**Метод Иинканализер:: Креатекустомрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="ef4b8-158">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="ef4b8-159">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ef4b8-159">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

