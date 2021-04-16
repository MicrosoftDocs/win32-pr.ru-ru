---
description: Содержит коллекцию объектов, реализующих интерфейс Ианалисисварнинг и являющихся результатом операции анализа рукописного ввода.
ms.assetid: 2118c18b-d316-4e91-8652-62969115e8b5
title: Интерфейс Ианалисисварнингс (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 938d406ea90d86cc05ac84b69304b7a85e0e54fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692448"
---
# <a name="ianalysiswarnings-interface"></a>Интерфейс Ианалисисварнингс

Содержит коллекцию объектов, реализующих интерфейс [**ианалисисварнинг**](ianalysiswarning.md) и являющихся результатом операции анализа рукописного ввода.

## <a name="members"></a>Элементы

Интерфейс **ианалисисварнингс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ианалисисварнингс** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ианалисисварнингс** содержит следующие методы.



| Метод                                                             | Описание                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**жетаналисисварнинг**](ianalysiswarnings-getanalysiswarning.md) | Извлекает объект [**ианалисисварнинг**](ianalysiswarning.md) по указанному индексу.<br/>                                       |
| [**GetCount**](ianalysiswarnings-getcount.md)                     | Возвращает количество объектов [**ианалисисварнинг**](ianalysiswarning.md) , содержащихся в коллекции **ианалисисварнингс** .<br/> |



 

## <a name="examples"></a>Примеры

В следующем примере показана структура обработчика событий для события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) . Обработчик проверяет [**ианалисисстатус:: Success**](ianalysisstatus-issuccessful.md). Если операция анализа создавала предупреждения, обработчик выполняет итерацию по коллекции объектов [**ианалисисварнинг**](ianalysiswarning.md) .


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ианалисисстатус**](ianalysisstatus.md)
</dt> <dt>

[**ианалисисварнинг**](ianalysiswarning.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

