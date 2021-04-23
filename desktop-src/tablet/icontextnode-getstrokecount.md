---
description: Возвращает число штрихов, связанных с объектом Иконтекстноде.
ms.assetid: bb3c1cb3-dcf6-4465-b1bc-5c613e9747da
title: 'Метод Иконтекстноде:: Жетстрокекаунт (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2652168fa2846995aeb17ec23c194f908f22e5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497583"
---
# <a name="icontextnodegetstrokecount-method"></a><span data-ttu-id="b970f-103">Метод Иконтекстноде:: Жетстрокекаунт</span><span class="sxs-lookup"><span data-stu-id="b970f-103">IContextNode::GetStrokeCount method</span></span>

<span data-ttu-id="b970f-104">Возвращает число штрихов, связанных с объектом [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b970f-104">Gets the number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b970f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b970f-105">Syntax</span></span>


```C++
HRESULT GetStrokeCount(
  [out] ULONG *pulStrokeCount
);
```



## <a name="parameters"></a><span data-ttu-id="b970f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b970f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b970f-107">*пулстрокекаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b970f-107">*pulStrokeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b970f-108">Число штрихов, связанных с объектом [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b970f-108">The number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b970f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b970f-109">Return value</span></span>

<span data-ttu-id="b970f-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b970f-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b970f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b970f-111">Remarks</span></span>

<span data-ttu-id="b970f-112">Связанные данные обводки имеют только рукописные узлы с конечными элементами (см. [**иконтекстноде:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="b970f-112">Only ink leaf context nodes have associated stroke data (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="b970f-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="b970f-113">Examples</span></span>

<span data-ttu-id="b970f-114">В этом примере показан метод, `ExploreContextNode` который изучает [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="b970f-114">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="b970f-115">Метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b970f-115">The method does the following:</span></span>

-   <span data-ttu-id="b970f-116">Возвращает тип узла контекста.</span><span class="sxs-lookup"><span data-stu-id="b970f-116">Gets the context node's type.</span></span>
-   <span data-ttu-id="b970f-117">Проверяет конкретные свойства типа узла, вызывая вспомогательный метод, если контекстный узел является неклассифицированным рукописным вводом, указанием анализа или узлом пользовательского распознавателя.</span><span class="sxs-lookup"><span data-stu-id="b970f-117">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="b970f-118">Проверяет каждый подузел, вызывая сам себя, если узел содержит подузлы.</span><span class="sxs-lookup"><span data-stu-id="b970f-118">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="b970f-119">Проверяет данные штриха для узла, вызывая вспомогательный метод, если этот узел является конечным узлом с рукописным вводом.</span><span class="sxs-lookup"><span data-stu-id="b970f-119">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b970f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b970f-120">Requirements</span></span>



| <span data-ttu-id="b970f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b970f-121">Requirement</span></span> | <span data-ttu-id="b970f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b970f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b970f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b970f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b970f-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b970f-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b970f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b970f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b970f-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b970f-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b970f-127">Header</span><span class="sxs-lookup"><span data-stu-id="b970f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b970f-128"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b970f-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b970f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b970f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b970f-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b970f-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b970f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b970f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b970f-132">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="b970f-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b970f-133">**Иконтекстноде:: Жетстрокеидс**</span><span class="sxs-lookup"><span data-stu-id="b970f-133">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="b970f-134">**Иконтекстноде:: Жетстрокеид**</span><span class="sxs-lookup"><span data-stu-id="b970f-134">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="b970f-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="b970f-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




