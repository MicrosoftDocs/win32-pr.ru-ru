---
title: Общие сведения о поставщиках автоматизации пользовательского интерфейса
description: В этом разделе приводятся общие сведения о том, как разработчики элементов управления реализуют поставщики автоматизации пользовательского интерфейса.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- Модель автоматизации пользовательского интерфейса, общие сведения о поставщиках
- Модель автоматизации пользовательского интерфейса, типы поставщиков
- Модель автоматизации пользовательского интерфейса, основные понятия поставщиков
- поставщики, сведения
- поставщики, типы
- поставщики, основные понятия
- поставщики, элементы
- поставщики, Навигация
- поставщики, представления
- поставщики, платформы
- поставщики, фрагменты
- поставщики, узлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986359"
---
# <a name="ui-automation-providers-overview"></a><span data-ttu-id="63816-115">Общие сведения о поставщиках автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="63816-115">UI Automation Providers Overview</span></span>

<span data-ttu-id="63816-116">Поставщик автоматизации пользовательского интерфейса Майкрософт — это программный объект, который предоставляет элемент пользовательского интерфейса приложения, чтобы клиентские приложения со специальными возможностями могли получать сведения об элементе и вызывать его функциональность.</span><span class="sxs-lookup"><span data-stu-id="63816-116">A Microsoft UI Automation provider is a software object that exposes an element of an application's UI so that accessibility client applications can retrieve information about the element and invoke its functionality.</span></span> <span data-ttu-id="63816-117">Как правило, каждый элемент управления или другой отдельный элемент в пользовательском интерфейсе имеет поставщик.</span><span class="sxs-lookup"><span data-stu-id="63816-117">In general, each control or other distinct element in a UI has a provider.</span></span>

<span data-ttu-id="63816-118">Корпорация Майкрософт предоставляет поставщик для каждого из стандартных элементов управления, предоставляемых Microsoft Win32, Windows Forms и Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="63816-118">Microsoft includes a provider for each of the standard controls that are supplied with Microsoft Win32, Windows Forms, and Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="63816-119">Это означает, что стандартные элементы управления автоматически предоставляются клиентам автоматизации пользовательского интерфейса. нет необходимости реализовывать интерфейсы специальных возможностей для стандартных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="63816-119">This means that the standard controls are automatically exposed to UI Automation clients; you do not need to implement any accessibility interfaces for the standard controls.</span></span>

<span data-ttu-id="63816-120">Если приложение содержит пользовательские элементы управления, необходимо реализовать поставщики автоматизации пользовательского интерфейса для этих элементов управления, чтобы сделать их доступными для клиентских приложений со специальными возможностями.</span><span class="sxs-lookup"><span data-stu-id="63816-120">If your application includes any custom controls, you need to implement UI Automation providers for those controls to make them accessible to accessibility client applications.</span></span> <span data-ttu-id="63816-121">Также необходимо реализовать поставщики для любых сторонних элементов управления, которые не включают в себя поставщика.</span><span class="sxs-lookup"><span data-stu-id="63816-121">You also need to implement providers for any third party controls that do not include a provider.</span></span> <span data-ttu-id="63816-122">Поставщик реализуется путем реализации интерфейсов поставщиков автоматизации пользовательского интерфейса и интерфейсов шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="63816-122">You implement a provider by implementing UI Automation provider interfaces and control pattern interfaces.</span></span>

<span data-ttu-id="63816-123">В этом разделе приводятся общие сведения о том, как разработчики элементов управления реализуют поставщики автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="63816-123">This topic provides an overview of how control developers implement UI Automation providers.</span></span> <span data-ttu-id="63816-124">Он включает в себя следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="63816-124">It includes the following sections.</span></span>

-   [<span data-ttu-id="63816-125">Типы поставщиков</span><span class="sxs-lookup"><span data-stu-id="63816-125">Types of Providers</span></span>](#types-of-providers)
-   [<span data-ttu-id="63816-126">Основные понятия поставщиков автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="63816-126">UI Automation Provider Concepts</span></span>](#ui-automation-provider-concepts)
    -   <span data-ttu-id="63816-127">[Elements (XElement Dynamic Property)](#elements) (Elements (Динамическое свойство XElement))</span><span class="sxs-lookup"><span data-stu-id="63816-127">[Elements](#elements)</span></span>
    -   [<span data-ttu-id="63816-128">Платформы</span><span class="sxs-lookup"><span data-stu-id="63816-128">Frameworks</span></span>](#frameworks)
    -   [<span data-ttu-id="63816-129">Фрагменты</span><span class="sxs-lookup"><span data-stu-id="63816-129">Fragments</span></span>](#fragments)
    -   [<span data-ttu-id="63816-130">Узлы</span><span class="sxs-lookup"><span data-stu-id="63816-130">Hosts</span></span>](#hosts)
-   [<span data-ttu-id="63816-131">См. также</span><span class="sxs-lookup"><span data-stu-id="63816-131">Related topics</span></span>](#related-topics)

## <a name="types-of-providers"></a><span data-ttu-id="63816-132">Типы поставщиков</span><span class="sxs-lookup"><span data-stu-id="63816-132">Types of Providers</span></span>

<span data-ttu-id="63816-133">Поставщики автоматизации пользовательского интерфейса делятся на две категории: поставщики на стороне сервера и поставщики (или *прокси*) на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="63816-133">UI Automation providers fall into two categories: server-side providers, and client-side (or *proxy*) providers.</span></span>

<span data-ttu-id="63816-134">Поставщик на стороне сервера — это объект, такой как пользовательский элемент управления, который содержит собственную реализацию соответствующих интерфейсов поставщика автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="63816-134">A server-side provider is an object, such as a custom control, that contains its own native implementation of the relevant UI Automation provider interfaces.</span></span> <span data-ttu-id="63816-135">Поставщик на стороне сервера взаимодействует с клиентскими приложениями через границу процесса, предоставляя свою реализацию интерфейсов поставщика ядру автоматизации пользовательского интерфейса, который службы запрашивают запросы от клиентов.</span><span class="sxs-lookup"><span data-stu-id="63816-135">A server-side provider communicates with client applications across the process boundary by exposing its implementation of the provider interfaces to the UI Automation core, which services requests from clients.</span></span> <span data-ttu-id="63816-136">Дополнительные сведения о поставщиках на стороне сервера см. [в разделе Реализация поставщика автоматизации пользовательского интерфейса Server-Side](uiauto-serversideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="63816-136">For more information about server-side providers, see [Implementing a Server-Side UI Automation Provider](uiauto-serversideprovider.md).</span></span>

<span data-ttu-id="63816-137">Поставщик на стороне клиента или прокси-сервер — это объект, реализующий интерфейсы поставщика автоматизации пользовательского интерфейса от имени элемента управления, не включающий полную реализацию поставщика.</span><span class="sxs-lookup"><span data-stu-id="63816-137">A client-side provider, or proxy, is an object that implements UI Automation provider interfaces on behalf of a control does not include a full provider implementation of its own.</span></span> <span data-ttu-id="63816-138">Без прокси-сервера такой элемент управления в значительной степени непрозрачен для автоматизации пользовательского интерфейса, который может предоставлять только основные сведения, доступные из дескриптора окна (**HWND**), например расположения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="63816-138">Without a proxy, such a control is largely opaque to UI Automation, which can supply only basic information available from the window handle (**HWND**), such as the control location.</span></span> <span data-ttu-id="63816-139">Как правило, поставщики прокси взаимодействуют с приложением через границу процесса, отправляя и получая сообщения Windows.</span><span class="sxs-lookup"><span data-stu-id="63816-139">Typically, proxy providers communicate with the application across the process boundary by sending and receiving Windows messages.</span></span> <span data-ttu-id="63816-140">Дополнительные сведения см. [в разделе Реализация поставщика автоматизации пользовательского интерфейса Client-Side (прокси)](uiauto-clientsideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="63816-140">For more information, see [Implementing a Client-Side (Proxy) UI Automation Provider](uiauto-clientsideprovider.md).</span></span>

## <a name="ui-automation-provider-concepts"></a><span data-ttu-id="63816-141">Основные понятия поставщиков автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="63816-141">UI Automation Provider Concepts</span></span>

<span data-ttu-id="63816-142">В этом разделе содержится краткое описание некоторых ключевых понятий, которые необходимо знать для реализации поставщиков автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="63816-142">This section provides brief explanations of some of the key concepts you need to understand in order to implement UI Automation providers.</span></span>

### <a name="elements"></a><span data-ttu-id="63816-143">Элементы</span><span class="sxs-lookup"><span data-stu-id="63816-143">Elements</span></span>

<span data-ttu-id="63816-144">Элементы модели автоматизации пользовательского интерфейса — это фрагменты пользовательского интерфейса — обычно окна или элементы управления, которые видимы для клиентов автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="63816-144">UI Automation elements are pieces of the UI—typically windows or controls—that are visible to UI Automation clients.</span></span> <span data-ttu-id="63816-145">В качестве примеров можно привести окна приложений, панели, кнопки, подсказки, списки и элементы списков.</span><span class="sxs-lookup"><span data-stu-id="63816-145">Examples include application windows, panes, buttons, tooltips, list boxes, and list items.</span></span>

<span data-ttu-id="63816-146">Элементы модели автоматизации пользовательского интерфейса предоставляются клиентам в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="63816-146">UI Automation elements are exposed to clients as a tree.</span></span> <span data-ttu-id="63816-147">Модель автоматизации пользовательского интерфейса конструирует дерево путем перехода от одного элемента к другому.</span><span class="sxs-lookup"><span data-stu-id="63816-147">UI Automation constructs the tree by navigating from one element to another.</span></span> <span data-ttu-id="63816-148">Для каждого элемента Навигация включается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="63816-148">Navigation is enabled by the provider for each element.</span></span> <span data-ttu-id="63816-149">Каждый элемент может указывать на собственный родительский элемент, его родственные элементы, а также его первый и последний дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="63816-149">Each element can point to its own parent element, its sibling elements, and its first and last child elements.</span></span>

<span data-ttu-id="63816-150">Клиент может видеть дерево модели автоматизации пользовательского интерфейса в трех основных представлениях, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="63816-150">A client can see the UI Automation tree in three principal views, as described in the following table:</span></span>



| <span data-ttu-id="63816-151">Представление</span><span class="sxs-lookup"><span data-stu-id="63816-151">View</span></span>         | <span data-ttu-id="63816-152">Описание</span><span class="sxs-lookup"><span data-stu-id="63816-152">Description</span></span>                                                    |
|--------------|----------------------------------------------------------------|
| <span data-ttu-id="63816-153">Базовое представление</span><span class="sxs-lookup"><span data-stu-id="63816-153">Raw view</span></span>     | <span data-ttu-id="63816-154">Включает все элементы.</span><span class="sxs-lookup"><span data-stu-id="63816-154">Includes all elements.</span></span>                                         |
| <span data-ttu-id="63816-155">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="63816-155">Control view</span></span> | <span data-ttu-id="63816-156">Включает элементы, которые являются элементами управления.</span><span class="sxs-lookup"><span data-stu-id="63816-156">Includes elements that are controls.</span></span>                           |
| <span data-ttu-id="63816-157">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="63816-157">Content view</span></span> | <span data-ttu-id="63816-158">Включает элементы управления, которые сообщают пользователю информацию.</span><span class="sxs-lookup"><span data-stu-id="63816-158">Includes control elements that convey information to the user.</span></span> |



 

<span data-ttu-id="63816-159">Поставщик в своей реализации определяет элемент как элемент содержимого или элемент управления.</span><span class="sxs-lookup"><span data-stu-id="63816-159">It is the responsibility of the provider implementation to define an element as a content element or a control element.</span></span> <span data-ttu-id="63816-160">Элементы управления могут быть или не быть также и элементами содержимого, но все элементы содержимого являются элементами управления.</span><span class="sxs-lookup"><span data-stu-id="63816-160">Control elements may or may not also be content elements, but all content elements are control elements.</span></span>

<span data-ttu-id="63816-161">Дополнительные сведения о клиентском представлении дерева см. в разделе [Общие сведения о дереве автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="63816-161">For more information on the client view of the tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

### <a name="frameworks"></a><span data-ttu-id="63816-162">Платформы</span><span class="sxs-lookup"><span data-stu-id="63816-162">Frameworks</span></span>

<span data-ttu-id="63816-163">Инфраструктура — это компонент, который управляет дочерними элементами управления, проверкой попадания и визуализацией в области экрана.</span><span class="sxs-lookup"><span data-stu-id="63816-163">A framework is a component that manages child controls, hit-testing, and rendering in an area of the screen.</span></span> <span data-ttu-id="63816-164">Например, окно Win32, которое часто называют **HWND**, может служить платформой, содержащей несколько элементов автоматизации пользовательского интерфейса, таких как строка меню, строка состояния и кнопки.</span><span class="sxs-lookup"><span data-stu-id="63816-164">For example, a Win32 window, often referred to as an **HWND**, can serve as a framework that contains multiple UI Automation elements, such as a menu bar, a status bar, and buttons.</span></span>

<span data-ttu-id="63816-165">Элементы управления контейнера Win32, такие как списки и элементы управления древовидного представления, считаются платформами, поскольку они содержат собственный код для отрисовки дочерних элементов и выполнения проверки попадания на них.</span><span class="sxs-lookup"><span data-stu-id="63816-165">Win32 container controls such as list boxes and tree-view controls are considered to be frameworks because they contain their own code for rendering child items and performing hit-testing on them.</span></span> <span data-ttu-id="63816-166">В отличие от этого, список WPF не является платформой, поскольку отрисовка и проверка попадания обрабатываются содержащим окном.</span><span class="sxs-lookup"><span data-stu-id="63816-166">By contrast, a WPF list box is not a framework, because the rendering and hit-testing is being handled by the containing window.</span></span>

<span data-ttu-id="63816-167">Пользовательский интерфейс в приложении может состоять из различных платформ.</span><span class="sxs-lookup"><span data-stu-id="63816-167">The UI in an application can be made up of different frameworks.</span></span> <span data-ttu-id="63816-168">Например, **HWND** в приложении может содержать динамический HTML (DHTML), который, в свою очередь, может содержать компонент, например поле со списком в **HWND**.</span><span class="sxs-lookup"><span data-stu-id="63816-168">For example, an **HWND** in an application might contain Dynamic HTML (DHTML) which in turn can contain a component such as a combo box in an **HWND**.</span></span>

### <a name="fragments"></a><span data-ttu-id="63816-169">Fragments</span><span class="sxs-lookup"><span data-stu-id="63816-169">Fragments</span></span>

<span data-ttu-id="63816-170">Полное поддерево элементов из определенной платформы называется фрагментом.</span><span class="sxs-lookup"><span data-stu-id="63816-170">A complete subtree of elements from a particular framework is called a fragment.</span></span> <span data-ttu-id="63816-171">Элемент на уровне корневого узла поддерева называется корнем фрагмента.</span><span class="sxs-lookup"><span data-stu-id="63816-171">The element at the root node of the subtree is called a fragment root.</span></span> <span data-ttu-id="63816-172">У корня фрагмента нет родителя, но он размещается в другой инфраструктуре, обычно в окне Win32 (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="63816-172">A fragment root does not have a parent, but is hosted within some other framework, usually a Win32 window (**HWND**).</span></span>

### <a name="hosts"></a><span data-ttu-id="63816-173">Узлы</span><span class="sxs-lookup"><span data-stu-id="63816-173">Hosts</span></span>

<span data-ttu-id="63816-174">Корневой узел каждого фрагмента должен размещаться в элементе, обычно в окне Win32 (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="63816-174">The root node of every fragment must be hosted in an element, usually a Win32 window (**HWND**).</span></span> <span data-ttu-id="63816-175">Исключением является рабочий стол, который не размещается ни в каком другом элементе.</span><span class="sxs-lookup"><span data-stu-id="63816-175">The exception is the desktop, which is not hosted in any other element.</span></span> <span data-ttu-id="63816-176">Узел пользовательского элемента управления — это **HWND** самого элемента управления, а не окна приложения или любого другого окна, которое может содержать группы элементов управления верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="63816-176">The host of a custom control is the **HWND** of the control itself, not the application window or any other window that might contain groups of top-level controls.</span></span>

<span data-ttu-id="63816-177">Узел фрагмента играет важную роль в предоставлении служб автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="63816-177">The host of a fragment plays an important role in providing UI Automation services.</span></span> <span data-ttu-id="63816-178">Он позволяет навигацию в корень фрагмента и предоставляет некоторые свойства по умолчанию, чтобы настраиваемому поставщику не требовалось реализовывать их.</span><span class="sxs-lookup"><span data-stu-id="63816-178">It enables navigation to the fragment root, and supplies some default properties so that the custom provider does not have to implement them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63816-179">См. также</span><span class="sxs-lookup"><span data-stu-id="63816-179">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="63816-180">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="63816-180">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="63816-181">Реализация поставщика автоматизации пользовательского интерфейса Client-Side</span><span class="sxs-lookup"><span data-stu-id="63816-181">Implementing a Client-Side UI Automation Provider</span></span>](uiauto-clientsideprovider.md)
</dt> <dt>

[<span data-ttu-id="63816-182">Реализация поставщика автоматизации пользовательского интерфейса Server-Side</span><span class="sxs-lookup"><span data-stu-id="63816-182">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="63816-183">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="63816-183">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




