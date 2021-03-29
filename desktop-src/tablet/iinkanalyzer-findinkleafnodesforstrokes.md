---
description: Получает конечные узлы рукописного ввода, содержащие указанные штрихи.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'Метод Иинканализер:: Финдинклеафнодесфорстрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897461"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a><span data-ttu-id="cb3c3-103">Метод Иинканализер:: Финдинклеафнодесфорстрокес</span><span class="sxs-lookup"><span data-stu-id="cb3c3-103">IInkAnalyzer::FindInkLeafNodesForStrokes method</span></span>

<span data-ttu-id="cb3c3-104">Получает конечные узлы рукописного ввода, содержащие указанные штрихи.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-104">Retrieves the ink leaf nodes that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb3c3-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="cb3c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb3c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb3c3-107">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb3c3-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3c3-108">Число переданных идентификаторов Stroke.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-108">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="cb3c3-109">*плстрокеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb3c3-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3c3-110">Массив идентификаторов Stroke.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-110">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="cb3c3-111">*ппконтекстнодесфаунд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb3c3-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3c3-112">Коллекция объектов [**иконтекстноде**](icontextnode.md) , которая содержит все конечные узлы рукописного ввода, содержащие штрихи с идентификаторами в массиве *плстрокеидс* .</span><span class="sxs-lookup"><span data-stu-id="cb3c3-112">The collection of [**IContextNode**](icontextnode.md) objects that contain all the ink leaf nodes that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb3c3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb3c3-113">Return value</span></span>

<span data-ttu-id="cb3c3-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cb3c3-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3c3-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb3c3-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cb3c3-116">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="cb3c3-117">Конечные узлы не содержат дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-117">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="cb3c3-118">Узлы рукописного ввода содержат данные Stroke.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-118">Ink nodes contain stroke data.</span></span> <span data-ttu-id="cb3c3-119">Примерами перьевых узлов являются Инкворд, Инкдравинг, Андинкбуллет [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="cb3c3-119">Examples of ink leaf nodes are InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="cb3c3-120">Дополнительные сведения см. в разделе [типы узлов контекста](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="cb3c3-120">For more information, see [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="cb3c3-121">Если ни один из узлов не содержит указанных штрихов, возвращается пустая коллекция [**иконтекстнодес**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="cb3c3-121">If no nodes contain the specified strokes, an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span> <span data-ttu-id="cb3c3-122">Аналогично, если *улстрокеидскаунт* равен нулю, возвращается пустая коллекция **иконтекстнодес** .</span><span class="sxs-lookup"><span data-stu-id="cb3c3-122">Similarly, if *ulStrokeIdsCount* is zero, an empty **IContextNodes** collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb3c3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="cb3c3-123">Requirements</span></span>



| <span data-ttu-id="cb3c3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="cb3c3-124">Requirement</span></span> | <span data-ttu-id="cb3c3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cb3c3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3c3-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb3c3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cb3c3-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cb3c3-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cb3c3-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb3c3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cb3c3-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cb3c3-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cb3c3-130">Header</span><span class="sxs-lookup"><span data-stu-id="cb3c3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb3c3-131"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cb3c3-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cb3c3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cb3c3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb3c3-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb3c3-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cb3c3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb3c3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3c3-135">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cb3c3-136">**Метод Иинканализер:: Финдинклеафнодес**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-136">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="cb3c3-137">**Метод Иинканализер:: Финдлеафнодес**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="cb3c3-138">**Метод Иинканализер:: Финдноде**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="cb3c3-139">**Метод Иинканализер:: Финднодесофтипе**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="cb3c3-140">**Метод Иинканализер:: Финднодесофтипефорстрокес**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-140">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="cb3c3-141">**Метод Иинканализер:: Финднодесофтипеинсубтри**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-141">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="cb3c3-142">**Метод Иинканализер:: Финднодесвискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-142">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="cb3c3-143">**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-143">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="cb3c3-144">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="cb3c3-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

