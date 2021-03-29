---
title: Рекомендации по реализации IAccessibleEx
description: Ядро автоматизации пользовательского интерфейса Майкрософт может извлекать все свойства Active Accessibility Microsoft для любого доступного объекта, предоставляемого сервером через интерфейс IAccessible.
ms.assetid: d047127c-1be2-4f34-bb97-330b5509ca0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82403a51e4848142a26194a98dce3922619b06f4
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "103785533"
---
# <a name="iaccessibleex-implementation-guidelines"></a>Рекомендации по реализации IAccessibleEx

Ядро автоматизации пользовательского интерфейса Майкрософт может извлекать все свойства Active Accessibility Microsoft для любого доступного объекта, предоставляемого сервером через интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . При реализации [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)необходимо предоставить только те аспекты функциональности пользовательского интерфейса, которые в противном случае не могут быть предоставлены через существующие свойства Microsoft Active Accessibility. В этом разделе определяются свойства автоматизации пользовательского интерфейса и шаблоны элементов управления, которые представляют функциональные возможности пользовательского интерфейса, не имеющие аналога в Microsoft Active Accessibility — они являются свойствами и шаблонами элементов управления, которые можно предоставить в реализации **IAccessibleEx** .

В этом разделе содержатся следующие подразделы.

-   [Свойства](#properties)
-   [Шаблоны элементов управления](#control-patterns)
-   [Виневентс для событий изменения свойств модели автоматизации пользовательского интерфейса](#winevents-for-ui-automation-property-changed-events)
-   [См. также](#related-topics)

## <a name="properties"></a>Свойства

Следующие свойства модели автоматизации пользовательского интерфейса не перекрываются с функциональностью Microsoft Active Accessibility. Их можно использовать в реализации [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) :

-   ариапропертиес
-   ариароле
-   AutomationId
-   ClassName
-   кликкаблепоинт
-   контроллерфор
-   culture
-   DescribedBy
-   фловсто
-   FrameworkId
-   исконтентелемент
-   исконтролелемент
-   исдатавалидфорформ
-   исрекуиредфорформ
-   ItemStatus
-   ItemType
-   LabeledBy
-   локализедконтролтипе
-   Orientation

Несмотря на то что свойства модели автоматизации пользовательского интерфейса Акцелераторкэй и AccessKey перекрываются со свойством Акккэйбоардшорткут Microsoft Active Accessibility, их все еще можно использовать в реализации [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для элементов управления, имеющих как ключ доступа, так и сочетание клавиш. Аналогичным образом свойство модели автоматизации пользовательского интерфейса ControlType перекрывается со свойством Microsoft Active Accessibility Аккроле, но его по-прежнему можно использовать в реализации **IAccessibleEx** , чтобы определить более конкретную роль для элемента управления.

Поскольку следующие свойства элементов модели автоматизации пользовательского интерфейса уже охвачены свойствами Microsoft Active Accessibility, их не нужно использовать в реализации [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .



| Свойство модели автоматизации пользовательского интерфейса | Эквивалент Microsoft Active Accessibility                                                                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| баундингректангле      | акклокатион                                                                                                                                                                   |
| хаскэйбоардфокус       | Аккстате, [ **Система состояний, \_ \_ нацеленная** на](object-state-constants.md)                                                                                       |
| IsEnabled              | Аккстате, [ **\_ Система состояний \_ недоступна**](object-state-constants.md)                                                                               |
| искэйбоардфокусабле    | Аккстате, [ **\_ \_ фокус системы состояния**](object-state-constants.md)                                                                                   |
| IsPassword             | Аккстате, [ **\_ \_ защищенная система состояний**](object-state-constants.md)                                                                                   |
| HelpText               | акчелп                                                                                                                                                                       |
| Имя                   | аккнаме                                                                                                                                                                       |
| нативевиндовхандле     | [**виндовфромакцессиблеобжект**](/windows/desktop/api/Oleacc/nf-oleacc-windowfromaccessibleobject)                                                                                                              |
| исоффскрин            | аккстате, [**\_ \_ невидимая**](object-state-constants.md)система состояния в системе состояния / [**\_ \_**](object-state-constants.md) |
| ProcessId              | Предоставлено ядром автоматизации пользовательского интерфейса                                                                                                                                                |



 

Для любого неподдерживаемого свойства модели автоматизации пользовательского интерфейса ваша реализация метода [**иравелементпровидерсимпле:: жетпропертивалуе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) должна задавать для параметра *претвал* значение VT \_ Empty и возвращать значение S \_ ОК. Возврат [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) может привести к удалению сопоставления по умолчанию для соответствующего свойства прокси MSAA-to-UIA.

## <a name="control-patterns"></a>Шаблоны элементов управления

Следующие шаблоны элементов управления модели автоматизации пользовательского интерфейса не перекрываются с функциональностью Microsoft Active Accessibility. Их можно использовать в реализации [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) :

-   Dock
-   ExpandCollapse
-   Макет Grid
-   GridItem
-   MultipleView
-   RangeValue
-   Scroll
-   ScrollItem
-   SynchronizedInput
-   Таблица
-   TableItem
-   Преобразование

Для шаблонов элементов управления RangeValue и Transform некоторые методы перекрываются между шаблоном элемента управления модели автоматизации пользовательского интерфейса и методами Microsoft Active Accessibility. В этих случаях оба должны быть реализованы. Например, Active Accessibility оба метода [**IAccessible:: Get \_ Акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) и [**IAccessible::p UT \_ акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue) должны быть реализованы, как и методы автоматизации пользовательского интерфейса [**IRangeValueProvider:: value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) и [**IRangeValueProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue) . На внутреннем уровне реализация может совместно использовать код. Это требование для реализации обоих наборов позволяет избежать частичной реализации интерфейса шаблона, сохраняя возможность использования интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) существующими клиентами Microsoft Active Accessibility.

Следующие шаблоны элементов управления модели автоматизации пользовательского интерфейса не требуются, если элемент управления имеет одну из ролей, описанных ниже. в противном случае они должны быть явно поддерживаются, если это уместно.



| Шаблон элемента управления модели автоматизации пользовательского интерфейса | Роль Microsoft Active Accessibility                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InvokePattern                 | [**Роль \_ Системные \_ кнопки**](object-roles.md), [**элемент \_ \_ MenuItem**](object-roles.md), система [**ролей \_ \_ буттондропдовн**](object-roles.md), [**\_ \_ SPLITBUTTON системы роли**](object-roles.md), а также любая другая роль, где значение свойства аккдефаултактион не равно **null**. |
| селектионитемпаттерн          | [**Роль \_ компонент \_ ListItem**](object-roles.md)системы, [ **\_ \_ переключатель системы роли**](object-roles.md)                                                                                                                                                                                                                                                 |
| селектионпаттерн              | [**\_список систем \_ ролей**](object-roles.md)                                                                                                                                                                                                                                                                                                                                    |
| тогглепаттерн                 | [**\_чеккбуттон системы \_ ролей**](object-roles.md)                                                                                                                                                                                                                                                                                                                      |
| ValuePattern                  | [**Роль \_ СИСТЕМНЫЙ \_ текст**](object-roles.md) (если он не доступен только для чтения), [**компонент \_ \_ PROGRESSBAR системы роли**](object-roles.md), [**\_ \_ поле со списком системы роли**](object-roles.md)и другие роли, если значение свойства акквалуе не равно **null**.                                                                            |
| WindowPattern                 | Автоматически поддерживается в Microsoft Win32 **HWND** верхнего уровня.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="winevents-for-ui-automation-property-changed-events"></a>Виневентс для событий изменения свойств модели автоматизации пользовательского интерфейса

В дополнение к событиям, определенным для [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), также определяются следующие идентификаторы событий, которые могут использоваться с реализацией [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) в качестве событий изменения свойств для соответствующих свойств автоматизации пользовательского интерфейса. Они используют тот же механизм, что и события, определенные для **IAccessible**. Дополнительные сведения см. в разделе [виневентс](winevents-infrastructure.md).



| Идентификатор WinEvent для реализаций IAccessibleEx                                                                                              | Связанный идентификатор WinEvent из Microsoft Active Accessibility                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**UIA \_ ариапропертиеспропертид**](uiauto-automation-element-propids.md)                                    | Нет                                                                                   |
| [**UIA \_ ариаролепропертид**](uiauto-automation-element-propids.md)                                                | Нет                                                                                   |
| [**UIA \_ контроллерфорпропертид**](uiauto-automation-element-propids.md)                                      | Нет                                                                                   |
| [**UIA \_ дескрибедбипропертид**](uiauto-automation-element-propids.md)                                          | Нет                                                                                   |
| [**UIA \_ експандколлапсикспандколлапсестатепропертид**](uiauto-control-pattern-propids.md) | [**\_STATECHANGE объекта \_ события**](event-constants.md)         |
| [**UIA \_ фловстопропертид**](uiauto-automation-element-propids.md)                                                  | Нет                                                                                   |
| [**UIA \_ инпутдискардедевентид**](uiauto-event-ids.md)                                                           | Нет                                                                                   |
| [**UIA \_ инпутреачедосерелементевентид**](uiauto-event-ids.md)                                       | Нет                                                                                   |
| [**UIA \_ инпутреачедтаржетевентид**](uiauto-event-ids.md)                                                   | Нет                                                                                   |
| [**UIA \_ исдатавалидфорформпропертид**](uiauto-automation-element-propids.md)                            | Нет                                                                                   |
| [**UIA \_ исенабледпропертид**](uiauto-automation-element-propids.md)                                              | [**\_STATECHANGE объекта \_ события**](event-constants.md)         |
| [**UIA \_ итемстатуспропертид**](uiauto-automation-element-propids.md)                                            | Нет                                                                                   |
| [**UIA \_ мултиплевиевкуррентвиевпропертид**](uiauto-control-pattern-propids.md)                     | Нет                                                                                   |
| [**UIA \_ скроллхоризонталлискроллаблепропертид**](uiauto-control-pattern-propids.md)           | Нет                                                                                   |
| [**UIA \_ скроллхоризонталскроллперцентпропертид**](uiauto-control-pattern-propids.md)         | [**\_контентскроллед объекта \_ события**](event-constants.md) |
| [**UIA \_ скроллхоризонталвиевсизепропертид**](uiauto-control-pattern-propids.md)                   | Нет                                                                                   |
| [**UIA \_ скроллвертикаллискроллаблепропертид**](uiauto-control-pattern-propids.md)               | Нет                                                                                   |
| [**UIA \_ скроллвертикалскроллперцентпропертид**](uiauto-control-pattern-propids.md)             | [**\_контентскроллед объекта \_ события**](event-constants.md) |
| [**UIA \_ скроллвертикалвиевсизепропертид**](uiauto-control-pattern-propids.md)                       | Нет                                                                                   |
| [**UIA \_ тогглетогглестатепропертид**](uiauto-control-pattern-propids.md)                                 | [**\_STATECHANGE объекта \_ события**](event-constants.md)         |



 

Для событий выше, которые имеют \_ значение объекта события \_ , указанное после них, и реализация [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) должна вызвать это событие в дополнение к перечисленному событию Changed. Это позволяет существующему клиентскому коду **IAccessibleEx** продолжать работу, а более детализированные сведения о событиях — заинтересованным клиентам.

## <a name="related-topics"></a>См. также

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Интерфейс IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




