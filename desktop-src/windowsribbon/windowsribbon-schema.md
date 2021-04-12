---
title: Объявление команд и элементов управления с разметкой ленты
description: Платформа Windows Ribbon использует язык разметки на основе XAML (XAML) для декларативной реализации внешнего вида приложения с лентой.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Лента Windows, структура разметки
- Лента, структура разметки
- Лента Windows, отделение презентации от логики команды
- Лента, отделение представления от логики команды
- Лента Windows, компоненты
- Лента, компоненты
- система команд для ленты Windows
- элементы управления для ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413384"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a><span data-ttu-id="76fec-111">Объявление команд и элементов управления с разметкой ленты</span><span class="sxs-lookup"><span data-stu-id="76fec-111">Declaring Commands and Controls with Ribbon Markup</span></span>

<span data-ttu-id="76fec-112">Платформа Windows Ribbon использует язык разметки на основе XAML (XAML) для декларативной реализации внешнего вида приложения с лентой.</span><span class="sxs-lookup"><span data-stu-id="76fec-112">The Windows Ribbon framework uses a markup language based on Extensible Application Markup Language (XAML) to declaratively implement the appearance of a Ribbon application.</span></span>

-   [<span data-ttu-id="76fec-113">Отделение представления от логики команды</span><span class="sxs-lookup"><span data-stu-id="76fec-113">Separating Presentation from Command Logic</span></span>](#separating-presentation-from-command-logic)
-   [<span data-ttu-id="76fec-114">Структура разметки</span><span class="sxs-lookup"><span data-stu-id="76fec-114">Markup Structure</span></span>](#markup-structure)
-   [<span data-ttu-id="76fec-115">Компоненты ленты</span><span class="sxs-lookup"><span data-stu-id="76fec-115">Ribbon Components</span></span>](#ribbon-components)
-   [<span data-ttu-id="76fec-116">См. также</span><span class="sxs-lookup"><span data-stu-id="76fec-116">Related topics</span></span>](#related-topics)

## <a name="separating-presentation-from-command-logic"></a><span data-ttu-id="76fec-117">Отделение представления от логики команды</span><span class="sxs-lookup"><span data-stu-id="76fec-117">Separating Presentation from Command Logic</span></span>

<span data-ttu-id="76fec-118">Разделение представлений и визуальных атрибутов из логики команды на ленте осуществляется через две разные, но зависимые платформы разработки.</span><span class="sxs-lookup"><span data-stu-id="76fec-118">The separation of presentation and visual attributes from command logic in the Ribbon framework is accomplished through two distinct, but dependent, development platforms.</span></span> <span data-ttu-id="76fec-119">Макеты элементов управления, поведение масштабирования, объявления команд и спецификации ресурсов — это домен времени разработки декларативного синтаксиса разметки на основе спецификации [XAML (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) .</span><span class="sxs-lookup"><span data-stu-id="76fec-119">Control layouts, scaling behaviors, Command declarations, and resource specifications are the design time domain of a declarative markup syntax based on the [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) specification.</span></span> <span data-ttu-id="76fec-120">Функции нижнего уровня, перехватчики приложения и обработчики команд определены в реализациях интерфейса на основе модели объектов (COM).</span><span class="sxs-lookup"><span data-stu-id="76fec-120">Low level functionality, application hooks, and Command handlers are defined in Component Object Model (COM)-based interface implementations.</span></span>

<span data-ttu-id="76fec-121">Такое разделение представления и логики предоставляет следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="76fec-121">This separation of presentation and logic provides the following benefits:</span></span>

-   <span data-ttu-id="76fec-122">Более эффективный цикл разработки приложений, позволяющий разработчикам пользовательского интерфейса и дизайнерам реализовывать графический интерфейс приложения Ribbon независимо от основных функциональных возможностей приложения.</span><span class="sxs-lookup"><span data-stu-id="76fec-122">A more efficient application development cycle which allows UI developers and designers to implement the GUI of the Ribbon application independently from the core application functionality.</span></span> <span data-ttu-id="76fec-123">Эта основная функциональность может быть оставлена выделенным разработчикам программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="76fec-123">This core functionality can be left to dedicated software developers.</span></span>
-   <span data-ttu-id="76fec-124">Менее дорогостоящее обслуживание, поскольку изменения графического пользовательского интерфейса возможны без изменений в основных функциях (и наоборот).</span><span class="sxs-lookup"><span data-stu-id="76fec-124">Less costly maintenance because changes to the GUI are possible without changes to core functionality (and vice versa).</span></span>
-   <span data-ttu-id="76fec-125">Простая спецификация строковых и графических ресурсов с помощью разметки.</span><span class="sxs-lookup"><span data-stu-id="76fec-125">Simple specification of string and image resources through markup.</span></span>
-   <span data-ttu-id="76fec-126">Простота создания прототипов.</span><span class="sxs-lookup"><span data-stu-id="76fec-126">Ease of prototyping.</span></span>

## <a name="markup-structure"></a><span data-ttu-id="76fec-127">Структура разметки</span><span class="sxs-lookup"><span data-stu-id="76fec-127">Markup Structure</span></span>

<span data-ttu-id="76fec-128">В структуре разметки платформы ленты существуют две отдельные ветви.</span><span class="sxs-lookup"><span data-stu-id="76fec-128">Two distinct branches exist within the structure of Ribbon framework markup.</span></span>

<span data-ttu-id="76fec-129">Первая ветвь содержит манифест объявлений команд и ресурсов (строк и изображений).</span><span class="sxs-lookup"><span data-stu-id="76fec-129">The first branch contains a manifest of Command and resource declarations (strings and images).</span></span> <span data-ttu-id="76fec-130">Каждая запись команды используется платформой для привязки элемента управления ленты с помощью идентификатора команды к обработчику команд, определенному в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="76fec-130">Each Command entry is used by the framework to bind a Ribbon control, through a Command ID, to a Command handler defined in the application code.</span></span>

<span data-ttu-id="76fec-131">Вторая ветвь содержит фактические объявления элементов управления.</span><span class="sxs-lookup"><span data-stu-id="76fec-131">The second branch contains the actual control declarations.</span></span> <span data-ttu-id="76fec-132">Каждый элемент управления связан с командой через атрибут *CommandName* , сопоставляемый с атрибутом *Name* , указанным в каждом объявлении команды.</span><span class="sxs-lookup"><span data-stu-id="76fec-132">Each control is associated with a Command through a *CommandName* attribute that maps to a *Name* attribute specified in each Command declaration.</span></span>

## <a name="ribbon-components"></a><span data-ttu-id="76fec-133">Компоненты ленты</span><span class="sxs-lookup"><span data-stu-id="76fec-133">Ribbon Components</span></span>

<span data-ttu-id="76fec-134">Функциональность пользовательского интерфейса платформы ленты предоставляется через [представления](windowsribbon-reference-elements-view.md).</span><span class="sxs-lookup"><span data-stu-id="76fec-134">Ribbon framework UI functionality is exposed through [Views](windowsribbon-reference-elements-view.md).</span></span> <span data-ttu-id="76fec-135">Представление — это, по сути, контейнер, такой как [**Ribbon**](windowsribbon-element-ribbon.md) и [**контекстпопуп**](windowsribbon-element-contextpopup.md), который используется для представления элементов управления платформы и команд, к которым они привязаны.</span><span class="sxs-lookup"><span data-stu-id="76fec-135">A View is essentially a container, such as the [**Ribbon**](windowsribbon-element-ribbon.md) and [**ContextPopup**](windowsribbon-element-contextpopup.md), that is used to present framework controls and the Commands they are bound to.</span></span>

<span data-ttu-id="76fec-136">Представление [**ленты**](windowsribbon-element-ribbon.md) состоит из нескольких компонентов, включающих [меню приложения](windowsribbon-controls-applicationmenu.md), [панель быстрого доступа (QAT)](windowsribbon-controls-quickaccesstoolbar.md) для отображения часто используемых команд из ленты, ядра и контекстных [вкладок](windowsribbon-controls-tab.md) , которые содержат [группы](windowsribbon-controls-group.md) элементов управления, и систему расширенного контекстного меню [**контекстпопуп**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="76fec-136">The [**Ribbon**](windowsribbon-element-ribbon.md) View is composed of several components that include an [Application Menu](windowsribbon-controls-applicationmenu.md), the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md) for displaying commonly used Commands from the ribbon UI, core and contextual [tabs](windowsribbon-controls-tab.md) that contain [groups](windowsribbon-controls-group.md) of controls, and the rich context menu system of the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="76fec-137">Все компоненты ленты объявляются в отдельном файле разметки, который:</span><span class="sxs-lookup"><span data-stu-id="76fec-137">All Ribbon components are declared in a standalone markup file that:</span></span>

-   <span data-ttu-id="76fec-138">Задает основные свойства для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="76fec-138">Specifies the basic properties for each element.</span></span>
-   <span data-ttu-id="76fec-139">Четко отображает иерархические связи.</span><span class="sxs-lookup"><span data-stu-id="76fec-139">Shows hierarchical relationships clearly.</span></span>
-   <span data-ttu-id="76fec-140">Предоставляет параметры макета и указания по масштабированию.</span><span class="sxs-lookup"><span data-stu-id="76fec-140">Supplies layout preferences and scaling hints.</span></span> <span data-ttu-id="76fec-141">Дополнительные сведения о шаблонах макета Ribbon Framework см. в разделе [Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="76fec-141">For more information on Ribbon framework layout templates, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>
-   <span data-ttu-id="76fec-142">Предоставляет способ определения ресурсов, таких как изображения и метки.</span><span class="sxs-lookup"><span data-stu-id="76fec-142">Provides a way to define resources such as images and labels.</span></span> <span data-ttu-id="76fec-143">Дополнительные сведения о ресурсах с изображениями см. в разделе [указание ресурсов изображения ленты](windowsribbon-imageformats.md).</span><span class="sxs-lookup"><span data-stu-id="76fec-143">For more information on image resources, see [Specifying Ribbon Image Resources](windowsribbon-imageformats.md).</span></span>

<span data-ttu-id="76fec-144">В следующих двух примерах разметки ленты показано, как набор элементов меню приложения ленты связан с именем команды и ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="76fec-144">The following two Ribbon markup examples demonstrate how a set of Ribbon Application Menu items are each associated with a Command name and ID.</span></span>

1.  <span data-ttu-id="76fec-145">В этом разделе показаны объявления команд, необходимые для меню приложения с основными командами, такими как создание, открытие и сохранение.</span><span class="sxs-lookup"><span data-stu-id="76fec-145">This section shows the Command declarations required for an Application Menu with basic commands such as New, Open, and Save.</span></span>
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  <span data-ttu-id="76fec-146">В этом разделе показаны связанные объявления элементов управления.</span><span class="sxs-lookup"><span data-stu-id="76fec-146">This section shows the associated Control declarations.</span></span>
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

<span data-ttu-id="76fec-147">Если разметка компилируется с помощью средства компиляции команд пользовательского интерфейса (УИКК), имена команд и идентификаторы помещаются в файл заголовка, используемый ведущим приложением ленты.</span><span class="sxs-lookup"><span data-stu-id="76fec-147">When the markup is compiled with the UI Command Compiler (UICC) tool, the Command names and IDs are placed into a header file used by the Ribbon host application.</span></span>

<span data-ttu-id="76fec-148">Ниже приведен пример файла заголовка, созданного УИКК.</span><span class="sxs-lookup"><span data-stu-id="76fec-148">The following is an example of a header file generated by UICC.</span></span>


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a><span data-ttu-id="76fec-149">См. также</span><span class="sxs-lookup"><span data-stu-id="76fec-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76fec-150">XAML (XAML)</span><span class="sxs-lookup"><span data-stu-id="76fec-150">Extensible Application Markup Language (XAML)</span></span>](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[<span data-ttu-id="76fec-151">Компиляция разметки ленты</span><span class="sxs-lookup"><span data-stu-id="76fec-151">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)
</dt> </dl>

 

 