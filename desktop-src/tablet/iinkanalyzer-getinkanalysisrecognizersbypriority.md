---
description: Извлекает упорядоченную коллекцию объектов Иинканалисисрекогнизер.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'Метод Иинканализер:: Жетинканалисисрекогнизерсбиприорити (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc663385006eedaca163f529af1f9f8a2da2eb5d3d41db823ffb53ee91775b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713414"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a>Метод Иинканализер:: Жетинканалисисрекогнизерсбиприорити

Извлекает упорядоченную коллекцию объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппинканалисисрекогнизерс* \[ заполняет\]
</dt> <dd>

Упорядоченная коллекция объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппинканалисисрекогнизерс* , когда больше не нужно использовать объект.

 

Порядок распознавателей в этой коллекции указывает порядок, в котором [**иинканализер**](iinkanalyzer.md) оценивает доступные Распознаватели. **Иинканализер** использует язык обводки в качестве основного критерия для применения [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md). В качестве вторичного критерия **иинканализер** сравнивает сведения о подсказках анализа с поддерживаемыми возможностями объекта **иинканалисисрекогнизер** (см. [**иинканалисисрекогнизер::**](iinkanalysisrecognizer-getcapabilities.md)GetObject). Дополнительные сведения о указаниях по анализу см. в разделе [**метод иинканализер:: креатеаналисишинт**](iinkanalyzer-createanalysishint.md).

Если в нескольких [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) поддерживается идентификатор языка, [**иинканализер**](iinkanalyzer.md) использует алгоритм "First-Fit" для выбора первого **иинканалисисрекогнизер** для анализа штрихов этого языка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**иинканалисисрекогнизерс**](iinkanalysisrecognizers.md)
</dt> <dt>

[**Метод Иинканализер:: Сесигхестприоритинканалисисрекогнизер**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

