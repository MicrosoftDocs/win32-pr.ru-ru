---
description: Добавляет данные Stroke для одного штриха в Иинканализер и присваивает штриху конкретный идентификатор языка и региональных параметров.
ms.assetid: 65eb805e-05ed-4144-b17e-872c47ab33fa
title: 'Метод Иинканализер:: Аддстрокефорлангуаже (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 674a58ef891d919d09f86f28a35748de3537db91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897470"
---
# <a name="iinkanalyzeraddstrokeforlanguage-method"></a><span data-ttu-id="ec7c2-103">Метод Иинканализер:: Аддстрокефорлангуаже</span><span class="sxs-lookup"><span data-stu-id="ec7c2-103">IInkAnalyzer::AddStrokeForLanguage method</span></span>

<span data-ttu-id="ec7c2-104">Добавляет данные Stroke для одного штриха в [**иинканализер**](iinkanalyzer.md) и присваивает штриху конкретный идентификатор языка и региональных параметров.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns a specific culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7c2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec7c2-105">Syntax</span></span>


```C++
HRESULT AddStrokeForLanguage(
  [in]  LONG         lStrokeId,
  [in]  LONG         lStrokeLCID,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="ec7c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec7c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec7c2-107">*лстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec7c2-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec7c2-108">Идентификатор добавляемого штриха.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="ec7c2-109">*лстрокелЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec7c2-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec7c2-110">Идентификатор языка и региональных параметров, присваиваемый обводке.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-110">The culture identifier to assign to the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="ec7c2-111">*улстрокепаккетдатакаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec7c2-111">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec7c2-112">Число пакетов в штрихе.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-112">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="ec7c2-113">*плстрокепаккетдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec7c2-113">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec7c2-114">Массив, содержащий данные пакета для штриха.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-114">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="ec7c2-115">*улстрокепаккетдескриптионкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec7c2-115">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec7c2-116">Число свойств в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-116">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="ec7c2-117">*пстрокепаккетдескриптионгуидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec7c2-117">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec7c2-118">Массив, содержащий идентификаторы свойств пакета.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-118">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="ec7c2-119">*ппконтекстнодестрокеаддедто* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ec7c2-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec7c2-120">Указатель, значение которого равно указателю [**иконтекстноде**](icontextnode.md) , содержащего только что добавленный росчерк.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-120">A pointer whose value is set to the pointer of the [**IContextNode**](icontextnode.md) that contains the newly added stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec7c2-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec7c2-121">Return value</span></span>

<span data-ttu-id="ec7c2-122">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ec7c2-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ec7c2-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec7c2-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ec7c2-124">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодестрокеаддедто* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="ec7c2-125">Если *ппконтекстнодестрокеаддедто* имеет **значение NULL**, это означает, что вызывающий объект не заинтересован в возвращаемом значении метода.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="ec7c2-126">[**Иинканализер**](iinkanalyzer.md) добавляет штрих в [**иконтекстноде**](icontextnode.md) типа унклассифиединк (см. раздел [типы узлов контекста](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="ec7c2-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="ec7c2-127">Этот узел находится в коллекции подузлов корневого узла (см. методы [**иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md) и [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="ec7c2-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="ec7c2-128">[**Иинканализер**](iinkanalyzer.md) назначает идентификатор языка и региональных параметров *лстрокелЦид* для штриха и добавляет штрих к первому узлу контекста унклассифиединк в корневом узле анализатора красок, который содержит штрихи с одним и тем же идентификатором языка и региональных параметров.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns *lStrokeLCID* culture identifier to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="ec7c2-129">Если анализатор рукописного ввода не имеет узла с таким же идентификатором языка и региональных параметров, он создает новый узел контекста Унклассифиединк в своем корневом узле и добавляет этот росчерк в новый узел контекста Унклассифиединк.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="ec7c2-130">*плстрокепаккетдата* содержит данные пакетов для всех точек в штрихе.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-130">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="ec7c2-131">*пстрокепаккетдескриптионгуидс* содержит глобальные уникальные идентификаторы (GUID), которые описывают типы данных пакетов, включаемые для каждой точки в штрихе.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="ec7c2-132">Полный список доступных свойств пакетов см. в разделе [константы паккетпропертигуидс](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ec7c2-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="ec7c2-133">Этот метод расширяет «грязную» область до объединения текущего значения области и ограничивающего прямоугольника добавленного штриха.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-133">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="ec7c2-134">Если [**иинканализер**](iinkanalyzer.md) уже содержит штрих с тем же идентификатором Stroke, **Иинканализер** возвращает **значение HRESULT** для **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="ec7c2-134">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec7c2-135">Требования</span><span class="sxs-lookup"><span data-stu-id="ec7c2-135">Requirements</span></span>



| <span data-ttu-id="ec7c2-136">Требование</span><span class="sxs-lookup"><span data-stu-id="ec7c2-136">Requirement</span></span> | <span data-ttu-id="ec7c2-137">Значение</span><span class="sxs-lookup"><span data-stu-id="ec7c2-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7c2-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec7c2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ec7c2-139">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ec7c2-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ec7c2-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec7c2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ec7c2-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ec7c2-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ec7c2-142">Header</span><span class="sxs-lookup"><span data-stu-id="ec7c2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec7c2-143"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ec7c2-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ec7c2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ec7c2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec7c2-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec7c2-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ec7c2-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec7c2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7c2-147">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="ec7c2-147">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ec7c2-148">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="ec7c2-148">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="ec7c2-149">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="ec7c2-149">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="ec7c2-150">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="ec7c2-150">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="ec7c2-151">**Метод Иинканализер:: Ремовестроке**</span><span class="sxs-lookup"><span data-stu-id="ec7c2-151">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="ec7c2-152">**Метод Иинканализер:: Ремовестрокес**</span><span class="sxs-lookup"><span data-stu-id="ec7c2-152">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="ec7c2-153">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ec7c2-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

