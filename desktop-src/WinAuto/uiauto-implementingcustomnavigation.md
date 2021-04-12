---
title: Шаблон элемента управления Кустомнавигатион
description: Описывает правила и соглашения для реализации интерфейса Икустомнавигатионпровидер, включая сведения о свойствах и методах.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253220"
---
# <a name="customnavigation-control-pattern"></a>Шаблон элемента управления Кустомнавигатион

Описывает правила и соглашения для реализации интерфейса **икустомнавигатионпровидер** , включая сведения о свойствах и методах. Шаблон элемента управления **кустомнавигатион** используется для обеспечения настраиваемой навигации между элементами управления в структурах, аналогичных иерархии, таких как элементы списка, маркированные списки, нумерованные списки и заголовки. Это позволяет поставщикам описывать структуры или определять связи перемещения, используя только элемент, а не только содержащий его элемент управления.

Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **икустомнавигатионпровидер**](#required-members-for-icustomnavigationprovider)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

При реализации поставщика **кустомнавигатион** Обратите внимание на следующие правила и соглашения.

-   Значения свойств для **поситионинсет**, **sizeof** и **Level** являются целочисленными значениями, основанными на единицах.
-   **Икустомнавигатионпровидер** не обеспечивает активную манипуляцию с элементом управления, например перемещением позиций, добавлением и удалением элементов, а также повышением и понижением уровней.
-   Элементы управления, которые реализуют **икустомнавигатионпровидер** , обычно имеют иерархическую структуру, но могут пропускать уровни с помощью метода **navigate** . Для шаблона требуются свойства **поситионинсет**, **sizeof** и **Level** .

## <a name="required-members-for-icustomnavigationprovider"></a>Обязательные члены для **икустомнавигатионпровидер**

Для реализации интерфейса **икустомнавигатионпровидер** требуются следующие свойства.



| Обязательные члены                                                                  | Тип члена | Примечания                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [**качедлевел**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | Свойство    | Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**качедпоситионинсет**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | Свойство    | Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**качедсизеофсет**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | Свойство    | Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**куррентлевел**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | Свойство    | Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**куррентпоситионинсет**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | Свойство    | Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**куррентсизеофсет**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | Свойство    | Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**Осуществляется**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | Метод      | Нет                                                                                |



 

Этот шаблон элемента управления не имеет связанных методов или событий.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Элемент управления ListItem](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[Элемент управления HeaderItem](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[Элемент управления DataItem](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




