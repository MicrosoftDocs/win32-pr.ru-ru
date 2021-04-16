---
description: Выполняет асинхронный анализ рукописного ввода.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'Метод Иинканализер:: Баккграунданализе (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542031"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a>Метод Иинканализер:: Баккграунданализе

Выполняет асинхронный анализ рукописного ввода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

При вызове этого метода [**иинканализер**](iinkanalyzer.md) выполняет анализ рукописного ввода в фоновом потоке.

Этот метод возвращает **\_ значение false** и не запускает новую операцию фонового анализа в следующих случаях.

-   [**Иинканализер**](iinkanalyzer.md) сейчас выполняет фоновый анализ.
-   "грязный" регион (см. [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)) представляет собой пустую область.

[**Иинканализер**](iinkanalyzer.md) анализирует рукописный ввод в своей «грязной» области во время вызова метода [**Иинканализер:: Analyze**](iinkanalyzer-analyze.md) или **иинканализер:: баккграунданализе**. Однако **иинканализер** может расширить операцию анализа, включив в нее соседние регионы.

Этот метод задает для "грязной" области пустой регион.

Если данные Stroke были добавлены в [**иинканализер**](iinkanalyzer.md) после вызова **метода Иинканализер:: баккграунданализе**, **иинканализер** может обновить "грязную" область на этапе согласования анализа рукописного ввода.

Настройка режимов анализа (см. [**метод иинканализер:: жетаналисисмодес**](iinkanalyzer-getanalysismodes.md)) указывает, как [**иинканализер**](iinkanalyzer.md) выполняет фоновый анализ. Дополнительные сведения о анализе рукописного ввода см. в разделе [Общие сведения об анализе рукописного текста](ink-analysis-overview.md).

Этот метод возвращает код ошибки при следующих обстоятельствах.

-   Приложение установило значение [**Аналисисмодес**](analysismodes.md) **Аналисисмодес \_ интермедиатересултс** в [**иинканализер**](iinkanalyzer.md) (см. [**метод иинканализер:: сетаналисисмодес**](iinkanalyzer-setanalysismodes.md)) и не обрабатывает событие [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) .
-   Приложение очистило значение [**Аналисисмодес**](analysismodes.md) **Аналисисмодес \_ аутоматикреконЦилиатион** в [**иинканализер**](iinkanalyzer.md) (см. [**метод иинканализер:: сетаналисисмодес**](iinkanalyzer-setanalysismodes.md)) и не обрабатывает событие [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .
-   Приложение не обрабатывает событие [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .
-   Приложение не обрабатывает событие [**\_ ианалисисевентс:: упдатестрокескаче**](-ianalysisevents-updatestrokescache.md) .

## <a name="examples"></a>Примеры

В следующем примере проверяется «грязный» регион анализатора рукописного ввода, а затем инициируется фоновый анализ рукописного ввода, если «грязная» область не пуста.


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
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

[**аналисисмодес**](analysismodes.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Жетаналисисмодес**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**Метод Иинканализер:: Сетаналисисмодес**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**Метод Иинканализер:: Жетдиртирегион**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Метод Иинканализер:: Сетдиртирегион**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Метод Иинканализер:: Жетрутноде**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




