---
title: Шаблон элемента управления Grid
description: Описывает правила и соглашения для реализации IGridProvider, включая сведения о свойствах и методах. Шаблон элемента управления Grid используется для поддержки элементов управления, которые действуют как контейнеры для коллекции дочерних элементов.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Grid
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Grid
- Модель автоматизации пользовательского интерфейса, IGridProvider
- IGridProvider
- реализация шаблонов элементов управления сетки модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Grid
- шаблоны элементов управления, IGridProvider
- шаблоны элементов управления, реализация сетки автоматизации пользовательского интерфейса
- шаблоны элементов управления, сетка
- интерфейсы, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067737"
---
# <a name="grid-control-pattern"></a>Шаблон элемента управления Grid

Описывает правила и соглашения для реализации [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), включая сведения о свойствах и методах. Шаблон элемента управления **Grid** используется для поддержки элементов управления, которые действуют как контейнеры для коллекции дочерних элементов.

Дочерние элементы этого элемента должны реализовать [**игридитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) и быть организованы в двухмерной логической системе координат, которую можно просмотреть по строкам и столбцам. Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **IGridProvider**](#required-members-for-igridprovider)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **Grid** Обратите внимание на следующие правила и соглашения.

-   Координаты сетки отсчитываются от нуля в левом верхнем углу (или в верхней правой ячейке в зависимости от языкового стандарта) с координатами (0, 0).
-   Если ячейка пуста, элемент автоматизации пользовательского интерфейса Майкрософт по-прежнему должен быть возвращен для поддержки свойства [**игридитемпровидер:: контаининггрид**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) этой ячейки. Это возможно, когда макет дочерних элементов сетки подобен массиву с переменной длиной (см. пример ниже).

    ![Пример элемента управления "Сетка" с пустыми координатами](images/grid.png)

-   Сетка с одним элементом по-прежнему необходима для реализации [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , если она логически считается сеткой. Количество дочерних элементов в сетке не имеет значения.
-   Скрытые строки и столбцы в зависимости от реализации поставщика могут быть загружены в дерево модели автоматизации пользовательского интерфейса, поэтому они будут отражены в свойствах [**IGridProvider:: ROWCOUNT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) и [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) . Если скрытые строки и столбцы еще не загружены, они не должны учитываться.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) не включает активную манипуляцию с сеткой; Для включения этой функции необходимо реализовать [**итрансформпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .
-   Используйте [**иуиаутоматионструктуречанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) для прослушивания в сетке изменений структуры или макета, например ячеек, которые были добавлены, удалены или объединены.
-   Используйте [**иуиаутоматионфокусчанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) , чтобы отвести обход элементов или ячеек сетки.

## <a name="required-members-for-igridprovider"></a>Обязательные члены для **IGridProvider**

Для реализации интерфейса [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) требуются следующие свойства и методы.



| Обязательные члены                                        | Тип члена | Примечания |
|---------------------------------------------------------|-------------|-------|
| [**Количества**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | Свойство    | Нет  |
| [**Число**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | Свойство    | Нет  |
| [**GetItem**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | Метод      | Нет  |



 

Этот шаблон элемента управления не имеет связанных событий.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Шаблон элемента управления GridItem](uiauto-implementinggriditem.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 




