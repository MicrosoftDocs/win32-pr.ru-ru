---
description: Возвращает тип объекта Иконтекстноде.
ms.assetid: 285384ce-5cdc-47f5-a1c4-6c6d7f18e215
title: 'Метод Иконтекстноде:: GetType (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 68b657d9acd6f25f7c067e339ec42c6994a34c48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145517"
---
# <a name="icontextnodegettype-method"></a><span data-ttu-id="6f295-103">Метод Иконтекстноде:: GetType</span><span class="sxs-lookup"><span data-stu-id="6f295-103">IContextNode::GetType method</span></span>

<span data-ttu-id="6f295-104">Возвращает тип объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="6f295-104">Retrieves the type of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f295-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f295-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] GUID *pContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="6f295-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f295-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f295-107">*пконтекстнодетипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6f295-107">*pContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f295-108">Тип объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="6f295-108">The type of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f295-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f295-109">Return value</span></span>

<span data-ttu-id="6f295-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6f295-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f295-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f295-111">Remarks</span></span>

<span data-ttu-id="6f295-112">Типы узлов описаны в константах [типов узлов контекста](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="6f295-112">Types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="6f295-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="6f295-113">Examples</span></span>

<span data-ttu-id="6f295-114">В следующем примере показан вспомогательный метод, который получает сведения об указанном узле, его параметре *пконтекстноде* .</span><span class="sxs-lookup"><span data-stu-id="6f295-114">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="6f295-115">Этот вспомогательный метод возвращает сведения из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="6f295-115">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="6f295-116">**Иконтекстноде:: GetId**</span><span class="sxs-lookup"><span data-stu-id="6f295-116">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   <span data-ttu-id="6f295-117">**Иконтекстноде:: GetType**</span><span class="sxs-lookup"><span data-stu-id="6f295-117">**IContextNode::GetType**</span></span>
-   [<span data-ttu-id="6f295-118">**Иконтекстноде:: OnLocation**</span><span class="sxs-lookup"><span data-stu-id="6f295-118">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="6f295-119">**Иконтекстноде:: Жетпарентноде**</span><span class="sxs-lookup"><span data-stu-id="6f295-119">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="6f295-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6f295-120">Requirements</span></span>



| <span data-ttu-id="6f295-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6f295-121">Requirement</span></span> | <span data-ttu-id="6f295-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6f295-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f295-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f295-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6f295-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6f295-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6f295-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f295-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6f295-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6f295-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6f295-127">Header</span><span class="sxs-lookup"><span data-stu-id="6f295-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f295-128"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6f295-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6f295-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6f295-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f295-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f295-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6f295-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f295-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f295-132">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="6f295-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6f295-133">Типы узлов контекста</span><span class="sxs-lookup"><span data-stu-id="6f295-133">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="6f295-134">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="6f295-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




