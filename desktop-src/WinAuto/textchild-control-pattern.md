---
title: Шаблон элемента управления Текстчилд
description: Содержит рекомендации и соглашения для реализации Итекстчилдпровидер, включая сведения о свойствах и методах. Шаблон элемента управления Текстчилд используется для доступа к ближайшему предку элемента, который поддерживает шаблон элемента управления Text.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Текстчилд
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Текстчилд
- Модель автоматизации пользовательского интерфейса, Итекстчилдпровидер
- ITextChildProvider
- реализация шаблонов элементов управления Текстчилд модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Текстчилд
- шаблоны элементов управления, Итекстчилдпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса Текстчилд
- шаблоны элементов управления, Текстчилд
- интерфейсы, Итекстчилдпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793615"
---
# <a name="textchild-control-pattern"></a>Шаблон элемента управления Текстчилд

Содержит рекомендации и соглашения для реализации [**итекстчилдпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), включая сведения о свойствах и методах. Шаблон элемента управления **текстчилд** используется для доступа к ближайшему предку элемента, который поддерживает шаблон элемента управления [Text](uiauto-implementingtextandtextrange.md) .

Например, предположим, что текст в документе содержит внедренное изображение и гиперссылку, как показано на следующем рисунке.

![снимок экрана с текстом, содержащим внедренное изображение и гиперссылку](images/textchild-pattern.png)

Если вы используете средства автоматизации пользовательского интерфейса Майкрософт для проверки дерева автоматизации пользовательского интерфейса для этого содержимого документа, оно может отобразить элемент документа с одним дочерним элементом, который представляет изображение, и другой дочерний элемент, представляющий гиперссылку. Пример:

![снимок экрана с командой "проверить отчет" в примере дерева элементов автоматизации пользовательского интерфейса](images/textchild-pattern-tree.png)

Как правило, элемент Document в предыдущем примере поддерживает шаблон элемента управления [Text](uiauto-implementingtextandtextrange.md) , но два дочерних элемента документа не имеют. Если клиентское приложение автоматизации пользовательского интерфейса содержит ссылку на элемент Image или элемент Hyperlink, клиент может использовать шаблон элемента управления **текстчилд** как удобный способ доступа к шаблону текстконтрол, предоставляемому содержащим элементом Document.

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации интерфейса [**итекстчилдпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) Обратите внимание на следующие правила и соглашения.

-   Свойство [**итекстчилдпровидер:: объект textcontainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) должно указывать ближайший элемент предка, который поддерживает интерфейс [**итекстпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , независимо от того, поддерживаются ли элементы, набольшиеся в цепочке предков, также поддерживать **итекстпровидер**.
-   Элемент не должен поддерживать интерфейс [**итекстпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) и [итекстчилдпровидер * *](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .
- Элемент, реализующий [**итекстчилдпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) , должен быть дочерним элементом или потомком элемента, реализующего [**итекстпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider). Этот элемент также не обязательно должен реализовывать [шаблон элемента управления Text](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).
-   Свойство [**итекстчилдпровидер:: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) должно указывать тот же текстовый диапазон, что и элемент, содержащийся в элементе Provider Text, когда его функция [**Итекстпровидер:: ранжефромчилд**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) вызывается с дочерним элементом text как вложенный дочерний элемент.

## <a name="required-members-for-itextchildprovider"></a>Обязательные члены для **итекстчилдпровидер**

Эти свойства и методы необходимы для реализации интерфейса [**итекстчилдпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .



| Обязательные члены                                                     | Тип члена | Примечания |
|----------------------------------------------------------------------|-------------|-------|
| [**Объект textcontainer**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | Свойство    | Нет  |
| [**TextRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | Свойство    | Нет  |



 

Этот шаблон элемента управления не имеет связанных методов или событий.

## <a name="related-topics"></a>См. также

**Зрения**

- [Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
- [Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
- [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)