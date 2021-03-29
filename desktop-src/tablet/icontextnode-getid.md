---
description: Возвращает идентификатор для объекта Иконтекстноде.
ms.assetid: 7578bcc1-7c69-45fc-b3c2-7350ce4df99c
title: 'Метод Иконтекстноде:: GetId (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ef316111c7464bac0339a4888b887bc5cf20b93f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897486"
---
# <a name="icontextnodegetid-method"></a><span data-ttu-id="8ea91-103">Метод Иконтекстноде:: GetId</span><span class="sxs-lookup"><span data-stu-id="8ea91-103">IContextNode::GetId method</span></span>

<span data-ttu-id="8ea91-104">Возвращает идентификатор для объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea91-104">Retrieves the identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea91-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ea91-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="8ea91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ea91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea91-107">*идентификатор процесса* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8ea91-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea91-108">Идентификатор объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea91-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea91-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ea91-109">Return value</span></span>

<span data-ttu-id="8ea91-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8ea91-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ea91-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ea91-111">Remarks</span></span>

<span data-ttu-id="8ea91-112">Анализатор рукописного ввода назначает уникальный идентификатор всем создаваемым контекстным узлам.</span><span class="sxs-lookup"><span data-stu-id="8ea91-112">The ink analyzer assigns a unique identifier to all context nodes it creates.</span></span> <span data-ttu-id="8ea91-113">Во время анализа рукописного ввода анализатор рукописного ввода может изменить идентификатор узла контекста.</span><span class="sxs-lookup"><span data-stu-id="8ea91-113">During ink analysis, the ink analyzer may change the identifier for a context node.</span></span> <span data-ttu-id="8ea91-114">Например, анализатор рукописного ввода может реклассифицировать один узел слова как два узла Word, а затем присвоить исходный идентификатор одному и новому идентификатору.</span><span class="sxs-lookup"><span data-stu-id="8ea91-114">For example, the ink analyzer may reclassify one word node as two word nodes and then assign the original identifier to one and a new identifier to the other.</span></span> <span data-ttu-id="8ea91-115">Или анализатор рукописного ввода может реклассифицировать два узла Word как один узел слов и назначить один из исходных идентификаторов новому узлу Word.</span><span class="sxs-lookup"><span data-stu-id="8ea91-115">Or, the ink analyzer may reclassify two word nodes as one word node and assign one of the original identifiers to the new word node.</span></span>

## <a name="examples"></a><span data-ttu-id="8ea91-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="8ea91-116">Examples</span></span>

<span data-ttu-id="8ea91-117">В следующем примере показан вспомогательный метод, который получает сведения об указанном узле, его параметре *пконтекстноде* .</span><span class="sxs-lookup"><span data-stu-id="8ea91-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="8ea91-118">Этот вспомогательный метод возвращает сведения из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="8ea91-118">This helper method returns information from the following methods.</span></span>

-   <span data-ttu-id="8ea91-119">**Иконтекстноде:: GetId**</span><span class="sxs-lookup"><span data-stu-id="8ea91-119">**IContextNode::GetId**</span></span>
-   [<span data-ttu-id="8ea91-120">**Иконтекстноде:: GetType**</span><span class="sxs-lookup"><span data-stu-id="8ea91-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="8ea91-121">**Иконтекстноде:: OnLocation**</span><span class="sxs-lookup"><span data-stu-id="8ea91-121">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="8ea91-122">**Иконтекстноде:: Жетпарентноде**</span><span class="sxs-lookup"><span data-stu-id="8ea91-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="8ea91-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8ea91-123">Requirements</span></span>



| <span data-ttu-id="8ea91-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8ea91-124">Requirement</span></span> | <span data-ttu-id="8ea91-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8ea91-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea91-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ea91-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea91-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8ea91-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8ea91-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ea91-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea91-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8ea91-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8ea91-130">Header</span><span class="sxs-lookup"><span data-stu-id="8ea91-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ea91-131"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8ea91-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8ea91-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8ea91-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ea91-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ea91-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8ea91-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ea91-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea91-135">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="8ea91-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8ea91-136">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="8ea91-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




