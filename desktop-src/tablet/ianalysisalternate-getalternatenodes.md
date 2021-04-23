---
description: Возвращает объекты Иконтекстноде, связанные с этим альтернативным.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'Метод Ианалисисалтернате:: Жеталтернатенодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682740"
---
# <a name="ianalysisalternategetalternatenodes-method"></a><span data-ttu-id="c2790-103">Метод Ианалисисалтернате:: Жеталтернатенодес</span><span class="sxs-lookup"><span data-stu-id="c2790-103">IAnalysisAlternate::GetAlternateNodes method</span></span>

<span data-ttu-id="c2790-104">Возвращает объекты [**иконтекстноде**](icontextnode.md) , связанные с этим альтернативным.</span><span class="sxs-lookup"><span data-stu-id="c2790-104">Gets the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2790-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2790-105">Syntax</span></span>


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a><span data-ttu-id="c2790-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2790-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2790-107">*ппалтернатенодес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c2790-107">*ppAlternateNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2790-108">Указатель на коллекцию [**иконтекстнодес**](icontextnodes.md) , содержащую объекты [**иконтекстноде**](icontextnode.md) , связанные с этим альтернативным.</span><span class="sxs-lookup"><span data-stu-id="c2790-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection that contains [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2790-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2790-109">Return value</span></span>

<span data-ttu-id="c2790-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c2790-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2790-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2790-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c2790-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппалтернатенодес* , когда больше не нужно использовать коллекцию узлов контекста.</span><span class="sxs-lookup"><span data-stu-id="c2790-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternateNodes* when you no longer need to use the context node collection.</span></span>

 

<span data-ttu-id="c2790-113">Этот метод возвращает конечные узлы контекста, связанные с этим альтернативным.</span><span class="sxs-lookup"><span data-stu-id="c2790-113">This method returns the leaf context nodes that are associated with this alternate.</span></span> <span data-ttu-id="c2790-114">Примерами конечных узлов являются узлы контекста Инкворд, Текстворд, Image, Инкдравинг и Инкбуллет.</span><span class="sxs-lookup"><span data-stu-id="c2790-114">Examples of leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet context nodes.</span></span> <span data-ttu-id="c2790-115">Дополнительные сведения см. в разделе [**иконтекстноде:: GetType**](icontextnode-gettype.md) и [типы узлов контекста](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="c2790-115">For more information, see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="c2790-116">Так как они соответствуют альтернативным объектам, эти объекты [**иконтекстноде**](icontextnode.md) не являются потомками корневого **иконтекстноде** объекта [**Иинканализер**](iinkanalyzer.md) (см. [**метод иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md)), если только они не являются верхним вариантом, который является первым элементом в коллекции [**ианалисисалтернатес**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="c2790-116">Because they correspond to alternates, these [**IContextNode**](icontextnode.md) objects are not descendants of the [**IInkAnalyzer**](iinkanalyzer.md) object's root **IContextNode** (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)) unless they are the top alternate, which is the first element in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2790-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c2790-117">Requirements</span></span>



| <span data-ttu-id="c2790-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c2790-118">Requirement</span></span> | <span data-ttu-id="c2790-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c2790-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2790-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2790-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2790-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c2790-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c2790-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2790-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2790-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c2790-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c2790-124">Header</span><span class="sxs-lookup"><span data-stu-id="c2790-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2790-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c2790-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c2790-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c2790-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2790-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2790-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c2790-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2790-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2790-129">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="c2790-129">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="c2790-130">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="c2790-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c2790-131">**иконтекстнодес**</span><span class="sxs-lookup"><span data-stu-id="c2790-131">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="c2790-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="c2790-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> <dt>

[<span data-ttu-id="c2790-133">System. Windows. Ink. Аналисискоре. Аналисисалтернатебасе. Алтернатенодес</span><span class="sxs-lookup"><span data-stu-id="c2790-133">System.Windows.Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes</span></span>](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

