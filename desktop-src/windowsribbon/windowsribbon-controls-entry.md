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
# <a name="windows-ribbon-framework-control-library"></a><span data-ttu-id="39f25-104">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="39f25-104">Windows Ribbon Framework Control Library</span></span>

<span data-ttu-id="39f25-105">В разделах, содержащихся в этом разделе, описывается набор элементов управления, включенных в платформу Windows Ribbon.</span><span class="sxs-lookup"><span data-stu-id="39f25-105">The topics contained in this section describe the set of controls that are included with the Windows Ribbon framework.</span></span> <span data-ttu-id="39f25-106">Перечисленные здесь элементы управления являются объектами пользовательского интерфейса на ленте, которые предоставляют функциональные возможности команды.</span><span class="sxs-lookup"><span data-stu-id="39f25-106">The controls listed here are the UI objects in a ribbon that expose Command functionality.</span></span>

-   [<span data-ttu-id="39f25-107">Введение</span><span class="sxs-lookup"><span data-stu-id="39f25-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="39f25-108">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="39f25-108">The Controls</span></span>](#windows-ribbon-framework-control-library)
    -   [<span data-ttu-id="39f25-109">Основные элементы управления</span><span class="sxs-lookup"><span data-stu-id="39f25-109">Basic Controls</span></span>](#basic-controls)
    -   [<span data-ttu-id="39f25-110">Контейнерные элементы управления</span><span class="sxs-lookup"><span data-stu-id="39f25-110">Container Controls</span></span>](#container-controls)
    -   [<span data-ttu-id="39f25-111">Специализированные элементы управления</span><span class="sxs-lookup"><span data-stu-id="39f25-111">Specialized Controls</span></span>](#specialized-controls)
-   [<span data-ttu-id="39f25-112">См. также</span><span class="sxs-lookup"><span data-stu-id="39f25-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="39f25-113">Введение</span><span class="sxs-lookup"><span data-stu-id="39f25-113">Introduction</span></span>

<span data-ttu-id="39f25-114">Платформа Ribbon состоит из таких компонентов, как [вкладки](windowsribbon-controls-tab.md) и [панель быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md), которые работают вместе, чтобы обеспечить широкие возможности пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="39f25-114">The Ribbon framework is composed of components such as [Tabs](windowsribbon-controls-tab.md) and the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md), that work together to deliver a rich UI experience.</span></span> <span data-ttu-id="39f25-115">По отдельности эти компоненты предоставляют различные типы команд, чтобы предоставить клиентам организованную и предсказуемую работу в приложениях на ленте.</span><span class="sxs-lookup"><span data-stu-id="39f25-115">Individually, these components expose different types of Commands to give customers an organized, predictable experience across Ribbon applications.</span></span> <span data-ttu-id="39f25-116">Например, каждая вкладка содержит команды, связанные с созданием и обработкой конкретных частей содержимого в рабочей области приложения, в то время как [меню приложения](windowsribbon-controls-applicationmenu.md) предоставляет функциональные возможности, связанные с полным проектом, например весь документ, изображение или фильм.</span><span class="sxs-lookup"><span data-stu-id="39f25-116">For example, each Tab exposes Commands related to creating and acting on specific parts of the content within the application workspace, whereas the [Application Menu](windowsribbon-controls-applicationmenu.md) exposes functionality related to a complete project, such as an entire document, picture, or movie.</span></span>

<span data-ttu-id="39f25-117">Этот раздел содержит полный список элементов управления ленты и содержит краткое описание для каждого элемента управления со ссылками на более подробную документацию, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="39f25-117">This topic provides a comprehensive list of Ribbon controls and includes a brief description for each control, with links to more detailed documentation where available.</span></span>

## <a name="the-controls"></a><span data-ttu-id="39f25-118">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="39f25-118">The Controls</span></span>

<span data-ttu-id="39f25-119">Платформа Ribbon состоит из двух [представлений](windowsribbon-reference-elements-view.md): представление [**ленты**](windowsribbon-element-ribbon.md) и представление [**контекстпопуп**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="39f25-119">The Ribbon framework is composed of two [Views](windowsribbon-reference-elements-view.md): the [**Ribbon**](windowsribbon-element-ribbon.md) View and the [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span> <span data-ttu-id="39f25-120">Каждое представление может содержать несколько компонентов, которые выступают в качестве контейнеров представления для всех элементов управления, которые визуализируются и управляются платформой.</span><span class="sxs-lookup"><span data-stu-id="39f25-120">Each View can host several components that act as presentation containers for all controls that are rendered and managed by the framework.</span></span>

<span data-ttu-id="39f25-121">В представлении [**ленты**](windowsribbon-element-ribbon.md) размещается элемент [**Аппликатионмену**](windowsribbon-element-applicationmenu.md) , элемент [**куиккакцесстулбар**](windowsribbon-element-quickaccesstoolbar.md) и панель команд ленты, а в представлении [**контекстпопуп**](windowsribbon-element-contextpopup.md) размещается элемент [**ContextMenu**](windowsribbon-element-contextmenu.md) , элемент [**минитулбар**](windowsribbon-element-minitoolbar.md) или оба этих элемента.</span><span class="sxs-lookup"><span data-stu-id="39f25-121">The [**Ribbon**](windowsribbon-element-ribbon.md) View hosts the [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element, [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) element, and ribbon command bar while the [**ContextPopup**](windowsribbon-element-contextpopup.md) View hosts a [**ContextMenu**](windowsribbon-element-contextmenu.md) element, a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element, or both.</span></span>

<span data-ttu-id="39f25-122">Каждый элемент управления платформы различает функциональные возможности, связанные с [**типом команды**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span><span class="sxs-lookup"><span data-stu-id="39f25-122">Each framework control is distinguished by the functionality associated with its [**Command type**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span></span>

### <a name="basic-controls"></a><span data-ttu-id="39f25-123">Основные элементы управления</span><span class="sxs-lookup"><span data-stu-id="39f25-123">Basic Controls</span></span>

<span data-ttu-id="39f25-124">Основные элементы управления состоят из одной или нескольких кнопок, которые можно вызывать одним щелчком мыши для выполнения простого действия.</span><span class="sxs-lookup"><span data-stu-id="39f25-124">Basic controls consist of one or more buttons that can be invoked by a single mouse click to perform a simple action.</span></span>

> [!Note]  
> <span data-ttu-id="39f25-125">[**Счетчик**](windowsribbon-element-spinner.md) является исключением, так как содержит элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="39f25-125">The [**Spinner**](windowsribbon-element-spinner.md) is an exception as it contains an edit control.</span></span>

 

<span data-ttu-id="39f25-126">В следующей таблице перечислены основные элементы управления в платформе Ribbon.</span><span class="sxs-lookup"><span data-stu-id="39f25-126">The following table lists the basic controls in the Ribbon framework.</span></span>



| <span data-ttu-id="39f25-127">Control</span><span class="sxs-lookup"><span data-stu-id="39f25-127">Control</span></span>                                                  | <span data-ttu-id="39f25-128">Элемент Markup</span><span class="sxs-lookup"><span data-stu-id="39f25-128">Markup Element</span></span>                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="39f25-129">Кнопка</span><span class="sxs-lookup"><span data-stu-id="39f25-129">Button</span></span>](windowsribbon-controls-button.md)              | [<span data-ttu-id="39f25-130">**Переключатель**</span><span class="sxs-lookup"><span data-stu-id="39f25-130">**Button**</span></span>](windowsribbon-element-button.md)             |
| [<span data-ttu-id="39f25-131">Флажок</span><span class="sxs-lookup"><span data-stu-id="39f25-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)         | [<span data-ttu-id="39f25-132">**Установка**</span><span class="sxs-lookup"><span data-stu-id="39f25-132">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)         |
| [<span data-ttu-id="39f25-133">Кнопка "Справка"</span><span class="sxs-lookup"><span data-stu-id="39f25-133">Help Button</span></span>](windowsribbon-controls-helpbutton.md)     | [<span data-ttu-id="39f25-134">**хелпбуттон**</span><span class="sxs-lookup"><span data-stu-id="39f25-134">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)     |
| [<span data-ttu-id="39f25-135">Spinner</span><span class="sxs-lookup"><span data-stu-id="39f25-135">Spinner</span></span>](windowsribbon-controls-spinner.md)            | [<span data-ttu-id="39f25-136">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="39f25-136">**Spinner**</span></span>](windowsribbon-element-spinner.md)           |
| [<span data-ttu-id="39f25-137">Выключатель</span><span class="sxs-lookup"><span data-stu-id="39f25-137">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md) | [<span data-ttu-id="39f25-138">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="39f25-138">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a><span data-ttu-id="39f25-139">Контейнерные элементы управления</span><span class="sxs-lookup"><span data-stu-id="39f25-139">Container Controls</span></span>

<span data-ttu-id="39f25-140">Контейнерные элементы управления состоят из групп элементов управления, меню, списков или коллекций элементов и команд.</span><span class="sxs-lookup"><span data-stu-id="39f25-140">Container controls are composed of groups of controls, menus, lists, or item and Command collections.</span></span>

<span data-ttu-id="39f25-141">Платформа различает два типа контейнеров: статический и динамический.</span><span class="sxs-lookup"><span data-stu-id="39f25-141">The framework distinguishes between two types of containers, static and dynamic.</span></span>

### <a name="static-containers"></a><span data-ttu-id="39f25-142">Статические контейнеры</span><span class="sxs-lookup"><span data-stu-id="39f25-142">Static Containers</span></span>

<span data-ttu-id="39f25-143">Статические контейнеры объявляются и заполняются вместе со всеми связанными ресурсами в файле разметки ленты.</span><span class="sxs-lookup"><span data-stu-id="39f25-143">Static containers are declared and populated, along with all associated resources, in the Ribbon markup file.</span></span> <span data-ttu-id="39f25-144">Эти элементы управления нельзя изменить во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="39f25-144">These controls cannot be modified at run time.</span></span>

<span data-ttu-id="39f25-145">К преимуществам статических элементов управления относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="39f25-145">The advantages of static controls include the following:</span></span>

-   <span data-ttu-id="39f25-146">Быстрое создание прототипов.</span><span class="sxs-lookup"><span data-stu-id="39f25-146">Rapid prototyping.</span></span> <span data-ttu-id="39f25-147">Статические элементы управления позволяют быстро создать макет Ribbon, похожий на окончательный дизайн ленты, для которого не требуется никакого сложного кода.</span><span class="sxs-lookup"><span data-stu-id="39f25-147">Static controls make it possible to quickly build a Ribbon mock-up resembling a final Ribbon design that requires no complicated code.</span></span>
-   <span data-ttu-id="39f25-148">Простые изменения.</span><span class="sxs-lookup"><span data-stu-id="39f25-148">Easy modifications.</span></span> <span data-ttu-id="39f25-149">Большинство элементов, атрибутов, ресурсов и макетов статических элементов управления могут быть изменены в разметке.</span><span class="sxs-lookup"><span data-stu-id="39f25-149">Most elements, attributes, resources, and layouts of static controls can be modified in markup.</span></span>
-   <span data-ttu-id="39f25-150">Единообразный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="39f25-150">Consistent UI.</span></span> <span data-ttu-id="39f25-151">Хорошо спроектированные приложения предоставляют единообразный и стабильный пользовательский интерфейс, который позволяет избежать изменений в меню и списках во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="39f25-151">Well-designed applications provide a consistent and stable UI that avoids changes to menus and lists at run time.</span></span>

<span data-ttu-id="39f25-152">В следующей таблице описаны статические элементы управления контейнера в платформе Ribbon.</span><span class="sxs-lookup"><span data-stu-id="39f25-152">The following table describes the static container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="39f25-153">Control</span><span class="sxs-lookup"><span data-stu-id="39f25-153">Control</span></span>                                                        | <span data-ttu-id="39f25-154">Элемент Markup</span><span class="sxs-lookup"><span data-stu-id="39f25-154">Markup Element</span></span>                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="39f25-155">Меню приложения</span><span class="sxs-lookup"><span data-stu-id="39f25-155">Application Menu</span></span>](windowsribbon-controls-applicationmenu.md) | [<span data-ttu-id="39f25-156">**аппликатионмену**</span><span class="sxs-lookup"><span data-stu-id="39f25-156">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md) |
| [<span data-ttu-id="39f25-157">Контекстное всплывающее окно</span><span class="sxs-lookup"><span data-stu-id="39f25-157">Context Popup</span></span>](windowsribbon-controls-contextpopup.md)       | [<span data-ttu-id="39f25-158">**контекстпопуп**</span><span class="sxs-lookup"><span data-stu-id="39f25-158">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)       |
| [<span data-ttu-id="39f25-159">Кнопка раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="39f25-159">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)  | [<span data-ttu-id="39f25-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="39f25-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)   |
| [<span data-ttu-id="39f25-161">Группа</span><span class="sxs-lookup"><span data-stu-id="39f25-161">Group</span></span>](windowsribbon-controls-group.md)                      | [<span data-ttu-id="39f25-162">**Группа**</span><span class="sxs-lookup"><span data-stu-id="39f25-162">**Group**</span></span>](windowsribbon-element-group.md)                     |
| [<span data-ttu-id="39f25-163">Группа меню</span><span class="sxs-lookup"><span data-stu-id="39f25-163">Menu Group</span></span>](windowsribbon-controls-menugroup.md)             | [<span data-ttu-id="39f25-164">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="39f25-164">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)             |
| [<span data-ttu-id="39f25-165">Разворачивающаяся кнопка</span><span class="sxs-lookup"><span data-stu-id="39f25-165">Split Button</span></span>](windowsribbon-controls-splitbutton.md)         | [<span data-ttu-id="39f25-166">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="39f25-166">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)         |
| [<span data-ttu-id="39f25-167">TAB</span><span class="sxs-lookup"><span data-stu-id="39f25-167">Tab</span></span>](windowsribbon-controls-tab.md)                          | [<span data-ttu-id="39f25-168">**TAB**</span><span class="sxs-lookup"><span data-stu-id="39f25-168">**Tab**</span></span>](windowsribbon-element-tab.md)                         |
| [<span data-ttu-id="39f25-169">Группа вкладок</span><span class="sxs-lookup"><span data-stu-id="39f25-169">Tab Group</span></span>](windowsribbon-controls-tabgroup.md)               | [<span data-ttu-id="39f25-170">**Группа вкладок**</span><span class="sxs-lookup"><span data-stu-id="39f25-170">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a><span data-ttu-id="39f25-171">Динамические контейнеры</span><span class="sxs-lookup"><span data-stu-id="39f25-171">Dynamic Containers</span></span>

<span data-ttu-id="39f25-172">Динамические контейнеры объявляются в файле разметки ленты.</span><span class="sxs-lookup"><span data-stu-id="39f25-172">Dynamic containers are declared in the Ribbon markup file.</span></span> <span data-ttu-id="39f25-173">Они имеют группу элементов или команд, которые создаются или изменяются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="39f25-173">They feature a group of items or Commands that are created or modified at run time.</span></span>

<span data-ttu-id="39f25-174">Подкласс динамических контейнеров, называемых галереями, различается по реализации интерфейса [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="39f25-174">A subclass of dynamic containers, called galleries, are distinguished by their implementation of the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="39f25-175">Этот интерфейс позволяет элементу управления предоставлять свой элемент или список команд в виде коллекции, а также поддерживать обновления в зависимости от взаимодействия с пользователем и условий времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="39f25-175">This interface allows a control to expose its item or Command list as a collection, and to support updates based on both user interaction and run-time conditions.</span></span> <span data-ttu-id="39f25-176">Дополнительные сведения см. в разделе [Работа с галереями](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="39f25-176">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="39f25-177">В следующей таблице перечислены динамические элементы управления контейнера в платформе Ribbon.</span><span class="sxs-lookup"><span data-stu-id="39f25-177">The following table lists the dynamic container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="39f25-178">Control</span><span class="sxs-lookup"><span data-stu-id="39f25-178">Control</span></span>                                                               | <span data-ttu-id="39f25-179">Элемент Markup</span><span class="sxs-lookup"><span data-stu-id="39f25-179">Markup Element</span></span>                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="39f25-180">Поле со списком</span><span class="sxs-lookup"><span data-stu-id="39f25-180">Combo Box</span></span>](windowsribbon-controls-combobox.md)                      | [<span data-ttu-id="39f25-181">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="39f25-181">**ComboBox**</span></span>](windowsribbon-element-combobox.md)                     |
| [<span data-ttu-id="39f25-182">Раскрывающийся список</span><span class="sxs-lookup"><span data-stu-id="39f25-182">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)       | [<span data-ttu-id="39f25-183">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="39f25-183">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       |
| [<span data-ttu-id="39f25-184">Коллекция на ленте</span><span class="sxs-lookup"><span data-stu-id="39f25-184">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)       | [<span data-ttu-id="39f25-185">**инриббонгаллери**</span><span class="sxs-lookup"><span data-stu-id="39f25-185">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       |
| [<span data-ttu-id="39f25-186">Панель быстрого доступа</span><span class="sxs-lookup"><span data-stu-id="39f25-186">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md) | [<span data-ttu-id="39f25-187">**куиккакцесстулбар**</span><span class="sxs-lookup"><span data-stu-id="39f25-187">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md) |
| [<span data-ttu-id="39f25-188">Недавние элементы</span><span class="sxs-lookup"><span data-stu-id="39f25-188">Recent Items</span></span>](windowsribbon-controls-recentitems.md)                | [<span data-ttu-id="39f25-189">**рецентитемс**</span><span class="sxs-lookup"><span data-stu-id="39f25-189">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)               |
| [<span data-ttu-id="39f25-190">Коллекция разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="39f25-190">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md) | [<span data-ttu-id="39f25-191">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="39f25-191">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a><span data-ttu-id="39f25-192">Специализированные элементы управления</span><span class="sxs-lookup"><span data-stu-id="39f25-192">Specialized Controls</span></span>

<span data-ttu-id="39f25-193">Платформа Ribbon содержит ряд специализированных элементов управления для определенных функций пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="39f25-193">The Ribbon framework contains a number of specialized controls for specific UI functionality.</span></span>

<span data-ttu-id="39f25-194">В следующей таблице перечислены специализированные элементы управления в платформе Ribbon.</span><span class="sxs-lookup"><span data-stu-id="39f25-194">The following table lists the specialized controls in the Ribbon framework.</span></span>



| <span data-ttu-id="39f25-195">Control</span><span class="sxs-lookup"><span data-stu-id="39f25-195">Control</span></span>                                                                  | <span data-ttu-id="39f25-196">Элемент Markup</span><span class="sxs-lookup"><span data-stu-id="39f25-196">Markup Element</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="39f25-197">Выбор цвета для раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="39f25-197">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | [<span data-ttu-id="39f25-198">**дропдовнколорпиккер**</span><span class="sxs-lookup"><span data-stu-id="39f25-198">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md) |
| [<span data-ttu-id="39f25-199">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="39f25-199">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | [<span data-ttu-id="39f25-200">**фонтконтрол**</span><span class="sxs-lookup"><span data-stu-id="39f25-200">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="39f25-201">См. также</span><span class="sxs-lookup"><span data-stu-id="39f25-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39f25-202">Основные сведения о командах и элементах управления</span><span class="sxs-lookup"><span data-stu-id="39f25-202">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 