---
title: Интерфейс IAccessibleEx
description: Элементы управления, у которых нет поставщика Microsoft UI Automation, но реализующие IAccessible, можно легко обновить, чтобы обеспечить некоторые функции автоматизации пользовательского интерфейса путем реализации интерфейса IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133002"
---
# <a name="the-iaccessibleex-interface"></a>Интерфейс IAccessibleEx

Элементы управления, у которых нет поставщика Microsoft UI Automation, но реализующие [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), можно легко обновить, чтобы обеспечить некоторые функции автоматизации пользовательского интерфейса путем реализации интерфейса [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Этот интерфейс позволяет элементу управления предоставлять свойства автоматизации пользовательского интерфейса и шаблоны элементов управления без необходимости полной реализации интерфейсов поставщика автоматизации пользовательского интерфейса, таких как [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Чтобы использовать **IAccessibleEx**, **иравелементпровидерфрагмент** и все другие интерфейсы автоматизации пользовательского интерфейса, включите в исходный код файл заголовка UIAutomation. h.

Например, рассмотрим пользовательский элемент управления, имеющий значение Range. Сервер Microsoft Active Accessibility для элемента управления определяет роль элемента управления и может возвращать его текущее значение. Однако, поскольку Microsoft Active Accessibility не определяет минимальное и максимальное свойства, сервер не имеет средств для возврата минимального и максимального значений элемента управления. Клиент автоматизации пользовательского интерфейса может получить роль элемента управления, текущее значение и другие свойства Microsoft Active Accessibility, так как ядро автоматизации пользовательского интерфейса может получить их через [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Однако без доступа к интерфейсу [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) в объекте модель автоматизации пользовательского интерфейса также не может получить максимальное и минимальное значения.

Разработчик элемента управления может предоставить полный поставщик автоматизации пользовательского интерфейса для элемента управления, но это означает дублирование большинства существующих функциональных возможностей реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : например, навигации и общих свойств. Вместо этого разработчик может по-прежнему использовать **IAccessible** для предоставления этой функции, добавляя поддержку свойств конкретного элемента управления через [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

## <a name="in-this-section"></a>Содержание раздела

-   [Рекомендации по реализации IAccessibleEx](iaccessibleex-implementation-guidelines.md)
-   [Реализация IAccessibleEx для поставщиков](implementing-iaccessibleex-for-providers.md)
-   [Использование IAccessibleEx из клиента](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Общая инфраструктура](common-infrastructure.md)
</dt> </dl>

 

 




