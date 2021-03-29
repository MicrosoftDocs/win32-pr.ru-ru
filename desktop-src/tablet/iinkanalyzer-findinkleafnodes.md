---
description: Извлекает все конечные узлы рукописного ввода.
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'Метод Иинканализер:: Финдинклеафнодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5ebcfe542ab03f2e3d3a24c29142e41433c9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897465"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a><span data-ttu-id="95229-103">Метод Иинканализер:: Финдинклеафнодес</span><span class="sxs-lookup"><span data-stu-id="95229-103">IInkAnalyzer::FindInkLeafNodes method</span></span>

<span data-ttu-id="95229-104">Извлекает все конечные узлы рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="95229-104">Retrieves all of the ink leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="95229-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95229-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="95229-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95229-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95229-107">*ппконтекстнодесфаунд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="95229-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95229-108">Указатель на коллекцию [**иконтекстнодес**](icontextnodes.md) , содержащую все конечные узлы рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="95229-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all ink leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95229-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95229-109">Return value</span></span>

<span data-ttu-id="95229-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="95229-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95229-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95229-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="95229-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="95229-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="95229-113">Конечные узлы не содержат дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="95229-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="95229-114">Узлы рукописного ввода содержат данные Stroke.</span><span class="sxs-lookup"><span data-stu-id="95229-114">Ink nodes contain stroke data.</span></span> <span data-ttu-id="95229-115">Примерами перьевых узлов являются объекты Инкворд, Инкдравинг и Инкбуллет [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="95229-115">Examples of ink leaf nodes are InkWord, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="95229-116">Дополнительные сведения см. в разделе [типы узлов контекста](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="95229-116">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95229-117">Требования</span><span class="sxs-lookup"><span data-stu-id="95229-117">Requirements</span></span>



| <span data-ttu-id="95229-118">Требование</span><span class="sxs-lookup"><span data-stu-id="95229-118">Requirement</span></span> | <span data-ttu-id="95229-119">Значение</span><span class="sxs-lookup"><span data-stu-id="95229-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95229-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95229-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95229-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="95229-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="95229-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95229-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95229-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="95229-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="95229-124">Header</span><span class="sxs-lookup"><span data-stu-id="95229-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="95229-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="95229-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="95229-126">DLL</span><span class="sxs-lookup"><span data-stu-id="95229-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95229-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95229-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="95229-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95229-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95229-129">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="95229-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="95229-130">**Метод Иинканализер:: Финдинклеафнодесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="95229-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="95229-131">**Метод Иинканализер:: Финдлеафнодес**</span><span class="sxs-lookup"><span data-stu-id="95229-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="95229-132">**Метод Иинканализер:: Финдноде**</span><span class="sxs-lookup"><span data-stu-id="95229-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="95229-133">**Метод Иинканализер:: Финднодесофтипе**</span><span class="sxs-lookup"><span data-stu-id="95229-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="95229-134">**Метод Иинканализер:: Финднодесофтипефорстрокес**</span><span class="sxs-lookup"><span data-stu-id="95229-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="95229-135">**Метод Иинканализер:: Финднодесофтипеинсубтри**</span><span class="sxs-lookup"><span data-stu-id="95229-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="95229-136">**Метод Иинканализер:: Финднодесвискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="95229-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="95229-137">**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**</span><span class="sxs-lookup"><span data-stu-id="95229-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="95229-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="95229-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

