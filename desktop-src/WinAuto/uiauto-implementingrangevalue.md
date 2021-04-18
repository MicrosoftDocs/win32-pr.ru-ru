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
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700605"
---
# <a name="rangevalue-control-pattern"></a>Шаблон элемента управления RangeValue

Описывает правила и соглашения для реализации [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), включая сведения о свойствах и методах. Шаблон элемента управления **RangeValue** используется для поддержки элементов управления, для которых можно задать значение в диапазоне.

Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **IRangeValueProvider**](#required-members-for-irangevalueprovider)
-   [См. также](#related-topics)

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
| [**Минимальные**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Свойство    | Нет  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | Метод      | Нет  |



 

Этот шаблон элемента управления не имеет связанных событий.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 




