---
title: Библиотека элементов управления платформы Windows ленты
description: В разделах, содержащихся в этом разделе, описывается набор элементов управления, включенных в платформу Windows Ribbon. Перечисленные здесь элементы управления являются объектами пользовательского интерфейса на ленте, которые предоставляют функциональные возможности команды.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672359"
---
# <a name="windows-ribbon-framework-control-library"></a>Библиотека элементов управления платформы Windows ленты

В разделах, содержащихся в этом разделе, описывается набор элементов управления, включенных в платформу Windows Ribbon. Перечисленные здесь элементы управления являются объектами пользовательского интерфейса на ленте, которые предоставляют функциональные возможности команды.

-   [Введение](#introduction)
-   [Элементы управления](#windows-ribbon-framework-control-library)
    -   [Основные элементы управления](#basic-controls)
    -   [Контейнерные элементы управления](#container-controls)
    -   [Специализированные элементы управления](#specialized-controls)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

Платформа Ribbon состоит из таких компонентов, как [вкладки](windowsribbon-controls-tab.md) и [панель быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md), которые работают вместе, чтобы обеспечить широкие возможности пользовательского интерфейса. По отдельности эти компоненты предоставляют различные типы команд, чтобы предоставить клиентам организованную и предсказуемую работу в приложениях на ленте. Например, каждая вкладка содержит команды, связанные с созданием и обработкой конкретных частей содержимого в рабочей области приложения, в то время как [меню приложения](windowsribbon-controls-applicationmenu.md) предоставляет функциональные возможности, связанные с полным проектом, например весь документ, изображение или фильм.

Этот раздел содержит полный список элементов управления ленты и содержит краткое описание для каждого элемента управления со ссылками на более подробную документацию, где это возможно.

## <a name="the-controls"></a>Элементы управления

Платформа Ribbon состоит из двух [представлений](windowsribbon-reference-elements-view.md): представление [**ленты**](windowsribbon-element-ribbon.md) и представление [**контекстпопуп**](windowsribbon-element-contextpopup.md) . Каждое представление может содержать несколько компонентов, которые выступают в качестве контейнеров представления для всех элементов управления, которые визуализируются и управляются платформой.

В представлении [**ленты**](windowsribbon-element-ribbon.md) размещается элемент [**Аппликатионмену**](windowsribbon-element-applicationmenu.md) , элемент [**куиккакцесстулбар**](windowsribbon-element-quickaccesstoolbar.md) и панель команд ленты, а в представлении [**контекстпопуп**](windowsribbon-element-contextpopup.md) размещается элемент [**ContextMenu**](windowsribbon-element-contextmenu.md) , элемент [**минитулбар**](windowsribbon-element-minitoolbar.md) или оба этих элемента.

Каждый элемент управления платформы различает функциональные возможности, связанные с [**типом команды**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).

### <a name="basic-controls"></a>Основные элементы управления

Основные элементы управления состоят из одной или нескольких кнопок, которые можно вызывать одним щелчком мыши для выполнения простого действия.

> [!Note]  
> [**Счетчик**](windowsribbon-element-spinner.md) является исключением, так как содержит элемент управления "поле ввода".

 

В следующей таблице перечислены основные элементы управления в платформе Ribbon.



| Control                                                  | Элемент Markup                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [Кнопка](windowsribbon-controls-button.md)              | [**Переключатель**](windowsribbon-element-button.md)             |
| [Флажок](windowsribbon-controls-checkbox.md)         | [**Установка**](windowsribbon-element-checkbox.md)         |
| [Кнопка "Справка"](windowsribbon-controls-helpbutton.md)     | [**хелпбуттон**](windowsribbon-element-helpbutton.md)     |
| [Spinner](windowsribbon-controls-spinner.md)            | [**Spinner**](windowsribbon-element-spinner.md)           |
| [Выключатель](windowsribbon-controls-togglebutton.md) | [**ToggleButton**](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a>Контейнерные элементы управления

Контейнерные элементы управления состоят из групп элементов управления, меню, списков или коллекций элементов и команд.

Платформа различает два типа контейнеров: статический и динамический.

### <a name="static-containers"></a>Статические контейнеры

Статические контейнеры объявляются и заполняются вместе со всеми связанными ресурсами в файле разметки ленты. Эти элементы управления нельзя изменить во время выполнения.

К преимуществам статических элементов управления относятся следующие.

-   Быстрое создание прототипов. Статические элементы управления позволяют быстро создать макет Ribbon, похожий на окончательный дизайн ленты, для которого не требуется никакого сложного кода.
-   Простые изменения. Большинство элементов, атрибутов, ресурсов и макетов статических элементов управления могут быть изменены в разметке.
-   Единообразный пользовательский интерфейс. Хорошо спроектированные приложения предоставляют единообразный и стабильный пользовательский интерфейс, который позволяет избежать изменений в меню и списках во время выполнения.

В следующей таблице описаны статические элементы управления контейнера в платформе Ribbon.



| Control                                                        | Элемент Markup                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [Меню приложения](windowsribbon-controls-applicationmenu.md) | [**аппликатионмену**](windowsribbon-element-applicationmenu.md) |
| [Контекстное всплывающее окно](windowsribbon-controls-contextpopup.md)       | [**контекстпопуп**](windowsribbon-element-contextpopup.md)       |
| [Кнопка раскрывающегося списка](windowsribbon-controls-dropdownbutton.md)  | [**DropDownButton**](windowsribbon-element-dropdownbutton.md)   |
| [Группа](windowsribbon-controls-group.md)                      | [**Группа**](windowsribbon-element-group.md)                     |
| [Группа меню](windowsribbon-controls-menugroup.md)             | [**менуграуп**](windowsribbon-element-menugroup.md)             |
| [Разворачивающаяся кнопка](windowsribbon-controls-splitbutton.md)         | [**SplitButton**](windowsribbon-element-splitbutton.md)         |
| [TAB](windowsribbon-controls-tab.md)                          | [**TAB**](windowsribbon-element-tab.md)                         |
| [Группа вкладок](windowsribbon-controls-tabgroup.md)               | [**Группа вкладок**](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a>Динамические контейнеры

Динамические контейнеры объявляются в файле разметки ленты. Они имеют группу элементов или команд, которые создаются или изменяются во время выполнения.

Подкласс динамических контейнеров, называемых галереями, различается по реализации интерфейса [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) . Этот интерфейс позволяет элементу управления предоставлять свой элемент или список команд в виде коллекции, а также поддерживать обновления в зависимости от взаимодействия с пользователем и условий времени выполнения. Дополнительные сведения см. в разделе [Работа с галереями](ribbon-controls-galleries.md).

В следующей таблице перечислены динамические элементы управления контейнера в платформе Ribbon.



| Control                                                               | Элемент Markup                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [Поле со списком](windowsribbon-controls-combobox.md)                      | [**ComboBox**](windowsribbon-element-combobox.md)                     |
| [Раскрывающийся список](windowsribbon-controls-dropdowngallery.md)       | [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)       |
| [Коллекция на ленте](windowsribbon-controls-inribbongallery.md)       | [**инриббонгаллери**](windowsribbon-element-inribbongallery.md)       |
| [Панель быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md) | [**куиккакцесстулбар**](windowsribbon-element-quickaccesstoolbar.md) |
| [Недавние элементы](windowsribbon-controls-recentitems.md)                | [**рецентитемс**](windowsribbon-element-recentitems.md)               |
| [Коллекция разделенных кнопок](windowsribbon-controls-splitbuttongallery.md) | [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a>Специализированные элементы управления

Платформа Ribbon содержит ряд специализированных элементов управления для определенных функций пользовательского интерфейса.

В следующей таблице перечислены специализированные элементы управления в платформе Ribbon.



| Control                                                                  | Элемент Markup                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Выбор цвета для раскрывающегося списка](windowsribbon-controls-dropdowncolorpicker.md) | [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) |
| [Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)                   | [**фонтконтрол**](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные сведения о командах и элементах управления](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 