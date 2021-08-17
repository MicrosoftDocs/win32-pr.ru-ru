---
title: Шаблон элемента управления Scroll
description: Описывает правила и соглашения для реализации Искроллпровидер, включая сведения о свойствах и методах. Шаблон элемента управления Scroll используется для поддержки элемента управления, который выступает в качестве прокручиваемого контейнера для коллекции дочерних объектов.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Scroll
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Scroll
- Модель автоматизации пользовательского интерфейса, Искроллпровидер
- IScrollProvider
- реализация шаблонов элемента управления Scroll модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Scroll
- шаблоны элементов управления, Искроллпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса прокрутка
- шаблоны элементов управления, прокрутка
- интерфейсы, Искроллпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d1cf3c04be18f362a64e619ec4659fac58923f29e6105174057b18a580f8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324402"
---
# <a name="scroll-control-pattern"></a>Шаблон элемента управления Scroll

Описывает правила и соглашения для реализации [**искроллпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), включая сведения о свойствах и методах. Шаблон элемента управления **Scroll** используется для поддержки элемента управления, который выступает в качестве прокручиваемого контейнера для коллекции дочерних объектов.

Элементу управления не требуется использовать полосы прокрутки для поддержки функций прокрутки, хотя обычно это делает. На следующем рисунке показан элемент управления прокрутки, который не использует полосы прокрутки. Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

![снимок экрана с элементом управления прокруткой без полос прокрутки](images/uia-scrollpattern-without-scrollbars.jpg)

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **искроллпровидер**](#required-members-for-iscrollprovider)
-   [Связанные темы](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации шаблона элемента управления **Scroll** Обратите внимание на следующие правила и соглашения.

-   Дочерние элементы этого элемента управления должны реализовывать [**искроллитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).
-   Полосы прокрутки элемента управления контейнера не поддерживают шаблон элемента управления **Scroll** . Вместо этого они должны поддерживать шаблон элемента управления [RangeValue](uiauto-implementingrangevalue.md) .
-   Если прокрутка измеряется в процентах, все значения или величины, связанные с делением шкалы прокрутки, должны быть нормализованы в диапазоне от 0 до 100.
-   Свойство [**искроллпровидер:: хоризонталлискроллабле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) и свойство [**вертикаллискроллабле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) не зависят от свойства, **включенного** .
-   Если свойство [**искроллпровидер:: хоризонталлискроллабле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) имеет **значение false**, то свойству [**хоризонталвиевсизе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) должно быть присвоено значение 100 (100%), а свойству [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) должно быть присвоено значение **UIA \_ скроллпаттернноскролл** (-1). Аналогично, если свойство [**вертикаллискроллабле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) имеет **значение false**, свойство [**вертикалвиевсизе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) должно иметь значение 100 (100%), а свойство [**вертикалскроллперцент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) должно иметь значение **UIA \_ скроллпаттернноскролл** (-1). Это позволяет клиенту Microsoft UI Automation использовать эти значения свойств в методе [**сетскроллперцент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) , одновременно избегая состояния гонки, если направление, в котором клиент не заинтересован в прокрутке, становится активным.
-   Свойство [**искроллпровидер:: HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) зависит от языкового стандарта. Если задать для **HorizontalScrollPercent** значение 100, расположение прокрутки элемента управления должно быть эквивалентно его крайней позиции для таких языков, как английский, чтение которых осуществляется слева направо. Кроме того, для таких языков, как арабский, который читается справа налево, установка **HorizontalScrollPercent** в 100 должна установить расположение прокрутки в самую левую позицию.

## <a name="required-members-for-iscrollprovider"></a>Обязательные члены для **искроллпровидер**

Для реализации интерфейса [**искроллпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) требуются следующие свойства и методы.



| Обязательные члены                                                                  | Тип члена | Примечания |
|-----------------------------------------------------------------------------------|-------------|-------|
| [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | Свойство    | Нет  |
| [**вертикалскроллперцент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | Свойство    | Нет  |
| [**хоризонталвиевсизе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | Свойство    | Нет  |
| [**вертикалвиевсизе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | Свойство    | Нет  |
| [**хоризонталлискроллабле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | Свойство    | Нет  |
| [**вертикаллискроллабле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | Свойство    | Нет  |
| [**Крутите**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | Метод      | Нет  |
| [**сетскроллперцент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | Метод      | Нет  |



 

Этот шаблон элемента управления не имеет связанных событий.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 




