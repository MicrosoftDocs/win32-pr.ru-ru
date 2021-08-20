---
title: Шаблон элемента управления RangeValue
description: Описывает правила и соглашения для реализации IRangeValueProvider, включая сведения о свойствах и методах. Шаблон элемента управления RangeValue используется для поддержки элементов управления, для которых можно задать значение в диапазоне.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления RangeValue
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления RangeValue
- Модель автоматизации пользовательского интерфейса, IRangeValueProvider
- IRangeValueProvider
- реализация шаблонов элементов управления RangeValue модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления RangeValue
- шаблоны элементов управления, IRangeValueProvider
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса RangeValue
- шаблоны элементов управления, RangeValue
- интерфейсы, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae87ca25fd1ada2f57ce77412fb589875792541fd2b5d31d6eb0aa86192dee36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114865"
---
# <a name="rangevalue-control-pattern"></a>Шаблон элемента управления RangeValue

Описывает правила и соглашения для реализации [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), включая сведения о свойствах и методах. Шаблон элемента управления **RangeValue** используется для поддержки элементов управления, для которых можно задать значение в диапазоне.

Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **IRangeValueProvider**](#required-members-for-irangevalueprovider)
-   [Связанные темы](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **RangeValue** Обратите внимание на следующие правила и соглашения.

-   Элементы управления позволяют повторную калибровку своих поддерживаемых свойств на основе языкового стандарта или предпочтений пользователя. Примером этого является элемент управления "Термометр", который можно задать для отображения температуры в шкале Цельсия или Фаренгейта.
-   Элементы управления, имеющие неоднозначные значения диапазона, такие как индикаторы выполнения или ползунки, должны нормализовать эти значения.

## <a name="required-members-for-irangevalueprovider"></a>Обязательные члены для **IRangeValueProvider**

Для реализации интерфейса [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) требуются следующие свойства и методы.



| Обязательные члены                                              | Тип члена | Примечания |
|---------------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | Свойство    | Нет  |
| [**Значение**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Свойство    | Нет  |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | Свойство    | Нет  |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Свойство    | Нет  |
| [**Максимум**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Свойство    | Нет  |
| [**Минимум**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Свойство    | Нет  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | Метод      | Нет  |



 

Этот шаблон элемента управления не имеет связанных событий.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 




