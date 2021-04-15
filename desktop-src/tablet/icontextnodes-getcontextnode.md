---
description: Извлекает объект Иконтекстноде по указанному индексу в данной коллекции.
ms.assetid: 4b266512-9e58-43d2-8430-68310230fc27
title: 'Метод Иконтекстнодес:: Жетконтекстноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ec907fdcac5a1ed18cca54c79a876959868f2ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497577"
---
# <a name="icontextnodesgetcontextnode-method"></a><span data-ttu-id="fafad-103">Метод Иконтекстнодес:: Жетконтекстноде</span><span class="sxs-lookup"><span data-stu-id="fafad-103">IContextNodes::GetContextNode method</span></span>

<span data-ttu-id="fafad-104">Извлекает объект [**иконтекстноде**](icontextnode.md) по указанному индексу в данной коллекции.</span><span class="sxs-lookup"><span data-stu-id="fafad-104">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fafad-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fafad-105">Syntax</span></span>


```C++
HRESULT GetContextNode(
  [in]  ULONG        ulIndex,
  [out] IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="fafad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fafad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fafad-107">*улиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fafad-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fafad-108">Отсчитываемый от нуля индекс объекта [**иконтекстноде**](icontextnode.md) , который необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="fafad-108">The zero-based index of the [**IContextNode**](icontextnode.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="fafad-109">*ппконтекстноде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fafad-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fafad-110">Указатель на [**иконтекстноде**](icontextnode.md) , на который указывает ссылка по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="fafad-110">Pointer to the [**IContextNode**](icontextnode.md) referenced at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fafad-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fafad-111">Return value</span></span>

<span data-ttu-id="fafad-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fafad-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fafad-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fafad-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fafad-114">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстноде* , когда больше не нужно использовать контекстный узел.</span><span class="sxs-lookup"><span data-stu-id="fafad-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNode* when you no longer need to use the context node.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fafad-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="fafad-115">Examples</span></span>

<span data-ttu-id="fafad-116">В этом примере показан метод, `ExploreContextNode` который изучает [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="fafad-116">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="fafad-117">Метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="fafad-117">The method does the following:</span></span>

-   <span data-ttu-id="fafad-118">Возвращает тип узла контекста.</span><span class="sxs-lookup"><span data-stu-id="fafad-118">Gets the context node's type.</span></span>
-   <span data-ttu-id="fafad-119">Проверяет конкретные свойства типа узла, вызывая вспомогательный метод, если контекстный узел является неклассифицированным рукописным вводом, указанием анализа или узлом пользовательского распознавателя.</span><span class="sxs-lookup"><span data-stu-id="fafad-119">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="fafad-120">Проверяет каждый подузел, вызывая сам себя, если узел содержит подузлы.</span><span class="sxs-lookup"><span data-stu-id="fafad-120">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="fafad-121">Проверяет данные штриха для узла, вызывая вспомогательный метод, если этот узел является конечным узлом с рукописным вводом.</span><span class="sxs-lookup"><span data-stu-id="fafad-121">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fafad-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fafad-122">Requirements</span></span>



| <span data-ttu-id="fafad-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fafad-123">Requirement</span></span> | <span data-ttu-id="fafad-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fafad-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fafad-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fafad-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fafad-126">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fafad-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fafad-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fafad-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fafad-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fafad-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fafad-129">Header</span><span class="sxs-lookup"><span data-stu-id="fafad-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fafad-130"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fafad-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fafad-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fafad-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fafad-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fafad-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fafad-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fafad-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fafad-134">**иконтекстнодес**</span><span class="sxs-lookup"><span data-stu-id="fafad-134">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="fafad-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="fafad-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

