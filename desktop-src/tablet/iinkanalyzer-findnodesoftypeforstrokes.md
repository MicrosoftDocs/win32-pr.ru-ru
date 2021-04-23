---
description: Извлекает все объекты Иконтекстноде указанного типа, содержащие указанные штрихи.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'Метод Иинканализер:: Финднодесофтипефорстрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711114"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a><span data-ttu-id="deb81-103">Метод Иинканализер:: Финднодесофтипефорстрокес</span><span class="sxs-lookup"><span data-stu-id="deb81-103">IInkAnalyzer::FindNodesOfTypeForStrokes method</span></span>

<span data-ttu-id="deb81-104">Извлекает все объекты [**иконтекстноде**](icontextnode.md) указанного типа, содержащие указанные штрихи.</span><span class="sxs-lookup"><span data-stu-id="deb81-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb81-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="deb81-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="deb81-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="deb81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb81-107">*пнодетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="deb81-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb81-108">Глобальный уникальный идентификатор (GUID), указывающий тип узла.</span><span class="sxs-lookup"><span data-stu-id="deb81-108">The globally unique identifier (GUID) that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="deb81-109">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="deb81-109">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb81-110">Число переданных идентификаторов Stroke.</span><span class="sxs-lookup"><span data-stu-id="deb81-110">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="deb81-111">*плстрокеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="deb81-111">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb81-112">Массив идентификаторов Stroke.</span><span class="sxs-lookup"><span data-stu-id="deb81-112">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="deb81-113">*ппконтекстнодесфаунд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="deb81-113">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deb81-114">Коллекция объектов [**иконтекстноде**](icontextnode.md) , содержащих все узлы типа *пнодетипе* , которые содержат штрихи с идентификаторами в массиве *плстрокеидс* .</span><span class="sxs-lookup"><span data-stu-id="deb81-114">The collection of [**IContextNode**](icontextnode.md) objects that contain all the nodes of type *pNodeType* that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb81-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="deb81-115">Return value</span></span>

<span data-ttu-id="deb81-116">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="deb81-116">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="deb81-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="deb81-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="deb81-118">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="deb81-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="deb81-119">Свойство *пнодетипе* должно содержать идентификатор GUID из констант [типов узлов контекста](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="deb81-119">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="deb81-120">Если указанный тип узла не является конечным узлом, но один из потомков узла ссылается на штрих в коллекции штрихов, этот узел добавляется в возвращаемую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="deb81-120">If the specified node type is not a leaf node, but one of the node's descendants references a stroke in the strokes collection, that node is added to the collection that is returned.</span></span>

<span data-ttu-id="deb81-121">Если [**иинканализер**](iinkanalyzer.md) не содержит таких [**иконтекстноде**](icontextnode.md), возвращается пустая коллекция [**иконтекстнодес**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="deb81-121">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="deb81-122">Требования</span><span class="sxs-lookup"><span data-stu-id="deb81-122">Requirements</span></span>



| <span data-ttu-id="deb81-123">Требование</span><span class="sxs-lookup"><span data-stu-id="deb81-123">Requirement</span></span> | <span data-ttu-id="deb81-124">Значение</span><span class="sxs-lookup"><span data-stu-id="deb81-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deb81-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="deb81-125">Minimum supported client</span></span><br/> | <span data-ttu-id="deb81-126">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="deb81-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="deb81-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="deb81-127">Minimum supported server</span></span><br/> | <span data-ttu-id="deb81-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="deb81-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="deb81-129">Header</span><span class="sxs-lookup"><span data-stu-id="deb81-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="deb81-130"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="deb81-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="deb81-131">DLL</span><span class="sxs-lookup"><span data-stu-id="deb81-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deb81-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="deb81-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="deb81-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="deb81-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb81-134">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="deb81-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="deb81-135">**Метод Иинканализер:: Финдинклеафнодес**</span><span class="sxs-lookup"><span data-stu-id="deb81-135">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="deb81-136">**Метод Иинканализер:: Финдинклеафнодесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="deb81-136">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="deb81-137">**Метод Иинканализер:: Финдлеафнодес**</span><span class="sxs-lookup"><span data-stu-id="deb81-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="deb81-138">**Метод Иинканализер:: Финдноде**</span><span class="sxs-lookup"><span data-stu-id="deb81-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="deb81-139">**Метод Иинканализер:: Финднодесофтипе**</span><span class="sxs-lookup"><span data-stu-id="deb81-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="deb81-140">**Метод Иинканализер:: Финднодесофтипеинсубтри**</span><span class="sxs-lookup"><span data-stu-id="deb81-140">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="deb81-141">**Метод Иинканализер:: Финднодесвискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="deb81-141">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="deb81-142">**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**</span><span class="sxs-lookup"><span data-stu-id="deb81-142">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="deb81-143">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="deb81-143">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

