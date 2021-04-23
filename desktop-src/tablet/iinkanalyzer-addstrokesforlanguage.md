---
description: Добавляет данные Stroke для нескольких штрихов в Иинканализер и присваивает заданный идентификатор языка и региональных параметров штрихам.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: 'Метод Иинканализер:: Аддстрокесфорлангуаже (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7f1c8bde9f1fe9d9c7123fa3c40540d0fd2660ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263146"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a><span data-ttu-id="66694-103">Метод Иинканализер:: Аддстрокесфорлангуаже</span><span class="sxs-lookup"><span data-stu-id="66694-103">IInkAnalyzer::AddStrokesForLanguage method</span></span>

<span data-ttu-id="66694-104">Добавляет данные Stroke для нескольких штрихов в [**иинканализер**](iinkanalyzer.md) и присваивает заданный идентификатор языка и региональных параметров штрихам.</span><span class="sxs-lookup"><span data-stu-id="66694-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the specified culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="66694-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66694-105">Syntax</span></span>


```C++
HRESULT AddStrokesForLanguage(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plIdofStrokesToAdd,
  [in]  LONG         lStrokesLCID,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="66694-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66694-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66694-107">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66694-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66694-108">Число добавляемых штрихов.</span><span class="sxs-lookup"><span data-stu-id="66694-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="66694-109">*плидофстрокестоадд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66694-109">*plIdofStrokesToAdd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66694-110">Массив, содержащий идентификаторы штрихов.</span><span class="sxs-lookup"><span data-stu-id="66694-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="66694-111">*лстрокеслЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66694-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66694-112">Значение, представляющее идентификатор языка и региональных параметров, присваиваемый штрихам.</span><span class="sxs-lookup"><span data-stu-id="66694-112">A value that represents the culture identifier to assign to the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="66694-113">*улстрокепаккетдескриптионкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66694-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66694-114">Число свойств в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="66694-114">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="66694-115">*пстрокепаккетдескриптионгуидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66694-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66694-116">Массив, содержащий идентификаторы свойств пакета.</span><span class="sxs-lookup"><span data-stu-id="66694-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="66694-117">*пулпаккетдатакаунтперстроке* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66694-117">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66694-118">Массив, содержащий количество пакетов в каждом штрихе.</span><span class="sxs-lookup"><span data-stu-id="66694-118">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="66694-119">*плстрокепаккетдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66694-119">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66694-120">Массив, содержащий данные пакета для штрихов.</span><span class="sxs-lookup"><span data-stu-id="66694-120">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="66694-121">*ппконтекстнодестрокеаддедто* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="66694-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66694-122">[**Иконтекстноде**](icontextnode.md) , к которому анализатор рукописного ввода добавил штрихи.</span><span class="sxs-lookup"><span data-stu-id="66694-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66694-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66694-123">Return value</span></span>

<span data-ttu-id="66694-124">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="66694-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="66694-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66694-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="66694-126">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодестрокеаддедто* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="66694-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="66694-127">Если *ппконтекстнодестрокеаддедто* имеет **значение NULL**, это означает, что вызывающий объект не заинтересован в возвращаемом значении метода.</span><span class="sxs-lookup"><span data-stu-id="66694-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="66694-128">[**Иинканализер**](iinkanalyzer.md) добавляет штрихи к [**иконтекстноде**](icontextnode.md) типа унклассифиединк (см. раздел [типы узлов контекста](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="66694-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="66694-129">Этот узел находится в коллекции подузлов корневого узла (см. методы [**иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md) и [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="66694-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="66694-130">[**Иинканализер**](iinkanalyzer.md) назначает идентификатор языка и региональных параметров *лстрокелЦид* штрихам и добавляет штрихи к первому узлу контекста унклассифиединк в корневом узле анализатора красок, который содержит штрихи с одним и тем же идентификатором языка и региональных параметров.</span><span class="sxs-lookup"><span data-stu-id="66694-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the *lStrokeLCID* culture identifier to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="66694-131">Если анализатор рукописного ввода не имеет узла с таким же идентификатором языка и региональных параметров, он создает новый узел контекста Унклассифиединк в своем корневом узле и добавляет штрихи в новый узел контекста Унклассифиединк.</span><span class="sxs-lookup"><span data-stu-id="66694-131">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="66694-132">*плстрокепаккетдата* содержит данные пакетов для всех штрихов.</span><span class="sxs-lookup"><span data-stu-id="66694-132">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="66694-133">*пстрокепаккетдескриптионгуидс* содержит глобальные уникальные идентификаторы (GUID), которые описывают типы данных пакетов, включаемых для каждой точки в каждом штрихе.</span><span class="sxs-lookup"><span data-stu-id="66694-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="66694-134">Полный список доступных свойств пакетов см. в разделе [константы паккетпропертигуидс](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="66694-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="66694-135">В одном вызове [**метода иинканализер:: аддстрокес**](iinkanalyzer-addstrokes.md)можно добавлять только штрихи с теми же описаниями пакетов.</span><span class="sxs-lookup"><span data-stu-id="66694-135">Only strokes with the same packet descriptions can be added in a single call to [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md).</span></span>

 

<span data-ttu-id="66694-136">Этот метод расширяет «грязную» область до объединения текущего значения области и ограничивающего прямоугольника добавленных штрихов.</span><span class="sxs-lookup"><span data-stu-id="66694-136">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="66694-137">Если [**иинканализер**](iinkanalyzer.md) уже содержит штрих с тем же идентификатором, что и один из добавляемых штрихов, **Иинканализер** возвращает **значение HRESULT** для **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="66694-137">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="66694-138">Требования</span><span class="sxs-lookup"><span data-stu-id="66694-138">Requirements</span></span>



| <span data-ttu-id="66694-139">Требование</span><span class="sxs-lookup"><span data-stu-id="66694-139">Requirement</span></span> | <span data-ttu-id="66694-140">Значение</span><span class="sxs-lookup"><span data-stu-id="66694-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66694-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66694-141">Minimum supported client</span></span><br/> | <span data-ttu-id="66694-142">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="66694-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="66694-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66694-143">Minimum supported server</span></span><br/> | <span data-ttu-id="66694-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="66694-144">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="66694-145">Header</span><span class="sxs-lookup"><span data-stu-id="66694-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="66694-146"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="66694-146"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="66694-147">DLL</span><span class="sxs-lookup"><span data-stu-id="66694-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66694-148"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66694-148"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="66694-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66694-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66694-150">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="66694-150">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="66694-151">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="66694-151">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="66694-152">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="66694-152">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="66694-153">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="66694-153">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="66694-154">**Метод Иинканализер:: Ремовестроке**</span><span class="sxs-lookup"><span data-stu-id="66694-154">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="66694-155">**Метод Иинканализер:: Ремовестрокес**</span><span class="sxs-lookup"><span data-stu-id="66694-155">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="66694-156">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="66694-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

