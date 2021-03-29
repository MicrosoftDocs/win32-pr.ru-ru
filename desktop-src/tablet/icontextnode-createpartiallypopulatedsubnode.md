---
description: Создает дочерний объект Иконтекстноде, который содержит только сведения о типе, идентификаторе и расположении.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'Метод Иконтекстноде:: Креатепартиаллипопулатедсубноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897490"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a><span data-ttu-id="386a7-103">Метод Иконтекстноде:: Креатепартиаллипопулатедсубноде</span><span class="sxs-lookup"><span data-stu-id="386a7-103">IContextNode::CreatePartiallyPopulatedSubNode method</span></span>

<span data-ttu-id="386a7-104">Создает дочерний объект [**иконтекстноде**](icontextnode.md) , который содержит только сведения о типе, идентификаторе и расположении.</span><span class="sxs-lookup"><span data-stu-id="386a7-104">Creates a child [**IContextNode**](icontextnode.md) object that contains only information about type, identifier, and location.</span></span>

## <a name="syntax"></a><span data-ttu-id="386a7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="386a7-105">Syntax</span></span>


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="386a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="386a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="386a7-107">*пнодетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="386a7-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386a7-108">Тип создаваемого узла контекста.</span><span class="sxs-lookup"><span data-stu-id="386a7-108">The type of context node to create.</span></span>

</dd> <dt>

<span data-ttu-id="386a7-109">*пнодеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="386a7-109">*pNodeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386a7-110">Идентификатор нового узла.</span><span class="sxs-lookup"><span data-stu-id="386a7-110">The identifier for the new node.</span></span>

</dd> <dt>

<span data-ttu-id="386a7-111">*пноделокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="386a7-111">*pNodeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386a7-112">Расположение нового узла.</span><span class="sxs-lookup"><span data-stu-id="386a7-112">The location of the new node.</span></span>

</dd> <dt>

<span data-ttu-id="386a7-113">*ппартиаллипопулатедконтекстнодекреатед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="386a7-113">*pPartiallyPopulatedContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="386a7-114">Указатель на новое, частично заполненное [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="386a7-114">A pointer to the new, partially populated [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="386a7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="386a7-115">Return value</span></span>

<span data-ttu-id="386a7-116">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="386a7-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="386a7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="386a7-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="386a7-118">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппартиаллипопулатедконтекстнодекреатед* , когда больше не нужно использовать контекстный узел.</span><span class="sxs-lookup"><span data-stu-id="386a7-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pPartiallyPopulatedContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="386a7-119">Новый [**иконтекстноде**](icontextnode.md) добавляется в коллекцию дочерних узлов этого узла контекста (см. раздел [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="386a7-119">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="386a7-120">При наличии существующих дочерних узлов вновь созданный **иконтекстноде** добавляется в качестве последнего дочернего узла.</span><span class="sxs-lookup"><span data-stu-id="386a7-120">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="386a7-121">Дополнительные сведения о типах, идентификаторах и расположении см. в разделе [**иконтекстноде:: GetType**](icontextnode-gettype.md), [**Иконтекстноде:: GetId**](icontextnode-getid.md)и [**иконтекстноде:: OnLocation**](icontextnode-getlocation.md).</span><span class="sxs-lookup"><span data-stu-id="386a7-121">For more information about type, identifier, and location, see [**IContextNode::GetType**](icontextnode-gettype.md), [**IContextNode::GetId**](icontextnode-getid.md), and [**IContextNode::GetLocation**](icontextnode-getlocation.md).</span></span>

<span data-ttu-id="386a7-122">Этот метод используется для прокси-сервера данных в качестве способа создания объекта [**иконтекстноде**](icontextnode.md) в дереве узлов контекста, прежде чем все сведения о нем доступны.</span><span class="sxs-lookup"><span data-stu-id="386a7-122">This method is used for data proxy as a way to create an [**IContextNode**](icontextnode.md) object in the context node tree before all the information about it is available.</span></span> <span data-ttu-id="386a7-123">Дополнительные сведения см. [в разделе Учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="386a7-123">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="386a7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="386a7-124">Requirements</span></span>



| <span data-ttu-id="386a7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="386a7-125">Requirement</span></span> | <span data-ttu-id="386a7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="386a7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="386a7-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="386a7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="386a7-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="386a7-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="386a7-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="386a7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="386a7-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="386a7-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="386a7-131">Header</span><span class="sxs-lookup"><span data-stu-id="386a7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="386a7-132"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="386a7-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="386a7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="386a7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="386a7-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="386a7-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="386a7-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="386a7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="386a7-136">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="386a7-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="386a7-137">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="386a7-137">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="386a7-138">**Иконтекстноде:: Жетпартиаллипопулатед**</span><span class="sxs-lookup"><span data-stu-id="386a7-138">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="386a7-139">Типы узлов контекста</span><span class="sxs-lookup"><span data-stu-id="386a7-139">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="386a7-140">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="386a7-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

