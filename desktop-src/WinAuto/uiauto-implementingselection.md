---
title: Шаблон элемента управления Selection
description: Описывает правила и соглашения для реализации Иселектионпровидер, включая сведения о свойствах, методах и событиях.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Selection
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Selection
- Модель автоматизации пользовательского интерфейса, Иселектионпровидер
- ISelectionProvider
- реализация шаблонов элементов управления для выбора модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления выбора
- шаблоны элементов управления, Иселектионпровидер
- шаблоны элементов управления, реализация выбора модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, выбор
- интерфейсы, Иселектионпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068033"
---
# <a name="selection-control-pattern"></a>Шаблон элемента управления Selection

Описывает правила и соглашения для реализации [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), включая сведения о свойствах, методах и событиях. Шаблон элемента управления **Selection** используется для поддержки элементов управления, которые действуют как контейнеры для коллекции выбираемых дочерних элементов. Дочерние элементы этого элемента должны реализовывать [**иселектионитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **иселектионпровидер**](#required-members-for-iselectionprovider)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **Selection** Обратите внимание на следующие правила и соглашения.

-   Элементы управления, реализующие [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) , позволяют выбирать как один, так и несколько дочерних элементов. Например, списки, представления списков и представления в виде дерева поддерживают множественный выбор, тогда как поля со списком, ползунки и группы переключателей поддерживают одиночный выбор.
-   Элементы управления, имеющие минимальный, максимальный и непрерывный диапазоны, такие как элемент **управления "ползунок" в** проигрывателе мультимедиа, должны реализовывать [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) вместо [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).
-   Элементы управления с одним выбором, которые управляют дочерними элементами управления, которые реализуют [**иравелементпровидерфрагментрут**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), такие как ползунок **разрешения экрана** в диалоговом окне **свойства отображения** для Windows или элемент управления выбора **цвета** из Microsoft Word (см. следующий рисунок), должны реализовывать [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider). их дочерние элементы должны реализовывать как [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) , так и [**иселектионитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

    ![изображение, показывающее пример сопоставления строк цветовой палитры](images/uia-valuepattern-colorpicker.jpg)

-   Меню не поддерживают шаблон элемента управления **Selection** . Если вы работаете с элементами меню, включающими как график, так и текст (например, элементы **области предварительного просмотра** в меню **вид** в Microsoft Outlook) и необходимо передать состояние, следует реализовать [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).

## <a name="required-members-for-iselectionprovider"></a>Обязательные члены для **иселектионпровидер**

Для реализации интерфейса [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) требуются следующие свойства, методы и события.



| Обязательные члены                                                                                | Тип члена | Примечания                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**канселектмултипле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | Свойство    | Нет                                                                        |
| [**исселектионрекуиред**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | Свойство    | Нет                                                                        |
| [**Выборка**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | Метод      | Нет                                                                        |
| [**\_Выбор UIA \_ инвалидатедевентид**](uiauto-event-ids.md) | Событие       | Это событие вызывается, когда выделение в контейнере значительно изменилось. |



 

Свойства [**иселектионпровидер:: исселектионрекуиред**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) и [**канселектмултипле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) могут быть динамическими. Например, начальное состояние элемента управления может не иметь элементов, выбранных по умолчанию, что означает, что **исселектионрекуиред** имеет значение false. Однако после выбора элемента элемент управления всегда должен иметь хотя бы один выбранный элемент. В редких случаях элемент управления также может разрешать выбор нескольких элементов при инициализации, но впоследствии разрешает выбор только одного элемента.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Шаблон элемента управления SelectionItem](uiauto-implementingselectionitem.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 




