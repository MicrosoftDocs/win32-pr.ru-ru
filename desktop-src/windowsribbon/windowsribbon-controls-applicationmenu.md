---
title: Меню приложения
description: Меню приложение — это главное меню для приложения, которое реализует платформу Windows Ribbon.
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890660"
---
# <a name="application-menu"></a>Меню приложения

Меню приложение — это главное меню для приложения, которое реализует платформу Windows Ribbon.

-   [Введение](#introduction)
-   [Компоненты меню «приложение»](#components-of-the-application-menu)
    -   [Менуграуп меню приложения](#application-menu-menugroup)
-   [Изменение размера меню приложения](#sizing-the-application-menu)
-   [Свойства меню приложения](#application-menu-properties)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

Меню приложения состоит из элемента управления "Кнопка раскрывающегося списка", в котором отображается меню с командами, которые предоставляют функциональные возможности, связанные с полным проектом, например весь документ, изображение или фильм. К примерам относятся команды **New**, **Open**, **Save** и **Exit** .

На следующем снимке экрана показано меню приложения.

![снимок экрана: список "меню приложения" и "Недавние элементы" на ленте "Paint для Windows 7".](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a>Компоненты меню «приложение»

Меню приложение является обязательным элементом в любом приложении ленты. Точка входа в меню приложение — это отличительная кнопка, которая отображается в виде первого элемента в строке [табуляции](windowsribbon-controls-tab.md) , как показано на следующем снимке экрана.

> [!Note]  
> Windows 8 и более новые: изображение кнопки меню приложения изменилось на метка: **файл**. Не рекомендуется использовать файл в качестве метки для любой из вкладок.

 

![снимок экрана: кнопка меню "приложение" в приложении WordPad для Windows 7.](images/overviews/applicationmenu-button.png)

При нажатии этой кнопки отображается расширенное меню, которое отображается на следующем снимке экрана (меню приложения из WordPad для Windows 7).

![снимок экрана: меню меню приложения WordPad для Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> При нажатии кнопки меню приложение не оказывает влияния на набор вкладок. Вместо этого фокус попадает на меню.

 

Меню приложение содержит две панели: список команд, представленных одним или несколькими элементами [**менуграуп**](windowsribbon-element-menugroup.md) , и список [последних элементов](windowsribbon-controls-recentitems.md) , представленный элементом [**аппликатионмену. рецентитемс**](windowsribbon-element-applicationmenu-recentitems.md) .

### <a name="application-menu-menugroup"></a>Менуграуп меню приложения

Элемент [**аппликатионмену**](windowsribbon-element-applicationmenu.md) должен содержать по крайней мере один дочерний элемент [**менуграуп**](windowsribbon-element-menugroup.md) , предоставляющий список команд уровня приложения. Если объявлено несколько элементов **менуграуп** , то между группами отображается разделительная линия, как показано на следующем снимке экрана.

![снимок экрана: меню приложения менуграуп.](images/overviews/applicationmenu-menugroup.png)

Ниже приведен список ограничений для элемента [**Менуграуп**](windowsribbon-element-menugroup.md) меню приложения.

-   Все элементы [**менуграуп**](windowsribbon-element-menugroup.md) должны быть объявлены с атрибутом *класса* со значением `MajorItems` .
-   Меню приложения  [**менуграуп**](windowsribbon-element-menugroup.md) поддерживает только [кнопку](windowsribbon-controls-button.md), [выключатель](windowsribbon-controls-togglebutton.md), [кнопку](windowsribbon-controls-dropdownbutton.md)с раскрывающимся списком, [разворачивающуюся кнопку](windowsribbon-controls-splitbutton.md), [раскрывающийся список](windowsribbon-controls-dropdowngallery.md)и элементы управления [коллекции разворачивающихся кнопок](windowsribbon-controls-splitbuttongallery.md) .
    > \[! Существенно\]  
    > Коллекции команд — это единственный тип коллекции, поддерживаемый в меню приложения. Дополнительные сведения об элементах управления галереи см. в разделе [Работа с галереями](./ribbon-controls-galleries.md).

     

При использовании [кнопки](windowsribbon-controls-button.md) или [выключателя](windowsribbon-controls-togglebutton.md) в [**менуграуп**](windowsribbon-element-menugroup.md)значение [**Command. Лабелтитле**](windowsribbon-element-command-labeltitle.md) отображается в меню, а значения [**Command. тултиптитле**](windowsribbon-element-command-tooltiptitle.md) и [**Command. тултипдескриптион**](windowsribbon-element-command-tooltipdescription.md) отображаются в виде подсказки, как показано на следующем снимке экрана.

![снимок экрана элемента управления "Кнопка" в меню "приложение".](images/overviews/applicationmenu-menubutton.png)

Если в меню приложения используется кнопка с раскрывающимся [списком](windowsribbon-controls-dropdownbutton.md), [разворачивающаяся кнопка](windowsribbon-controls-splitbutton.md), [раскрывающийся список](windowsribbon-controls-dropdowngallery.md)или [коллекция разворачивающихся кнопок](windowsribbon-controls-splitbuttongallery.md) , то часть меню отображается как всплывающее окно, которое охватывает и скрывает панель « **недавние элементы** ».

Для элементов управления " [разворачивающаяся кнопка](windowsribbon-controls-splitbutton.md) " и ["](windowsribbon-controls-dropdownbutton.md) раскрывающийся список" значение [**Command. лабелдескриптион**](windowsribbon-element-command-labeldescription.md) отображается встроенным во всплывающем меню, чтобы визуально помочь пользователям в обнаружении функциональных возможностей команды. Отображаемое значение **Command. лабелдескриптион** программно разбивается на две строки, и предпринимается попытка точно вписать значение в область **недавние элементы** ниже. Если значение **Command. лабелдескриптион** не умещается, всплывающее окно будет развернуто в соответствии с наибольшим значением [**Command. Comment**](windowsribbon-element-command-comment.md) в [**менуграуп**](windowsribbon-element-menugroup.md).

На следующем снимке экрана показаны эти режимы работы во всплывающем окне [разворачивающейся кнопки](windowsribbon-controls-splitbutton.md) .

![снимок экрана всплывающего окна элемента управления "список" в меню приложения.](images/overviews/applicationmenu-menuflyout.png)

С помощью раскрывающейся [коллекции](windowsribbon-controls-dropdowngallery.md) и [коллекции разделенных кнопок](windowsribbon-controls-splitbuttongallery.md)отображаются только метка и изображение.

## <a name="sizing-the-application-menu"></a>Изменение размера меню приложения

Размер меню приложения обрабатывается платформой Ribbon. Если указаны очень длинные строки для значения [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или [**Command. лабелдескриптион**](windowsribbon-element-command-labeldescription.md)или используется длинный список команд, меню будет масштабироваться в соответствии с содержимым. Некоторые формы коррекции включают в себя увеличение размера всплывающих списков или панелей меню, а также добавление средств просмотра панорамы при необходимости прокрутки.

## <a name="application-menu-properties"></a>Свойства меню приложения

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления меню приложения.

Как правило, свойство меню приложения обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается, а обновления свойств определяются методом обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется, и приложение не запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, платформа требует свойство при активации вкладки и отображении элемента управления в ленте или при отображении подсказки.



| Ключ свойства                                                                                     | Примечания                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [UI \_ PKEY \_ тултипдескриптион](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Может обновляться только через недействительность. |
| [UI \_ PKEY \_ тултиптитле](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Может обновляться только через недействительность. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Библиотека элементов управления платформы Windows ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Аппликатионмену, элемент разметки**](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 