---
description: Перемещает указанный Иинканалисисрекогнизер в первую точку в списке распознавателей рукописного ввода в объекте Иинканализер.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'Метод Иинканализер:: Сесигхестприоритинканалисисрекогнизер (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897450"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a>Метод Иинканализер:: Сесигхестприоритинканалисисрекогнизер

Перемещает указанный [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) в первую точку в списке распознавателей рукописного ввода в объекте [**иинканализер**](iinkanalyzer.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканалисисрекогнизер* \[ окне\]
</dt> <dd>

[**Иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , помещаемый в первую позицию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Чтобы получить список распознавателей рукописного ввода в порядке приоритета, вызовите [**метод иинканализер:: жетинканалисисрекогнизерсбиприорити**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).

Этот метод не влияет на порядок остальных объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) в списке распознавателей рукописного ввода в объекте [**иинканализер**](iinkanalyzer.md) .

Порядок распознавателей рукописного ввода, возвращаемых [**методом иинканализер:: жетинканалисисрекогнизерсбиприорити**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) , указывает порядок, в котором [**иинканализер**](iinkanalyzer.md) оценивает доступные объекты [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .

Использование распознавателей рукописного ввода оценивается в соответствии с их порядком в списке.

Во время анализа рукописного ввода [**иинканализер**](iinkanalyzer.md) перебирает Распознаватели рукописного ввода в своем списке до тех пор, пока не обнаружит распознаватель, поддерживающий язык и другие свойства штрихов. Этот распознаватель используется для распознавания рукописного ввода для этих штрихов.

Если [**иинканализер**](iinkanalyzer.md) не находит [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , который поддерживает набор штрихов во время анализа, **иинканализер** создает [**ианалисисварнинг**](ianalysiswarning.md) с кодом предупреждения **аналисисварнингкоде \_ InkAnalysisRecognizerNotInstalled** (см. [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md)).

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

[**Метод Иинканализер:: Жетинканалисисрекогнизерсбиприорити**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[**иинканалисисрекогнизерс**](iinkanalysisrecognizers.md)
</dt> <dt>

[**ианалисисварнинг**](ianalysiswarning.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




