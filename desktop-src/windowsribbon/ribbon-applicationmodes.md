---
title: Перенастройка ленты с помощью режимов приложения
description: Платформа Windows Ribbon поддерживает динамическую перенастройку и предоставление основных элементов пользовательского интерфейса Ribbon во время выполнения на основе состояния приложения (также называемого контекстом).
ms.assetid: 8e9d85c5-33e4-4212-b9e4-2fc3b492c273
keywords:
- Лента Windows, перенастройка в режимах приложений
- Лента, повторная настройка с использованием режимов приложения
- Перенастройка ленты Windows с использованием режимов приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d206c238e6fe7463562077daaa52a5522a79d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412979"
---
# <a name="reconfiguring-the-ribbon-with-application-modes"></a><span data-ttu-id="8e7d6-106">Перенастройка ленты с помощью режимов приложения</span><span class="sxs-lookup"><span data-stu-id="8e7d6-106">Reconfiguring the Ribbon with Application Modes</span></span>

<span data-ttu-id="8e7d6-107">Платформа Windows Ribbon поддерживает динамическую перенастройку и предоставление основных элементов пользовательского интерфейса Ribbon во время выполнения на основе состояния приложения (также называемого контекстом).</span><span class="sxs-lookup"><span data-stu-id="8e7d6-107">The Windows Ribbon framework supports the dynamic reconfiguring and exposing of core elements of the Ribbon UI at run time, based on the application's state (also referred to as context).</span></span> <span data-ttu-id="8e7d6-108">Объявления и связанные с определенными элементами в разметке, различные состояния, поддерживаемые приложением, называются режимами приложения.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-108">Declared and associated with specific elements in markup, the various states supported by an application are referred to as application modes.</span></span>

-   [<span data-ttu-id="8e7d6-109">Введение</span><span class="sxs-lookup"><span data-stu-id="8e7d6-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="8e7d6-110">Контекстный пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="8e7d6-110">Contextual User Interface</span></span>](#contextual-user-interface)
    -   [<span data-ttu-id="8e7d6-111">Простой сценарий режима приложения</span><span class="sxs-lookup"><span data-stu-id="8e7d6-111">A Simple Application Mode Scenario</span></span>](#a-simple-application-mode-scenario)
-   [<span data-ttu-id="8e7d6-112">Реализация режимов приложения</span><span class="sxs-lookup"><span data-stu-id="8e7d6-112">Implementing Application Modes</span></span>](#implementing-application-modes)
    -   [<span data-ttu-id="8e7d6-113">Идентифицируйте режимы</span><span class="sxs-lookup"><span data-stu-id="8e7d6-113">Identify the Modes</span></span>](#identify-the-modes)
    -   [<span data-ttu-id="8e7d6-114">Назначение элементов управления режимам приложений</span><span class="sxs-lookup"><span data-stu-id="8e7d6-114">Assign Controls to Application Modes</span></span>](#assign-controls-to-application-modes)
    -   [<span data-ttu-id="8e7d6-115">Переключение режимов во время выполнения</span><span class="sxs-lookup"><span data-stu-id="8e7d6-115">Switch Modes at Runtime</span></span>](#switch-modes-at-runtime)
-   [<span data-ttu-id="8e7d6-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="8e7d6-116">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="8e7d6-117">См. также</span><span class="sxs-lookup"><span data-stu-id="8e7d6-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="8e7d6-118">Введение</span><span class="sxs-lookup"><span data-stu-id="8e7d6-118">Introduction</span></span>

<span data-ttu-id="8e7d6-119">Режимы приложений состоят из логических групп элементов управления, предоставляющих некоторые основные функциональные возможности приложений в пользовательском интерфейсе Ribbon.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-119">Application modes consist of logical groups of controls that expose some core application functionality in the Ribbon UI.</span></span> <span data-ttu-id="8e7d6-120">Эти режимы динамически включаются или отключаются приложением с помощью вызова метода Framework [**иуифрамеворк:: сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes), который включает или выключает видимость одного или нескольких режимов приложения.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-120">These modes are dynamically enabled or disabled by the application through a call to the framework method [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes), which turns the visibility of one or more application modes on or off.</span></span>

## <a name="contextual-user-interface"></a><span data-ttu-id="8e7d6-121">Контекстный пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="8e7d6-121">Contextual User Interface</span></span>

<span data-ttu-id="8e7d6-122">Платформа Ribbon обеспечивает широкие возможности взаимодействия с пользователем, включая динамические элементы управления, которые легко реагируют на взаимодействие с пользователем и контекст приложения.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-122">The Ribbon framework provides rich user experience by incorporating dynamic controls that respond seamlessly to user interaction and application context.</span></span> <span data-ttu-id="8e7d6-123">Этот богатый контекстный пользовательский интерфейс доставляется с помощью сочетания следующих механизмов:</span><span class="sxs-lookup"><span data-stu-id="8e7d6-123">This rich contextual UI is delivered through a combination of the following mechanisms:</span></span>

-   <span data-ttu-id="8e7d6-124">Коллекции элементов управления, которые поддерживают динамическую обработку коллекций элементов.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-124">Galleries - collection-based controls that support the dynamic manipulation of their item collections.</span></span>
-   <span data-ttu-id="8e7d6-125">Контекстные вкладки — вкладки ленты, видимость которых определяется изменением контекста рабочей области, например выбором изображения в документе.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-125">Contextual tabs - ribbon tabs that have their visibility determined by a change in workspace context, such as the selection of an image in a document.</span></span>
-   <span data-ttu-id="8e7d6-126">Режимы приложений — основные функциональные возможности приложения, зависящие от контекста приложения.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-126">Application modes - core application functionality that is dependent on application context.</span></span>

<span data-ttu-id="8e7d6-127">В некоторых отношениях режимы приложения функционально похожи на контекстные вкладки.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-127">In some respects, application modes appear functionally similar to contextual tabs.</span></span> <span data-ttu-id="8e7d6-128">Однако фундаментальное различие заключается в намерениях и области каждого из них.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-128">However, the fundamental distinction lies in the intent and scope of each.</span></span>

<span data-ttu-id="8e7d6-129">Контекстные элементы управления активируются в ответ на изменение контекста в приложении.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-129">Contextual controls are activated in response to a change of context within an application.</span></span> <span data-ttu-id="8e7d6-130">Например, в Microsoft Paint для Windows 7 контекстная вкладка, содержащая группы команд, связанных с текстом, отображается, когда пользователь вставляет текстовую область в рабочую область.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-130">For example, in Microsoft Paint for Windows 7, a contextual tab that contains groups of text-related commands is displayed when a user inserts a text area into the workspace.</span></span> <span data-ttu-id="8e7d6-131">Эта контекстная вкладка не содержит основных команд для приложения и предоставляется только в пользовательском интерфейсе, так как контекст *в* приложении изменился.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-131">This contextual tab does not contain core commands for the application and is only exposed in the UI because the context *within* the application has changed.</span></span> <span data-ttu-id="8e7d6-132">Основные функциональные возможности приложения (команды редактирования изображений) по-прежнему связаны и доступны пользователю, даже если отображается контекстная вкладка.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-132">The core functionality of the application (the image editing commands) is still relevant and available to the user, even with the contextual tab visible.</span></span>

<span data-ttu-id="8e7d6-133">Режимы приложений отличаются от контекстных элементов управления тем, что они перестраивают функциональность в ответ на изменения в контексте, в котором работает приложение.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-133">Application modes differ from contextual controls in that they reconfigure functionality in response to changes in the context that the application is operating in.</span></span> <span data-ttu-id="8e7d6-134">Режимы приложений располагаются на более высоком уровне абстракции; они предоставляют способ перенастройки основных функций приложения вместо временного предоставления функциональных возможностей, которые не являются основными компонентами пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-134">Application modes sit at a higher level of abstraction; they provide a way to reconfigure the core functionality of an application instead of temporarily exposing functionality that is not a core component of the UI.</span></span> <span data-ttu-id="8e7d6-135">Например, в Microsoft Paint для Windows 7 параметр в режиме приложения возникает при вызове команды **предварительного просмотра** .</span><span class="sxs-lookup"><span data-stu-id="8e7d6-135">For example, in Microsoft Paint for Windows 7, a switch in application mode occurs when the **Print preview** command is invoked.</span></span> <span data-ttu-id="8e7d6-136">Когда Microsoft Paint переключается на **Предварительный просмотр**, контекст, в котором выполняется приложение, изменяется от редактирования до предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-136">When Microsoft Paint switches to **Print preview**, the context that the application is operating in changes from editing to previewing.</span></span> <span data-ttu-id="8e7d6-137">В результате основные функциональные возможности приложения меняются до тех пор, пока **Предварительный просмотр** не будет отменен и приложение снова войдет в контекст редактирования.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-137">As a result, the core functionality of the application changes until the **Print preview** is canceled and the application enters the editing context again.</span></span>

### <a name="a-simple-application-mode-scenario"></a><span data-ttu-id="8e7d6-138">Простой сценарий режима приложения</span><span class="sxs-lookup"><span data-stu-id="8e7d6-138">A Simple Application Mode Scenario</span></span>

<span data-ttu-id="8e7d6-139">В следующем сценарии показано использование режимов приложения в приложении с именем Риббонапп для предоставления дискретных аспектов основных функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-139">The following scenario demonstrates how application modes are used, in an application called RibbonApp, to expose discrete aspects of core functionality.</span></span>

<span data-ttu-id="8e7d6-140">В Риббонапп определены два режима приложений:</span><span class="sxs-lookup"><span data-stu-id="8e7d6-140">Two application modes are defined in RibbonApp:</span></span>

-   <span data-ttu-id="8e7d6-141">**Простой** режим предоставляет основные команды в пользовательском интерфейсе ленты.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-141">**Simple** mode exposes basic commands throughout the Ribbon UI.</span></span> <span data-ttu-id="8e7d6-142">Эти команды отображаются всегда, независимо от того, какой режим приложения активен.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-142">These commands appear at all times, no matter which application mode is active.</span></span>
-   <span data-ttu-id="8e7d6-143">**Расширенный** режим предоставляет сложные команды, предназначенные для опытных пользователей приложения.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-143">**Advanced** mode exposes complex commands intended for expert users of the application.</span></span> <span data-ttu-id="8e7d6-144">Эти расширенные команды отображаются в пользовательском интерфейсе ленты в дополнение к простым командам.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-144">These advanced commands appear throughout the Ribbon UI, in addition to the simple commands.</span></span>

<span data-ttu-id="8e7d6-145">По умолчанию Риббонапп имеет значение открыть в **простом** режиме, а команды, необходимые начинающим пользователям, отображаются в **меню приложение** и на вкладке **Главная** . На следующем снимке экрана показано **меню приложения** риббонапп и вкладка **Главная** в **простом** режиме, в которых выделяются модальные элементы управления.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-145">By default, RibbonApp is set to open in **Simple** mode, and the commands required by novice users are displayed in the **Application Menu** and the **Home** tab. The following screen shots show the RibbonApp **Application Menu** and **Home** tab in **Simple** mode, highlighting the modal controls.</span></span>

![снимок экрана, на котором показана вкладка для режима простого приложения.](images/overviews/appmode-hometab.png)![снимок экрана, показывающий меню приложения для режима простого приложения.](images/overviews/appmode-simpleappmenu.png)

<span data-ttu-id="8e7d6-148">Хотя эти команды могут быть достаточными для начинающих пользователей, Риббонапп также поддерживает опытных пользователей в **расширенном** режиме, что при активации с помощью кнопки **переключиться на расширенный режим** в **меню приложение** отображаются дополнительные основные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-148">While these commands may be sufficient for novice users, the RibbonApp also supports expert users through an **Advanced** mode that, when activated by clicking the **Switch to Advanced Mode** button in the **Application Menu**, displays additional core functionality.</span></span>

<span data-ttu-id="8e7d6-149">Этот сценарий легко реализовать путем привязки различных элементов в разметке к дискретным режимам приложений, которые могут быть включены и отключены по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-149">This scenario is easily implemented by binding various elements in markup to discrete application modes that can be turned on and off as required.</span></span> <span data-ttu-id="8e7d6-150">На следующих снимках экрана показано **меню приложения** риббонапп и вкладка **Главная** в **расширенном** режиме, в которых выделяются модальные элементы управления.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-150">The following screen shots show the RibbonApp **Application Menu** and **Home** tab in **Advanced** mode, highlighting the modal controls.</span></span>

![снимок экрана, на котором показана вкладка для расширенного режима приложения.](images/overviews/appmode-advancedtab.png)![снимок экрана с меню приложения для режима расширенного приложения.](images/overviews/appmode-advancedappmenu.png)

## <a name="implementing-application-modes"></a><span data-ttu-id="8e7d6-153">Реализация режимов приложения</span><span class="sxs-lookup"><span data-stu-id="8e7d6-153">Implementing Application Modes</span></span>

<span data-ttu-id="8e7d6-154">В этом разделе описаны три действия, которые обычно необходимы для реализации режимов работы платформы ленты.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-154">This section outlines the three steps typically required for the implementation of Ribbon framework application modes.</span></span> <span data-ttu-id="8e7d6-155">Риббонапп используется для предоставления примера для каждого шага.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-155">RibbonApp is used to provide an example for each step.</span></span>

### <a name="identify-the-modes"></a><span data-ttu-id="8e7d6-156">Идентифицируйте режимы</span><span class="sxs-lookup"><span data-stu-id="8e7d6-156">Identify the Modes</span></span>

<span data-ttu-id="8e7d6-157">Каждый режим в приложении должен представлять собой логический набор функциональных возможностей, которые зависят от контекста, в котором приложение может выполнять работу.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-157">Each mode in an application should represent a logical set of functionality that depends on the context an application is able to operate in.</span></span> <span data-ttu-id="8e7d6-158">Например, если приложение отображает элементы управления, которые имеют смысл только при обнаружении сетевого подключения, эти элементы управления работают в контексте сети, который может по высоте создавать **сетевой** режим.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-158">For example, if an application displays controls that are only relevant when a network connection is detected, those controls operate within a networking context that might justify the creation of a **Network** mode.</span></span>

<span data-ttu-id="8e7d6-159">Риббонапп имеет два контекста, которые могут быть активными в любое заданное время: **Simple** и **Advanced**.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-159">RibbonApp has two contexts that can be active at any given time: **Simple** and **Advanced**.</span></span> <span data-ttu-id="8e7d6-160">Поэтому для Риббонапп требуется два режима: **простой** и **Расширенный**.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-160">Therefore, RibbonApp requires two modes: **Simple** and **Advanced**.</span></span>

### <a name="assign-controls-to-application-modes"></a><span data-ttu-id="8e7d6-161">Назначение элементов управления режимам приложений</span><span class="sxs-lookup"><span data-stu-id="8e7d6-161">Assign Controls to Application Modes</span></span>

<span data-ttu-id="8e7d6-162">После определения режимов приложения присвойте каждому элементу управления Ribbon режим, объявляя атрибут *аппликатионмодес* в разметке для элементов управления, поддерживающих режимы приложений.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-162">Once the application modes have been identified, assign each Ribbon control to a mode by declaring an *ApplicationModes* attribute in markup for those control elements that support application modes.</span></span>

<span data-ttu-id="8e7d6-163">Представление ленты позволяет задавать режимы для следующих элементов управления:</span><span class="sxs-lookup"><span data-stu-id="8e7d6-163">The Ribbon View allows modes to be specified on the following control elements:</span></span>

-   <span data-ttu-id="8e7d6-164">Основные элементы [**вкладки**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="8e7d6-164">Core [**Tab**](windowsribbon-element-tab.md) elements.</span></span>
-   <span data-ttu-id="8e7d6-165">Элементы [**группы**](windowsribbon-element-group.md) , являющиеся дочерними элементами базового элемента [**вкладки**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="8e7d6-165">[**Group**](windowsribbon-element-group.md) elements that are child elements of a core [**Tab**](windowsribbon-element-tab.md) element.</span></span>
-   <span data-ttu-id="8e7d6-166">Элементы [**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md)и [**DropDownButton**](windowsribbon-element-dropdownbutton.md) , назначенные элементу [**менуграуп**](windowsribbon-element-menugroup.md) в [меню приложения](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="8e7d6-166">[**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md), and [**DropDownButton**](windowsribbon-element-dropdownbutton.md) elements assigned to a [**MenuGroup**](windowsribbon-element-menugroup.md) within the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="8e7d6-167">Элементы [**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md)и [**DropDownButton**](windowsribbon-element-dropdownbutton.md) не могут быть назначены в режиме, если они не размещены в [меню приложения](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="8e7d6-167">[**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md), and [**DropDownButton**](windowsribbon-element-dropdownbutton.md) elements cannot be assigned to a mode unless hosted in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

     

<span data-ttu-id="8e7d6-168">В платформе Ribbon эти элементы управления называются модальными элементами управления.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-168">In the Ribbon framework, these control elements are referred to as modal controls.</span></span> <span data-ttu-id="8e7d6-169">Они отображаются, только если в пользовательском интерфейсе активен режим, к которому они привязаны.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-169">They appear only if a mode to which they are bound is active in the UI.</span></span>

<span data-ttu-id="8e7d6-170">Элементы управления, содержащиеся в модальном элементе управления, наследуют поведение режима приложения.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-170">Control elements that are contained within a modal control inherit the application mode behavior.</span></span> <span data-ttu-id="8e7d6-171">Например, если модальный элемент управления [**группы**](windowsribbon-element-group.md) назначен **расширенному** режиму, а **Расширенный** режим неактивен, то эта **Группа** и все элементы управления в ней, модальные или другие, не будут отображаться в ленте.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-171">For example, if a [**Group**](windowsribbon-element-group.md) modal control is assigned to an **Advanced** mode and the **Advanced** mode is not active, then that **Group** and any controls in it, modal or otherwise, will not be visible in the Ribbon UI.</span></span>

<span data-ttu-id="8e7d6-172">При использовании атрибута *аппликатионмодес* режимы присваиваются модальным элементам управления в связи 1: N (один ко многим), где один модальный элемент управления может быть связан с несколькими режимами.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-172">With the use of the *ApplicationModes* attribute, modes are assigned to modal controls in a 1:N (one-to-many) relationship, where a single modal control can be associated with several modes.</span></span>

<span data-ttu-id="8e7d6-173">Платформа ленты относится к режимам с цифрами от 0 до 31. режим 0 считался режимом по умолчанию, который автоматически активируется при запуске приложения Ribbon.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-173">The Ribbon framework refers to modes numerically, from 0 to 31, with mode 0 considered the default mode that is automatically activated when a Ribbon application starts.</span></span> <span data-ttu-id="8e7d6-174">Любой модальный элемент управления, не указывающий атрибут *аппликатионмодес* , считается членом режима по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-174">Any modal control that does not specify an *ApplicationModes* attribute is considered to be a member of the default mode.</span></span>

<span data-ttu-id="8e7d6-175">В Риббонапп используется режим по умолчанию с **расширенными** функциями режима **, который отображается** только в том случае, если он инициирован пользователем.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-175">In RibbonApp, **Simple** is the default mode, with **Advanced** mode functionality displayed only when it is initiated by the user.</span></span>

<span data-ttu-id="8e7d6-176">В следующем примере показана разметка, необходимая для Риббонапп.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-176">The following example demonstrates the markup required for RibbonApp.</span></span>


```C++
<Application.Views>
  <Ribbon>

    <!--Application Menu-->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName='cmdAppMenu'>                    
        <MenuGroup>
          <Button CommandName='cmdSave'/>                        
          <Button CommandName='cmdExportMetadata' ApplicationModes='1'/>                   
        </MenuGroup>              
        <MenuGroup>
          <Button CommandName='cmdSwitchModes' ApplicationModes ='0,1'/>
          <Button CommandName='cmdExit'/>
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
            
    <!--Tabs-->
    <Ribbon.Tabs>
      <!--Home Tab-->
      <Tab CommandName='cmdHomeTab'>
                    
        <!--Scaling Policy for Home tab-->
        <Tab.ScalingPolicy>
          <ScalingPolicy>
            <ScalingPolicy.IdealSizes>
              <Scale Group='cmdSimpleControlsGroup' Size='Medium'/>                                
            </ScalingPolicy.IdealSizes>                     
          </ScalingPolicy>
        </Tab.ScalingPolicy>     
                    
        <!--Simple Controls Group-->
        <Group CommandName='cmdSimpleControlsGroup' SizeDefinition='ThreeButtons-OneBigAndTwoSmall'>                        
          <Button CommandName="cmdPaste" />
          <Button CommandName='cmdCut'/>                        
          <Button CommandName='cmdCopy'/>                        
        </Group>
      </Tab>
                
      <!--Advanced Tab-->
      <Tab CommandName='cmdAdvancedTab' ApplicationModes='1'>
        <!--Advanced Controls Group-->
        <Group CommandName='cmdMetadataGroup' ApplicationModes='1' SizeDefinition='TwoButtons'>
          <Button CommandName='cmdEditMetadata' />
          <Button CommandName='cmdCheckErrors' />
        </Group>
      </Tab>
    </Ribbon.Tabs>                   
                             
  </Ribbon>         
</Application.Views>
```



<span data-ttu-id="8e7d6-177">В этом примере показано следующее:</span><span class="sxs-lookup"><span data-stu-id="8e7d6-177">This example demonstrates the following:</span></span>

-   <span data-ttu-id="8e7d6-178">Режим по умолчанию 0 не требуется объявлять явным образом.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-178">Default mode 0 does not need to be explicitly declared.</span></span> <span data-ttu-id="8e7d6-179">Поскольку модальные элементы управления, не указывающие атрибут *аппликатионмодес* , автоматически привязываются к Mode 0 (**простой** режим в примере риббонапп), нет необходимости явно объявлять атрибут для модальных элементов управления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-179">Because modal controls that do not specify the *ApplicationModes* attribute are automatically bound to mode 0 (**Simple** mode in the RibbonApp example), there is no need to explicitly declare the attribute for default modal controls.</span></span>
-   <span data-ttu-id="8e7d6-180">Элементы управления могут быть привязаны к нескольким режимам.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-180">Controls can be bound to multiple modes.</span></span> <span data-ttu-id="8e7d6-181">Для Риббонапп единственной потребностью в атрибуте *аппликатионмодес* в элементе управления **простого** режима является `cmdSwitchModes` кнопка, так как она является частью как **простых** , так и **расширенных** режимов.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-181">For RibbonApp, the only need for the *ApplicationModes* attribute in a **Simple** mode control is the `cmdSwitchModes` button , since it is a part of both **Simple** and **Advanced** modes.</span></span> <span data-ttu-id="8e7d6-182">Если один из режимов активен, этот элемент управления появится в [меню приложение](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="8e7d6-182">If either mode is active, this control will appear in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="8e7d6-183">Модальные элементы управления не наследуются от своих родителей.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-183">Modal controls do not inherit from their parents.</span></span> <span data-ttu-id="8e7d6-184">Вкладка **Дополнительно** в риббонапп содержит группу **метаданных** . Оба этих модальных элемента управления назначены режиму 1 (**Расширенный** режим).</span><span class="sxs-lookup"><span data-stu-id="8e7d6-184">The **Advanced** tab of RibbonApp contains a **Metadata** group; both of these modal controls are assigned to mode 1 (**Advanced** mode).</span></span> <span data-ttu-id="8e7d6-185">При назначении вкладки " **Дополнительно** " в режиме 1 дочерние элементы управления, такие как группа **метаданных** , не присваиваются автоматически в режиме 1.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-185">Assigning the **Advanced** tab to mode 1 does not automatically assign child controls, such as the **Metadata** group, to mode 1.</span></span> <span data-ttu-id="8e7d6-186">Это позволяет независимо включать или отключать любую группу на вкладке во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-186">This allows any group within a tab to be independently enabled or disabled at runtime.</span></span>
-   <span data-ttu-id="8e7d6-187">Немодальные элементы управления по-прежнему могут полагаться на переключения режима.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-187">Non-modal controls can still rely on mode switches.</span></span> <span data-ttu-id="8e7d6-188">Кнопки **изменить метаданные** и **проверить на ошибки** в риббонапп предназначены для опытных пользователей и доступны только в том случае, если пользователь переключается в **Расширенный** режим.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-188">The **Edit Metadata** and **Check for Errors** buttons of RibbonApp are for advanced users and available only when the user switches to **Advanced** mode.</span></span> <span data-ttu-id="8e7d6-189">Элементы управления "Кнопка", которые не размещаются в [меню приложения](windowsribbon-controls-applicationmenu.md) , не являются модальными; Однако поскольку эти кнопки размещаются внутри модального элемента управления (группы **метаданных** ), они отображаются, когда группа видима.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-189">Button controls that are not hosted inside the [Application Menu](windowsribbon-controls-applicationmenu.md) are non-modal; however, because these buttons are hosted inside a modal control (the **Metadata** group), they are visible when the group is visible.</span></span> <span data-ttu-id="8e7d6-190">Поэтому эти кнопки появляются при активации расширенного режима, а группа **метаданных** — в пользовательском интерфейсе ленты.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-190">Therefore, these buttons appear when the advanced mode is activated and the **Metadata** group is exposed in the Ribbon UI.</span></span>

### <a name="switch-modes-at-runtime"></a><span data-ttu-id="8e7d6-191">Переключение режимов во время выполнения</span><span class="sxs-lookup"><span data-stu-id="8e7d6-191">Switch Modes at Runtime</span></span>

<span data-ttu-id="8e7d6-192">После определения режимов в разметке их можно легко включить или отключить в ответ на контекстные события.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-192">After modes are defined in markup, they can be easily enabled or disabled in response to contextual events.</span></span> <span data-ttu-id="8e7d6-193">Как упоминалось ранее, приложения ленты всегда запускаются в режиме по умолчанию 0.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-193">As mentioned previously, Ribbon applications always start in the default mode 0.</span></span> <span data-ttu-id="8e7d6-194">После того как приложение инициализировано, а режим 0 активен, набор активных режимов можно изменить, вызвав функцию [**иуифрамеворк:: сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) .</span><span class="sxs-lookup"><span data-stu-id="8e7d6-194">After the application has initialized and mode 0 is active, the set of active modes can be changed by calling the [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) function.</span></span> <span data-ttu-id="8e7d6-195">Эта функция принимает 32-разрядное целое число в качестве побитового представления режимов, которые должны быть активными; Наименьший значащий бит представляет режим 0, а наиболее значимый бит — режим 31.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-195">This function takes a 32-bit integer as a bitwise representation of the modes that should be active; the least significant bit represents mode 0 and the most significant bit represents mode 31.</span></span> <span data-ttu-id="8e7d6-196">Если бит имеет значение 0, то этот режим неактивен в ИНТЕРФЕЙСе ленты.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-196">If a bit is set to zero, the mode is not active in the Ribbon UI.</span></span>

<span data-ttu-id="8e7d6-197">В Риббонапп, когда пользователь включает **Расширенный** режим, расширенные команды отображаются рядом с простыми командами.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-197">In RibbonApp, when a user enables **Advanced** mode, the advanced commands are displayed alongside the simple commands.</span></span> <span data-ttu-id="8e7d6-198">Обработчик команд для кнопки " **переключиться на расширенный режим** " вызывает [**Иуифрамеворк:: сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) , чтобы установить режимы 0 (**простой**) и 1 (**Дополнительно**) в качестве активных в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-198">The command handler for the **Switch to Advanced Mode** button calls [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) in order to set modes 0 (**Simple**) and 1 (**Advanced**) as active in the UI.</span></span> <span data-ttu-id="8e7d6-199">Ниже приведен пример кода Риббонапп для этого вызова функции:</span><span class="sxs-lookup"><span data-stu-id="8e7d6-199">The following example is the RibbonApp code for this function call :</span></span>


```C++
const int SIMPLE_MODE = 0;
const int ADVANCED_MODE = 1;
pFramework->SetModes( UI_MAKEAPPMODE(SIMPLE_MODE) | UI_MAKEAPPMODE(ADVANCED_MODE) );
```



> [!Note]  
> <span data-ttu-id="8e7d6-200">Макрос макеаппмоде в пользовательском интерфейсе платформы Ribbon \_ упрощает задачу настройки этих битов при подготовке к вызову [**иуифрамеворк:: сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes).</span><span class="sxs-lookup"><span data-stu-id="8e7d6-200">The Ribbon framework UI\_MAKEAPPMODE macro simplifies the task of setting these bits correctly in preparation for the call to [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes).</span></span>

 

<span data-ttu-id="8e7d6-201">В этом примере показано следующее:</span><span class="sxs-lookup"><span data-stu-id="8e7d6-201">This example demonstrates the following:</span></span>

-   <span data-ttu-id="8e7d6-202">Используйте \_ макрос макеаппмоде пользовательского интерфейса для создания набора режимов.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-202">Use the UI\_MAKEAPPMODE macro to build a mode set.</span></span>
-   <span data-ttu-id="8e7d6-203">Режимы задаются явным образом и атомарно.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-203">Modes are set explicitly and atomically.</span></span> <span data-ttu-id="8e7d6-204">Целочисленное значение, передаваемое в [**иуифрамеворк:: сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) , представляет режимы, которые будут активны после возврата функции.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-204">The integer value that is passed to [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) represents the modes that will be active after the function returns.</span></span> <span data-ttu-id="8e7d6-205">Хотя **простой** режим был ранее активен, **Иуифрамеворк:: сетмодес** должен указывать, что **простой** режим остается активным при активации **расширенного** режима.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-205">Although the **Simple** mode was previously active, **IUIFramework::SetModes** must indicate that the **Simple** mode remain active when the **Advanced** mode is activated.</span></span>
-   <span data-ttu-id="8e7d6-206">Режим по умолчанию можно удалить.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-206">The default mode can be removed.</span></span> <span data-ttu-id="8e7d6-207">Хотя в Риббонапп режим по умолчанию (Mode 0) никогда не удаляется, его можно удалить с помощью следующего вызова: `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))` , предоставляя только расширенные команды в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-207">Although in RibbonApp the default mode (mode 0) is never removed, it can be removed with the following call: `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))`, exposing only the advanced commands in the UI.</span></span>

> [!Note]  
> <span data-ttu-id="8e7d6-208">При перенастройке режимов приложения лента будет пытаться сохранить ранее выбранную вкладку в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-208">When the modes of an application are reconfigured, the Ribbon will attempt to preserve the previously selected tab in the UI.</span></span> <span data-ttu-id="8e7d6-209">Если новый набор режимов больше не содержит вкладку, выбранную перед вызовом, лента выберет вкладку в макете, которая находится ближе всего к [меню приложения](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="8e7d6-209">If the new set of modes no longer contains the tab that was selected before the call, the Ribbon will select the tab in its layout that is closest to the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="8e7d6-210">Эта вкладка предназначена для того, чтобы содержать команды, наиболее важные для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-210">This tab is meant to contain the commands that are most relevant to the user.</span></span> <span data-ttu-id="8e7d6-211">Дополнительные сведения см. в разделе [руководства пользователя ленты](https://msdn.microsoft.com/library/cc872782.aspx).</span><span class="sxs-lookup"><span data-stu-id="8e7d6-211">For more information, see [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx).</span></span>

 

## <a name="remarks"></a><span data-ttu-id="8e7d6-212">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e7d6-212">Remarks</span></span>

<span data-ttu-id="8e7d6-213">На ленте должен быть хотя бы один активный режим.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-213">The Ribbon must have at least one active mode at all times.</span></span> <span data-ttu-id="8e7d6-214">Если приложение пытается отключить все режимы путем вызова [**иуифрамеворк:: сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) с нулевым значением режима, возвращается ошибка E, \_ а активный режим остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-214">If an application attempts to deactivate all modes by calling [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) with a mode value of 0, E\_FAIL is returned and the active mode set remains unchanged.</span></span>

<span data-ttu-id="8e7d6-215">Для платформы требуется, чтобы в пользовательском интерфейсе ленты существовала хотя бы одна вкладка.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-215">The framework requires that at least one tab exist in the Ribbon UI at all times.</span></span> <span data-ttu-id="8e7d6-216">В результате должна существовать хотя бы одна вкладка, предоставляемая режимом по умолчанию (Mode 0) и после каждого переключения режима.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-216">As a result, there must be at least one tab exposed by the default mode (mode 0) and after each mode switch.</span></span>

<span data-ttu-id="8e7d6-217">В режимах приложения влияют не все области пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-217">Not all areas of the Ribbon UI are affected by application modes.</span></span> <span data-ttu-id="8e7d6-218">Например, если отключение режима приводит к удалению кнопок с ленты, которые ранее были добавлены на [панель быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md), эти кнопки остаются на панели быстрого доступа, что позволяет пользователям выполнять команды, привязанные к кнопкам.</span><span class="sxs-lookup"><span data-stu-id="8e7d6-218">For example, if disabling a mode causes the disappearance of buttons from the Ribbon that were previously added to the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md), those buttons remain in the Quick Access Toolbar, allowing users to execute the Commands bound to the buttons.</span></span> <span data-ttu-id="8e7d6-219">Как правило, если команда принадлежит одному или нескольким неактивным режимам, эту команду также следует отключить, установив свойство [UI \_ PKEY \_ Enabled](windowsribbon-reference-properties-uipkey-enabled.md) в значение 0 (вариант \_ false).</span><span class="sxs-lookup"><span data-stu-id="8e7d6-219">As a general rule, if a Command belongs to one or more inactive modes, then that Command should also be disabled by setting the [UI\_PKEY\_Enabled](windowsribbon-reference-properties-uipkey-enabled.md) property to 0 (VARIANT\_FALSE) .</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e7d6-220">См. также</span><span class="sxs-lookup"><span data-stu-id="8e7d6-220">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e7d6-221">Рекомендации по работе пользователя с лентой</span><span class="sxs-lookup"><span data-stu-id="8e7d6-221">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="8e7d6-222">Отображение контекстных вкладок</span><span class="sxs-lookup"><span data-stu-id="8e7d6-222">Displaying Contextual Tabs</span></span>](ribbon-contextualtabs.md)
</dt> </dl>

 

 