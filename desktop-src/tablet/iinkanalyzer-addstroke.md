---
description: Добавляет данные Stroke для одного штриха в Иинканализер и присваивает штриху идентификатор языка и региональных параметров активного потока ввода.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: 'Метод Иинканализер:: Аддстроке (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc946e7975772eb7be6fff54d01bb1a6dae8ebe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263147"
---
# <a name="iinkanalyzeraddstroke-method"></a><span data-ttu-id="45cca-103">Метод Иинканализер:: Аддстроке</span><span class="sxs-lookup"><span data-stu-id="45cca-103">IInkAnalyzer::AddStroke method</span></span>

<span data-ttu-id="45cca-104">Добавляет данные Stroke для одного штриха в [**иинканализер**](iinkanalyzer.md) и присваивает штриху идентификатор языка и региональных параметров активного потока ввода.</span><span class="sxs-lookup"><span data-stu-id="45cca-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45cca-105">Syntax</span></span>


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="45cca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="45cca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45cca-107">*лстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45cca-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45cca-108">Идентификатор добавляемого штриха.</span><span class="sxs-lookup"><span data-stu-id="45cca-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="45cca-109">*улстрокепаккетдатакаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45cca-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45cca-110">Число пакетов в штрихе.</span><span class="sxs-lookup"><span data-stu-id="45cca-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="45cca-111">*плстрокепаккетдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45cca-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45cca-112">Массив, содержащий данные пакета для штриха.</span><span class="sxs-lookup"><span data-stu-id="45cca-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="45cca-113">*улстрокепаккетдескриптионкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45cca-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45cca-114">Число свойств пакетов в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="45cca-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="45cca-115">*пстрокепаккетдескриптионгуидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45cca-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45cca-116">Массив, содержащий идентификаторы свойств пакета.</span><span class="sxs-lookup"><span data-stu-id="45cca-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="45cca-117">*ппконтекстнодестрокеаддедто* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="45cca-117">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45cca-118">Указатель на [**иконтекстноде**](icontextnode.md) , к которому [**иинканализер**](iinkanalyzer.md) добавил штрих.</span><span class="sxs-lookup"><span data-stu-id="45cca-118">A pointer to the [**IContextNode**](icontextnode.md) to which the [**IInkAnalyzer**](iinkanalyzer.md) added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45cca-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45cca-119">Return value</span></span>

<span data-ttu-id="45cca-120">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="45cca-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="45cca-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45cca-121">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="45cca-122">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодестрокеаддедто* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="45cca-122">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="45cca-123">Если *ппконтекстнодестрокеаддедто* имеет **значение NULL**, это означает, что вызывающий объект не заинтересован в возвращаемом значении метода.</span><span class="sxs-lookup"><span data-stu-id="45cca-123">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="45cca-124">[**Иинканализер**](iinkanalyzer.md) добавляет штрих в [**иконтекстноде**](icontextnode.md) типа унклассифиединк (см. раздел [типы узлов контекста](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="45cca-124">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="45cca-125">Этот узел находится в коллекции подузлов корневого узла (см. методы [**иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md) и [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="45cca-125">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="45cca-126">[**Иинканализер**](iinkanalyzer.md) назначает идентификатор языка и региональных параметров для активного входного потока штриху и добавляет штрих в первый узел унклассифиединк контекста в корневом узле анализатора красок, который содержит штрихи с одним и тем же идентификатором языка и региональных параметров.</span><span class="sxs-lookup"><span data-stu-id="45cca-126">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="45cca-127">Если анализатор рукописного ввода не имеет узла с таким же идентификатором языка и региональных параметров, он создает новый узел контекста Унклассифиединк в своем корневом узле и добавляет этот росчерк в новый узел контекста Унклассифиединк.</span><span class="sxs-lookup"><span data-stu-id="45cca-127">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="45cca-128">*плстрокепаккетдата* содержит данные пакетов для всех точек в штрихе.</span><span class="sxs-lookup"><span data-stu-id="45cca-128">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="45cca-129">*пстрокепаккетдескриптионгуидс* содержит глобальные уникальные идентификаторы (GUID), которые описывают типы данных пакетов, включаемые для каждой точки в штрихе.</span><span class="sxs-lookup"><span data-stu-id="45cca-129">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="45cca-130">Полный список доступных свойств пакетов см. в разделе [константы паккетпропертигуидс](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="45cca-130">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="45cca-131">Этот метод расширяет «грязную» область до объединения текущего значения области и ограничивающего прямоугольника добавленного штриха.</span><span class="sxs-lookup"><span data-stu-id="45cca-131">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="45cca-132">Если [**иинканализер**](iinkanalyzer.md) уже содержит штрих с тем же идентификатором Stroke, **Иинканализер** возвращает **значение HRESULT** для **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="45cca-132">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="45cca-133">Требования</span><span class="sxs-lookup"><span data-stu-id="45cca-133">Requirements</span></span>



| <span data-ttu-id="45cca-134">Требование</span><span class="sxs-lookup"><span data-stu-id="45cca-134">Requirement</span></span> | <span data-ttu-id="45cca-135">Значение</span><span class="sxs-lookup"><span data-stu-id="45cca-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45cca-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45cca-136">Minimum supported client</span></span><br/> | <span data-ttu-id="45cca-137">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="45cca-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="45cca-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45cca-138">Minimum supported server</span></span><br/> | <span data-ttu-id="45cca-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="45cca-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="45cca-140">Header</span><span class="sxs-lookup"><span data-stu-id="45cca-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="45cca-141"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="45cca-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="45cca-142">DLL</span><span class="sxs-lookup"><span data-stu-id="45cca-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45cca-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45cca-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="45cca-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45cca-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45cca-145">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="45cca-145">**InkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="45cca-146">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="45cca-146">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="45cca-147">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="45cca-147">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="45cca-148">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="45cca-148">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="45cca-149">**Метод Иинканализер:: Ремовестроке**</span><span class="sxs-lookup"><span data-stu-id="45cca-149">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="45cca-150">**Метод Иинканализер:: Ремовестрокес**</span><span class="sxs-lookup"><span data-stu-id="45cca-150">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="45cca-151">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="45cca-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

