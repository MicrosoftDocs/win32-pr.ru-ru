---
description: Возвращает корневой Иконтекстноде дерева контекста объекта Иинканализер.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: 'Метод Иинканализер:: Жетрутноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5ff2181eacd3df1d2815448a0c2d7cafce4d521fa0abbc7b26492d9c078982dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713424"
---
# <a name="iinkanalyzergetrootnode-method"></a>Метод Иинканализер:: Жетрутноде

Возвращает корневой [**иконтекстноде**](icontextnode.md) дерева контекста объекта [**иинканализер**](iinkanalyzer.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппрутноде* \[ заполняет\]
</dt> <dd>

Корневой [**иконтекстноде**](icontextnode.md) контекстного дерева объекта [**иинканализер**](iinkanalyzer.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппрутноде* , когда больше не нужно использовать корневой узел.

 

[**Иинканализер**](iinkanalyzer.md) поддерживает дерево объектов [**иконтекстноде**](icontextnode.md) . Эти объекты содержат входные данные для анализа и результаты анализа. Когда штрихи изначально добавляются в **иинканализер**, **Иинканализер** назначает их **иконтекстноде** типа унклассифиединк (см. раздел [**Иконтекстноде:: GetType**](icontextnode-gettype.md) и [типы узлов контекста](context-node-types.md)). После анализа штрихов **иинканализер** назначает их соответствующим объектам **иконтекстноде** в дереве. Дополнительные сведения об использовании **иинканализер** для анализа рукописного ввода см. в разделе [Общие сведения о анализе рукописного ввода](ink-analysis-overview.md).

## <a name="examples"></a>Примеры

В следующем примере показан метод, который просматривает дерево результатов [**иконтекстноде**](icontextnode.md) анализатора рукописного ввода. Если Иинканлизер в настоящее время не выполняет анализ рукописного ввода, метод выполняет следующие операции.

-   Возвращает верхнюю строку распознавания.
-   Возвращает корневой узел анализатора рукописного ввода.
-   Вызывает вспомогательный метод, `ExploreContextNode` для проверки корневого узла и его дочерних узлов.


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
    }

    return hr;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[Типы узлов контекста](context-node-types.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

