---
description: Извлекает все объекты Иконтекстноде указанного типа, являющиеся потомками указанного объекта Иконтекстноде.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: 'Метод Иинканализер:: Финднодесофтипеинсубтри (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 545e56d297b053b5b6f5dc61f944d6a4f6d4e03c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711113"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a><span data-ttu-id="eea86-103">Метод Иинканализер:: Финднодесофтипеинсубтри</span><span class="sxs-lookup"><span data-stu-id="eea86-103">IInkAnalyzer::FindNodesOfTypeInSubTree method</span></span>

<span data-ttu-id="eea86-104">Извлекает все объекты [**иконтекстноде**](icontextnode.md) указанного типа, являющиеся потомками указанного объекта **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="eea86-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea86-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eea86-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="eea86-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eea86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea86-107">*пнодетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eea86-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea86-108">**Идентификатор GUID** , указывающий тип узла.</span><span class="sxs-lookup"><span data-stu-id="eea86-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="eea86-109">*пконтекстнодетосеарчфром* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eea86-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea86-110">Объект [**иконтекстноде**](icontextnode.md) , потомки которого ищутся.</span><span class="sxs-lookup"><span data-stu-id="eea86-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="eea86-111">*ппконтекстнодесфаунд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eea86-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eea86-112">Коллекция [**иконтекстнодес**](icontextnodes.md) , содержащая все узлы типа *пнодетипе* , которые являются потомками *пконтекстнодетосеарчфром*.</span><span class="sxs-lookup"><span data-stu-id="eea86-112">The [**IContextNodes**](icontextnodes.md) collection containing all nodes of type *pNodeType* that are descendants of *pContextNodeToSearchFrom*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eea86-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eea86-113">Return value</span></span>

<span data-ttu-id="eea86-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="eea86-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eea86-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eea86-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="eea86-116">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="eea86-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="eea86-117">Если [**иинканализер**](iinkanalyzer.md) не содержит узел *пконтекстнодетосеарчфром* , этот метод возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="eea86-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="eea86-118">Свойство *пнодетипе* должно содержать глобальный уникальный идентификатор (GUID) из констант [типов узлов контекста](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="eea86-118">The *pNodeType* property must contain a globally unique identifier (GUID) from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="eea86-119">Если [**иинканализер**](iinkanalyzer.md) не содержит таких [**иконтекстноде**](icontextnode.md), возвращается пустая коллекция [**иконтекстнодес**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="eea86-119">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea86-120">Требования</span><span class="sxs-lookup"><span data-stu-id="eea86-120">Requirements</span></span>



| <span data-ttu-id="eea86-121">Требование</span><span class="sxs-lookup"><span data-stu-id="eea86-121">Requirement</span></span> | <span data-ttu-id="eea86-122">Значение</span><span class="sxs-lookup"><span data-stu-id="eea86-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eea86-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eea86-123">Minimum supported client</span></span><br/> | <span data-ttu-id="eea86-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="eea86-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eea86-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eea86-125">Minimum supported server</span></span><br/> | <span data-ttu-id="eea86-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="eea86-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="eea86-127">Header</span><span class="sxs-lookup"><span data-stu-id="eea86-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea86-128"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eea86-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="eea86-129">DLL</span><span class="sxs-lookup"><span data-stu-id="eea86-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eea86-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eea86-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="eea86-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eea86-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea86-132">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="eea86-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="eea86-133">**Метод Иинканализер:: Финдинклеафнодес**</span><span class="sxs-lookup"><span data-stu-id="eea86-133">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="eea86-134">**Метод Иинканализер:: Финдинклеафнодесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="eea86-134">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="eea86-135">**Метод Иинканализер:: Финдлеафнодес**</span><span class="sxs-lookup"><span data-stu-id="eea86-135">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="eea86-136">**Метод Иинканализер:: Финдноде**</span><span class="sxs-lookup"><span data-stu-id="eea86-136">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="eea86-137">**Метод Иинканализер:: Финднодесофтипе**</span><span class="sxs-lookup"><span data-stu-id="eea86-137">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="eea86-138">**Метод Иинканализер:: Финднодесофтипефорстрокес**</span><span class="sxs-lookup"><span data-stu-id="eea86-138">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="eea86-139">**Метод Иинканализер:: Финднодесвискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="eea86-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="eea86-140">**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**</span><span class="sxs-lookup"><span data-stu-id="eea86-140">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="eea86-141">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="eea86-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

