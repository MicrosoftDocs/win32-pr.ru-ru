---
description: Возвращает прямые дочерние узлы объекта Иконтекстноде.
ms.assetid: 50ce2fa4-031e-42e9-8e47-c0d3c2d2b4df
title: 'Метод Иконтекстноде:: Жетсубнодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetSubNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5c0526ca4a5b4db355c1f895a44ebbf634cb8bc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692442"
---
# <a name="icontextnodegetsubnodes-method"></a><span data-ttu-id="0c0d9-103">Метод Иконтекстноде:: Жетсубнодес</span><span class="sxs-lookup"><span data-stu-id="0c0d9-103">IContextNode::GetSubNodes method</span></span>

<span data-ttu-id="0c0d9-104">Возвращает прямые дочерние узлы объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="0c0d9-104">Gets the direct child nodes of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c0d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c0d9-105">Syntax</span></span>


```C++
HRESULT GetSubNodes(
  [out] IContextNodes **ppSubContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="0c0d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c0d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c0d9-107">*ппсубконтекстнодес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0c0d9-107">*ppSubContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c0d9-108">Коллекция объектов [**иконтекстноде**](icontextnode.md) , которые являются прямыми дочерними узлами этого **иконтекстноде**.</span><span class="sxs-lookup"><span data-stu-id="0c0d9-108">A collection of the [**IContextNode**](icontextnode.md) objects that are direct child nodes of this **IContextNode**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c0d9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c0d9-109">Return value</span></span>

<span data-ttu-id="0c0d9-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0c0d9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0c0d9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c0d9-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="0c0d9-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппсубконтекстнодес* , когда больше не нужно использовать коллекцию подузлов.</span><span class="sxs-lookup"><span data-stu-id="0c0d9-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSubContextNodes* when you no longer need to use the collection of subnodes.</span></span>

 

<span data-ttu-id="0c0d9-113">Это возвращает только прямые дочерние узлы, а не все узлы-потомки.</span><span class="sxs-lookup"><span data-stu-id="0c0d9-113">This returns only the direct child nodes, not all of the descendant nodes.</span></span>

## <a name="examples"></a><span data-ttu-id="0c0d9-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="0c0d9-114">Examples</span></span>

<span data-ttu-id="0c0d9-115">В этом примере показан метод, `ExploreContextNode` который изучает [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="0c0d9-115">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="0c0d9-116">Метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0c0d9-116">The method does the following:</span></span>

-   <span data-ttu-id="0c0d9-117">Возвращает тип узла контекста.</span><span class="sxs-lookup"><span data-stu-id="0c0d9-117">Gets the context node's type.</span></span>
-   <span data-ttu-id="0c0d9-118">Проверяет конкретные свойства типа узла, вызывая вспомогательный метод, если контекстный узел является неклассифицированным рукописным вводом, указанием анализа или узлом пользовательского распознавателя.</span><span class="sxs-lookup"><span data-stu-id="0c0d9-118">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="0c0d9-119">Проверяет каждый подузел, вызывая сам себя, если узел содержит подузлы.</span><span class="sxs-lookup"><span data-stu-id="0c0d9-119">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="0c0d9-120">Проверяет данные штриха для узла, вызывая вспомогательный метод, если этот узел является конечным узлом с рукописным вводом.</span><span class="sxs-lookup"><span data-stu-id="0c0d9-120">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="0c0d9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0c0d9-121">Requirements</span></span>



| <span data-ttu-id="0c0d9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0c0d9-122">Requirement</span></span> | <span data-ttu-id="0c0d9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0c0d9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c0d9-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c0d9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0c0d9-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0c0d9-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0c0d9-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c0d9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0c0d9-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0c0d9-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0c0d9-128">Header</span><span class="sxs-lookup"><span data-stu-id="0c0d9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c0d9-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0c0d9-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0c0d9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0c0d9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c0d9-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c0d9-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0c0d9-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c0d9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c0d9-133">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="0c0d9-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="0c0d9-134">**Иконтекстноде:: Жетпарентноде**</span><span class="sxs-lookup"><span data-stu-id="0c0d9-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="0c0d9-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="0c0d9-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

