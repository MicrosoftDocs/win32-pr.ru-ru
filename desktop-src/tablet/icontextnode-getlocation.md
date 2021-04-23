---
description: Извлекает расположение и размер объекта Иконтекстноде.
ms.assetid: 40787a9b-1017-4209-aec8-09b7332bfa8a
title: 'Метод Иконтекстноде:: OnLocation (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13366442399961eaba7a411b1b3c87171f0879b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711135"
---
# <a name="icontextnodegetlocation-method"></a><span data-ttu-id="9d857-103">Метод Иконтекстноде:: OnLocation</span><span class="sxs-lookup"><span data-stu-id="9d857-103">IContextNode::GetLocation method</span></span>

<span data-ttu-id="9d857-104">Извлекает расположение и размер объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="9d857-104">Retrieves the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d857-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d857-105">Syntax</span></span>


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="9d857-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d857-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d857-107">*ппианалисисрегион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9d857-107">*ppIAnalysisRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d857-108">Указатель на расположение и размер объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="9d857-108">A pointer to the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d857-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d857-109">Return value</span></span>

<span data-ttu-id="9d857-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9d857-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d857-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d857-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9d857-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппианалисисрегион* , когда больше не нужно использовать область анализа.</span><span class="sxs-lookup"><span data-stu-id="9d857-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppIAnalysisRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="9d857-113">Расположение узла контейнера определяется путем поиска объединения всех расположений конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="9d857-113">The location for a container node is determined by finding the union of all the leaf's locations.</span></span> <span data-ttu-id="9d857-114">Положение конечного узла для рукописного ввода определяется путем поиска объединения ограничивающего прямоугольника связанных штрихов.</span><span class="sxs-lookup"><span data-stu-id="9d857-114">The location for an ink leaf node is determined by finding the union of the bounding box of the associated strokes.</span></span> <span data-ttu-id="9d857-115">Расположение конечного узла, не являющегося рукописным, задается при создании узла и может быть обновлено с помощью [**иконтекстноде:: SetLocation**](icontextnode-setlocation.md).</span><span class="sxs-lookup"><span data-stu-id="9d857-115">The location for a non-ink leaf node is set when the node is created and can be updated using [**IContextNode::SetLocation**](icontextnode-setlocation.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9d857-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="9d857-116">Examples</span></span>

<span data-ttu-id="9d857-117">В следующем примере показан вспомогательный метод, который получает сведения об указанном узле, его параметре *пконтекстноде* .</span><span class="sxs-lookup"><span data-stu-id="9d857-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="9d857-118">Этот вспомогательный метод возвращает сведения из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="9d857-118">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="9d857-119">**Иконтекстноде:: GetId**</span><span class="sxs-lookup"><span data-stu-id="9d857-119">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="9d857-120">**Иконтекстноде:: GetType**</span><span class="sxs-lookup"><span data-stu-id="9d857-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   <span data-ttu-id="9d857-121">**Иконтекстноде:: OnLocation**</span><span class="sxs-lookup"><span data-stu-id="9d857-121">**IContextNode::GetLocation**</span></span>
-   [<span data-ttu-id="9d857-122">**Иконтекстноде:: Жетпарентноде**</span><span class="sxs-lookup"><span data-stu-id="9d857-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="9d857-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9d857-123">Requirements</span></span>



| <span data-ttu-id="9d857-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9d857-124">Requirement</span></span> | <span data-ttu-id="9d857-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9d857-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d857-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d857-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9d857-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9d857-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9d857-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d857-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9d857-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9d857-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9d857-130">Header</span><span class="sxs-lookup"><span data-stu-id="9d857-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d857-131"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9d857-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9d857-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9d857-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d857-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d857-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9d857-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d857-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d857-135">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="9d857-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9d857-136">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="9d857-136">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="9d857-137">**Иконтекстноде:: SetLocation**</span><span class="sxs-lookup"><span data-stu-id="9d857-137">**IContextNode::SetLocation**</span></span>](icontextnode-setlocation.md)
</dt> <dt>

[<span data-ttu-id="9d857-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9d857-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

