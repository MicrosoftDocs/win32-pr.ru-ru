---
description: Извлекает все объекты Иконтекстноде указанного типа.
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: 'Метод Иинканализер:: Финднодесофтипе (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51611fd4b3c77b43f2ea0d967f81dcc9547edb24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897458"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a><span data-ttu-id="bce15-103">Метод Иинканализер:: Финднодесофтипе</span><span class="sxs-lookup"><span data-stu-id="bce15-103">IInkAnalyzer::FindNodesOfType method</span></span>

<span data-ttu-id="bce15-104">Извлекает все объекты [**иконтекстноде**](icontextnode.md) указанного типа.</span><span class="sxs-lookup"><span data-stu-id="bce15-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce15-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bce15-105">Syntax</span></span>


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="bce15-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bce15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce15-107">*пнодетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bce15-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bce15-108">**Идентификатор GUID** , указывающий тип узла.</span><span class="sxs-lookup"><span data-stu-id="bce15-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="bce15-109">*ппконтекстнодесфаунд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bce15-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bce15-110">Указатель на [**иконтекстнодес**](icontextnodes.md) , содержащий все узлы типа *пнодетипе*.</span><span class="sxs-lookup"><span data-stu-id="bce15-110">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes of type *pNodeType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce15-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bce15-111">Return value</span></span>

<span data-ttu-id="bce15-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bce15-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bce15-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bce15-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="bce15-114">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="bce15-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="bce15-115">Свойство *пнодетипе* должно содержать идентификатор GUID из констант [типов узлов контекста](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="bce15-115">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="bce15-116">Если [**иинканализер**](iinkanalyzer.md) не содержит таких [**иконтекстноде**](icontextnode.md), возвращается пустая коллекция [**иконтекстнодес**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="bce15-116">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="bce15-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bce15-117">Requirements</span></span>



| <span data-ttu-id="bce15-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bce15-118">Requirement</span></span> | <span data-ttu-id="bce15-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bce15-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bce15-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bce15-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bce15-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bce15-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bce15-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bce15-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bce15-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bce15-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bce15-124">Header</span><span class="sxs-lookup"><span data-stu-id="bce15-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bce15-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bce15-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bce15-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bce15-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bce15-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bce15-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bce15-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bce15-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce15-129">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="bce15-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="bce15-130">**Метод Иинканализер:: Финдинклеафнодес**</span><span class="sxs-lookup"><span data-stu-id="bce15-130">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="bce15-131">**Метод Иинканализер:: Финдинклеафнодесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="bce15-131">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="bce15-132">**Метод Иинканализер:: Финдлеафнодес**</span><span class="sxs-lookup"><span data-stu-id="bce15-132">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="bce15-133">**Метод Иинканализер:: Финдноде**</span><span class="sxs-lookup"><span data-stu-id="bce15-133">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="bce15-134">**Метод Иинканализер:: Финднодесофтипефорстрокес**</span><span class="sxs-lookup"><span data-stu-id="bce15-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="bce15-135">**Метод Иинканализер:: Финднодесофтипеинсубтри**</span><span class="sxs-lookup"><span data-stu-id="bce15-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="bce15-136">**Метод Иинканализер:: Финднодесвискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="bce15-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="bce15-137">**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**</span><span class="sxs-lookup"><span data-stu-id="bce15-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="bce15-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="bce15-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

