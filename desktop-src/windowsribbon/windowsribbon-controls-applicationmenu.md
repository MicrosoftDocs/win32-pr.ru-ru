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
# <a name="application-menu"></a><span data-ttu-id="8ea5a-103">Меню приложения</span><span class="sxs-lookup"><span data-stu-id="8ea5a-103">Application Menu</span></span>

<span data-ttu-id="8ea5a-104">Меню приложение — это главное меню для приложения, которое реализует платформу Windows Ribbon.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-104">The Application Menu is the main menu for an application that implements the Windows Ribbon framework.</span></span>

-   [<span data-ttu-id="8ea5a-105">Введение</span><span class="sxs-lookup"><span data-stu-id="8ea5a-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="8ea5a-106">Компоненты меню «приложение»</span><span class="sxs-lookup"><span data-stu-id="8ea5a-106">Components of the Application Menu</span></span>](#components-of-the-application-menu)
    -   [<span data-ttu-id="8ea5a-107">Менуграуп меню приложения</span><span class="sxs-lookup"><span data-stu-id="8ea5a-107">Application Menu MenuGroup</span></span>](#application-menu-menugroup)
-   [<span data-ttu-id="8ea5a-108">Изменение размера меню приложения</span><span class="sxs-lookup"><span data-stu-id="8ea5a-108">Sizing the Application Menu</span></span>](#sizing-the-application-menu)
-   [<span data-ttu-id="8ea5a-109">Свойства меню приложения</span><span class="sxs-lookup"><span data-stu-id="8ea5a-109">Application Menu Properties</span></span>](#application-menu-properties)
-   [<span data-ttu-id="8ea5a-110">См. также</span><span class="sxs-lookup"><span data-stu-id="8ea5a-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="8ea5a-111">Введение</span><span class="sxs-lookup"><span data-stu-id="8ea5a-111">Introduction</span></span>

<span data-ttu-id="8ea5a-112">Меню приложения состоит из элемента управления "Кнопка раскрывающегося списка", в котором отображается меню с командами, которые предоставляют функциональные возможности, связанные с полным проектом, например весь документ, изображение или фильм.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-112">The Application Menu is composed of a drop-down button control that displays a menu containing Commands that expose functionality related to a complete project, such as an entire document, picture, or movie.</span></span> <span data-ttu-id="8ea5a-113">К примерам относятся команды **New**, **Open**, **Save** и **Exit** .</span><span class="sxs-lookup"><span data-stu-id="8ea5a-113">Examples include the **New**, **Open**, **Save**, and **Exit** Commands.</span></span>

<span data-ttu-id="8ea5a-114">На следующем снимке экрана показано меню приложения.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-114">The following screen shot illustrates the Application Menu.</span></span>

![снимок экрана: список "меню приложения" и "Недавние элементы" на ленте "Paint для Windows 7".](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a><span data-ttu-id="8ea5a-116">Компоненты меню «приложение»</span><span class="sxs-lookup"><span data-stu-id="8ea5a-116">Components of the Application Menu</span></span>

<span data-ttu-id="8ea5a-117">Меню приложение является обязательным элементом в любом приложении ленты.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-117">The Application Menu is a mandatory element in any Ribbon application.</span></span> <span data-ttu-id="8ea5a-118">Точка входа в меню приложение — это отличительная кнопка, которая отображается в виде первого элемента в строке [табуляции](windowsribbon-controls-tab.md) , как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-118">The entry point into the Application Menu is a distinctive button that appears as the first item in the [Tab](windowsribbon-controls-tab.md) row, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="8ea5a-119">Windows 8 и более новые: изображение кнопки меню приложения изменилось на метка: **файл**.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-119">Windows 8 and newer: Application Menu button image changed to label: **File**.</span></span> <span data-ttu-id="8ea5a-120">Не рекомендуется использовать файл в качестве метки для любой из вкладок.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-120">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

![снимок экрана: кнопка меню "приложение" в приложении WordPad для Windows 7.](images/overviews/applicationmenu-button.png)

<span data-ttu-id="8ea5a-122">При нажатии этой кнопки отображается расширенное меню, которое отображается на следующем снимке экрана (меню приложения из WordPad для Windows 7).</span><span class="sxs-lookup"><span data-stu-id="8ea5a-122">When clicked, this button displays the rich menu that is shown in the following screen shot (the Application Menu from WordPad for Windows 7).</span></span>

![снимок экрана: меню меню приложения WordPad для Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> <span data-ttu-id="8ea5a-124">При нажатии кнопки меню приложение не оказывает влияния на набор вкладок. Вместо этого фокус попадает на меню.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-124">There is no impact on the tab set when the Application Menu button is clicked; instead, the focus enters the menu.</span></span>

 

<span data-ttu-id="8ea5a-125">Меню приложение содержит две панели: список команд, представленных одним или несколькими элементами [**менуграуп**](windowsribbon-element-menugroup.md) , и список [последних элементов](windowsribbon-controls-recentitems.md) , представленный элементом [**аппликатионмену. рецентитемс**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea5a-125">The Application Menu contains two panes: a list of Commands represented by one or more [**MenuGroup**](windowsribbon-element-menugroup.md) elements, and a [Recent Items](windowsribbon-controls-recentitems.md) list represented by an [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

### <a name="application-menu-menugroup"></a><span data-ttu-id="8ea5a-126">Менуграуп меню приложения</span><span class="sxs-lookup"><span data-stu-id="8ea5a-126">Application Menu MenuGroup</span></span>

<span data-ttu-id="8ea5a-127">Элемент [**аппликатионмену**](windowsribbon-element-applicationmenu.md) должен содержать по крайней мере один дочерний элемент [**менуграуп**](windowsribbon-element-menugroup.md) , предоставляющий список команд уровня приложения.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-127">The [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element must contain at least one [**MenuGroup**](windowsribbon-element-menugroup.md) child element that exposes a list of application-level commands.</span></span> <span data-ttu-id="8ea5a-128">Если объявлено несколько элементов **менуграуп** , то между группами отображается разделительная линия, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-128">If multiple **MenuGroup** elements are declared, a divider line is drawn between the groups, as shown in the following screen shot.</span></span>

![снимок экрана: меню приложения менуграуп.](images/overviews/applicationmenu-menugroup.png)

<span data-ttu-id="8ea5a-130">Ниже приведен список ограничений для элемента [**Менуграуп**](windowsribbon-element-menugroup.md) меню приложения.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-130">The following is a list of constraints for a [**MenuGroup**](windowsribbon-element-menugroup.md) element of an Application Menu:</span></span>

-   <span data-ttu-id="8ea5a-131">Все элементы [**менуграуп**](windowsribbon-element-menugroup.md) должны быть объявлены с атрибутом *класса* со значением `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="8ea5a-131">All [**MenuGroup**](windowsribbon-element-menugroup.md) items must be declared with a *Class* attribute value of `MajorItems`.</span></span>
-   <span data-ttu-id="8ea5a-132">Меню приложения  [**менуграуп**](windowsribbon-element-menugroup.md) поддерживает только [кнопку](windowsribbon-controls-button.md), [выключатель](windowsribbon-controls-togglebutton.md), [кнопку](windowsribbon-controls-dropdownbutton.md)с раскрывающимся списком, [разворачивающуюся кнопку](windowsribbon-controls-splitbutton.md), [раскрывающийся список](windowsribbon-controls-dropdowngallery.md)и элементы управления [коллекции разворачивающихся кнопок](windowsribbon-controls-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea5a-132">An Application Menu  [**MenuGroup**](windowsribbon-element-menugroup.md) supports only the [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), and [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) controls.</span></span>
    > <span data-ttu-id="8ea5a-133">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="8ea5a-133">\[!Important\]</span></span>  
    > <span data-ttu-id="8ea5a-134">Коллекции команд — это единственный тип коллекции, поддерживаемый в меню приложения.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-134">Command galleries are the only type of gallery that are supported in the Application Menu.</span></span> <span data-ttu-id="8ea5a-135">Дополнительные сведения об элементах управления галереи см. в разделе [Работа с галереями](./ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="8ea5a-135">See [Working with Galleries](./ribbon-controls-galleries.md), for more information on gallery controls.</span></span>

     

<span data-ttu-id="8ea5a-136">При использовании [кнопки](windowsribbon-controls-button.md) или [выключателя](windowsribbon-controls-togglebutton.md) в [**менуграуп**](windowsribbon-element-menugroup.md)значение [**Command. Лабелтитле**](windowsribbon-element-command-labeltitle.md) отображается в меню, а значения [**Command. тултиптитле**](windowsribbon-element-command-tooltiptitle.md) и [**Command. тултипдескриптион**](windowsribbon-element-command-tooltipdescription.md) отображаются в виде подсказки, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-136">When a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) is used in a [**MenuGroup**](windowsribbon-element-menugroup.md), the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is displayed in the menu and the values of [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) and [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) are displayed as the tooltip, as shown in the following screen shot.</span></span>

![снимок экрана элемента управления "Кнопка" в меню "приложение".](images/overviews/applicationmenu-menubutton.png)

<span data-ttu-id="8ea5a-138">Если в меню приложения используется кнопка с раскрывающимся [списком](windowsribbon-controls-dropdownbutton.md), [разворачивающаяся кнопка](windowsribbon-controls-splitbutton.md), [раскрывающийся список](windowsribbon-controls-dropdowngallery.md)или [коллекция разворачивающихся кнопок](windowsribbon-controls-splitbuttongallery.md) , то часть меню отображается как всплывающее окно, которое охватывает и скрывает панель « **недавние элементы** ».</span><span class="sxs-lookup"><span data-stu-id="8ea5a-138">When a [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), or [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) is used in the Application Menu, the menu portion is displayed as a flyout that covers and conceals the **Recent items** pane.</span></span>

<span data-ttu-id="8ea5a-139">Для элементов управления " [разворачивающаяся кнопка](windowsribbon-controls-splitbutton.md) " и ["](windowsribbon-controls-dropdownbutton.md) раскрывающийся список" значение [**Command. лабелдескриптион**](windowsribbon-element-command-labeldescription.md) отображается встроенным во всплывающем меню, чтобы визуально помочь пользователям в обнаружении функциональных возможностей команды.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-139">For [Split Button](windowsribbon-controls-splitbutton.md) and [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) controls, the value of [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) is shown inline in the flyout menu to visually assist users with discovering the Command functionality.</span></span> <span data-ttu-id="8ea5a-140">Отображаемое значение **Command. лабелдескриптион** программно разбивается на две строки, и предпринимается попытка точно вписать значение в область **недавние элементы** ниже.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-140">The displayed value of **Command.LabelDescription** is programmatically broken over a two-line span, and an attempt is made to fit the value exactly over the **Recent items** pane beneath.</span></span> <span data-ttu-id="8ea5a-141">Если значение **Command. лабелдескриптион** не умещается, всплывающее окно будет развернуто в соответствии с наибольшим значением [**Command. Comment**](windowsribbon-element-command-comment.md) в [**менуграуп**](windowsribbon-element-menugroup.md).</span><span class="sxs-lookup"><span data-stu-id="8ea5a-141">If the **Command.LabelDescription** value does not fit, the flyout will expand to accommodate the longest [**Command.Comment**](windowsribbon-element-command-comment.md) value in the [**MenuGroup**](windowsribbon-element-menugroup.md).</span></span>

<span data-ttu-id="8ea5a-142">На следующем снимке экрана показаны эти режимы работы во всплывающем окне [разворачивающейся кнопки](windowsribbon-controls-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea5a-142">The following screen shot illustrates these behaviors in a [Split Button](windowsribbon-controls-splitbutton.md) flyout.</span></span>

![снимок экрана всплывающего окна элемента управления "список" в меню приложения.](images/overviews/applicationmenu-menuflyout.png)

<span data-ttu-id="8ea5a-144">С помощью раскрывающейся [коллекции](windowsribbon-controls-dropdowngallery.md) и [коллекции разделенных кнопок](windowsribbon-controls-splitbuttongallery.md)отображаются только метка и изображение.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-144">With a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) and a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md), only a label and an image are shown.</span></span>

## <a name="sizing-the-application-menu"></a><span data-ttu-id="8ea5a-145">Изменение размера меню приложения</span><span class="sxs-lookup"><span data-stu-id="8ea5a-145">Sizing the Application Menu</span></span>

<span data-ttu-id="8ea5a-146">Размер меню приложения обрабатывается платформой Ribbon.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-146">Sizing of the Application Menu is handled by the Ribbon framework.</span></span> <span data-ttu-id="8ea5a-147">Если указаны очень длинные строки для значения [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или [**Command. лабелдескриптион**](windowsribbon-element-command-labeldescription.md)или используется длинный список команд, меню будет масштабироваться в соответствии с содержимым.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-147">If very long strings are supplied for the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), or a long list of Commands is used, the menu will adjust its size to accommodate the contents.</span></span> <span data-ttu-id="8ea5a-148">Некоторые формы коррекции включают в себя увеличение размера всплывающих списков или панелей меню, а также добавление средств просмотра панорамы при необходимости прокрутки.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-148">Some forms of adjustment include expanding the size of flyouts or menu panes, and adding pan viewers when scrolling is required.</span></span>

## <a name="application-menu-properties"></a><span data-ttu-id="8ea5a-149">Свойства меню приложения</span><span class="sxs-lookup"><span data-stu-id="8ea5a-149">Application Menu Properties</span></span>

<span data-ttu-id="8ea5a-150">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления меню приложения.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-150">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Application Menu control.</span></span>

<span data-ttu-id="8ea5a-151">Как правило, свойство меню приложения обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="8ea5a-151">Typically, an Application Menu property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="8ea5a-152">Событие "недействительность" обрабатывается, а обновления свойств определяются методом обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="8ea5a-152">The invalidation event is handled and the property updates are defined by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="8ea5a-153">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется, и приложение не запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-153">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed and the application is not queried for an updated property value until the property is required by the framework.</span></span> <span data-ttu-id="8ea5a-154">Например, платформа требует свойство при активации вкладки и отображении элемента управления в ленте или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-154">For example, the framework requires the property when a tab is activated and a control is revealed in the ribbon UI, or when a tooltip is displayed.</span></span>



| <span data-ttu-id="8ea5a-155">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="8ea5a-155">Property key</span></span>                                                                                     | <span data-ttu-id="8ea5a-156">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ea5a-156">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="8ea5a-157">UI \_ PKEY \_ тултипдескриптион</span><span class="sxs-lookup"><span data-stu-id="8ea5a-157">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="8ea5a-158">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-158">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="8ea5a-159">UI \_ PKEY \_ тултиптитле</span><span class="sxs-lookup"><span data-stu-id="8ea5a-159">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="8ea5a-160">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-160">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8ea5a-161">См. также</span><span class="sxs-lookup"><span data-stu-id="8ea5a-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ea5a-162">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="8ea5a-162">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="8ea5a-163">**Аппликатионмену, элемент разметки**</span><span class="sxs-lookup"><span data-stu-id="8ea5a-163">**ApplicationMenu markup element**</span></span>](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 