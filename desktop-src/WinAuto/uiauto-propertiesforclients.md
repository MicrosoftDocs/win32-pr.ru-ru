---
title: Получение свойств элементов модели автоматизации пользовательского интерфейса
description: Свойства объектов Иуиаутоматионелемент содержат сведения об элементах пользовательского интерфейса, обычно элементах управления.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- Клиенты, получение элементов модели автоматизации пользовательского интерфейса
- Клиенты, элементы модели автоматизации пользовательского интерфейса
- Клиенты, свойства
- Клиенты, получение свойств
- Клиенты, свойства модели автоматизации пользовательского интерфейса
- Модель автоматизации пользовательского интерфейса, получение элементов
- Модель автоматизации пользовательского интерфейса, элементы
- Модель автоматизации пользовательского интерфейса, свойства
- Автоматизация пользовательского интерфейса, получение свойств
- получение свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691620"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a>Получение свойств элементов модели автоматизации пользовательского интерфейса

Свойства объектов [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) содержат сведения об элементах пользовательского интерфейса, обычно элементах управления. Свойства элемента являются универсальными; то есть, не относится к типу элемента управления. Свойства элемента, зависящие от элемента управления, предоставляются интерфейсом шаблона элемента управления.

Свойства автоматизации пользовательского интерфейса Майкрософт доступны только для чтения. Чтобы задать свойства элемента управления, вы должны использовать методы соответствующего шаблона элемента управления. Например, используйте [**иуиаутоматионскроллпаттерн:: Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) , чтобы изменить значения позиций прокручиваемого окна.

Для повышения производительности значения свойств элементов управления и шаблонов элементов управления могут быть кэшированы при извлечении элементов. Дополнительные сведения см. в разделе [кэширование свойств и шаблонов элементов управления автоматизации пользовательского интерфейса](uiauto-cachingforclients.md).

В этом разделе содержатся следующие подразделы.

-   [Идентификаторы свойств](#property-ids)
-   [Условия свойств](#property-conditions)
-   [Получение свойств](#retrieving-properties)
-   [Значения свойств по умолчанию](#default-property-values)
-   [См. также](#related-topics)

## <a name="property-ids"></a>Идентификаторы свойств

Идентификаторы свойств определены в UIAutomationClient. h. Они используются для указания свойств при оформлении подписки на события изменения свойств, извлечения значений свойств и конструирования условий свойств. Идентификаторы свойств также обозначают свойство, которое было изменено при вызове [**иуиаутоматионпропертичанжедевенсандлер:: хандлепропертичанжедевент**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) .

Список идентификаторов свойств модели автоматизации пользовательского интерфейса см. в разделе [идентификаторы свойств](uiauto-entry-propids.md).

## <a name="property-conditions"></a>Условия свойств

Идентификаторы свойств используются при конструировании объектов [**иуиаутоматионпропертикондитион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) , которые используются для поиска элементов автоматизации пользовательского интерфейса. Например, может потребоваться найти элемент с определенным именем или все включенные элементы управления. Каждое условие свойства указывает идентификатор свойства и значение, которым должно соответствовать свойство.

Дополнительные сведения см. в следующих справочных разделах.

-   [**Иуиаутоматион:: Креатепропертикондитион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [**Иуиаутоматион:: Креатепропертикондитионекс**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [**Иуиаутоматионелемент:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [**Иуиаутоматионелемент:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a>Получение свойств

Некоторые универсальные свойства и все свойства шаблона элемента управления доступны как свойства в интерфейсе шаблона [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) или элемента управления и могут извлекаться с помощью метода доступа, такого как [**Иуиаутоматионелемент:: куррентнаме**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) или [**качеддоккпоситион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).

Кроме того, любое текущее или кэшированное свойство (кроме свойств шаблона элемента управления) можно получить с помощью одного из следующих методов:

-   [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [**жеткуррентпропертивалуикс**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [**жеткачедпропертивалуе**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [**жеткачедпропертивалуикс**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

Эти методы обеспечивают немного более высокую производительность и доступ к полному спектру свойств. Однако значения возвращаются в структурах [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , тогда как методы доступа к отдельным свойствам приводят значение к соответствующему типу.

## <a name="default-property-values"></a>Значения свойств по умолчанию

Если поставщик автоматизации пользовательского интерфейса не реализует свойство, то модель автоматизации пользовательского интерфейса может предоставить значение по умолчанию. Например, если поставщик элемента управления не поддерживает свойство, идентифицируемое [**UIA \_ хелптекстпропертид**](uiauto-automation-element-propids.md), то модель автоматизации пользовательского интерфейса возвращает пустую строку. Аналогично, если поставщик не поддерживает свойство, идентифицируемое [**UIA \_ Исдоккпаттернаваилаблепропертид**](uiauto-control-pattern-availability-propids.md), модель автоматизации пользовательского интерфейса возвращает **значение false**.

Разница между [**иуиаутоматионелемент:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) и [**жеткуррентпропертивалуикс**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (и между аналогичными парами методов) заключается в том, что метод "ex" может указывать, что значение по умолчанию не возвращается. В этом случае возвращаемое значение является особой уникальной константой, указывающей, что свойство не поддерживается. При получении этого значения приложение может предоставить собственное значение или просто игнорировать свойство.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие сведения о свойствах автоматизированного пользовательского интерфейса](uiauto-propertiesoverview.md)
</dt> <dt>

[Идентификаторы свойств](uiauto-entry-propids.md)
</dt> </dl>

 

 