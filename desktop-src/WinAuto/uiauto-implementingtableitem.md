---
title: Шаблон элемента управления TableItem
description: Описывает правила и соглашения для реализации Итаблеитемпровидер, включая сведения о методах. Шаблон элемента управления TableItem используется для поддержки дочерних элементов управления контейнеров, реализующих Итаблепровидер.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления TableItem
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления TableItem
- Модель автоматизации пользовательского интерфейса, Итаблеитемпровидер
- ITableItemProvider
- реализация шаблонов элементов управления TableItem модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления TableItem
- шаблоны элементов управления, Итаблеитемпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса TableItem
- шаблоны элементов управления, TableItem
- интерфейсы, Итаблеитемпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774813"
---
# <a name="tableitem-control-pattern"></a>Шаблон элемента управления TableItem

Описывает правила и соглашения для реализации [**итаблеитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), включая сведения о методах. Шаблон элемента управления **TableItem** используется для поддержки дочерних элементов управления контейнеров, реализующих [**итаблепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).

Доступ к отдельным функциям ячейки обеспечивается необходимой, параллельной реализацией [**игридитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider). Этот шаблон элемента управления является аналогом **игридитемпровидер** с различием того, что любой элемент управления, реализующий [**итаблеитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) , должен программно предоставлять связь между отдельной ячейкой и сведениями о строках и столбцах. Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **итаблеитемпровидер**](#required-members-for-itableitemprovider)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **TableItem** Обратите внимание на следующие правила и соглашения.

-   Сведения о связанных функциях элементов сетки см. в разделе [шаблон элемента управления GridItem](uiauto-implementinggriditem.md).

## <a name="required-members-for-itableitemprovider"></a>Обязательные члены для **итаблеитемпровидер**

Для реализации интерфейса [**итаблеитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) требуются следующие методы.



| Обязательные члены                                                               | Тип члена | Примечания |
|--------------------------------------------------------------------------------|-------------|-------|
| [**жетколумнхеадеритемс**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | Метод      | Нет  |
| [**жетровхеадеритемс**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | Метод      | Нет  |



 

Этот шаблон элемента управления не имеет связанных свойств или событий.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Шаблон элемента управления Table](uiauto-implementingtable.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 




