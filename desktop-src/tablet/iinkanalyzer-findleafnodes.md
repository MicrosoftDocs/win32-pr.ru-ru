---
description: Извлекает все конечные узлы.
ms.assetid: 5534053c-c5b9-4576-857f-c8af39e821a7
title: 'Метод Иинканализер:: Финдлеафнодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f923afe94c25e45dbcbfe79d554282b69ebec3a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542023"
---
# <a name="iinkanalyzerfindleafnodes-method"></a><span data-ttu-id="b8a79-103">Метод Иинканализер:: Финдлеафнодес</span><span class="sxs-lookup"><span data-stu-id="b8a79-103">IInkAnalyzer::FindLeafNodes method</span></span>

<span data-ttu-id="b8a79-104">Извлекает все конечные узлы.</span><span class="sxs-lookup"><span data-stu-id="b8a79-104">Retrieves all of the leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a79-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8a79-105">Syntax</span></span>


```C++
HRESULT FindLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="b8a79-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8a79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a79-107">*ппконтекстнодесфаунд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b8a79-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a79-108">Указатель на коллекцию [**иконтекстнодес**](icontextnodes.md) , содержащую все конечные узлы.</span><span class="sxs-lookup"><span data-stu-id="b8a79-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a79-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8a79-109">Return value</span></span>

<span data-ttu-id="b8a79-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b8a79-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8a79-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8a79-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b8a79-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="b8a79-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="b8a79-113">Конечные узлы не содержат дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="b8a79-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="b8a79-114">Примерами перьевых узлов являются объекты Инкворд, Текстворд, Image, Инкдравинг и Инкбуллет [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b8a79-114">Examples of ink leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="b8a79-115">Дополнительные сведения см. в разделе [типы узлов контекста](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="b8a79-115">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a79-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b8a79-116">Requirements</span></span>



| <span data-ttu-id="b8a79-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b8a79-117">Requirement</span></span> | <span data-ttu-id="b8a79-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b8a79-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a79-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8a79-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a79-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b8a79-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b8a79-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8a79-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a79-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b8a79-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b8a79-123">Header</span><span class="sxs-lookup"><span data-stu-id="b8a79-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8a79-124"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b8a79-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b8a79-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b8a79-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8a79-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8a79-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b8a79-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8a79-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a79-128">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="b8a79-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b8a79-129">**Метод Иинканализер:: Финдинклеафнодес**</span><span class="sxs-lookup"><span data-stu-id="b8a79-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="b8a79-130">**Метод Иинканализер:: Финдинклеафнодесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="b8a79-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="b8a79-131">**Метод Иинканализер:: Финдноде**</span><span class="sxs-lookup"><span data-stu-id="b8a79-131">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="b8a79-132">**Метод Иинканализер:: Финднодесофтипе**</span><span class="sxs-lookup"><span data-stu-id="b8a79-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="b8a79-133">**Метод Иинканализер:: Финднодесофтипефорстрокес**</span><span class="sxs-lookup"><span data-stu-id="b8a79-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="b8a79-134">**Метод Иинканализер:: Финднодесофтипеинсубтри**</span><span class="sxs-lookup"><span data-stu-id="b8a79-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="b8a79-135">**Метод Иинканализер:: Финднодесвискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b8a79-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="b8a79-136">**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**</span><span class="sxs-lookup"><span data-stu-id="b8a79-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="b8a79-137">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="b8a79-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

