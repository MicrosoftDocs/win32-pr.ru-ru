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
# <a name="icontextnodegetid-method"></a>Метод Иконтекстноде:: GetId

Возвращает идентификатор для объекта [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetId(
  [out] GUID *pId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор процесса* \[ заполняет\]
</dt> <dd>

Идентификатор объекта [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Анализатор рукописного ввода назначает уникальный идентификатор всем создаваемым контекстным узлам. Во время анализа рукописного ввода анализатор рукописного ввода может изменить идентификатор узла контекста. Например, анализатор рукописного ввода может реклассифицировать один узел слова как два узла Word, а затем присвоить исходный идентификатор одному и новому идентификатору. Или анализатор рукописного ввода может реклассифицировать два узла Word как один узел слов и назначить один из исходных идентификаторов новому узлу Word.

## <a name="examples"></a>Примеры

В следующем примере показан вспомогательный метод, который получает сведения об указанном узле, его параметре *пконтекстноде* . Этот вспомогательный метод возвращает сведения из следующих методов.

-   **Иконтекстноде:: GetId**
-   [**Иконтекстноде:: GetType**](icontextnode-gettype.md)
-   [**Иконтекстноде:: OnLocation**](icontextnode-getlocation.md)
-   [**Иконтекстноде:: Жетпарентноде**](icontextnode-getparentnode.md)


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




