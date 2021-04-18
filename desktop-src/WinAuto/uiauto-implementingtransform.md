---
title: Преобразование шаблона элемента управления
description: Описывает правила и соглашения для реализации Итрансформпровидер и ITransformProvider2, включая сведения о свойствах и методах.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Transform
- Модель автоматизации пользовательского интерфейса, шаблон элемента Transform
- Модель автоматизации пользовательского интерфейса, Итрансформпровидер
- ITransformProvider
- реализация шаблонов элементов управления преобразования модели автоматизации пользовательского интерфейса
- Преобразование шаблонов элементов управления
- шаблоны элементов управления, Итрансформпровидер
- шаблоны элементов управления, реализация преобразования модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, преобразование
- интерфейсы, Итрансформпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533344"
---
# <a name="transform-control-pattern"></a>Преобразование шаблона элемента управления

Описывает правила и соглашения для реализации [**итрансформпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) и [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), включая сведения о свойствах и методах. Шаблон элемента управления Transform используется для поддержки элементов управления, которые можно перемещать, изменять их размер или вращать в двухмерном пространстве.

Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **итрансформпровидер**](#required-members-for-itransformprovider)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **Transform** Обратите внимание на следующие правила и соглашения.

-   Поддержка этого шаблона элемента управления не ограничена объектами на рабочем столе. Этот шаблон элемента управления также должен поддерживаться дочерними элементами объекта контейнера, если эти дочерние элементы можно перемещать, изменять их размер или свободно поворачивать в пределах контейнера.
-   Объект нельзя перемещать, изменять его размер или поворачивать таким образом, что его итоговое положение на экране окажется полностью вне координат своего контейнера и поэтому он станет недоступным для клавиатуры или мыши (например, когда окно верхнего уровня перемещается за пределы экрана или дочерний объект перемещается за пределы границ окна просмотра контейнера). В этих случаях объект помещается максимально близко к запрошенным экранным координатам с переопределением верхней или левой координаты, чтобы они находились в границах контейнера.
-   Для систем с несколькими мониторами при перемещении объекта, изменении его размера или повороте полностью за пределами координат объединенного рабочего стола объект помещается на основном мониторе максимально близко к запрошенным координатам.
-   Все параметры и значения свойств являются абсолютными и не зависят от языка и региональных параметров.

## <a name="required-members-for-itransformprovider"></a>Обязательные члены для **итрансформпровидер**

Для реализации интерфейса [**итрансформпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) требуются следующие свойства и методы.



| Обязательные члены                                         | Тип члена | Примечания |
|----------------------------------------------------------|-------------|-------|
| [**канмове**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | Свойство    | Нет  |
| [**канресизе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | Свойство    | Нет  |
| [**канротате**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | Свойство    | Нет  |
| [**Переместить**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | Метод      | Нет  |
| [**Изменить размер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | Метод      | Нет  |
| [**Поворот**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | Метод      | Нет  |



 

Для реализации интерфейса [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) требуются следующие дополнительные свойства и методы.



| Обязательные члены                                              | Тип члена | Примечания |
|---------------------------------------------------------------|-------------|-------|
| [**канзум**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | Свойство    | Нет  |
| [**Масштаб**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | Метод      | Нет  |
| [**зумбюнит**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | Метод      | Нет  |
| [**зумлевел**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | Свойство    | Нет  |
| [**зуммаксимум**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | Свойство    | Нет  |
| [**зумминимум**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | Свойство    | Нет  |



 

Этот шаблон элемента управления не имеет связанных событий.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 