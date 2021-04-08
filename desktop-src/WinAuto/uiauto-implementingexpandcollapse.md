---
title: Шаблон элемента управления ExpandCollapse
description: Описывает правила и соглашения для реализации Иекспандколлапсепровидер, включая сведения о свойствах, методах и событиях.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления ExpandCollapse
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления ExpandCollapse
- Модель автоматизации пользовательского интерфейса, Иекспандколлапсепровидер
- IExpandCollapseProvider
- реализация шаблонов элементов управления ExpandCollapse модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления ExpandCollapse
- шаблоны элементов управления, Иекспандколлапсепровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса ExpandCollapse
- шаблоны элементов управления, ExpandCollapse
- интерфейсы, Иекспандколлапсепровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bd28ddcc201dcff0a4811a1eb8e04670f93091
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067738"
---
# <a name="expandcollapse-control-pattern"></a>Шаблон элемента управления ExpandCollapse

Описывает правила и соглашения для реализации [**иекспандколлапсепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider), включая сведения о свойствах, методах и событиях. Шаблон элемента управления **ExpandCollapse** используется для поддержки элементов управления, которые визуально разворачиваются для отображения большего содержимого и сворачиваются для скрытия содержимого.

Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **иекспандколлапсепровидер**](#required-members-for-iexpandcollapseprovider)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **ExpandCollapse** Обратите внимание на следующие правила и соглашения.

-   Агрегатные элементы управления, построенные с помощью дочерних объектов, которые предоставляют пользовательский интерфейс с функциональностью развертывания и свертывания, должны поддерживать шаблон элемента управления **ExpandCollapse** , а их дочерние элементы — нет. Например, элемент управления "поле со списком" создается с помощью сочетания элементов управления "список", "Кнопка" и "Правка", но это только родительское поле со списком, которое должно поддерживать шаблон элемента управления **ExpandCollapse** .
    > [!Note]  
    > Исключением является элемент управления Menu, который представляет собой статистическое выражение отдельных объектов пунктов меню. Объекты пунктов меню могут поддерживать шаблон элемента управления **ExpandCollapse** , но родительский элемент управления Menu не может. Аналогичное исключение применяется к элементам управления "дерево" и "элемент дерева".

     

-   Если для элемента управления [**иекспандколлапсепровидер:: ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) задано значение **ExpandCollapseState \_ леафноде**, то все функции **ExpandCollapse** в настоящее время неактивны для элемента управления, и единственной информацией, которая может быть получена с помощью этого шаблона элемента управления, является **ExpandCollapseState**. При последующем добавлении каких-либо дочерних объектов активируется функция **ExpandCollapseState** Changes и **ExpandCollapse** .
-   [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) относится только к видимости непосредственных дочерних объектов; Он не ссылается на видимость всех объектов-потомков.
-   Функция [**иекспандколлапсепровидер:: Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) и [**сворачивания**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) зависит от конкретного элемента управления. Ниже представлены примеры такого поведения.
    -   Меню Office Personal может быть элементом меню с тремя состояниями ("развернуто", "свернуто" и "Партиаллекспандед"), где элемент управления определяет состояние, которое необходимо принять при вызове [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) или [**сворачивания**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) .
    -   При вызове [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) для элемента дерева могут отображаться все потомки или только непосредственные дочерние элементы.
    -   Если вызов метода [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) или [**сворачивания**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) для элемента управления поддерживает состояние его потомков, необходимо отправить событие изменения видимости, а не событие изменения состояния. Если родительский элемент управления не сохраняет состояние его потомков при свертывании, элемент управления может уничтожить все потомки, которые больше не видны, и вызвать уничтоженное событие. или может изменить [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) для каждого потомка и вызвать событие изменения видимости.
-   Чтобы гарантировать навигацию, желательно, чтобы объект находящегося в дереве Microsoft UI Automation (с соответствующим состоянием видимости), независимо от его родителей- [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate). Если потомки создаются по запросу, они могут отображаться только в дереве модели автоматизации пользовательского интерфейса после того, как они отображаются в первый раз или только когда они видимы.

## <a name="required-members-for-iexpandcollapseprovider"></a>Обязательные члены для **иекспандколлапсепровидер**

Для реализации интерфейса [**иекспандколлапсепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) требуются следующие свойства, методы и события.



| Обязательные члены                                                                                    | Тип члена | Примечания                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | Свойство    | Нет                                                                   |
| [**Разверните**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | Метод      | Нет                                                                   |
| [**Свернуть**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | Метод      | Нет                                                                   |
| [**иуиаутоматионпропертичанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Событие       | Этот элемент управления не имеет связанных событий; Используйте этот универсальный обработчик событий. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 




