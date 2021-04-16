---
description: Добавляет данные Stroke для нескольких штрихов в Иинканализер и присваивает штрихам идентификаторы языка и региональных параметров активного потока ввода.
ms.assetid: 4a8d6828-699b-465d-b057-197866ff069f
title: 'Метод Иинканализер:: Аддстрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc616f8a388010df2b3d39ea55622d81fa5ce3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692430"
---
# <a name="iinkanalyzeraddstrokes-method"></a><span data-ttu-id="9fc35-103">Метод Иинканализер:: Аддстрокес</span><span class="sxs-lookup"><span data-stu-id="9fc35-103">IInkAnalyzer::AddStrokes method</span></span>

<span data-ttu-id="9fc35-104">Добавляет данные Stroke для нескольких штрихов в [**иинканализер**](iinkanalyzer.md) и присваивает штрихам идентификаторы языка и региональных параметров активного потока ввода.</span><span class="sxs-lookup"><span data-stu-id="9fc35-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc35-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fc35-105">Syntax</span></span>


```C++
HRESULT AddStrokes(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="9fc35-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fc35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc35-107">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fc35-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc35-108">Число добавляемых штрихов.</span><span class="sxs-lookup"><span data-stu-id="9fc35-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="9fc35-109">*плстрокеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fc35-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc35-110">Массив, содержащий идентификаторы штрихов.</span><span class="sxs-lookup"><span data-stu-id="9fc35-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9fc35-111">*улстрокепаккетдескриптионкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fc35-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc35-112">Число свойств в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="9fc35-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="9fc35-113">*пстрокепаккетдескриптионгуидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fc35-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc35-114">Массив, содержащий идентификаторы свойств пакета.</span><span class="sxs-lookup"><span data-stu-id="9fc35-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9fc35-115">*пулпаккетдатакаунтперстроке* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fc35-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc35-116">Массив, содержащий количество пакетов в каждом штрихе.</span><span class="sxs-lookup"><span data-stu-id="9fc35-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="9fc35-117">*плстрокепаккетдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fc35-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc35-118">Массив, содержащий данные пакета для штрихов.</span><span class="sxs-lookup"><span data-stu-id="9fc35-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="9fc35-119">*ппконтекстнодестрокеаддедто* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9fc35-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc35-120">[**Иконтекстноде**](icontextnode.md) , к которому анализатор рукописного ввода добавил штрихи.</span><span class="sxs-lookup"><span data-stu-id="9fc35-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc35-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fc35-121">Return value</span></span>

<span data-ttu-id="9fc35-122">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9fc35-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc35-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fc35-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9fc35-124">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодестрокеаддедто* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="9fc35-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="9fc35-125">Если *ппконтекстнодестрокеаддедто* имеет **значение NULL**, это означает, что вызывающий объект не заинтересован в возвращаемом значении метода.</span><span class="sxs-lookup"><span data-stu-id="9fc35-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="9fc35-126">[**Иинканализер**](iinkanalyzer.md) добавляет штрихи к [**иконтекстноде**](icontextnode.md) типа унклассифиединк (см. раздел [типы узлов контекста](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="9fc35-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="9fc35-127">Этот узел находится в коллекции подузлов корневого узла (см. методы [**иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md) и [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="9fc35-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="9fc35-128">[**Иинканализер**](iinkanalyzer.md) присваивает идентификатор языка и региональных параметров активного входного потока штрихам и добавляет эти штрихи к первому узлу контекста унклассифиединк в корневом узле анализатора красок, содержащему штрихи с одним и тем же идентификатором языка и региональных параметров.</span><span class="sxs-lookup"><span data-stu-id="9fc35-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="9fc35-129">Если анализатор рукописного ввода не имеет узла с таким же идентификатором языка и региональных параметров, он создает новый узел контекста Унклассифиединк в своем корневом узле и добавляет штрихи в новый узел контекста Унклассифиединк.</span><span class="sxs-lookup"><span data-stu-id="9fc35-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="9fc35-130">*плстрокепаккетдата* содержит данные пакетов для всех штрихов.</span><span class="sxs-lookup"><span data-stu-id="9fc35-130">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="9fc35-131">*пстрокепаккетдескриптионгуидс* содержит глобальные уникальные идентификаторы (GUID), которые описывают типы данных пакетов, включаемых для каждой точки в каждом штрихе.</span><span class="sxs-lookup"><span data-stu-id="9fc35-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="9fc35-132">Полный список доступных свойств пакетов см. в разделе [константы паккетпропертигуидс](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9fc35-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="9fc35-133">В одном вызове **метода иинканализер:: аддстрокес** можно добавлять только штрихи с теми же описаниями пакетов.</span><span class="sxs-lookup"><span data-stu-id="9fc35-133">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokes Method**.</span></span>

 

<span data-ttu-id="9fc35-134">Этот метод расширяет «грязную» область до объединения текущего значения области и ограничивающего прямоугольника добавленных штрихов.</span><span class="sxs-lookup"><span data-stu-id="9fc35-134">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="9fc35-135">Если [**иинканализер**](iinkanalyzer.md) уже содержит штрих с тем же идентификатором, что и один из добавляемых штрихов, **Иинканализер** возвращает **значение HRESULT** для **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="9fc35-135">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc35-136">Требования</span><span class="sxs-lookup"><span data-stu-id="9fc35-136">Requirements</span></span>



| <span data-ttu-id="9fc35-137">Требование</span><span class="sxs-lookup"><span data-stu-id="9fc35-137">Requirement</span></span> | <span data-ttu-id="9fc35-138">Значение</span><span class="sxs-lookup"><span data-stu-id="9fc35-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc35-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fc35-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc35-140">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9fc35-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9fc35-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fc35-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc35-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9fc35-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9fc35-143">Header</span><span class="sxs-lookup"><span data-stu-id="9fc35-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fc35-144"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9fc35-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9fc35-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9fc35-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fc35-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fc35-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9fc35-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fc35-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc35-148">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="9fc35-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9fc35-149">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="9fc35-149">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="9fc35-150">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="9fc35-150">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="9fc35-151">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="9fc35-151">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="9fc35-152">**Метод Иинканализер:: Ремовестроке**</span><span class="sxs-lookup"><span data-stu-id="9fc35-152">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="9fc35-153">**Метод Иинканализер:: Ремовестрокес**</span><span class="sxs-lookup"><span data-stu-id="9fc35-153">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="9fc35-154">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9fc35-154">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

