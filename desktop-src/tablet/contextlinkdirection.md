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
# <a name="contextlinkdirection-enumeration"></a>Перечисление Контекстлинкдиректион

Задает направление объекта [**иконтекстлинк**](icontextlink.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**Контекстлинкдиректион \_ линксвис**
</dt> <dd>

[**Иконтекстноде**](icontextnode.md) — это направленный рисунок, который указывает на сторону от [**иконтекстлинк**](icontextlink.md).

</dd> <dt>

<span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**Контекстлинкдиректион \_ линксфром**
</dt> <dd>

[**Иконтекстноде**](icontextnode.md) — это направленный рисунок, указывающий на [**иконтекстлинк**](icontextlink.md).

</dd> <dt>

<span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**Контекстлинкдиректион \_ линксто**
</dt> <dd>

В ссылке нет направленных рисунков. Например, рисунок рукописного ввода может подчеркнуть рукописное слово. Направление не выводится из подчеркивания.

</dd> </dl>

## <a name="examples"></a>Примеры

В следующем примере принимается объект [**иконтекстноде**](icontextnode.md) , `m_pSelectedNode` и сохраняются все объекты **иконтекстноде** , на которые он ссылается, путем прохода вверх по дереву предков и добавления объектов в `CArray` объект `linkedToNodes` . `CheckHResult` — Это функция, которая принимает `HRESULT` и получает строку и создает исключение, созданное со строкой, если `HRESULT` не **выполнено**.


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстлинк**](icontextlink.md)
</dt> <dt>

[**Иконтекстноде:: Аддконтекстлинк**](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




