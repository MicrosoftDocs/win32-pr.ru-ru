---
title: Приложение G Active Accessibility Bridge в модель автоматизации пользовательского интерфейса
description: Это приложение содержит сведения о Microsoft Active Accessibility Bridge.
ms.assetid: f19036c7-5a18-4faa-a98d-564e5e63a94f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5fdc1ebc4d6e17781e383463974f78bb9334aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681438"
---
# <a name="appendix-g-active-accessibility-bridge-to-ui-automation"></a>Приложение ж. Active Accessibility Bridge в модель автоматизации пользовательского интерфейса

Это приложение содержит сведения о Microsoft Active Accessibility Bridge. Мост Active Accessibility позволяет приложениям, реализующим Microsoft Active Accessibility, получать доступ к приложениям, реализующим автоматизацию пользовательского интерфейса Майкрософт. Благодаря объединению Microsoft Active Accessibility и модели автоматизации пользовательского интерфейса, клиенты на основе Microsoft Active Accessibility, такие как скринреадер в Windows XP, могут программно взаимодействовать с поставщиками автоматизации пользовательского интерфейса, основанными на автоматизации UI, например с приложением Windows Presentation Foundation (WPF). Он является частью собственного базового API модели автоматизации пользовательского интерфейса (UIAutomationCore.dll).

Active Accessibility мост сопоставляет свойства и события модели автоматизации пользовательского интерфейса со свойствами Microsoft Active Accessibility. В следующих таблицах методы и свойства интерфейса Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) сопоставляются с АВТОМАТИЗАЦИЕЙ пользовательского интерфейса. Используйте эти таблицы, чтобы определить необходимые методы написания кода для разработки клиента на основе Microsoft Active Accessibility.

### <a name="navigation-and-hierarchy-properties"></a>Свойства навигации и иерархии



| IAccessible, свойство                                                     | Свойство модели автоматизации пользовательского интерфейса          |
|--------------------------------------------------------------------------|---------------------------------|
| [**получить \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Не реализовано                 |
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Производный от дерева модели автоматизации пользовательского интерфейса |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Производный от дерева модели автоматизации пользовательского интерфейса |
| [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)              | Не реализовано                 |



 

### <a name="descriptive-properties-and-methods"></a>Описательные свойства и методы



| IAccessible                                                                          | Автоматизация пользовательского интерфейса                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)            | Дополнительные сведения см. в разделе Типы элементов управления и таблица Аккроле.                                                                                                                                                                                                                                                                     |
| [**получить \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Дополнительные сведения см. в разделе Типы элементов управления и таблица Аккроле.                                                                                                                                                                                                                                                                     |
| [**получить \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Акцесскэйпропертйор Акцелераторкэйпроперти; При наличии обоих типов Акцесскэйпроперти имеет приоритет.                                                                                                                                                                                                                         |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | NameProperty                                                                                                                                                                                                                                                                                                             |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Контролтипепроперти. Дополнительные сведения см. в разделе Типы элементов управления и таблица Аккроле.                                                                                                                                                                                                                                                |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Дополнительные сведения см. в разделе Типы элементов управления и таблица Аккроле.                                                                                                                                                                                                                                                                     |
| [**получить \_ акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | Валуепроперти; поддерживается для типов элементов управления, поддерживающих шаблон элемента управления [value](uiauto-implementingvalue.md) или шаблон элемента управления [RangeValue](uiauto-implementingrangevalue.md) . Значения RangeValue согласуются с поведением Microsoft Active Accessibility (от 0 до 100). Элементы Value используют строку. |
| [**разместить \_ акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)                       | Валуепроперти; поддерживается для типов элементов управления, которые поддерживают шаблон элемента управления [value](uiauto-implementingvalue.md) или шаблон элемента управления [RangeValue](uiauto-implementingrangevalue.md)                                                                                                                                      |
| [**получить \_ акчелп**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | хелптекстпроперти                                                                                                                                                                                                                                                                                                         |
| [**получить \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Не реализовано                                                                                                                                                                                                                                                                                                          |
| [**получить \_ акчелптопик**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | Не реализовано                                                                                                                                                                                                                                                                                                          |



 

### <a name="control-types-and-accrole"></a>Типы элементов управления и Аккроле

Роль Microsoft Active Accessibility по умолчанию [**— \_ \_ клиент системы роли**](object-roles.md). Если для типа элемента управления не найдено действие по умолчанию, то Active Accessibility Bridge также будет использовать следующие доступные шаблоны элементов управления: [Invoke](uiauto-implementinginvoke.md), [ExpandCollapse](uiauto-implementingexpandcollapse.md)и [Toggle](uiauto-implementingtoggle.md). Например, элемент управления GroupBox не имеет действия по умолчанию. Если он поддерживает ExpandCollapse, то мост Active Accessibility будет использовать его для действия по умолчанию.



| Тип элемента управления модели автоматизации пользовательского интерфейса                              | аккроле                                                                     | Действие по умолчанию                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| [Кнопка](uiauto-supportbuttoncontroltype.md)           | [**\_кнопка системы \_ роли**](object-roles.md)     | Сочетание клавиш                                                    |
| [Календар](uiauto-supportcalendarcontroltype.md)       | [**\_клиент системы \_ роли**](object-roles.md)             | Нет                                                     |
| [CheckBox](uiauto-supportcheckboxcontroltype.md)       | [**\_чеккбуттон системы \_ ролей**](object-roles.md)   | Установить или снять флажок (переключатель)                                   |
| [ComboBox](uiauto-supportcomboboxcontroltype.md)       | [**\_ \_ поле со списком для системы роли**](object-roles.md)         | Нет                                                     |
| Особые настройки                                                  | [**\_клиент системы \_ роли**](object-roles.md)             | Нет                                                     |
| [DataGrid](uiauto-supportdatagridcontroltype.md)       | [**\_список систем \_ ролей**](object-roles.md)                 | Нет                                                     |
| [DataItem](uiauto-supportdataitemcontroltype.md)       | [**\_ListItem системы \_ роли**](object-roles.md)         | Нет                                                     |
| [Document](uiauto-supportdocumentcontroltype.md)       | [**\_документ системы \_ роли**](object-roles.md)         | Нет                                                     |
| [Правка](uiauto-supporteditcontroltype.md)               | [**\_системный \_ текст роли**](object-roles.md)                 | Нет                                                     |
| [Группа](uiauto-supportgroupcontroltype.md)             | [**\_ \_ группирование системы ролей**](object-roles.md)         | Нет                                                     |
| [Header](uiauto-supportheadercontroltype.md)           | [**\_список систем \_ ролей**](object-roles.md)                 | Нет                                                     |
| [HeaderItem](uiauto-supportheaderitemcontroltype.md)   | [**\_колумнхеадер системы \_ ролей**](object-roles.md) | Щелкните                                                    |
| [Гиперссылка](uiauto-supporthyperlinkcontroltype.md)     | [**\_ссылка на систему роли \_**](object-roles.md)                 | Переход (сопоставления для вызова)                                    |
| [Изображение](uiauto-supportimagecontroltype.md)             | [**\_график системы \_ роли**](object-roles.md)           | Нет                                                     |
| [Список](uiauto-supportlistcontroltype.md)               | [**\_список систем \_ ролей**](object-roles.md)                 | Нет                                                     |
| [ListItem](uiauto-supportlistitemcontroltype.md)       | [**\_ListItem системы \_ роли**](object-roles.md)         | Дважды щелкните                                             |
| [Меню](uiauto-supportmenucontroltype.md)               | [**\_менупопуп системы \_ ролей**](object-roles.md)       | Нет                                                     |
| [MenuBar](uiauto-supportmenubarcontroltype.md)         | [**\_ \_ строка подменю системы ролей**](object-roles.md)           | Нет                                                     |
| [MenuItem](uiauto-supportmenuitemcontroltype.md)       | [**\_ \_ пункт MenuItem системы роли**](object-roles.md)         | Выполнить или открыть/закрыть для пунктов меню, имеющих дочерние элементы. |
| [Панель](uiauto-supportpanecontroltype.md)               | [**\_область системы \_ роли**](object-roles.md)                 | Нет                                                     |
| [ProgressBar](uiauto-supportprogressbarcontroltype.md) | [**компонент \_ PROGRESSBAR системы ролей \_**](object-roles.md)   | Нет                                                     |
| [RadioButton](uiauto-supportradiobuttoncontroltype.md) | [**\_переключатель системы \_ роли**](object-roles.md)   | службы "Функции Azure"                                                    |
| [Элемента](uiauto-supportscrollbarcontroltype.md)     | [**\_ \_ полоса прокрутки системы роли**](object-roles.md)       | Нет                                                     |
| [Ползунок](uiauto-supportslidercontroltype.md)           | [**\_ \_ ползунок системы роли**](object-roles.md)             | Нет                                                     |
| [Spinner](uiauto-supportspinnercontroltype.md)         | [**\_спинбуттон системы \_ ролей**](object-roles.md)     | Нет                                                     |
| [SplitButton](uiauto-supportsplitbuttoncontroltype.md) | [**\_SPLITBUTTON системы \_ ролей**](object-roles.md)   | Нет                                                     |
| [StatusBar](uiauto-supportstatusbarcontroltype.md)     | [**\_системный \_ StatusBar для роли**](object-roles.md)       | Нет                                                     |
| [TAB](uiauto-supporttabcontroltype.md)                 | [**\_пажетаблист системы \_ ролей**](object-roles.md)   | Нет                                                     |
| [TabItem](uiauto-supporttabitemcontroltype.md)         | [**\_пажетаб системы \_ ролей**](object-roles.md)           | Коммутатор                                                   |
| [Таблица](uiauto-supporttablecontroltype.md)             | [**\_системная \_ Таблица ролей**](object-roles.md)               | Нет                                                     |
| [Text](uiauto-supporttextcontroltype.md)               | [**\_статиктекст системы \_ ролей**](object-roles.md)     | Нет                                                     |
| [Типа](uiauto-supportthumbcontroltype.md)             | [**\_индикатор системы \_ роли**](object-roles.md)       | Нет                                                     |
| [TitleBar](uiauto-supporttitlebarcontroltype.md)       | [**\_заголовок системы \_ роли**](object-roles.md)         | Нет                                                     |
| [Панелей](uiauto-supporttoolbarcontroltype.md)         | [**\_ \_ панель инструментов системы роли**](object-roles.md)           | Нет                                                     |
| [ToolTip](uiauto-supporttooltipcontroltype.md)         | [**\_ \_ всплывающая подсказка системы роли**](object-roles.md)           | Нет                                                     |
| [Дерево](uiauto-supporttreecontroltype.md)               | [**\_Структура системы \_ роли**](object-roles.md)           | Нет                                                     |
| [TreeItem](uiauto-supporttreeitemcontroltype.md)       | [**\_аутлинеитем системы \_ ролей**](object-roles.md)   | Развернуть или свернуть                                       |
| [Окно](uiauto-supportwindowcontroltype.md)           | [**\_окно системы \_ роли**](object-roles.md)             | Нет                                                     |



 

### <a name="ui-automation-properties-and-accstate"></a>Свойства модели автоматизации пользовательского интерфейса и Аккстате



| аккстате                                                                                      | Свойство модели автоматизации пользовательского интерфейса                                                                                                                                                        | Изменение состояния триггеров |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [**\_Система состояний \_ проверена**](object-state-constants.md)                 | Для ControlType = "CheckBox" используйте Тогглестате. on. Для "RadioButton" используйте [ **селектионитемпаттерн:: SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected) | Да                   |
| [**Система состояний с \_ \_ фокусом**](object-state-constants.md)             | искэйбоардфокусаблепроперти                                                                                                                                                   | Нет                    |
| [**Система состояний, \_ \_ нацеленная на**](object-state-constants.md)                 | хаскэйбоардфокуспроперти                                                                                                                                                      | Нет                    |
| [**\_Система состояний \_ защищена**](object-state-constants.md)             | испассвордпроперти                                                                                                                                                            | Нет                    |
| [**Система состояний, \_ \_ только для чтения**](object-state-constants.md)               | Исреадонлипроперти (шаблон элемента управления Value и шаблон элемента управления RangeValue)                                                                                                     | Нет                    |
| [**\_Система состояний \_ недоступна**](object-state-constants.md)         | исенабледпроперти                                                                                                                                                             | Да                   |
| [**\_системное состояние \_ связано**](object-state-constants.md)                   | Контролтипепроперти = "гиперссылка"                                                                                                                                             | Нет                    |
| [**\_Выбор системы \_ состояния**](object-state-constants.md)           | Селектионитемпаттерн поддерживается                                                                                                                                             | Нет                    |
| [**\_ \_ выбранная система состояний**](object-state-constants.md)               | Исселектедпроперти (шаблон элемента управления SelectionItem)                                                                                                                            | Нет                    |
| [**\_Система состояний \_ свернута**](object-state-constants.md)             | ExpandCollapseState = свернутый                                                                                                                                               | Да                   |
| [**\_Система состояний \_ развернута**](object-state-constants.md)               | ExpandCollapseState = развернутый или Партиаллекспандед                                                                                                                           | Да                   |
| [**\_хаспопуп системы \_ состояний**](object-state-constants.md)               | Элементы меню, поддерживающие развертывание/свертывание                                                                                                                                       | Нет                    |
| [**\_ \_ смешанная система состояний**](object-state-constants.md)                     | Тогглестате = неопределенный                                                                                                                                                   | Нет                    |
| [**\_немалым системы \_ состояний**](object-state-constants.md)               | [**Иуиаутоматионтрансформпаттерн:: Канресизе**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize)                                                                     | Нет                    |
| [**\_ \_ перемещаемая система состояний**](object-state-constants.md)               | [**Иуиаутоматионтрансформпаттерн:: Канмове**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove)                                                                         | Нет                    |
| [**\_МНОГОвыборочная система состояний \_**](object-state-constants.md) | [**Иуиаутоматионселектионпаттерн:: Канселектмултипле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple)                                                     | Нет                    |



 

### <a name="selection-and-focus"></a>Выделение и фокус



| IAccessible                                                            | Автоматизация пользовательского интерфейса                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)         | [**Иуиаутоматион:: FocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)        |
| [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                | Дополнительные сведения см. в разделе Свойства автоматизации пользовательского интерфейса и таблице Аккселект Селфлагс.             |
| [**получить \_ аккселектион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) | [**Селектионпаттерн:: выделять**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) |



 

### <a name="ui-automation-properties-and-accselect-selflags"></a>Свойства модели автоматизации пользовательского интерфейса и Аккселект Селфлагс



| Аккселект Селфлагс                                                  | Свойство модели автоматизации пользовательского интерфейса                                                                                                         |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**СЕЛФЛАГ \_ None**](selflag.md)                       | Недоступно                                                                                                                  |
| СЕЛФЛАГ \_ такфокус                                                   | [**Иуиаутоматионелемент:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)                                                 |
| [**СЕЛФЛАГ \_ такеселектион**](selflag.md)     | [**Иуиаутоматионселектионитемпаттерн:: SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)                           |
| [**СЕЛФЛАГ \_ аддселектион**](selflag.md)       | [**Иуиаутоматионселектионитемпаттерн:: Аддтоселектион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)           |
| СЕЛФЛАГ \_ такеремовеселектион                                        | [**Иуиаутоматионселектионитемпаттерн:: Ремовефромселектион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) |
| [**СЕЛФЛАГ \_ екстендселектион**](selflag.md) | Недоступно                                                                                                                  |



 

### <a name="spatial-mapping"></a>Пространственное сопоставление



| IAccessible                                                 | Автоматизация пользовательского интерфейса                                                                                                                        |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) | баундингректанглепроперти                                                                                                            |
| [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)   | [**Иравелементпровидерфрагментрут:: Елементпровидерфромпоинт**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint) |



 

### <a name="events"></a>События



| System-Level константы событий                                                             | Автоматизация пользовательского интерфейса                                                                                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**\_менупопупстарт системы \_ событий**](event-constants.md)     | [**UIA \_ Менуопенедевентид**](uiauto-event-ids.md) (Примечание. необходимо проверить, является ли это всплывающим окном.) |
| [**\_менупопупенд системы \_ событий**](event-constants.md)         | [**UIA \_ менуклоседевентид**](uiauto-event-ids.md)                                                |
| [**\_менустарт системы \_ событий**](event-constants.md)               | [**UIA \_ менумодестартевентид**](uiauto-event-ids.md)                                          |
| [**\_менуенд системы \_ событий**](event-constants.md)                   | [**UIA \_ менумодиндевентид**](uiauto-event-ids.md)                                              |
| [**\_системный \_ звук события**](event-constants.md)                       |                                                                                                                         |
| [**\_системное \_ оповещение о событиях**](event-constants.md)                       |                                                                                                                         |
| [**\_каптурестарт системы \_ событий**](event-constants.md)         |                                                                                                                         |
| [**\_каптуринд системы \_ событий**](event-constants.md)             |                                                                                                                         |
| [**\_диалогстарт системы \_ событий**](event-constants.md)           |                                                                                                                         |
| [**\_диаложенд системы \_ событий**](event-constants.md)               |                                                                                                                         |
| [**\_мовесизестарт системы \_ событий**](event-constants.md)       |                                                                                                                         |
| [**\_мовесизинд системы \_ событий**](event-constants.md)           |                                                                                                                         |
| [**\_контексселпстарт системы \_ событий**](event-constants.md) |                                                                                                                         |
| [**\_контексселпенд системы \_ событий**](event-constants.md)     | Неприменимо                                                                                                            |
| [**\_драгдропстарт системы \_ событий**](event-constants.md)       |                                                                                                                         |
| [**\_драгдропенд системы \_ событий**](event-constants.md)           |                                                                                                                         |
| [**\_свитчстарт системы \_ событий**](event-constants.md)           | Неприменимо                                                                                                            |
| [**\_свитченд системы \_ событий**](event-constants.md)               | Неприменимо                                                                                                            |
| [**\_минимизестарт системы \_ событий**](event-constants.md)       |                                                                                                                         |
| [**\_минимизинд системы \_ событий**](event-constants.md)           |                                                                                                                         |
| [**\_ \_ передний план системы событий**](event-constants.md)             |                                                                                                                         |
| [**\_скроллингстарт системы \_ событий**](event-constants.md)     | Недоступно                                                                                                           |
| [**\_скроллинженд системы \_ событий**](event-constants.md)         | Недоступно                                                                                                           |



 



| Object-Level константы событий                                                           | Автоматизация пользовательского интерфейса                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_фокус объекта \_ события**](event-constants.md)                     | аутоматионфокусчанжедевент                                                            |
| [**\_валуечанже объекта \_ события**](event-constants.md)         | Валуепроперти (шаблон элемента управления Value и шаблон элемента управления RangeValue)                   |
| [**\_Выбор объектов \_ событий**](event-constants.md)             | Елементселектедевент (шаблон элемента управления SelectionItem)                                   |
| [**\_селектионадд объекта \_ события**](event-constants.md)       | Елементаддедтоселектионевент (шаблон элемента управления SelectionItem)                           |
| [**\_селектионремове объекта \_ события**](event-constants.md) | елементремоведфромселектионевент                                                       |
| [**\_селектионвисин объекта \_ события**](event-constants.md) | евентсселектионинвалидатедевент                                                        |
| [**\_STATECHANGE объекта \_ события**](event-constants.md)         | Сведения о состояниях, вызывающих изменение состояния, см. в разделе Свойства автоматизации пользовательского интерфейса и таблица Аккстате. |



 

 

 




