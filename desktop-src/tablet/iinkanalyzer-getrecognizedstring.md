---
description: Возвращает наиболее подходящую строку результатов операции распознавания для всего дерева узлов контекста в Иинканализер.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: 'Метод Иинканализер:: Жетрекогнизедстринг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810006"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a>Метод Иинканализер:: Жетрекогнизедстринг

Возвращает наиболее подходящую строку результатов операции распознавания для всего дерева узлов контекста в [**иинканализер**](iinkanalyzer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбстррекогнизедстринг* \[ заполняет\]
</dt> <dd>

Наиболее подходящий результат операции распознавания для всего дерева узлов контекста в [**иинканализер**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для *пбстррекогнизедстринг* , когда больше не нужно использовать строку.

 

Этот метод возвращает то же значение, что и данные свойства корневого узла для распознанной строки. (См. раздел [**иинканализер:: Жетрутноде Method**](iinkanalyzer-getrootnode.md), [**Иконтекстноде:: Жетпропертидата**](icontextnode-getpropertydata.md)и [Свойства контекстного узла](context-node-properties.md).)

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

