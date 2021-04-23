---
description: Возвращает родительский узел этого Иконтекстноде в дереве узлов контекста.
ms.assetid: 782fd973-f8f3-4902-b8e0-cc5e70a66d28
title: 'Метод Иконтекстноде:: Жетпарентноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetParentNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 50bba716486910802e91cbe6d3f003d172f1cb29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542063"
---
# <a name="icontextnodegetparentnode-method"></a><span data-ttu-id="bf73e-103">Метод Иконтекстноде:: Жетпарентноде</span><span class="sxs-lookup"><span data-stu-id="bf73e-103">IContextNode::GetParentNode method</span></span>

<span data-ttu-id="bf73e-104">Возвращает родительский узел этого [**иконтекстноде**](icontextnode.md) в дереве узлов контекста.</span><span class="sxs-lookup"><span data-stu-id="bf73e-104">Retrieves the parent node of this [**IContextNode**](icontextnode.md) in the context node tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf73e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf73e-105">Syntax</span></span>


```C++
HRESULT GetParentNode(
  [out] IContextNode **ppParentContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="bf73e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf73e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf73e-107">*пппарентконтекстноде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf73e-107">*ppParentContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf73e-108">Указатель на родительский узел этого объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="bf73e-108">A pointer to the parent node of this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf73e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf73e-109">Return value</span></span>

<span data-ttu-id="bf73e-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bf73e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf73e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf73e-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="bf73e-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *пппарентконтекстноде* , когда больше не нужно использовать родительский узел контекста.</span><span class="sxs-lookup"><span data-stu-id="bf73e-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppParentContextNode* when you no longer need to use the parent context node.</span></span>

 

<span data-ttu-id="bf73e-113">Если это корневой узел, параметр *пппарентконтекстноде* имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="bf73e-113">If this is the root node, the *ppParentContextNode* parameter is set to **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="bf73e-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="bf73e-114">Examples</span></span>

<span data-ttu-id="bf73e-115">В следующем примере показан вспомогательный метод, который получает сведения об указанном узле, его параметре *пконтекстноде* .</span><span class="sxs-lookup"><span data-stu-id="bf73e-115">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="bf73e-116">Этот вспомогательный метод возвращает сведения из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="bf73e-116">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="bf73e-117">**Иконтекстноде:: GetId**</span><span class="sxs-lookup"><span data-stu-id="bf73e-117">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="bf73e-118">**Иконтекстноде:: GetType**</span><span class="sxs-lookup"><span data-stu-id="bf73e-118">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="bf73e-119">**Иконтекстноде:: OnLocation**</span><span class="sxs-lookup"><span data-stu-id="bf73e-119">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   <span data-ttu-id="bf73e-120">**Иконтекстноде:: Жетпарентноде**</span><span class="sxs-lookup"><span data-stu-id="bf73e-120">**IContextNode::GetParentNode**</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bf73e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bf73e-121">Requirements</span></span>



| <span data-ttu-id="bf73e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bf73e-122">Requirement</span></span> | <span data-ttu-id="bf73e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bf73e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf73e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf73e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bf73e-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bf73e-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bf73e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf73e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bf73e-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bf73e-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bf73e-128">Header</span><span class="sxs-lookup"><span data-stu-id="bf73e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf73e-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bf73e-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bf73e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bf73e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf73e-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf73e-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bf73e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf73e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf73e-133">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="bf73e-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="bf73e-134">**Иконтекстноде:: Жетсубнодес**</span><span class="sxs-lookup"><span data-stu-id="bf73e-134">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="bf73e-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="bf73e-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

