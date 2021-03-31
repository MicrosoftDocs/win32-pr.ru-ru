---
description: Задает направление объекта Иконтекстлинк.
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: Перечисление Контекстлинкдиректион (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContextLinkDirection
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 82e10c7e908b4cc4035d8bfdde55d863f7b6ecf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910447"
---
# <a name="contextlinkdirection-enumeration"></a><span data-ttu-id="955f6-103">Перечисление Контекстлинкдиректион</span><span class="sxs-lookup"><span data-stu-id="955f6-103">ContextLinkDirection enumeration</span></span>

<span data-ttu-id="955f6-104">Задает направление объекта [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="955f6-104">Specifies the direction of an [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="955f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="955f6-105">Syntax</span></span>


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a><span data-ttu-id="955f6-106">Константы</span><span class="sxs-lookup"><span data-stu-id="955f6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="955f6-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**Контекстлинкдиректион \_ линксвис**</span><span class="sxs-lookup"><span data-stu-id="955f6-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection\_LinksWith**</span></span>
</dt> <dd>

<span data-ttu-id="955f6-108">[**Иконтекстноде**](icontextnode.md) — это направленный рисунок, который указывает на сторону от [**иконтекстлинк**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="955f6-108">The [**IContextNode**](icontextnode.md) is a directional drawing that points away from the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="955f6-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**Контекстлинкдиректион \_ линксфром**</span><span class="sxs-lookup"><span data-stu-id="955f6-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection\_LinksFrom**</span></span>
</dt> <dd>

<span data-ttu-id="955f6-110">[**Иконтекстноде**](icontextnode.md) — это направленный рисунок, указывающий на [**иконтекстлинк**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="955f6-110">The [**IContextNode**](icontextnode.md) is a directional drawing that points to the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="955f6-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**Контекстлинкдиректион \_ линксто**</span><span class="sxs-lookup"><span data-stu-id="955f6-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection\_LinksTo**</span></span>
</dt> <dd>

<span data-ttu-id="955f6-112">В ссылке нет направленных рисунков.</span><span class="sxs-lookup"><span data-stu-id="955f6-112">There are no directional drawings in the link.</span></span> <span data-ttu-id="955f6-113">Например, рисунок рукописного ввода может подчеркнуть рукописное слово.</span><span class="sxs-lookup"><span data-stu-id="955f6-113">For example, an ink drawing can underline an ink word.</span></span> <span data-ttu-id="955f6-114">Направление не выводится из подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="955f6-114">There is no direction inferred from the underline.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="955f6-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="955f6-115">Examples</span></span>

<span data-ttu-id="955f6-116">В следующем примере принимается объект [**иконтекстноде**](icontextnode.md) , `m_pSelectedNode` и сохраняются все объекты **иконтекстноде** , на которые он ссылается, путем прохода вверх по дереву предков и добавления объектов в `CArray` объект `linkedToNodes` .</span><span class="sxs-lookup"><span data-stu-id="955f6-116">The following example takes an [**IContextNode**](icontextnode.md) object, `m_pSelectedNode`, and saves all the **IContextNode** objects that it links to by walking up the ancestor tree and adding the objects into a `CArray` object, `linkedToNodes`.</span></span> <span data-ttu-id="955f6-117">`CheckHResult` — Это функция, которая принимает `HRESULT` и получает строку и создает исключение, созданное со строкой, если `HRESULT` не **выполнено**.</span><span class="sxs-lookup"><span data-stu-id="955f6-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
// Find all first ancestor that contains links of type Enclose
CArray<IContextNode*,IContextNode*> linkedToNodes = CArray<IContextNode*,IContextNode*>();
IContextNode* pAncestor;
CheckHResult(m_pSelectedNode->GetParentNode(&pAncestor),
    "IContextNode::GetParentNode failed");
while (pAncestor != NULL)
{
    // Get the links
    IContextLinks* pLinks;
    CheckHResult(pAncestor->GetContextLinks(&pLinks),
        "IContextNode::GetContextLinks failed");
    ULONG nLinks;
    CheckHResult(pLinks->GetCount(&nLinks), "IContextLinks::GetCount failed");
    for (ULONG i = 0; i < nLinks; i++)
    {
        IContextLink* pLink;
        CheckHResult(pLinks->GetContextLink(i, &pLink),
            "IContextLinks::GetContextLink failed");
        // Check link direction
        ContextLinkDirection linkDirection;
        CheckHResult(pLink->GetContextLinkDirection(&linkDirection),
            "IContextLink:GetContextLinkDirection failed");
        if (linkDirection == ContextLinkDirection_LinksTo)
        {
            // Get source node and add the array
            IContextNode* pSourceNode;
            CheckHResult(pLink->GetSourceNode(&pSourceNode),
                "IContextLink::GetSourceNode failed");
            linkedToNodes.Add(pSourceNode);
        }
    }
            
    // Go up another level
    IContextNode* pNewAncestor;
    CheckHResult(pAncestor->GetParentNode(&pNewAncestor),
        "IContextNode::GetParentNode failed");
    pAncestor = pNewAncestor;
}
```



## <a name="requirements"></a><span data-ttu-id="955f6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="955f6-118">Requirements</span></span>



| <span data-ttu-id="955f6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="955f6-119">Requirement</span></span> | <span data-ttu-id="955f6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="955f6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="955f6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="955f6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="955f6-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="955f6-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="955f6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="955f6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="955f6-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="955f6-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="955f6-125">Header</span><span class="sxs-lookup"><span data-stu-id="955f6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="955f6-126"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="955f6-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="955f6-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="955f6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="955f6-128">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="955f6-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="955f6-129">**Иконтекстноде:: Аддконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="955f6-129">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




