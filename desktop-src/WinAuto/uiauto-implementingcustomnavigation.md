---
title: Шаблон элемента управления Кустомнавигатион
description: Описывает правила и соглашения для реализации интерфейса Икустомнавигатионпровидер, включая сведения о свойствах и методах.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4499f5b031b5b5a9391f0c0078cb64c4c2715b61052c324cc2c2b19ccb2f5d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899563"
---
# <a name="customnavigation-control-pattern"></a>Шаблон элемента управления Кустомнавигатион

Описывает правила и соглашения для реализации интерфейса **икустомнавигатионпровидер** , включая сведения о свойствах и методах. Шаблон элемента управления **кустомнавигатион** используется для обеспечения настраиваемой навигации между элементами управления в структурах, аналогичных иерархии, таких как элементы списка, маркированные списки, нумерованные списки и заголовки. Это позволяет поставщикам описывать структуры или определять связи перемещения, используя только элемент, а не только содержащий его элемент управления.

Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Обязательные члены для **икустомнавигатионпровидер**](#required-members-for-icustomnavigationprovider)
-   [Связанные темы](#related-topics)

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
| [**Перейти.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | Метод      | Нет                                                                                |



 

Этот шаблон элемента управления не имеет связанных методов или событий.

## <a name="related-topics"></a>Связанные темы

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

 

 




