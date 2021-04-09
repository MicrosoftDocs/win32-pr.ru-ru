---
title: Шаблон элемента управления Спреадшититем
description: Описывает правила и соглашения для реализации Испреадшититемпровидер, включая сведения о свойствах и методах.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Спреадшититем
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Спреадшититем
- Модель автоматизации пользовательского интерфейса, Испреадшититемпровидер
- ISpreadsheetItemProvider
- Реализация шаблона элемента управления Спреадшититем модели автоматизации пользовательского интерфейса
- Шаблон элемента управления Спреадшититем
- шаблоны элементов управления, Испреадшититемпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса Спреадшититем
- шаблоны элементов управления, Спреадшититем
- интерфейсы, Испреадшититемпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070492"
---
# <a name="spreadsheetitem-control-pattern"></a>Шаблон элемента управления Спреадшититем

Описывает правила и соглашения для реализации [**испреадшититемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), включая сведения о свойствах и методах. Шаблон элемента управления **спреадшититем** используется для предоставления свойств ячейки электронной таблицы или другого документа, основанного на сетке.

Шаблон элемента управления **спреадшититем** тесно связан с шаблоном элемента управления [GridItem](uiauto-implementinggriditem.md) . элементы управления, реализующие шаблон элемента управления **спреадшититем** , должны также реализовать шаблон элемента управления GridItem. Элементы управления могут также реализовывать шаблон элемента управления [TableItem](uiauto-implementingtableitem.md) , если это уместно. Примеры элементов управления, реализующих эти шаблоны элементов управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **испреадшититемпровидер**](#required-members-for-ispreadsheetitemprovider)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **спреадшититем** Обратите внимание на следующие правила и соглашения.

-   При реализации методов [**испреадшититемпровидер:: жетаннотатионобжектс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) и [**Испреадшититемпровидер:: жетаннотатионтипес**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) обратитесь к документации по [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Эти методы возвращают массивы, чтобы предоставить поставщикам возможность поддерживать несколько заметок в одной ячейке.
-   Некоторые типы заметок не нуждаются в полной реализации интерфейса [**ианнотатионпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Например, можно представить простой индикатор орфографической ошибки, [**жетаннотатионтипес**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) возвратить идентификатор атрибута текста [**аннотатионтипе \_ спеллинжеррор**](uiauto-annotation-type-identifiers.md), а [**жетаннотатионобжектс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) возвращать значение null.

## <a name="required-members-for-ispreadsheetitemprovider"></a>Обязательные члены для **испреадшититемпровидер**

Для реализации интерфейса [**испреадшититемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) требуются следующие свойства и методы.



| Обязательные члены                                                                         | Тип члена | Примечания                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Формула**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | Свойство    | Реализовать отдельное свойство [**формулы**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) необходимо потому, что свойство [value](value-property.md) ячейки обычно возвращает вычисленное значение ячейки. Если формула не задана, свойство **формулы** должно иметь **значение NULL** . |
| [**жетаннотатионобжектс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | Метод      | Возвращает массив поставщиков элементов, которые ссылаются на заметки, связанные с этой ячейкой. Указатели в массиве могут иметь значение null, если в заметке отсутствует связанный поставщик.                                                                                                       |
| [**жетаннотатионтипес**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | Метод      | Возвращает массив идентификаторов типа аннотации, описывающих заметки в этой ячейке. Размер массива должен совпадать с размером массива, возвращаемого функцией [**жетаннотатионобжектс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).                                         |



 

Этот шаблон элемента управления не имеет связанных событий.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Шаблон элемента управления электронной таблицей](uiauto-implementingspreadsheet.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 