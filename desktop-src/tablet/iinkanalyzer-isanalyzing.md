---
description: Извлекает значение, указывающее, выполняет ли Иинканализер анализ рукописного ввода.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: 'Метод Иинканализер:: (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1dc0a10bfcafb5972413eb1d1d0880a63db69498c38481cc0cbf6bb58e5f69f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092054"
---
# <a name="iinkanalyzerisanalyzing-method"></a>Метод Иинканализер::

Извлекает значение, указывающее, выполняет ли [**иинканализер**](iinkanalyzer.md) анализ рукописного ввода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбанализинг* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если [**иинканализер**](iinkanalyzer.md) выполняет анализ рукописного ввода; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Это свойство имеет **значение \_ true** , если [**иинканализер**](iinkanalyzer.md) выполняет синхронный или асинхронный анализ.

## <a name="examples"></a>Примеры

В следующем примере показан метод, который просматривает дерево результатов [**иконтекстноде**](icontextnode.md) анализатора рукописного ввода. Если анализатор рукописного ввода в настоящее время не выполняет анализ рукописного ввода, метод выполняет следующие операции.

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




