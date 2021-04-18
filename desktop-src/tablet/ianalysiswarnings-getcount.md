---
description: Возвращает количество объектов Ианалисисварнинг, содержащихся в коллекции Ианалисисварнингс.
ms.assetid: a0ad46d5-fb1b-40f6-bfc1-28ea1bf4eb44
title: 'Метод Ианалисисварнингс:: NOCOUNT (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc795d310f4bc532a39e2c1a2b4d2ba68f0401f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692449"
---
# <a name="ianalysiswarningsgetcount-method"></a>Метод Ианалисисварнингс:: NOCOUNT

Возвращает количество объектов [**ианалисисварнинг**](ianalysiswarning.md) , содержащихся в коллекции [**ианалисисварнингс**](ianalysiswarnings.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулкаунт* \[ out, retval\]
</dt> <dd>

Количество объектов [**ианалисисварнинг**](ianalysiswarning.md) , содержащихся в коллекции [**ианалисисварнингс**](ianalysiswarnings.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="examples"></a>Примеры

В следующем примере показана структура обработчика событий для события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) . Обработчик проверяет [**ианалисисстатус:: Success**](ianalysisstatus-issuccessful.md). Если операция анализа создает предупреждения, обработчик выполняет итерацию по коллекции объектов [**ианалисисварнинг**](ianalysiswarning.md) .


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

[**ианалисисварнингс**](ianalysiswarnings.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




