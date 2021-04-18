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
# <a name="icontextnodegetlocation-method"></a>Метод Иконтекстноде:: OnLocation

Извлекает расположение и размер объекта [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппианалисисрегион* \[ заполняет\]
</dt> <dd>

Указатель на расположение и размер объекта [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппианалисисрегион* , когда больше не нужно использовать область анализа.

 

Расположение узла контейнера определяется путем поиска объединения всех расположений конечного объекта. Положение конечного узла для рукописного ввода определяется путем поиска объединения ограничивающего прямоугольника связанных штрихов. Расположение конечного узла, не являющегося рукописным, задается при создании узла и может быть обновлено с помощью [**иконтекстноде:: SetLocation**](icontextnode-setlocation.md).

## <a name="examples"></a>Примеры

В следующем примере показан вспомогательный метод, который получает сведения об указанном узле, его параметре *пконтекстноде* . Этот вспомогательный метод возвращает сведения из следующих методов.

-   [**Иконтекстноде:: GetId**](icontextnode-getid.md)
-   [**Иконтекстноде:: GetType**](icontextnode-gettype.md)
-   **Иконтекстноде:: OnLocation**
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

[**ианалисисрегион**](ianalysisregion.md)
</dt> <dt>

[**Иконтекстноде:: SetLocation**](icontextnode-setlocation.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

