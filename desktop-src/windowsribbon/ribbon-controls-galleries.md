---
title: Работа с коллекциями
description: Платформа Windows Ribbon предоставляет разработчикам надежную и согласованную модель управления динамическим содержимым в различных элементах управления, основанных на коллекциях.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Лента Windows, коллекции
- Лента, коллекции
- Лента Windows, элемент управления Дропдовнгаллери
- Лента, элемент управления Дропдовнгаллери
- Лента Windows, элемент управления Сплитбуттонгаллери
- Лента, элемент управления Сплитбуттонгаллери
- Элемент управления Дропдовнгаллери
- Элемент управления Сплитбуттонгаллери
- коллекции для ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793074"
---
# <a name="working-with-galleries"></a><span data-ttu-id="44278-112">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="44278-112">Working with Galleries</span></span>

<span data-ttu-id="44278-113">Платформа Windows Ribbon предоставляет разработчикам надежную и согласованную модель управления динамическим содержимым в различных элементах управления, основанных на коллекциях.</span><span class="sxs-lookup"><span data-stu-id="44278-113">The Windows Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="44278-114">Адаптируя и перестраивая ленту, эти динамические элементы управления позволяют платформе реагировать на взаимодействие пользователя как в ведущем приложении, так и на ленте, а также обеспечивают гибкость при обработке различных сред выполнения.</span><span class="sxs-lookup"><span data-stu-id="44278-114">By adapting and reconfiguring the Ribbon UI, these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

-   [<span data-ttu-id="44278-115">Введение</span><span class="sxs-lookup"><span data-stu-id="44278-115">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="44278-116">Коллекции</span><span class="sxs-lookup"><span data-stu-id="44278-116">Galleries</span></span>](#working-with-galleries)
    -   [<span data-ttu-id="44278-117">Коллекции элементов</span><span class="sxs-lookup"><span data-stu-id="44278-117">Item Galleries</span></span>](#item-galleries)
    -   [<span data-ttu-id="44278-118">Коллекции команд</span><span class="sxs-lookup"><span data-stu-id="44278-118">Command Galleries</span></span>](#command-galleries)
    -   [<span data-ttu-id="44278-119">Элементы управления галереи</span><span class="sxs-lookup"><span data-stu-id="44278-119">Gallery Controls</span></span>](#working-with-galleries)
-   [<span data-ttu-id="44278-120">Реализация коллекции</span><span class="sxs-lookup"><span data-stu-id="44278-120">How to Implement a Gallery</span></span>](#how-to-implement-a-gallery)
    -   [<span data-ttu-id="44278-121">Основные компоненты</span><span class="sxs-lookup"><span data-stu-id="44278-121">The Basic Components</span></span>](#the-basic-components)
    -   [<span data-ttu-id="44278-122">Объявление элементов управления в разметке</span><span class="sxs-lookup"><span data-stu-id="44278-122">Declare the Controls in Markup</span></span>](#declare-the-controls-in-markup)
    -   [<span data-ttu-id="44278-123">Создание обработчика команд</span><span class="sxs-lookup"><span data-stu-id="44278-123">Create a Command Handler</span></span>](#create-a-command-handler)
    -   [<span data-ttu-id="44278-124">Привязка обработчика команд</span><span class="sxs-lookup"><span data-stu-id="44278-124">Bind the Command Handler</span></span>](#bind-the-command-handler)
    -   [<span data-ttu-id="44278-125">Инициализация коллекции</span><span class="sxs-lookup"><span data-stu-id="44278-125">Initialize a Collection</span></span>](#initialize-a-collection)
    -   [<span data-ttu-id="44278-126">Обработку событий коллекции</span><span class="sxs-lookup"><span data-stu-id="44278-126">Handle Collection Events</span></span>](#handle-collection-events)
-   [<span data-ttu-id="44278-127">См. также</span><span class="sxs-lookup"><span data-stu-id="44278-127">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="44278-128">Введение</span><span class="sxs-lookup"><span data-stu-id="44278-128">Introduction</span></span>

<span data-ttu-id="44278-129">Эта возможность платформы Ribbon динамически адаптируется к условиям времени выполнения, требованиям приложений и вводу конечных пользователей, что приводит к расширению возможностей пользовательского интерфейса платформы и предоставляет разработчикам гибкие возможности для удовлетворения широкого спектра потребностей клиентов.</span><span class="sxs-lookup"><span data-stu-id="44278-129">This ability of the Ribbon framework to dynamically adapt to run-time conditions, application requirements, and end-user input highlights the rich UI capabilities of the framework, and provides developers with the flexibility to cater to a broad range of customer needs.</span></span>

<span data-ttu-id="44278-130">Основное внимание в этом руководства состоит в том, чтобы описать динамические элементы управления галереи, поддерживаемые платформой, объяснить их различия, обсудить, когда и где их лучше использовать, и продемонстрировать, как они могут быть включены в приложение ленты.</span><span class="sxs-lookup"><span data-stu-id="44278-130">The focus of this guide is to describe the dynamic gallery controls supported by the framework, explain their differences, discuss when and where they may best be used, and demonstrate how they can be incorporated into a Ribbon application.</span></span>

## <a name="galleries"></a><span data-ttu-id="44278-131">Коллекции</span><span class="sxs-lookup"><span data-stu-id="44278-131">Galleries</span></span>

<span data-ttu-id="44278-132">Галереи функционально и графически имеют богатые элементы управления "список".</span><span class="sxs-lookup"><span data-stu-id="44278-132">Galleries are functionally and graphically rich list box controls.</span></span> <span data-ttu-id="44278-133">Коллекцию элементов коллекции можно упорядочить по категориям, отображаемым в гибких макетах столбцов и строк, представленных изображениями и текстом, а также в зависимости от типа коллекции, поддерживающей динамический просмотр.</span><span class="sxs-lookup"><span data-stu-id="44278-133">The item collection of a gallery can be organized by categories, displayed in flexible column and row-based layouts, represented with images and text, and depending on the type of gallery, support live previewing.</span></span>

<span data-ttu-id="44278-134">Коллекции функционально отличаются от других динамических элементов управления ленты по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="44278-134">Galleries are functionally distinct from other dynamic Ribbon controls for the following reasons:</span></span>

-   <span data-ttu-id="44278-135">Коллекции реализуют интерфейс [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , который определяет различные методы управления коллекциями элементов коллекции.</span><span class="sxs-lookup"><span data-stu-id="44278-135">Galleries implement the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface that defines the various methods for manipulating gallery item collections.</span></span>
-   <span data-ttu-id="44278-136">Коллекции можно обновлять во время выполнения на основе действий, которые выполняются непосредственно на ленте, например, когда пользователь добавляет команду на панель быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="44278-136">Galleries can be updated at run time, based on activity that occurs directly in the Ribbon, such as when a user adds a Command to the Quick Access Toolbar (QAT).</span></span>
-   <span data-ttu-id="44278-137">Коллекции могут обновляться во время выполнения на основе действий, которые происходят косвенно из среды выполнения, например, если драйвер принтера поддерживает только книжные макеты страниц.</span><span class="sxs-lookup"><span data-stu-id="44278-137">Galleries can be updated at run time, based on activity that occurs indirectly from the run-time environment, such as when a printer driver supports portrait page layouts only.</span></span>
-   <span data-ttu-id="44278-138">Коллекции можно обновлять во время выполнения на основе действий, которые происходят косвенно в ведущем приложении, например, когда пользователь выбирает элемент в документе.</span><span class="sxs-lookup"><span data-stu-id="44278-138">Galleries can be updated at run time, based on activity that occurs indirectly in the host application, such as when a user selects an item in a document.</span></span>

<span data-ttu-id="44278-139">Платформа Ribbon предоставляет два типа коллекций: коллекции элементов и коллекции команд.</span><span class="sxs-lookup"><span data-stu-id="44278-139">The Ribbon framework exposes two types of galleries: item galleries and Command galleries.</span></span>

### <a name="item-galleries"></a><span data-ttu-id="44278-140">Коллекции элементов</span><span class="sxs-lookup"><span data-stu-id="44278-140">Item Galleries</span></span>

<span data-ttu-id="44278-141">Коллекции элементов содержат коллекцию связанных элементов, основанную на индексах, где каждый элемент представлен изображением, строкой или обоими элементами.</span><span class="sxs-lookup"><span data-stu-id="44278-141">Item galleries contain an index-based collection of related items where each item is represented by an image, a string, or both.</span></span> <span data-ttu-id="44278-142">Элемент управления привязан к одному обработчику команды, который использует значение индекса, определяемое свойством [UI \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) .</span><span class="sxs-lookup"><span data-stu-id="44278-142">The control is bound to a single Command handler that relies on the index value that is identified by the [UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) property.</span></span>

<span data-ttu-id="44278-143">Коллекции элементов поддерживают динамическое представление, что означает отображение результата команды на основе фокуса ввода-вывода без фиксации или фактического вызова команды.</span><span class="sxs-lookup"><span data-stu-id="44278-143">Item galleries support live previewing, which means displaying a Command result, based on mouseover or focus, without committing to or actually invoking the Command.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44278-144">Платформа не поддерживает размещение коллекций элементов в меню приложения.</span><span class="sxs-lookup"><span data-stu-id="44278-144">The framework does not support hosting item galleries in the Application Menu.</span></span>

 

### <a name="command-galleries"></a><span data-ttu-id="44278-145">Коллекции команд</span><span class="sxs-lookup"><span data-stu-id="44278-145">Command Galleries</span></span>

<span data-ttu-id="44278-146">Коллекции команд содержат коллекцию уникальных неиндексированных элементов.</span><span class="sxs-lookup"><span data-stu-id="44278-146">Command galleries contain a collection of distinct, non-indexed items.</span></span> <span data-ttu-id="44278-147">Каждый элемент представлен одним элементом управления, привязанным к обработчику команд с помощью идентификатора команды.</span><span class="sxs-lookup"><span data-stu-id="44278-147">Each item is represented by a single control bound to a Command handler through a Command ID.</span></span> <span data-ttu-id="44278-148">Как и автономные элементы управления, каждый элемент в коллекции команд направляет события ввода в связанный обработчик команды — сама коллекция команд не прослушивает события.</span><span class="sxs-lookup"><span data-stu-id="44278-148">Like standalone controls, each item in a Command gallery routes input events to an associated Command handler—the Command gallery itself does not listen for events.</span></span>

<span data-ttu-id="44278-149">Коллекции команд не поддерживают динамический просмотр.</span><span class="sxs-lookup"><span data-stu-id="44278-149">Command galleries do not support live previewing.</span></span>

### <a name="gallery-controls"></a><span data-ttu-id="44278-150">Элементы управления галереи</span><span class="sxs-lookup"><span data-stu-id="44278-150">Gallery Controls</span></span>

<span data-ttu-id="44278-151">В платформе Ribbon есть четыре элемента управления галереи: [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md), [**инриббонгаллери**](windowsribbon-element-inribbongallery.md)и [**ComboBox**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="44278-151">There are four gallery controls in the Ribbon framework: the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), and the [**ComboBox**](windowsribbon-element-combobox.md).</span></span> <span data-ttu-id="44278-152">Все, за исключением **поля со списком** , можно реализовать как коллекцию элементов или коллекцию команд.</span><span class="sxs-lookup"><span data-stu-id="44278-152">All except the **ComboBox** can be implemented as either an item gallery or a Command gallery.</span></span>

### <a name="dropdowngallery"></a><span data-ttu-id="44278-153">дропдовнгаллери</span><span class="sxs-lookup"><span data-stu-id="44278-153">DropDownGallery</span></span>

<span data-ttu-id="44278-154">[**Дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) — это кнопка, которая отображает раскрывающийся список, содержащий коллекцию взаимоисключающих элементов или команд.</span><span class="sxs-lookup"><span data-stu-id="44278-154">A [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) is a button that displays a drop-down list that contains a collection of mutually exclusive items or Commands.</span></span>

<span data-ttu-id="44278-155">На следующем снимке экрана показан [раскрывающийся список](windowsribbon-controls-dropdowngallery.md) элементов управления "Коллекция ленты" в Microsoft Paint для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="44278-155">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![снимок экрана с раскрывающимся элементом управления галереи в Microsoft Paint для Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a><span data-ttu-id="44278-157">сплитбуттонгаллери</span><span class="sxs-lookup"><span data-stu-id="44278-157">SplitButtonGallery</span></span>

<span data-ttu-id="44278-158">[**Сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) — это составной элемент управления, предоставляющий один элемент или команду по умолчанию из своей коллекции на основной кнопке и отображающий другие элементы или команды в взаимоисключающем раскрывающемся списке, который отображается при нажатии на вторичную кнопку.</span><span class="sxs-lookup"><span data-stu-id="44278-158">A [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) is a composite control that exposes a single default item or Command from its collection on a primary button, and displays other items or commands in a mutually exclusive drop-down list that is displayed when a secondary button is clicked.</span></span>

<span data-ttu-id="44278-159">На следующем снимке экрана показан элемент управления ["коллекция кнопок с разделением ленты"](windowsribbon-controls-splitbuttongallery.md) в Microsoft Paint для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="44278-159">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![снимок экрана: элемент управления "коллекция разделенных кнопок" в Microsoft Paint для Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a><span data-ttu-id="44278-161">инриббонгаллери</span><span class="sxs-lookup"><span data-stu-id="44278-161">InRibbonGallery</span></span>

<span data-ttu-id="44278-162">[**Инриббонгаллери**](windowsribbon-element-inribbongallery.md) — это коллекция, в которой отображается коллекция связанных элементов или команд на ленте.</span><span class="sxs-lookup"><span data-stu-id="44278-162">An [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is a gallery that displays a collection of related items or Commands in the Ribbon.</span></span> <span data-ttu-id="44278-163">Если в коллекции слишком много элементов, для показа остальной части коллекции в развернутой области предоставляется стрелка развертывания.</span><span class="sxs-lookup"><span data-stu-id="44278-163">If there are too many items in the gallery, an expand arrow is provided to display the rest of the collection in an expanded pane.</span></span>

<span data-ttu-id="44278-164">На следующем снимке экрана показана лента в элементе управления " [Коллекция ленты](windowsribbon-controls-inribbongallery.md) " в Microsoft Paint для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="44278-164">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![снимок экрана: элемент управления "Коллекция на ленте" на ленте Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a><span data-ttu-id="44278-166">ComboBox</span><span class="sxs-lookup"><span data-stu-id="44278-166">ComboBox</span></span>

<span data-ttu-id="44278-167">[**ComboBox**](windowsribbon-element-combobox.md) — это список из одного столбца, который содержит коллекцию элементов со статическим элементом управления или элементом управления "поле ввода" и стрелкой раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="44278-167">A [**ComboBox**](windowsribbon-element-combobox.md) is a single-column list box that contains a collection of items with either a static control or edit control and dropdown arrow.</span></span> <span data-ttu-id="44278-168">Часть элемента управления отображается в списке, когда пользователь щелкает стрелку раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="44278-168">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

<span data-ttu-id="44278-169">На следующем снимке экрана показан элемент управления [поля со списком](windowsribbon-controls-combobox.md) ленты в Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="44278-169">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![снимок экрана элемента управления ComboBox на ленте Microsoft Paint.](images/controls/combobox.png)

<span data-ttu-id="44278-171">Поскольку [**ComboBox**](windowsribbon-element-combobox.md) является исключительно коллекцией элементов, он не поддерживает командные элементы.</span><span class="sxs-lookup"><span data-stu-id="44278-171">Because the [**ComboBox**](windowsribbon-element-combobox.md) is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="44278-172">Он также является единственным элементом управления "Коллекция", который не поддерживает пространство команд.</span><span class="sxs-lookup"><span data-stu-id="44278-172">It is also the only gallery control that does not support a Command Space.</span></span> <span data-ttu-id="44278-173">(Пространство команд — это коллекция команд, которые объявляются в разметке и перечислены в нижней части коллекции элементов или коллекции команд.)</span><span class="sxs-lookup"><span data-stu-id="44278-173">(A Command Space is a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery.)</span></span>

<span data-ttu-id="44278-174">В следующем примере кода показана разметка, необходимая для объявления пространства команд с тремя кнопками в [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="44278-174">The following code example shows the markup required to declare a three-button Command Space in a [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



<span data-ttu-id="44278-175">На следующем снимке экрана показана Командная область из трех кнопок в предыдущем примере кода.</span><span class="sxs-lookup"><span data-stu-id="44278-175">The following screen shot illustrates the three-button Command Space of the preceding code example.</span></span>

![снимок экрана командного пространства с тремя кнопками в дропдовнгаллери.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a><span data-ttu-id="44278-177">Реализация коллекции</span><span class="sxs-lookup"><span data-stu-id="44278-177">How to Implement a Gallery</span></span>

<span data-ttu-id="44278-178">В этом разделе обсуждаются сведения о реализации коллекций лент и описывается их внедрение в приложение для ленты.</span><span class="sxs-lookup"><span data-stu-id="44278-178">This section discusses the implementation details of Ribbon galleries and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="the-basic-components"></a><span data-ttu-id="44278-179">Основные компоненты</span><span class="sxs-lookup"><span data-stu-id="44278-179">The Basic Components</span></span>

<span data-ttu-id="44278-180">В этом разделе описывается набор свойств и методов, образующих основу динамического содержимого в платформе Ribbon и поддерживающий Добавление, удаление, обновление и иным образом Управление содержимым и визуальным макетом коллекций лент во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="44278-180">This section describes the set of properties and methods that form the backbone of dynamic content in the Ribbon framework and support adding, deleting, updating, and otherwise manipulating the content and visual layout of Ribbon galleries at run time.</span></span>

### <a name="iuicollection"></a><span data-ttu-id="44278-181">иуиколлектион</span><span class="sxs-lookup"><span data-stu-id="44278-181">IUICollection</span></span>

<span data-ttu-id="44278-182">Для коллекций требуется базовый набор методов для доступа к отдельным элементам в коллекциях и управления ими.</span><span class="sxs-lookup"><span data-stu-id="44278-182">Galleries require a basic set of methods to access and manipulate the individual items in their collections.</span></span>

<span data-ttu-id="44278-183">Интерфейс [иенумункновн](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) определяет эти методы, а платформа дополняет свои функциональные возможности дополнительными методами, определенными в интерфейсе [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="44278-183">The [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) interface defines these methods, and the framework supplements their functionality with additional methods that are defined in the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="44278-184">**Иуиколлектион** реализуется платформой для каждого объявления галереи в разметке ленты.</span><span class="sxs-lookup"><span data-stu-id="44278-184">**IUICollection** is implemented by the framework for each gallery declaration in the Ribbon markup.</span></span>

<span data-ttu-id="44278-185">Если требуется дополнительная функциональность, не предоставляемую интерфейсом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , то пользовательский объект коллекции, реализуемый ведущим приложением и производный от [иенумункновн](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) , можно заменить на коллекцию платформы.</span><span class="sxs-lookup"><span data-stu-id="44278-185">If additional functionality is required that is not provided by the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface, then a custom collection object that is implemented by the host application and derived from [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) can be substituted for the framework collection.</span></span>

### <a name="iuicollectionchangedevent"></a><span data-ttu-id="44278-186">иуиколлектиончанжедевент</span><span class="sxs-lookup"><span data-stu-id="44278-186">IUICollectionChangedEvent</span></span>

<span data-ttu-id="44278-187">Чтобы приложение отвечало на изменения коллекции коллекции, оно должно реализовать интерфейс [**иуиколлектиончанжедевент**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) .</span><span class="sxs-lookup"><span data-stu-id="44278-187">For an application to respond to changes in a gallery collection, it must implement the [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) interface.</span></span> <span data-ttu-id="44278-188">Приложения могут подписываться на уведомления из объекта [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) с помощью прослушивателя событий [**иуиколлектиончанжедевент:: OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) .</span><span class="sxs-lookup"><span data-stu-id="44278-188">Applications can subscribe to notifications from an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [**IUICollectionChangedEvent::OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) event listener.</span></span>

<span data-ttu-id="44278-189">Когда приложение заменяет коллекцию коллекции, предоставленную платформой, пользовательской коллекцией, приложение должно реализовать интерфейс [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) .</span><span class="sxs-lookup"><span data-stu-id="44278-189">When the application replaces the gallery collection provided by the framework with a custom collection, the application should implement the [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface.</span></span> <span data-ttu-id="44278-190">Если [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) не реализован, приложение не сможет уведомить платформу об изменениях в пользовательской коллекции, требующих динамических обновлений для элемента управления галереи.</span><span class="sxs-lookup"><span data-stu-id="44278-190">If [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, then the application is unable to notify the framework of changes in the custom collection that require dynamic updates to the gallery control.</span></span>

<span data-ttu-id="44278-191">В тех случаях, когда [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) не реализован, элемент управления галереи может быть обновлен только путем недействительности через [**Иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) и [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)или путем вызова [**иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="44278-191">In those cases where [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, the gallery control can be updated only by invalidation through [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) and [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), or by calling [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>

### <a name="iuisimplepropertyset"></a><span data-ttu-id="44278-192">иуисимплепропертисет</span><span class="sxs-lookup"><span data-stu-id="44278-192">IUISimplePropertySet</span></span>

<span data-ttu-id="44278-193">Приложения должны реализовывать Иуисимплепропертисет для каждого элемента или команды в коллекции коллекции.</span><span class="sxs-lookup"><span data-stu-id="44278-193">Applications must implement IUISimplePropertySet for each item or Command in a gallery collection.</span></span> <span data-ttu-id="44278-194">Однако свойства, которые могут быть запрошены с помощью [**иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) , различаются.</span><span class="sxs-lookup"><span data-stu-id="44278-194">However, the properties that can be requested with [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) vary.</span></span>

<span data-ttu-id="44278-195">Элементы определяются и привязываются к коллекции через ключ свойства [ \_ \_ ItemsSource пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) и предоставляют свойства объекту [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="44278-195">Items are defined and bound to a gallery through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key and expose properties with an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="44278-196">Допустимые свойства элементов коллекций элементов ([**\_ \_ коллекция COMMANDTYPE ИП**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="44278-196">The valid properties for items in item galleries ([**UI\_COMMANDTYPE\_COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="44278-197">Некоторые свойства элементов, например [ \_ \_ подпись PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md), могут быть определены в разметке.</span><span class="sxs-lookup"><span data-stu-id="44278-197">Some item properties, such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), can be defined in markup.</span></span> <span data-ttu-id="44278-198">Дополнительные сведения см. в справочной документации по [ключам свойств](windowsribbon-reference-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="44278-198">For more detail, see the [Property Keys](windowsribbon-reference-properties.md) reference documentation.</span></span>

 



<span data-ttu-id="44278-199">Control</span><span class="sxs-lookup"><span data-stu-id="44278-199">Control</span></span>

<span data-ttu-id="44278-200">Свойства</span><span class="sxs-lookup"><span data-stu-id="44278-200">Properties</span></span>

[<span data-ttu-id="44278-201">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="44278-201">**ComboBox**</span></span>](windowsribbon-element-combobox.md)

<span data-ttu-id="44278-202">[Пользовательский интерфейс \_ \_Метка PKEY](windowsribbon-reference-properties-uipkey-label.md), [ \_ \_ КодТипа пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="44278-202">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="44278-203">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="44278-203">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)

<span data-ttu-id="44278-204">[Пользовательский интерфейс \_ \_Метка PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ итемимаже](windowsribbon-reference-properties-uipkey-itemimage.md) , [ \_ \_ КодТипа пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="44278-204">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="44278-205">**инриббонгаллери**</span><span class="sxs-lookup"><span data-stu-id="44278-205">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)

<span data-ttu-id="44278-206">[Пользовательский интерфейс \_ \_Метка PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ итемимаже](windowsribbon-reference-properties-uipkey-itemimage.md) , [ \_ \_ КодТипа пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="44278-206">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="44278-207">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="44278-207">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)

<span data-ttu-id="44278-208">[Пользовательский интерфейс \_ \_Метка PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ итемимаже](windowsribbon-reference-properties-uipkey-itemimage.md), [ \_ \_ КодТипа пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="44278-208">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

<span data-ttu-id="44278-209">[Пользовательский интерфейс \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) — это свойство коллекции элементов.</span><span class="sxs-lookup"><span data-stu-id="44278-209">[UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) is a property of the item gallery.</span></span>



 

<span data-ttu-id="44278-210">Допустимые свойства элементов для коллекций команд ([**Пользовательский интерфейс \_ COMMANDTYPE \_ COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="44278-210">The valid item properties for Command galleries ([**UI\_COMMANDTYPE\_COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>



| <span data-ttu-id="44278-211">Control</span><span class="sxs-lookup"><span data-stu-id="44278-211">Control</span></span>                                                                | <span data-ttu-id="44278-212">Свойства</span><span class="sxs-lookup"><span data-stu-id="44278-212">Properties</span></span>                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44278-213">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="44278-213">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       | <span data-ttu-id="44278-214">[Пользовательский интерфейс \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [Пользовательский \_ интерфейс \_ PKEY](windowsribbon-reference-properties-uipkey-commandtype.md) , [ \_ \_ КодТипа ИП, Пользовательский интерфейс PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="44278-214">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="44278-215">**инриббонгаллери**</span><span class="sxs-lookup"><span data-stu-id="44278-215">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       | <span data-ttu-id="44278-216">[Пользовательский интерфейс \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [Пользовательский \_ интерфейс \_ PKEY](windowsribbon-reference-properties-uipkey-commandtype.md) , [ \_ \_ КодТипа ИП, Пользовательский интерфейс PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="44278-216">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="44278-217">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="44278-217">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) | <span data-ttu-id="44278-218">[Пользовательский интерфейс \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [Пользовательский \_ интерфейс \_ PKEY](windowsribbon-reference-properties-uipkey-commandtype.md), [ \_ \_ КодТипа ИП, Пользовательский интерфейс PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="44278-218">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>  |



 

<span data-ttu-id="44278-219">Категории используются для упорядочения элементов и команд в коллекциях.</span><span class="sxs-lookup"><span data-stu-id="44278-219">Categories are used to organize items and Commands in galleries.</span></span> <span data-ttu-id="44278-220">Категории определяются и привязываются к коллекции через ключ свойства " [ \_ \_ категории PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-categories.md) " и предоставляют свойства с объектом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , относящимся к категории.</span><span class="sxs-lookup"><span data-stu-id="44278-220">Categories are defined and bound to a gallery through the [UI\_PKEY\_Categories](windowsribbon-reference-properties-uipkey-categories.md) property key and expose properties with a category-specific [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="44278-221">Категории не имеют CommandType и не поддерживают взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="44278-221">Categories do not have a CommandType and do not support user interaction.</span></span> <span data-ttu-id="44278-222">Например, категории не могут стать SelectedItem в коллекции элементов и не привязаны к команде в коллекции команд.</span><span class="sxs-lookup"><span data-stu-id="44278-222">For example, categories cannot become the SelectedItem in an item gallery, and they are not bound to a Command in a Command gallery.</span></span> <span data-ttu-id="44278-223">Как и другие свойства элемента коллекции, свойства категории, такие как [ \_ \_ Метка PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md) и свойство [UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-categoryid.md) , могут быть получены путем вызова [**иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span><span class="sxs-lookup"><span data-stu-id="44278-223">Like other gallery item properties, category properties such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) and [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) can be retrieved by calling [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44278-224">[**Иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) должен возвращать [**\_ коллекцию UI \_ инвалидиндекс**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) , когда для элемента, не имеющего связанной категории, запрашивается [ \_ \_ КодТипа пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-categoryid.md) .</span><span class="sxs-lookup"><span data-stu-id="44278-224">[**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) should return [**UI\_COLLECTION\_INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) when [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) is requested for an item that does not have an associated category.</span></span>

 

### <a name="declare-the-controls-in-markup"></a><span data-ttu-id="44278-225">Объявление элементов управления в разметке</span><span class="sxs-lookup"><span data-stu-id="44278-225">Declare the Controls in Markup</span></span>

<span data-ttu-id="44278-226">Коллекции, как и все элементы управления ленты, должны быть объявлены в разметке.</span><span class="sxs-lookup"><span data-stu-id="44278-226">Galleries, like all Ribbon controls, must be declared in markup.</span></span> <span data-ttu-id="44278-227">Коллекция определяется в разметке как коллекция элементов или коллекция команд, и объявляются различные сведения о презентации.</span><span class="sxs-lookup"><span data-stu-id="44278-227">A gallery is identified in markup as an item gallery or Command gallery, and various presentation details are declared.</span></span> <span data-ttu-id="44278-228">В отличие от других элементов управления, коллекции должны объявляться в разметке только базовый элемент управления или контейнер коллекции.</span><span class="sxs-lookup"><span data-stu-id="44278-228">Unlike other controls, galleries require the base control only, or collection container, to be declared in markup.</span></span> <span data-ttu-id="44278-229">Фактические коллекции заполняются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="44278-229">The actual collections are populated at run time.</span></span> <span data-ttu-id="44278-230">При объявлении коллекции в разметке атрибут *Type* используется, чтобы указать, является ли коллекция коллекцией элементов коллекции команд.</span><span class="sxs-lookup"><span data-stu-id="44278-230">When a gallery is declared in markup, the *Type* attribute is used to specify whether the gallery is an item gallery of a Command gallery.</span></span>

<span data-ttu-id="44278-231">Существует ряд необязательных атрибутов макета для каждого из обсуждаемых здесь элементов управления.</span><span class="sxs-lookup"><span data-stu-id="44278-231">There are a number of optional layout attributes available for each of the controls discussed here.</span></span> <span data-ttu-id="44278-232">Эти атрибуты предоставляют разработчикам параметры для платформы, которые непосредственно влияют на то, как элемент управления заполняется и отображается на ленте.</span><span class="sxs-lookup"><span data-stu-id="44278-232">These attributes provide developer preferences for the framework to follow that directly affect how a control is populated and displayed in a ribbon.</span></span> <span data-ttu-id="44278-233">Параметры, применимые в разметке, связаны с шаблонами вывода и макета и поведением, обсуждаемым в разделе [Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="44278-233">The preferences applicable in markup are related to the display and layout templates and behaviors discussed in [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="44278-234">Если определенный элемент управления не разрешает предпочтения макета непосредственно в разметке или не заданы параметры макета, платформа определяет зависящие от конкретного элемента соглашения о отображении в зависимости от объема доступного пространства экрана.</span><span class="sxs-lookup"><span data-stu-id="44278-234">If a particular control does not allow layout preferences directly in markup, or the layout preferences are not specified, then the framework defines control-specific display conventions based on the amount of screen space available.</span></span>

<span data-ttu-id="44278-235">В следующих примерах показано, как включить набор коллекций в ленту.</span><span class="sxs-lookup"><span data-stu-id="44278-235">The following examples demonstrate how to incorporate a set of galleries into a Ribbon.</span></span>

### <a name="command-declarations"></a><span data-ttu-id="44278-236">Объявления команд</span><span class="sxs-lookup"><span data-stu-id="44278-236">Command Declarations</span></span>

<span data-ttu-id="44278-237">Команды должны объявляться с атрибутом *CommandName* , который используется для связывания элемента управления или набора элементов управления с командой.</span><span class="sxs-lookup"><span data-stu-id="44278-237">Commands should be declared with a *CommandName* attribute that is used to associate a control, or set of controls, with the Command.</span></span>

<span data-ttu-id="44278-238">Атрибут *CommandId* , используемый для привязки команды к обработчику команд при компиляции разметки, также можно указать здесь.</span><span class="sxs-lookup"><span data-stu-id="44278-238">A *CommandId* attribute used to bind a Command to a Command handler when the markup is compiled can also be specified here.</span></span> <span data-ttu-id="44278-239">Если идентификатор не указан, то он создается платформой.</span><span class="sxs-lookup"><span data-stu-id="44278-239">If no ID is provided, then one is generated by the framework.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a><span data-ttu-id="44278-240">Объявления элементов управления</span><span class="sxs-lookup"><span data-stu-id="44278-240">Control Declarations</span></span>

<span data-ttu-id="44278-241">Этот раздел содержит примеры, демонстрирующие базовую разметку элемента управления, необходимую для различных типов коллекций.</span><span class="sxs-lookup"><span data-stu-id="44278-241">This section contains examples that demonstrate the basic control markup required for the various gallery types.</span></span> <span data-ttu-id="44278-242">В них показано, как объявить элементы управления галереи и связать их с командой с помощью атрибута *CommandName* .</span><span class="sxs-lookup"><span data-stu-id="44278-242">They show how to declare the gallery controls and associate them with a Command through the *CommandName* attribute.</span></span>

<span data-ttu-id="44278-243">В следующем примере показано объявление элемента управления для [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) , где атрибут *Type* используется, чтобы указать, что это коллекция команд.</span><span class="sxs-lookup"><span data-stu-id="44278-243">The following example shows a control declaration for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) where the *Type* attribute is used to specify that this is a Command gallery.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



<span data-ttu-id="44278-244">В следующем примере показано объявление элемента управления для [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="44278-244">The following example shows a control declaration for the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



<span data-ttu-id="44278-245">В следующем примере показано объявление элемента управления для [**инриббонгаллери**](windowsribbon-element-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="44278-245">The following example shows a control declaration for the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).</span></span>

> [!Note]  
> <span data-ttu-id="44278-246">Поскольку [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) предназначен для вывода на ленту подмножества коллекции элементов без активации раскрывающегося меню, он предоставляет ряд необязательных атрибутов, управляющих его размером и макетом элемента при инициализации ленты.</span><span class="sxs-lookup"><span data-stu-id="44278-246">Because the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is designed to display a subset of its item collection in the Ribbon without activating a drop-down menu, it provides a number of optional attributes that govern its size and item layout on Ribbon initialization.</span></span> <span data-ttu-id="44278-247">Эти атрибуты являются уникальными для **инриббонгаллери** и недоступны из других динамических элементов управления.</span><span class="sxs-lookup"><span data-stu-id="44278-247">These attributes are unique to the **InRibbonGallery** and are not available from the other dynamic controls.</span></span>

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



<span data-ttu-id="44278-248">В следующем примере показано объявление элемента управления для [**ComboBox**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="44278-248">The following example shows a control declaration for the [**ComboBox**](windowsribbon-element-combobox.md).</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a><span data-ttu-id="44278-249">Создание обработчика команд</span><span class="sxs-lookup"><span data-stu-id="44278-249">Create a Command Handler</span></span>

<span data-ttu-id="44278-250">Для каждой команды платформе Ribbon требуется соответствующий обработчик команд в ведущем приложении.</span><span class="sxs-lookup"><span data-stu-id="44278-250">For each Command, the Ribbon framework requires a corresponding Command handler in the host application.</span></span> <span data-ttu-id="44278-251">Обработчики команд реализуются ведущим приложением ленты и являются производными от интерфейса [**иуикоммандхандлер**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .</span><span class="sxs-lookup"><span data-stu-id="44278-251">Command handlers are implemented by the Ribbon host application and are derived from the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span>

> [!Note]  
> <span data-ttu-id="44278-252">К одному обработчику команды можно привязать несколько команд.</span><span class="sxs-lookup"><span data-stu-id="44278-252">Multiple Commands can be bound to a single Command handler.</span></span>

 

<span data-ttu-id="44278-253">Обработчик команд выполняет две задачи:</span><span class="sxs-lookup"><span data-stu-id="44278-253">A Command handler serves two purposes:</span></span>

-   <span data-ttu-id="44278-254">[**Иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) отвечает на запросы обновления свойств.</span><span class="sxs-lookup"><span data-stu-id="44278-254">[**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responds to property update requests.</span></span> <span data-ttu-id="44278-255">Значения свойств команд, таких как [ \_ \_ включенный ИП UI](windowsribbon-reference-properties-uipkey-enabled.md) или [ \_ \_ подпись PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md), задаются посредством вызовов [**иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) или [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="44278-255">The values of Command properties, such as [UI\_PKEY\_Enabled](windowsribbon-reference-properties-uipkey-enabled.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), are set through calls to [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) or [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span>
-   <span data-ttu-id="44278-256">[**Иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) отвечает на выполнение событий.</span><span class="sxs-lookup"><span data-stu-id="44278-256">[**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responds to execute events.</span></span> <span data-ttu-id="44278-257">Этот метод поддерживает следующие три состояния выполнения, заданные параметром [**\_ Ексекутионверб пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) .</span><span class="sxs-lookup"><span data-stu-id="44278-257">This method supports the following three execution states that are specified by the [**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) parameter.</span></span>
    -   <span data-ttu-id="44278-258">Состояние выполнения (или фиксация в) выполняет все команды, с которыми связан обработчик.</span><span class="sxs-lookup"><span data-stu-id="44278-258">The Execute state executes, or commits to, any commands to which the handler is bound.</span></span>
    -   <span data-ttu-id="44278-259">Предварительный просмотр позволяет просмотреть все команды, к которым привязан обработчик.</span><span class="sxs-lookup"><span data-stu-id="44278-259">The Preview state previews any commands to which the handler is bound.</span></span> <span data-ttu-id="44278-260">Это по сути выполняет команды без фиксации в результате.</span><span class="sxs-lookup"><span data-stu-id="44278-260">This essentially executes the commands without committing to the result.</span></span>
    -   <span data-ttu-id="44278-261">Состояние Канцелпревиев отменяет все предварительно просмотрные команды.</span><span class="sxs-lookup"><span data-stu-id="44278-261">The CancelPreview state cancels any previewed Commands.</span></span> <span data-ttu-id="44278-262">Это необходимо для поддержки прохода по меню или списку и последовательного предварительного просмотра и отмены результатов по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="44278-262">This is required to support traversal through a menu or list and sequentially preview and undo the results as required.</span></span>

<span data-ttu-id="44278-263">В следующем примере показан обработчик команд коллекции.</span><span class="sxs-lookup"><span data-stu-id="44278-263">The following example demonstrates a gallery command handler.</span></span>


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a><span data-ttu-id="44278-264">Привязка обработчика команд</span><span class="sxs-lookup"><span data-stu-id="44278-264">Bind the Command Handler</span></span>

<span data-ttu-id="44278-265">После определения обработчика команд должна быть привязана к обработчику.</span><span class="sxs-lookup"><span data-stu-id="44278-265">After you define a Command handler, the Command must be bound to the handler.</span></span>

<span data-ttu-id="44278-266">В следующем примере показано, как привязать команду коллекции к конкретному обработчику команды.</span><span class="sxs-lookup"><span data-stu-id="44278-266">The following example demonstrates how to bind a gallery Command to a specific Command handler.</span></span> <span data-ttu-id="44278-267">В этом случае элементы управления [**ComboBox**](windowsribbon-element-combobox.md) и Gallery привязываются к соответствующим обработчикам команд.</span><span class="sxs-lookup"><span data-stu-id="44278-267">In this case, both the [**ComboBox**](windowsribbon-element-combobox.md) and gallery controls are bound to their respective Command handlers.</span></span>


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a><span data-ttu-id="44278-268">Инициализация коллекции</span><span class="sxs-lookup"><span data-stu-id="44278-268">Initialize a Collection</span></span>

<span data-ttu-id="44278-269">В следующем примере демонстрируется пользовательская реализация [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) для коллекций элементов и команд.</span><span class="sxs-lookup"><span data-stu-id="44278-269">The following example demonstrates a custom implementation of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) for both item and Command galleries.</span></span>

<span data-ttu-id="44278-270">Класс Цитемпропертиес в этом примере является производным от [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span><span class="sxs-lookup"><span data-stu-id="44278-270">The CItemProperties class in this example is derived from [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span></span> <span data-ttu-id="44278-271">В дополнение к обязательному методу [**иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)класс Цитемпропертиес реализует набор вспомогательных функций для инициализации и отслеживания индексов.</span><span class="sxs-lookup"><span data-stu-id="44278-271">In addition to the required method [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), the CItemProperties class implements a set of helper functions for initialization and index tracking.</span></span>


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a><span data-ttu-id="44278-272">Обработку событий коллекции</span><span class="sxs-lookup"><span data-stu-id="44278-272">Handle Collection Events</span></span>

<span data-ttu-id="44278-273">В следующем примере демонстрируется реализация Иуиколлектиончанжедевент.</span><span class="sxs-lookup"><span data-stu-id="44278-273">The following example demonstrates an IUICollectionChangedEvent implementation.</span></span>


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="44278-274">См. также</span><span class="sxs-lookup"><span data-stu-id="44278-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44278-275">Свойства коллекции</span><span class="sxs-lookup"><span data-stu-id="44278-275">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="44278-276">Создание приложения для ленты</span><span class="sxs-lookup"><span data-stu-id="44278-276">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="44278-277">Основные сведения о командах и элементах управления</span><span class="sxs-lookup"><span data-stu-id="44278-277">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> <dt>

[<span data-ttu-id="44278-278">Рекомендации по работе пользователя с лентой</span><span class="sxs-lookup"><span data-stu-id="44278-278">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="44278-279">Процесс разработки ленты</span><span class="sxs-lookup"><span data-stu-id="44278-279">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[<span data-ttu-id="44278-280">Пример коллекции</span><span class="sxs-lookup"><span data-stu-id="44278-280">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 