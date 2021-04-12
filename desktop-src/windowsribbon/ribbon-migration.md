---
title: Переход на платформу Windows Ribbon
description: Приложение, основанное на традиционных меню, панелях инструментов и диалоговых окнах, может быть перенесено в многофункциональный, динамический и контекстный пользовательский интерфейс в командной системе Windows Ribbon Framework.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Лента Windows, миграция на
- Лента, миграция в
- Переход на ленту Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74822781f891815c6eb30d9e15a7f7efaa983fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487960"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a><span data-ttu-id="69afe-106">Переход на платформу Windows Ribbon</span><span class="sxs-lookup"><span data-stu-id="69afe-106">Migrating to the Windows Ribbon Framework</span></span>

<span data-ttu-id="69afe-107">Приложение, основанное на традиционных меню, панелях инструментов и диалоговых окнах, может быть перенесено в многофункциональный, динамический и контекстный пользовательский интерфейс в командной системе Windows Ribbon Framework.</span><span class="sxs-lookup"><span data-stu-id="69afe-107">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven UI of the Windows Ribbon framework Command system.</span></span> <span data-ttu-id="69afe-108">Это простой и эффективный способ модернизировать и ревитализе приложение, одновременно улучшая доступность, удобство использования и возможность обнаружения его функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="69afe-108">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

## <a name="introduction"></a><span data-ttu-id="69afe-109">Введение</span><span class="sxs-lookup"><span data-stu-id="69afe-109">Introduction</span></span>

<span data-ttu-id="69afe-110">Как правило, перенос существующего приложения на платформу Ribbon включает в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="69afe-110">In general, migrating an existing application to the Ribbon framework involves the following:</span></span>

-   <span data-ttu-id="69afe-111">Разработка макета ленты и управления организацией, которая предоставляет функциональные возможности существующего приложения и является достаточно гибкой для поддержки новых функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="69afe-111">Designing a Ribbon layout and control organization that exposes the functionality of the existing application and is flexible enough to support new functionality.</span></span>
-   <span data-ttu-id="69afe-112">Адаптация кода существующего приложения.</span><span class="sxs-lookup"><span data-stu-id="69afe-112">Adapting the code of the existing application.</span></span>
-   <span data-ttu-id="69afe-113">Перенос существующих ресурсов приложения (строк и изображений) в платформу ленты.</span><span class="sxs-lookup"><span data-stu-id="69afe-113">Migrating existing application resources (strings and images) to the Ribbon framework.</span></span>

> [!Note]  
> <span data-ttu-id="69afe-114">Чтобы определить, является ли приложение подходящим кандидатом для ленты, необходимо проверить [рекомендации по работе пользователя с лентой](https://msdn.microsoft.com/library/cc872782.aspx) .</span><span class="sxs-lookup"><span data-stu-id="69afe-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed to determine if the application is a suitable candidate for a Ribbon UI.</span></span>

 

## <a name="design-the-ribbon-layout"></a><span data-ttu-id="69afe-115">Создание макета ленты</span><span class="sxs-lookup"><span data-stu-id="69afe-115">Design the Ribbon Layout</span></span>

<span data-ttu-id="69afe-116">Потенциальные разработки ленты и макеты элементов управления можно определить, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69afe-116">Potential Ribbon UI designs and control layouts can be identified by performing these steps:</span></span>

1.  <span data-ttu-id="69afe-117">Инвентаризация всех существующих функций.</span><span class="sxs-lookup"><span data-stu-id="69afe-117">Taking inventory of all existing functionality.</span></span>
2.  <span data-ttu-id="69afe-118">Преобразование этой функции в команды ленты.</span><span class="sxs-lookup"><span data-stu-id="69afe-118">Translating this functionality into Ribbon Commands.</span></span>
3.  <span data-ttu-id="69afe-119">Упорядочение команд в логические группы.</span><span class="sxs-lookup"><span data-stu-id="69afe-119">Organizing the Commands into logical groups.</span></span>

### <a name="take-inventory"></a><span data-ttu-id="69afe-120">Взять инвентаризацию</span><span class="sxs-lookup"><span data-stu-id="69afe-120">Take Inventory</span></span>

<span data-ttu-id="69afe-121">В платформе Ribbon функциональные возможности, предоставляемые приложением, которое управляет состоянием или представлением рабочей области или документа, рассматриваются как команда.</span><span class="sxs-lookup"><span data-stu-id="69afe-121">In the Ribbon framework, the functionality exposed by an application that manipulates the state or the view of a workspace or document is considered a command.</span></span> <span data-ttu-id="69afe-122">Состав команды может различаться и зависит от природы и домена существующего приложения.</span><span class="sxs-lookup"><span data-stu-id="69afe-122">What constitutes a command may vary and depends on the nature and domain of the existing application.</span></span>

<span data-ttu-id="69afe-123">В следующей таблице приведен набор основных команд для гипотетического приложения для редактирования текста:</span><span class="sxs-lookup"><span data-stu-id="69afe-123">The following table lists a set of basic commands for a hypothetical text editing application:</span></span>



| <span data-ttu-id="69afe-124">Символ</span><span class="sxs-lookup"><span data-stu-id="69afe-124">Symbol</span></span>           | <span data-ttu-id="69afe-125">ID</span><span class="sxs-lookup"><span data-stu-id="69afe-125">ID</span></span>     | <span data-ttu-id="69afe-126">Описание</span><span class="sxs-lookup"><span data-stu-id="69afe-126">Description</span></span>               |
|------------------|--------|---------------------------|
| <span data-ttu-id="69afe-127">\_файл идентификатора \_ New</span><span class="sxs-lookup"><span data-stu-id="69afe-127">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="69afe-128">0xE100</span><span class="sxs-lookup"><span data-stu-id="69afe-128">0xE100</span></span> | <span data-ttu-id="69afe-129">Новый документ</span><span class="sxs-lookup"><span data-stu-id="69afe-129">New document</span></span>              |
| <span data-ttu-id="69afe-130">файл идентификатора — \_ \_ Сохранение</span><span class="sxs-lookup"><span data-stu-id="69afe-130">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="69afe-131">0xE103</span><span class="sxs-lookup"><span data-stu-id="69afe-131">0xE103</span></span> | <span data-ttu-id="69afe-132">Сохранить документ</span><span class="sxs-lookup"><span data-stu-id="69afe-132">Save document</span></span>             |
| <span data-ttu-id="69afe-133">\_файл идентификатора \_ SAVEAS</span><span class="sxs-lookup"><span data-stu-id="69afe-133">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="69afe-134">0xE104</span><span class="sxs-lookup"><span data-stu-id="69afe-134">0xE104</span></span> | <span data-ttu-id="69afe-135">Сохранить как... Откроется</span><span class="sxs-lookup"><span data-stu-id="69afe-135">Save As... (dialog)</span></span>       |
| <span data-ttu-id="69afe-136">\_файл идентификатора \_ открыт</span><span class="sxs-lookup"><span data-stu-id="69afe-136">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="69afe-137">0xE101</span><span class="sxs-lookup"><span data-stu-id="69afe-137">0xE101</span></span> | <span data-ttu-id="69afe-138">Открыть... Откроется</span><span class="sxs-lookup"><span data-stu-id="69afe-138">Open... (dialog)</span></span>          |
| <span data-ttu-id="69afe-139">\_ \_ выход из файла идентификатора</span><span class="sxs-lookup"><span data-stu-id="69afe-139">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="69afe-140">0xE102</span><span class="sxs-lookup"><span data-stu-id="69afe-140">0xE102</span></span> | <span data-ttu-id="69afe-141">Выход из приложения</span><span class="sxs-lookup"><span data-stu-id="69afe-141">Exit the application</span></span>      |
| <span data-ttu-id="69afe-142">\_Отмена изменения \_ идентификатора</span><span class="sxs-lookup"><span data-stu-id="69afe-142">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="69afe-143">0xE12B</span><span class="sxs-lookup"><span data-stu-id="69afe-143">0xE12B</span></span> | <span data-ttu-id="69afe-144">Отменить</span><span class="sxs-lookup"><span data-stu-id="69afe-144">Undo</span></span>                      |
| <span data-ttu-id="69afe-145">\_Изменение идентификатора \_ Вырезать</span><span class="sxs-lookup"><span data-stu-id="69afe-145">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="69afe-146">0xE123</span><span class="sxs-lookup"><span data-stu-id="69afe-146">0xE123</span></span> | <span data-ttu-id="69afe-147">Вырезать выделенный текст</span><span class="sxs-lookup"><span data-stu-id="69afe-147">Cut selected text</span></span>         |
| <span data-ttu-id="69afe-148">Идентификатор \_ изменения \_ копии</span><span class="sxs-lookup"><span data-stu-id="69afe-148">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="69afe-149">0xE122</span><span class="sxs-lookup"><span data-stu-id="69afe-149">0xE122</span></span> | <span data-ttu-id="69afe-150">Копировать выделенный текст</span><span class="sxs-lookup"><span data-stu-id="69afe-150">Copy selected text</span></span>        |
| <span data-ttu-id="69afe-151">изменение кода при \_ \_ вставке</span><span class="sxs-lookup"><span data-stu-id="69afe-151">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="69afe-152">0xE125</span><span class="sxs-lookup"><span data-stu-id="69afe-152">0xE125</span></span> | <span data-ttu-id="69afe-153">Вставить текст из буфера обмена</span><span class="sxs-lookup"><span data-stu-id="69afe-153">Paste text from clipboard</span></span> |
| <span data-ttu-id="69afe-154">ID \_ Правка \_ очистить</span><span class="sxs-lookup"><span data-stu-id="69afe-154">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="69afe-155">0xE120</span><span class="sxs-lookup"><span data-stu-id="69afe-155">0xE120</span></span> | <span data-ttu-id="69afe-156">Удалить выделенный текст</span><span class="sxs-lookup"><span data-stu-id="69afe-156">Delete selected text</span></span>      |
| <span data-ttu-id="69afe-157">\_масштаб представления \_ идентификатора</span><span class="sxs-lookup"><span data-stu-id="69afe-157">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="69afe-158">1242</span><span class="sxs-lookup"><span data-stu-id="69afe-158">1242</span></span>   | <span data-ttu-id="69afe-159">Масштаб... Откроется</span><span class="sxs-lookup"><span data-stu-id="69afe-159">Zoom... (dialog)</span></span>          |



 

<span data-ttu-id="69afe-160">При создании инвентаризации команд Изучите существующие меню и панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="69afe-160">Look beyond existing menus and toolbars when building an inventory of commands.</span></span> <span data-ttu-id="69afe-161">Рассмотрим все способы взаимодействия пользователя с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="69afe-161">Consider all the ways a user can interact with the workspace.</span></span> <span data-ttu-id="69afe-162">Хотя не каждая команда подходит для включения на ленту, это упражнение может очень хорошо представлять команды, которые ранее были скрыты слоями пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="69afe-162">Even though not every command is suitable for inclusion in the Ribbon, this exercise may very well expose commands that were previously obscured by layers of UI.</span></span>

### <a name="translate"></a><span data-ttu-id="69afe-163">Перевод</span><span class="sxs-lookup"><span data-stu-id="69afe-163">Translate</span></span>

<span data-ttu-id="69afe-164">Не все команды должны быть представлены в пользовательском интерфейсе ленты.</span><span class="sxs-lookup"><span data-stu-id="69afe-164">Not every command needs to be represented in the Ribbon UI.</span></span> <span data-ttu-id="69afe-165">Например, при вводе текста, изменении выделенного фрагмента, прокрутки или перемещении точки вставки с помощью мыши все поля указываются как команды в гипотетическом текстовом редакторе, однако они не подходят для отображения на панели команд, так как каждая из них включает непосредственное взаимодействие с пользовательским интерфейсом приложения.</span><span class="sxs-lookup"><span data-stu-id="69afe-165">For example, entering text, changing a selection, scrolling, or moving the insertion-point with the mouse all qualify as commands in the hypothetical text editor, however, these are not suitable to expose in a command bar as each involves a direct interaction with the UI of the application.</span></span>

<span data-ttu-id="69afe-166">И наоборот, некоторые функции могут не рассматриваться как команды в традиционном смысле.</span><span class="sxs-lookup"><span data-stu-id="69afe-166">Conversely, some functionality may not be thought of as a command in the traditional sense.</span></span> <span data-ttu-id="69afe-167">Например, вместо скрытия в диалоговом окне настройки полей принтера могут быть представлены на ленте как группа элементов управления "Счетчик" в контекстной вкладке или [режиме приложения](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="69afe-167">For example, instead of being buried in a dialog box, printer page-margin adjustments could be represented in the Ribbon as a group of Spinner controls in a contextual tab or [application mode](ribbon-applicationmodes.md).</span></span>

> [!Note]  
> <span data-ttu-id="69afe-168">Запишите числовой идентификатор, который может быть назначен каждой команде.</span><span class="sxs-lookup"><span data-stu-id="69afe-168">Make note of the numeric ID that may be assigned to each command.</span></span> <span data-ttu-id="69afe-169">Некоторые платформы пользовательского интерфейса, такие как Microsoft Foundation Classes (MFC), определяют идентификаторы для таких команд, как меню File и Edit (0xE100 to 0xE200).</span><span class="sxs-lookup"><span data-stu-id="69afe-169">Some UI frameworks, such as Microsoft Foundation Classes (MFC), define IDs for commands such as the file and edit menu (0xE100 to 0xE200).</span></span>

 

### <a name="organize"></a><span data-ttu-id="69afe-170">Организация</span><span class="sxs-lookup"><span data-stu-id="69afe-170">Organize</span></span>

<span data-ttu-id="69afe-171">Прежде чем пытаться упорядочить учетные записи команд, необходимо ознакомиться с рекомендациями [пользователя на ленте](https://msdn.microsoft.com/library/cc872782.aspx) , чтобы получить рекомендации при реализации пользовательского интерфейса Ribbon.</span><span class="sxs-lookup"><span data-stu-id="69afe-171">Before attempting to organize the command inventory, the [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed for best practices when implementing a Ribbon UI.</span></span>

<span data-ttu-id="69afe-172">Как правило, к организации команды ленты можно применить следующие правила.</span><span class="sxs-lookup"><span data-stu-id="69afe-172">In general, the following rules can be applied to Ribbon Command organization:</span></span>

-   <span data-ttu-id="69afe-173">Команды, которые работают с файлом или общим приложением, скорее всего, находятся в [меню приложения](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="69afe-173">Commands that operate on the file or the overall application most likely belong in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="69afe-174">Часто используемые команды, такие как вырезание, копирование и вставка (как в примере текстового редактора), обычно размещаются на вкладке «Главная» по умолчанию. В более сложных приложениях они могут дублироваться в других местах в пользовательском интерфейсе ленты.</span><span class="sxs-lookup"><span data-stu-id="69afe-174">Frequently used Commands such as Cut, Copy, and Paste (as in the text editor example) are typically placed on a default home tab. In more complex applications, they may be duplicated elsewhere in the Ribbon UI.</span></span>
-   <span data-ttu-id="69afe-175">Важные или часто используемые команды могут гарантировать включение по умолчанию на [панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="69afe-175">Important or frequently used Commands might warrant default inclusion in the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="69afe-176">Платформа Ribbon также предоставляет элементы управления ContextMenu и Минитулбар через представление Контекстпопуп.</span><span class="sxs-lookup"><span data-stu-id="69afe-176">The Ribbon framework also provides ContextMenu and MiniToolbar controls through the ContextPopup View.</span></span> <span data-ttu-id="69afe-177">Эти функции не являются обязательными, но если приложение содержит одно или несколько существующих контекстных меню, миграция содержащихся в них команд может привести к повторному использованию существующей базы кода с автоматической привязкой к существующим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="69afe-177">These features are not mandatory, but if your application has one or more existing context menus then migrating the commands they contain may allow the reuse of the existing codebase with automatic binding to existing resources.</span></span>

<span data-ttu-id="69afe-178">Так как каждое приложение отличается, ознакомьтесь с рекомендациями и попытайтесь применить их к максимальному экстенту.</span><span class="sxs-lookup"><span data-stu-id="69afe-178">Because every application is different, read the guidelines and try to apply them to the fullest extent possible.</span></span> <span data-ttu-id="69afe-179">Одной из целей платформы Ribbon является предоставление привычного, единообразного взаимодействия с пользователем, и эта цель будет более достижима, если разработка новых приложений потребует максимально возможного отражения существующих приложений ленты.</span><span class="sxs-lookup"><span data-stu-id="69afe-179">One of the goals of the Ribbon framework is to provide a familiar, consistent user experience and this goal will be more achievable if designs for new applications mirror existing Ribbon applications as much as possible.</span></span>

## <a name="adapt-your-code"></a><span data-ttu-id="69afe-180">Адаптация кода</span><span class="sxs-lookup"><span data-stu-id="69afe-180">Adapt Your Code</span></span>

<span data-ttu-id="69afe-181">После того как команды ленты определены и организованы в логические группы, количество этапов, связанных с внедрением платформы Ribbon в существующий код приложения, зависит от сложности исходного приложения.</span><span class="sxs-lookup"><span data-stu-id="69afe-181">Once the Ribbon Commands have been identified and organized into logical groupings, the number of steps involved when incorporating the Ribbon framework into existing application code depends on the complexity of the original application.</span></span> <span data-ttu-id="69afe-182">Как правило, существует три основных шага:</span><span class="sxs-lookup"><span data-stu-id="69afe-182">In general, there are three basic steps:</span></span>

-   <span data-ttu-id="69afe-183">Создайте разметку ленты на основе схемы команды и спецификации макета.</span><span class="sxs-lookup"><span data-stu-id="69afe-183">Create the Ribbon markup based on the Command organization and layout specification.</span></span>
-   <span data-ttu-id="69afe-184">Замените функциональные возможности меню и панелей инструментов прежними возможностями на ленте.</span><span class="sxs-lookup"><span data-stu-id="69afe-184">Replace legacy menu and toolbar functionality with Ribbon functionality.</span></span>
-   <span data-ttu-id="69afe-185">Реализация адаптера Иуикоммандхандлер.</span><span class="sxs-lookup"><span data-stu-id="69afe-185">Implement an IUICommandHandler adapter.</span></span>

### <a name="create-the-markup"></a><span data-ttu-id="69afe-186">Создание разметки</span><span class="sxs-lookup"><span data-stu-id="69afe-186">Create The Markup</span></span>

<span data-ttu-id="69afe-187">Список команд, а также их организация и макет объявляются через файл разметки ленты, используемый [компилятором разметки ленты](windowsribbon-intentcl.md).</span><span class="sxs-lookup"><span data-stu-id="69afe-187">The list of commands as well as their organization and layout are declared through the Ribbon markup file which is consumed by the [Ribbon markup compiler](windowsribbon-intentcl.md).</span></span>

> [!Note]  
> <span data-ttu-id="69afe-188">Многие шаги, необходимые для адаптации существующего приложения, похожи на те, которые необходимы для запуска нового приложения на ленте.</span><span class="sxs-lookup"><span data-stu-id="69afe-188">Many of the steps required to adapt an existing application are similar to those required to start a new Ribbon application.</span></span> <span data-ttu-id="69afe-189">Дополнительные сведения см. в руководстве по [созданию приложения](windowsribbon-stepbystep.md) для создания ленты.</span><span class="sxs-lookup"><span data-stu-id="69afe-189">For more information, see the [Creating a Ribbon Application](windowsribbon-stepbystep.md) tutorial for a new Ribbon application walkthrough.</span></span>

 

<span data-ttu-id="69afe-190">Разметка ленты состоит из двух основных разделов.</span><span class="sxs-lookup"><span data-stu-id="69afe-190">There are two primary sections to the Ribbon markup.</span></span> <span data-ttu-id="69afe-191">Первый раздел представляет собой манифест команд и связанных с ними ресурсов (строк и изображений).</span><span class="sxs-lookup"><span data-stu-id="69afe-191">The first section is a manifest of Commands and their associated resources (strings and images).</span></span> <span data-ttu-id="69afe-192">Во втором разделе задается структура и размещение элементов управления на ленте.</span><span class="sxs-lookup"><span data-stu-id="69afe-192">The second section specifies the structure and placement of controls on the Ribbon.</span></span>

<span data-ttu-id="69afe-193">Разметка для простого текстового редактора может выглядеть примерно так, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="69afe-193">The markup for the simple text editor might look something like the following example:</span></span>

> [!Note]  
> <span data-ttu-id="69afe-194">Ресурсы изображений и строк описаны далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="69afe-194">Image and string resources are covered later in this article.</span></span>

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



<span data-ttu-id="69afe-195">Чтобы избежать переопределения символов, определяемых платформой пользовательского интерфейса, например MFC, в предыдущем примере для каждой команды используются несколько различных имен символов (идентификатор \_ файла \_ New или \_ cmd \_ New).</span><span class="sxs-lookup"><span data-stu-id="69afe-195">To avoid redefining symbols that are defined by a UI framework such as MFC, the previous example uses slightly different symbol names for each Command (ID\_FILE\_NEW versus ID\_CMD\_NEW).</span></span> <span data-ttu-id="69afe-196">Однако числовой идентификатор, назначенный каждой команде, должен остаться прежним.</span><span class="sxs-lookup"><span data-stu-id="69afe-196">However, the numeric ID assigned to each Command must remain the same.</span></span>

<span data-ttu-id="69afe-197">Чтобы интегрировать файл разметки в приложение, настройте пользовательский этап сборки для запуска компилятора разметки ленты UICC.exe.</span><span class="sxs-lookup"><span data-stu-id="69afe-197">To integrate the markup file into an application, configure a custom build step to run the Ribbon markup compiler, UICC.exe.</span></span> <span data-ttu-id="69afe-198">Полученные файлы заголовков и ресурсов затем включаются в существующий проект.</span><span class="sxs-lookup"><span data-stu-id="69afe-198">The resulting header and resource files are then incorporated into the existing project.</span></span> <span data-ttu-id="69afe-199">Если в примере текстового редактора текстовое приложение имеет имя "Риббонпад", требуется Командная строка с пользовательской сборкой, аналогичная следующей:</span><span class="sxs-lookup"><span data-stu-id="69afe-199">If the example text editor Ribbon application is named "RibbonPad", a custom-build command line similar to the following is required:</span></span>


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



<span data-ttu-id="69afe-200">Компилятор разметки создает двоичный файл, файл заголовка (H) и файл ресурса (RC).</span><span class="sxs-lookup"><span data-stu-id="69afe-200">The markup compiler creates a binary file, a header (H) file and a resource (RC) file.</span></span> <span data-ttu-id="69afe-201">Поскольку существующее приложение, скорее всего, имеет существующий RC-файл, включите созданные файлы H и RC в этот RC-файл, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="69afe-201">Because the existing application likely has an existing RC file, include the generated H and RC files in that RC file, as shown in the following example:</span></span>


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a><span data-ttu-id="69afe-202">Замена устаревших меню и панелей инструментов</span><span class="sxs-lookup"><span data-stu-id="69afe-202">Replace Legacy Menus and Toolbars</span></span>

<span data-ttu-id="69afe-203">Для замены стандартных меню и панелей инструментов на ленту в устаревшем приложении необходимо следующее:</span><span class="sxs-lookup"><span data-stu-id="69afe-203">Replacing standard menus and toolbars with a ribbon in a legacy application requires the following:</span></span>

1.  <span data-ttu-id="69afe-204">Удаление ссылок на ресурсы панели инструментов и меню из файла ресурсов приложения.</span><span class="sxs-lookup"><span data-stu-id="69afe-204">Remove toolbar and menu resource references from the application's resource file.</span></span>
2.  <span data-ttu-id="69afe-205">Удалить все коды инициализации панели инструментов и строки меню.</span><span class="sxs-lookup"><span data-stu-id="69afe-205">Delete all toolbar and menu bar initialization code.</span></span>
3.  <span data-ttu-id="69afe-206">Удалите код, используемый для присоединения панели инструментов или строки меню к окну верхнего уровня приложения.</span><span class="sxs-lookup"><span data-stu-id="69afe-206">Delete any code used to attach a toolbar or menu bar to the top-level window of the application.</span></span>
4.  <span data-ttu-id="69afe-207">Создайте экземпляр платформы Ribbon.</span><span class="sxs-lookup"><span data-stu-id="69afe-207">Instantiate the Ribbon framework.</span></span>
5.  <span data-ttu-id="69afe-208">Присоедините ленту к окну верхнего уровня приложения.</span><span class="sxs-lookup"><span data-stu-id="69afe-208">Attach the ribbon to the top-level window of the application.</span></span>
6.  <span data-ttu-id="69afe-209">Загрузите скомпилированную разметку.</span><span class="sxs-lookup"><span data-stu-id="69afe-209">Load the compiled markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69afe-210">Существующие строки состояния и таблицы сочетаний клавиш должны сохраняться, так как платформа Ribbon не заменяет эти функции.</span><span class="sxs-lookup"><span data-stu-id="69afe-210">Existing status bar and keyboard shortcut tables should be preserved as the Ribbon framework does not replace these features.</span></span>

 

<span data-ttu-id="69afe-211">В следующем примере показано, как инициализировать платформу с помощью [**иуифрамеворк:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span><span class="sxs-lookup"><span data-stu-id="69afe-211">The following example demonstrates how to initialize the framework using [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span></span>


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



<span data-ttu-id="69afe-212">В следующем примере показано, как использовать [**иуифрамеворк:: лоадуи**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) для загрузки скомпилированной разметки:</span><span class="sxs-lookup"><span data-stu-id="69afe-212">The following example demonstrates how to use [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to load the compiled markup:</span></span>


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



<span data-ttu-id="69afe-213">Класс Каппликатион, упомянутый выше, должен реализовать пару интерфейсов модели COM, определенных платформой Ribbon: [**иуиаппликатион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) и [**иуикоммандхандлер**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span><span class="sxs-lookup"><span data-stu-id="69afe-213">The CApplication class, referred to above, must implement a pair of Component Object Model (COM) interfaces defined by the Ribbon framework: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) and [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span></span>

<span data-ttu-id="69afe-214">[**Иуиаппликатион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) предоставляет основной интерфейс обратного вызова между платформой и приложением (например, высота ленты передается через [**Иуиаппликатион:: онвиевчанжед**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)), а обратные вызовы для отдельных команд предоставляются в ответ на [**иуиаппликатион:: онкреатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span><span class="sxs-lookup"><span data-stu-id="69afe-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) provides the main callback interface between the framework and the application (for example, the height of the ribbon is communicated through [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) while the callbacks for individual Commands are provided in response to [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span></span>

<span data-ttu-id="69afe-215">**Совет.** Для некоторых платформ приложений, таких как MFC, необходимо учитывать высоту линейки ленты при отрисовке пространства документа приложения.</span><span class="sxs-lookup"><span data-stu-id="69afe-215">**Tip:** Some application frameworks, such as MFC, require that the height of the ribbon bar be taken into account when rendering the document space of the application.</span></span> <span data-ttu-id="69afe-216">В таких случаях Добавление скрытого окна для наложения панели ленты и принудительное заполнение области документа необходимой высотой.</span><span class="sxs-lookup"><span data-stu-id="69afe-216">In these cases, the addition of a hidden window to overlay the ribbon bar and force the document space to the desired height is necessary.</span></span> <span data-ttu-id="69afe-217">Пример такого подхода, в котором функция макета вызывается на основе высоты ленты, возвращенной методом [**иуириббон:: Height**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) , см. в [примере хтмледитриббон](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="69afe-217">For an example of this approach, where a layout function is called based on the ribbon height returned by the [**IUIRibbon::GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) method, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

<span data-ttu-id="69afe-218">В следующем примере кода демонстрируется реализация [**иуиаппликатион:: онвиевчанжед**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) :</span><span class="sxs-lookup"><span data-stu-id="69afe-218">The following code example demonstrates an [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) implementation:</span></span>


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a><span data-ttu-id="69afe-219">Реализация адаптера Иуикоммандхандлер</span><span class="sxs-lookup"><span data-stu-id="69afe-219">Implement an IUICommandHandler Adapter</span></span>

<span data-ttu-id="69afe-220">В зависимости от структуры исходного приложения может быть проще иметь несколько реализаций обработчиков команд или один обработчик команд для промежуточного вызова, вызывающий логику существующей команды приложения.</span><span class="sxs-lookup"><span data-stu-id="69afe-220">Depending on the design of the original application, it may be easier to have multiple Command handler implementations, or a single bridging Command handler that invokes the existing-application command logic.</span></span> <span data-ttu-id="69afe-221">Многие приложения используют \_ Командные сообщения WM для этой цели, где достаточно предоставить один обработчик команд для всех целей, который просто перенаправляет \_ Командные сообщения WM в окно верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="69afe-221">Many applications use WM\_COMMAND messages for this purpose where it is sufficient to provide a single, all-purpose command handler that simply forwards WM\_COMMAND messages to the top-level window.</span></span>

<span data-ttu-id="69afe-222">Однако этот подход требует специальной обработки команд, таких как **выход** или **закрытие**.</span><span class="sxs-lookup"><span data-stu-id="69afe-222">However, this approach requires special handling for Commands such as **Exit** or **Close**.</span></span> <span data-ttu-id="69afe-223">Поскольку лента не может быть уничтожена во время обработки окна сообщения, \_ сообщение закрытия WM должно быть отправлено в поток пользовательского интерфейса приложения и не должно обрабатываться синхронно, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="69afe-223">Because the Ribbon cannot be destroyed while it's processing a window message, the WM\_CLOSE message should be posted to the UI thread of the application and should not be processed synchronously, as shown in the following example:</span></span>


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a><span data-ttu-id="69afe-224">Перенос ресурсов</span><span class="sxs-lookup"><span data-stu-id="69afe-224">Migrating Resources</span></span>

<span data-ttu-id="69afe-225">Когда манифест команд определен, была объявлена структура ленты и код приложения, адаптированный для размещения платформы Ribbon, последний шаг — это спецификация строковых и графических ресурсов для каждой команды.</span><span class="sxs-lookup"><span data-stu-id="69afe-225">When the manifest of commands has been defined, the structure of the Ribbon has been declared, and the application code adapted to host the Ribbon framework, the final step is the specification of string and image resources for each Command.</span></span>

> [!Note]  
> <span data-ttu-id="69afe-226">Строковые и графические ресурсы обычно предоставляются в файле разметки.</span><span class="sxs-lookup"><span data-stu-id="69afe-226">String and image resources are typically provided in the markup file.</span></span> <span data-ttu-id="69afe-227">Однако их можно создавать или заменять программно, реализовав метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="69afe-227">However, they can be generated or replaced programmatically by implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

 

### <a name="string-resources"></a><span data-ttu-id="69afe-228">Строковые ресурсы</span><span class="sxs-lookup"><span data-stu-id="69afe-228">String Resources</span></span>

<span data-ttu-id="69afe-229">[**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) — это наиболее распространенное строковое свойство, определенное для команды.</span><span class="sxs-lookup"><span data-stu-id="69afe-229">[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is the most common string property defined for a Command.</span></span> <span data-ttu-id="69afe-230">Они подготавливаются к просмотру как текстовые метки для вкладок, групп и отдельных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="69afe-230">These are rendered as the text labels for tabs, groups, and individual controls.</span></span> <span data-ttu-id="69afe-231">Строку метки из устаревшего элемента меню обычно можно повторно использовать для **команды. лабелтитле** без изменения.</span><span class="sxs-lookup"><span data-stu-id="69afe-231">A label string from a legacy menu item can typically be re-used for a **Command.LabelTitle** without much editing.</span></span>

<span data-ttu-id="69afe-232">Однако следующие соглашения были изменены с появлением ленты.</span><span class="sxs-lookup"><span data-stu-id="69afe-232">However, the following conventions have changed with the advent of the Ribbon:</span></span>

-   <span data-ttu-id="69afe-233">Суффикс многоточия (...), используемый для обозначения команды запуска диалогового окна, больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="69afe-233">The ellipsis (...) suffix, used to indicate a dialog-launching command, is no longer necessary.</span></span>
-   <span data-ttu-id="69afe-234">Амперсанд (&) по-прежнему может использоваться для указания сочетания клавиш для команды, отображаемой в меню, но свойство [**Command. KeyTip**](windowsribbon-element-command-keytip.md) , поддерживаемое платформой, соответствует той же цели.</span><span class="sxs-lookup"><span data-stu-id="69afe-234">The ampersand (&) can still be used to indicate a keyboard-shortcut for a Command that appears in a menu, but the [**Command.Keytip**](windowsribbon-element-command-keytip.md) property supported by the framework fulfills a similar purpose.</span></span>

<span data-ttu-id="69afe-235">При обращении к примеру текстового редактора можно указать следующие строки для Лабелтитле и KeyTip:</span><span class="sxs-lookup"><span data-stu-id="69afe-235">Referring back to the text editor example, the following strings for LabelTitle and Keytip could be specified:</span></span>



| <span data-ttu-id="69afe-236">Символ</span><span class="sxs-lookup"><span data-stu-id="69afe-236">Symbol</span></span>           | <span data-ttu-id="69afe-237">Исходная строка</span><span class="sxs-lookup"><span data-stu-id="69afe-237">Original string</span></span> | <span data-ttu-id="69afe-238">Строка Лабелтитле</span><span class="sxs-lookup"><span data-stu-id="69afe-238">LabelTitle string</span></span> | <span data-ttu-id="69afe-239">Строка keytip</span><span class="sxs-lookup"><span data-stu-id="69afe-239">Keytip string</span></span> |
|------------------|-----------------|-------------------|---------------|
| <span data-ttu-id="69afe-240">\_файл идентификатора \_ New</span><span class="sxs-lookup"><span data-stu-id="69afe-240">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="69afe-241">&New</span><span class="sxs-lookup"><span data-stu-id="69afe-241">&New</span></span>            | <span data-ttu-id="69afe-242">&New</span><span class="sxs-lookup"><span data-stu-id="69afe-242">&New</span></span>              | <span data-ttu-id="69afe-243">Нет</span><span class="sxs-lookup"><span data-stu-id="69afe-243">N</span></span>             |
| <span data-ttu-id="69afe-244">файл идентификатора — \_ \_ Сохранение</span><span class="sxs-lookup"><span data-stu-id="69afe-244">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="69afe-245">&сохранить</span><span class="sxs-lookup"><span data-stu-id="69afe-245">&Save</span></span>           | <span data-ttu-id="69afe-246">&сохранить</span><span class="sxs-lookup"><span data-stu-id="69afe-246">&Save</span></span>             | <span data-ttu-id="69afe-247">S</span><span class="sxs-lookup"><span data-stu-id="69afe-247">S</span></span>             |
| <span data-ttu-id="69afe-248">\_файл идентификатора \_ SAVEAS</span><span class="sxs-lookup"><span data-stu-id="69afe-248">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="69afe-249">Сохранить &как...</span><span class="sxs-lookup"><span data-stu-id="69afe-249">Save &As…</span></span>       | <span data-ttu-id="69afe-250">Сохранить &как</span><span class="sxs-lookup"><span data-stu-id="69afe-250">Save &as</span></span>          | <span data-ttu-id="69afe-251">Объект</span><span class="sxs-lookup"><span data-stu-id="69afe-251">A</span></span>             |
| <span data-ttu-id="69afe-252">\_файл идентификатора \_ открыт</span><span class="sxs-lookup"><span data-stu-id="69afe-252">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="69afe-253">&открыть...</span><span class="sxs-lookup"><span data-stu-id="69afe-253">&Open…</span></span>          | <span data-ttu-id="69afe-254">&amp;Open</span><span class="sxs-lookup"><span data-stu-id="69afe-254">&Open</span></span>             | <span data-ttu-id="69afe-255">O</span><span class="sxs-lookup"><span data-stu-id="69afe-255">O</span></span>             |
| <span data-ttu-id="69afe-256">\_ \_ выход из файла идентификатора</span><span class="sxs-lookup"><span data-stu-id="69afe-256">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="69afe-257">Вы&ход</span><span class="sxs-lookup"><span data-stu-id="69afe-257">E&xit</span></span>           | <span data-ttu-id="69afe-258">Вы&ход</span><span class="sxs-lookup"><span data-stu-id="69afe-258">E&xit</span></span>             | <span data-ttu-id="69afe-259">X</span><span class="sxs-lookup"><span data-stu-id="69afe-259">X</span></span>             |
| <span data-ttu-id="69afe-260">\_Отмена изменения \_ идентификатора</span><span class="sxs-lookup"><span data-stu-id="69afe-260">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="69afe-261">&отменить</span><span class="sxs-lookup"><span data-stu-id="69afe-261">&Undo</span></span>           | <span data-ttu-id="69afe-262">Отменить</span><span class="sxs-lookup"><span data-stu-id="69afe-262">Undo</span></span>              | <span data-ttu-id="69afe-263">Z</span><span class="sxs-lookup"><span data-stu-id="69afe-263">Z</span></span>             |
| <span data-ttu-id="69afe-264">\_Изменение идентификатора \_ Вырезать</span><span class="sxs-lookup"><span data-stu-id="69afe-264">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="69afe-265">Cu&t</span><span class="sxs-lookup"><span data-stu-id="69afe-265">Cu&t</span></span>            | <span data-ttu-id="69afe-266">Cu&t</span><span class="sxs-lookup"><span data-stu-id="69afe-266">Cu&t</span></span>              | <span data-ttu-id="69afe-267">X</span><span class="sxs-lookup"><span data-stu-id="69afe-267">X</span></span>             |
| <span data-ttu-id="69afe-268">Идентификатор \_ изменения \_ копии</span><span class="sxs-lookup"><span data-stu-id="69afe-268">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="69afe-269">Копирование &</span><span class="sxs-lookup"><span data-stu-id="69afe-269">&Copy</span></span>           | <span data-ttu-id="69afe-270">Копирование &</span><span class="sxs-lookup"><span data-stu-id="69afe-270">&Copy</span></span>             | <span data-ttu-id="69afe-271">C</span><span class="sxs-lookup"><span data-stu-id="69afe-271">C</span></span>             |
| <span data-ttu-id="69afe-272">изменение кода при \_ \_ вставке</span><span class="sxs-lookup"><span data-stu-id="69afe-272">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="69afe-273">&вставить</span><span class="sxs-lookup"><span data-stu-id="69afe-273">&Paste</span></span>          | <span data-ttu-id="69afe-274">&вставить</span><span class="sxs-lookup"><span data-stu-id="69afe-274">&Paste</span></span>            | <span data-ttu-id="69afe-275">V</span><span class="sxs-lookup"><span data-stu-id="69afe-275">V</span></span>             |
| <span data-ttu-id="69afe-276">ID \_ Правка \_ очистить</span><span class="sxs-lookup"><span data-stu-id="69afe-276">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="69afe-277">&удалить</span><span class="sxs-lookup"><span data-stu-id="69afe-277">&Delete</span></span>         | <span data-ttu-id="69afe-278">&удалить</span><span class="sxs-lookup"><span data-stu-id="69afe-278">&Delete</span></span>           | <span data-ttu-id="69afe-279">D</span><span class="sxs-lookup"><span data-stu-id="69afe-279">D</span></span>             |
| <span data-ttu-id="69afe-280">\_масштаб представления \_ идентификатора</span><span class="sxs-lookup"><span data-stu-id="69afe-280">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="69afe-281">&масштаб...</span><span class="sxs-lookup"><span data-stu-id="69afe-281">&Zoom…</span></span>          | <span data-ttu-id="69afe-282">Масштабирование</span><span class="sxs-lookup"><span data-stu-id="69afe-282">Zoom</span></span>              | <span data-ttu-id="69afe-283">Z</span><span class="sxs-lookup"><span data-stu-id="69afe-283">Z</span></span>             |



 

<span data-ttu-id="69afe-284">Ниже приведен список других свойств строки, которые должны быть установлены для большинства команд:</span><span class="sxs-lookup"><span data-stu-id="69afe-284">The following is a list of other string properties which should be set on most Commands:</span></span>

-   [<span data-ttu-id="69afe-285">**Command. Лабелдескриптион**</span><span class="sxs-lookup"><span data-stu-id="69afe-285">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)
-   [<span data-ttu-id="69afe-286">**Command. Тултиптитле**</span><span class="sxs-lookup"><span data-stu-id="69afe-286">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
-   [<span data-ttu-id="69afe-287">**Command. Тултипдескриптион**</span><span class="sxs-lookup"><span data-stu-id="69afe-287">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)

<span data-ttu-id="69afe-288">Вкладки, группы и другие функции пользовательского интерфейса ленты теперь можно объявить с помощью всех указанных строковых и графических ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69afe-288">Tabs, Groups, and other Ribbon UI features can now be declared with all string and image resources specified.</span></span>

<span data-ttu-id="69afe-289">В следующем примере разметки ленты показаны различные строковые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="69afe-289">The following Ribbon markup example demonstrates various string resources:</span></span>


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a><span data-ttu-id="69afe-290">Ресурсы изображений</span><span class="sxs-lookup"><span data-stu-id="69afe-290">Image Resources</span></span>

<span data-ttu-id="69afe-291">Платформа Ribbon поддерживает форматы изображений, обеспечивающие более широкие возможности оформления, чем форматы изображений, поддерживаемые предыдущими компонентами меню и панелей инструментов.</span><span class="sxs-lookup"><span data-stu-id="69afe-291">The Ribbon framework supports image formats that provide a much richer look and feel than the image formats supported by previous menu and toolbar components.</span></span>

<span data-ttu-id="69afe-292">Для Windows 8 и более поздних версий платформа Ribbon поддерживает следующие форматы графики: 32-битовые растровые файлы ARGB (BMP) и PNG-файлы с прозрачностью.</span><span class="sxs-lookup"><span data-stu-id="69afe-292">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="69afe-293">Для Windows 7 и более ранних версий ресурсы образа должны соответствовать стандартному графическому формату BMP, используемому в Windows.</span><span class="sxs-lookup"><span data-stu-id="69afe-293">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="69afe-294">Существующие файлы изображений можно преобразовать в любой из форматов.</span><span class="sxs-lookup"><span data-stu-id="69afe-294">Existing image files can be converted to either format.</span></span> <span data-ttu-id="69afe-295">Однако результаты могут быть менее удовлетворительными, если файлы изображений не поддерживают сглаживание и прозрачность.</span><span class="sxs-lookup"><span data-stu-id="69afe-295">However, the results may be less than satisfactory if the image files do not support antialiasing and transparency.</span></span>

 

<span data-ttu-id="69afe-296">Невозможно указать один размер по умолчанию для ресурсов изображений в платформе Ribbon.</span><span class="sxs-lookup"><span data-stu-id="69afe-296">It is not possible to specify a single default size for image resources in the Ribbon framework.</span></span> <span data-ttu-id="69afe-297">Однако для поддержки [адаптивного макета](windowsribbon-templates.md) элементов управления изображения могут быть указаны в двух размерах (большие и небольшие).</span><span class="sxs-lookup"><span data-stu-id="69afe-297">However, to support [adaptive layout](windowsribbon-templates.md) of controls, images can be specified in two sizes (large and small) .</span></span> <span data-ttu-id="69afe-298">Все изображения в платформе ленты масштабируются в соответствии с разрешением точек на дюйм (DPI) монитора с точно отображаемым размером, зависящим от этого параметра dpi.</span><span class="sxs-lookup"><span data-stu-id="69afe-298">All images in the Ribbon framework are scaled according to the dots per inch (dpi) resolution of the display with the exact rendered size dependent on this dpi setting.</span></span> <span data-ttu-id="69afe-299">Дополнительные сведения см. в разделе [указание ресурсов изображения ленты](windowsribbon-imageformats.md) .</span><span class="sxs-lookup"><span data-stu-id="69afe-299">See [Specifying Ribbon Image Resources](windowsribbon-imageformats.md) for more information.</span></span>

<span data-ttu-id="69afe-300">В следующем примере показано, как в разметке указываются ссылки на образы, относящиеся к dpi.</span><span class="sxs-lookup"><span data-stu-id="69afe-300">The following example demonstrates how a set of dpi-specific images are referenced in markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="69afe-301">См. также</span><span class="sxs-lookup"><span data-stu-id="69afe-301">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69afe-302">Указание ресурсов изображения ленты</span><span class="sxs-lookup"><span data-stu-id="69afe-302">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 