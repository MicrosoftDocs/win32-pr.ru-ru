---
description: Представляет предупреждение или ошибку, возникающую во время операции анализа рукописного ввода.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Интерфейс Ианалисисварнинг (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 27e00533894560a84e73f8eb5682d1b70789ab5f2b21be5d6fe3682c543be6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940384"
---
# <a name="ianalysiswarning-interface"></a>Интерфейс Ианалисисварнинг

Представляет предупреждение или ошибку, возникающую во время операции анализа рукописного ввода.

## <a name="members"></a>Элементы

Интерфейс **ианалисисварнинг** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ианалисисварнинг** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ианалисисварнинг** содержит следующие методы.



| Метод                                                            | Описание                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**жетбаккграундеррор**](ianalysiswarning-getbackgrounderror.md) | Возвращает код ошибки для фоновой операции анализа рукописного ввода, если произошла ошибка.<br/>                                    |
| [**Указание**](ianalysiswarning-gethint.md)                       | Извлекает подсказку анализа, вызвавшую это предупреждение<br/>                                                                        |
| [**жетнодеидс**](ianalysiswarning-getnodeids.md)                 | Возвращает идентификаторы всех соответствующих узлов контекста, связанных с данным предупреждением.<br/>                              |
| [**жетварнингкоде**](ianalysiswarning-getwarningcode.md)         | Извлекает тип предупреждения, произошедшего с помощью перечисления [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode) .<br/> |



 

## <a name="remarks"></a>Remarks

Типы предупреждений, которые могут возникнуть, описаны перечислением [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode) . Часто предупреждения возникают при попытке использовать функцию, которая не поддерживается [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , используемой [**иинканализер**](iinkanalyzer.md) .

Некоторые предупреждения указывают на то, что [**иинканализер**](iinkanalyzer.md) не завершил операцию анализа. Дополнительные сведения см. в разделе [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode).

## <a name="examples"></a>Примеры

В следующем примере показана структура обработчика событий для события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) . Обработчик проверяет [**ианалисисстатус:: Success**](ianalysisstatus-issuccessful.md). Если операция анализа создает предупреждения, обработчик выполняет итерацию по коллекции объектов **ианалисисварнинг** .


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
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

[**ианалисисварнингс**](ianalysiswarnings.md)
</dt> <dt>

[**аналисисварнингкоде**](analysiswarningcode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

