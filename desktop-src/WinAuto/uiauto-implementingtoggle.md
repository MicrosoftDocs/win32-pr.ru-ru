---
title: Переключить шаблон элемента управления
description: Описывает правила и соглашения для реализации IToggleProvider, включая сведения о свойствах и методах. Шаблон элемента управления Toggle используется для поддержки элементов управления, которые могут циклически проходить по набору состояний и поддерживать состояние после установки.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Toggle
- Модель автоматизации пользовательского интерфейса, переключить шаблон элемента управления
- Модель автоматизации пользовательского интерфейса, IToggleProvider
- IToggleProvider
- реализация шаблонов элементов управления для модели автоматизации пользовательского интерфейса
- Переключить шаблоны элементов управления
- шаблоны элементов управления, IToggleProvider
- шаблоны элементов управления, реализация переключателя модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, переключатель
- интерфейсы, IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410763"
---
# <a name="toggle-control-pattern"></a>Переключить шаблон элемента управления

Описывает правила и соглашения для реализации [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), включая сведения о свойствах и методах. Шаблон элемента управления **Toggle** используется для поддержки элементов управления, которые могут циклически проходить по набору состояний и поддерживать состояние после установки.

Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **IToggleProvider**](#required-members-for-itoggleprovider)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **Toggle** Обратите внимание на следующие правила и соглашения.

-   Элементы управления, которые не сохраняют состояние при активации, такие как кнопки, кнопки панели инструментов и гиперссылки, должны реализовывать [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .
-   Элемент управления должен циклически переключаться по его состояниям ([**тогглестате**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) в следующем порядке: **тогглестате \_ On**, **тогглестате \_ Off** и, если поддерживается, **тогглестате \_ неопределенный**.
-   **Переключатель** не предоставляет метод Set-State из-за проблем, связанных с прямым заданием флажка с тремя состояниями, без прохода по соответствующей последовательности [**тогглестате**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) .
-   Элемент управления "переключатель" не реализует [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), так как он не способен циклически проходить по его допустимым состояниям.

## <a name="required-members-for-itoggleprovider"></a>Обязательные члены для **IToggleProvider**

Для реализации интерфейса [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) требуются следующие свойства и методы.



| Обязательные члены                                          | Тип члена | Примечания |
|-----------------------------------------------------------|-------------|-------|
| [**Переключение**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | Метод      | Нет  |
| [**тогглестате**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | Свойство    | Нет  |



 

Этот шаблон элемента управления не имеет связанных событий.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 




