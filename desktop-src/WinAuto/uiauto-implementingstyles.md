---
title: Шаблон элемента управления Styles
description: Описывает правила и соглашения для реализации Истилеспровидер, включая сведения о свойствах и методах. Шаблон элемента управления Styles используется для описания элемента пользовательского интерфейса, имеющего конкретный стиль, цвет заливки, шаблон заливки или форму.
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Styles
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Styles
- Модель автоматизации пользовательского интерфейса, Истилеспровидер
- IStylesProvider
- Реализация шаблона элемента управления стилей автоматизации пользовательского интерфейса
- Шаблон элемента управления Styles
- шаблоны элементов управления, Истилеспровидер
- шаблоны элементов управления, реализация стилей автоматизации пользовательского интерфейса
- шаблоны элементов управления, стили
- интерфейсы, Истилеспровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611e2f1979aaa4744ce3ff39965053f63399b2b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793351"
---
# <a name="styles-control-pattern"></a>Шаблон элемента управления Styles

Описывает правила и соглашения для реализации [**истилеспровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider), включая сведения о свойствах и методах. Шаблон элемента управления **styles** используется для описания элемента пользовательского интерфейса, имеющего конкретный стиль, цвет заливки, шаблон заливки или форму.

Шаблон элемента управления **styles** особенно полезен для описания элементов в документе, которые часто имеют такие стили. Обычно стили содержат информацию, которая полезна для клиентов с ограниченными возможностями. Например, стиль может описывать определенную строку как заголовок документа или определенный объект блок-схемы как ромб или окружность. Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **истилеспровидер**](#required-members-for-istylesprovider)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **styles** Обратите внимание на следующие правила и соглашения.

-   Файл заголовка UIAutomationClient. h определяет набор именованных постоянных значений, используемых для определения нескольких распространенных стилей. Дополнительные сведения см. в разделе [**идентификаторы стилей**](uiauto-style-identifiers.md).
-   Если вы используете [**стилеид \_ Custom**](uiauto-style-identifiers.md), необходимо реализовать свойство [**истилеспровидер:: stylename**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) , чтобы позволить клиентам обнаруживать имя стиля. Не нужно реализовывать свойство **stylename** для стандартного стиля, поскольку Microsoft UI Automation предоставляет имя по умолчанию, но его можно реализовать, если необходимо переопределить имя по умолчанию.
-   Другие свойства в шаблоне **стилей** являются необязательными. Поставщик может возвращать [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) для свойства, которое не поддерживается.
-   Стили в текстовом диапазоне можно представить с помощью следующих атрибутов текста:
    -   При ответе на запрос атрибута Text [**стилеид**](uiauto-textattribute-ids.md) текстовый диапазон должен возвращать один из идентификаторов стилей, описанных в разделе [**идентификаторы стилей**](uiauto-style-identifiers.md).
    -   Если [**используется \_ Настраиваемый стилеид**](uiauto-style-identifiers.md) , текстовый диапазон должен возвращать строковое значение для атрибута Text [**stylename**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) , чтобы клиенты могут обнаружить имя стиля.
    -   Текстовый диапазон, имеющий несколько стилей, таких как заголовок и нормальный текст, должен возвращать специальное свойство [**Ресерведмикседаттрибутевалуе**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) автоматизации пользовательского интерфейса для свойств [**стилеид**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) и [**stylename**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) . Клиент, получивший этот ответ, может разделить текстовый диапазон, чтобы найти место начала и конца стилей.
-   Приложения могут использовать разнообразные стили для описания объектов, но модель автоматизации пользовательского интерфейса представляет только самые распространенные. Для представления дополнительных атрибутов стиля, таких как цвет границы, поставщик может возвращать список дополнительных атрибутов в свойстве [**расширенных свойств**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) . По сути, это контейнер свойств с набором расширенных свойств, например "BorderColor = 0xFF0000; BorderStyle = пунктир ". Значения расширенных свойств могут быть специфичными для приложения.

## <a name="required-members-for-istylesprovider"></a>Обязательные члены для **истилеспровидер**

Для реализации интерфейса [**истилеспровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) требуются следующие свойства.



| Обязательные члены                                                            | Тип члена | Примечания |
|-----------------------------------------------------------------------------|-------------|-------|
| [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | Свойство    | Нет  |
| [**FillColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | Свойство    | Нет  |
| [**филлпаттернколор**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | Свойство    | Нет  |
| [**филлпаттернстиле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | Свойство    | Нет  |
| [**Фигурная**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | Свойство    | Нет  |
| [**стилеид**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | Свойство    | Нет  |
| [**ИмяСтиля**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | Свойство    | Нет  |



 

Этот шаблон элемента управления не имеет связанных методов или событий.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 