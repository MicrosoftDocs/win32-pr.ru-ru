---
title: Шаблон элемента управления SelectionItem
description: Описывает правила и соглашения для реализации Иселектионитемпровидер, включая сведения о свойствах, методах и событиях.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления SelectionItem
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления SelectionItem
- Модель автоматизации пользовательского интерфейса, Иселектионитемпровидер
- ISelectionItemProvider
- реализация шаблонов элементов управления SelectionItem модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления SelectionItem
- шаблоны элементов управления, Иселектионитемпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса SelectionItem
- шаблоны элементов управления, SelectionItem
- интерфейсы, Иселектионитемпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700487"
---
# <a name="selectionitem-control-pattern"></a>Шаблон элемента управления SelectionItem

Описывает правила и соглашения для реализации [**иселектионитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), включая сведения о свойствах, методах и событиях. Шаблон элемента управления **SelectionItem** используется для поддержки элементов управления, которые действуют как отдельные, выбираемые дочерние элементы элементов управления контейнера, реализующие [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).

Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **иселектионитемпровидер**](#required-members-for-iselectionitemprovider)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **SelectionItem** Обратите внимание на следующие правила и соглашения.

-   Элементы управления с одним выбором, которые управляют дочерними элементами управления, которые реализуют [**иравелементпровидерфрагментрут**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), такие как ползунок **разрешения экрана** в диалоговом окне **свойства отображения** для Windows, должны реализовывать [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider). их дочерние элементы должны реализовывать как [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) , так и [**иселектионитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

## <a name="required-members-for-iselectionitemprovider"></a>Обязательные члены для **иселектионитемпровидер**

Для реализации интерфейса [**иселектионитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) требуются следующие свойства, методы и события.



| Обязательные члены                                                                                                                        | Тип члена | Примечания |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [**аддтоселектион**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | Метод      | Нет  |
| [**IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | Свойство    | Нет  |
| [**ремовефромселектион**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | Метод      | Нет  |
| [**Метьте**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | Метод      | Нет  |
| [**селектионконтаинер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | Свойство    | Нет  |
| [**UIA \_ SelectionItem \_ елементаддедтоселектионевентид**](uiauto-event-ids.md)         | Событие       | Нет  |
| [**UIA \_ SelectionItem \_ елементремоведфромселектионевентид**](uiauto-event-ids.md) | Событие       | Нет  |
| [**UIA \_ SelectionItem \_ елементселектедевентид**](uiauto-event-ids.md)                         | Событие       | Нет  |



 

Если результат [**SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), [**аддтоселектион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)или [**ремовефромселектион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) является одним выбранным элементом, должно быть создано событие **елементселектед** ([**UIA \_ SelectionItem \_ елементселектедевентид**](uiauto-event-ids.md)). в противном случае создайте события **елементаддедтоселектион** ([**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)) или **ElementRemovedFromSelection** ([**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) соответственно.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 




