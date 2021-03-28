---
description: Обработчики контекстного меню, также известные как обработчики контекстного меню или обработчиков команд, являются типом обработчика типов файлов. Как и все такие обработчики, они являются внутрипроцессный COM-объектами, реализованными в виде библиотек DLL.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Создание обработчиков контекстного меню
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "103913927"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="134b0-104">Создание обработчиков контекстного меню</span><span class="sxs-lookup"><span data-stu-id="134b0-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="134b0-105">Обработчики контекстного меню, также известные как обработчики контекстного меню или обработчиков команд, являются типом обработчика типов файлов.</span><span class="sxs-lookup"><span data-stu-id="134b0-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="134b0-106">Как и все такие обработчики, они являются внутрипроцессный COM-объектами, реализованными в виде библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="134b0-106">Like all such handlers, they are in-process Component Object Model (COM) objects implemented as DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="134b0-107">При регистрации обработчиков, работающих в контексте 32-разрядных приложений, существуют особые рекомендации для 64-разрядных систем: при вызове команд оболочки в контексте 32-разрядного приложения Подсистема WOW64 перенаправляет доступ к некоторым путям в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="134b0-107">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="134b0-108">Если обработчик. exe хранится в одном из этих путей, он недоступен в этом контексте.</span><span class="sxs-lookup"><span data-stu-id="134b0-108">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="134b0-109">Поэтому в качестве решения сохраните EXE-файл в пути, который не перенаправлен, или сохраните версию заглушки exe-файла, которая запускает реальную версию.</span><span class="sxs-lookup"><span data-stu-id="134b0-109">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

<span data-ttu-id="134b0-110">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="134b0-110">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="134b0-111">Канонические команды</span><span class="sxs-lookup"><span data-stu-id="134b0-111">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="134b0-112">Расширенные глаголы</span><span class="sxs-lookup"><span data-stu-id="134b0-112">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="134b0-113">Настройка контекстного меню с помощью статических команд</span><span class="sxs-lookup"><span data-stu-id="134b0-113">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="134b0-114">Активация обработчика с помощью интерфейса интерфейс IDropTarget</span><span class="sxs-lookup"><span data-stu-id="134b0-114">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="134b0-115">Указание расположения и порядка статических глаголов</span><span class="sxs-lookup"><span data-stu-id="134b0-115">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="134b0-116">Размещение команд в верхней или нижней части меню</span><span class="sxs-lookup"><span data-stu-id="134b0-116">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="134b0-117">Создание статических каскадных меню</span><span class="sxs-lookup"><span data-stu-id="134b0-117">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="134b0-118">Получение динамического поведения для статических команд с помощью расширенного синтаксиса запросов</span><span class="sxs-lookup"><span data-stu-id="134b0-118">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="134b0-119">Не рекомендуется: связывание команд с командами платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="134b0-119">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="134b0-120">Завершение задач реализации команд</span><span class="sxs-lookup"><span data-stu-id="134b0-120">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="134b0-121">Настройка контекстного меню для предопределенных объектов оболочки</span><span class="sxs-lookup"><span data-stu-id="134b0-121">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="134b0-122">Расширение нового подменю</span><span class="sxs-lookup"><span data-stu-id="134b0-122">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="134b0-123">Подавление команд и управление видимостью</span><span class="sxs-lookup"><span data-stu-id="134b0-123">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="134b0-124">Применение модели выбора глагола</span><span class="sxs-lookup"><span data-stu-id="134b0-124">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="134b0-125">Использование атрибутов элементов</span><span class="sxs-lookup"><span data-stu-id="134b0-125">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="134b0-126">Реализация пользовательских команд для папок с помощью Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="134b0-126">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="134b0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="134b0-127">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="134b0-128">Канонические команды</span><span class="sxs-lookup"><span data-stu-id="134b0-128">Canonical Verbs</span></span>

<span data-ttu-id="134b0-129">Приложения обычно отвечают за предоставление локализованных отображаемых строк для глаголов, которые они определяют.</span><span class="sxs-lookup"><span data-stu-id="134b0-129">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="134b0-130">Однако для обеспечения степени независимости от языка система определяет стандартный набор часто используемых глаголов, называемых каноническими глаголами.</span><span class="sxs-lookup"><span data-stu-id="134b0-130">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="134b0-131">Каноническая команда никогда не отображается для пользователя и может использоваться с любым языком пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="134b0-131">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="134b0-132">Система использует каноническое имя для автоматического создания правильно локализованной отображаемой строки.</span><span class="sxs-lookup"><span data-stu-id="134b0-132">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="134b0-133">Например, отображаемая строка команды открытия задается как **открытая** в системе на английском языке и как эквивалент немецкого в системе на немецком языке.</span><span class="sxs-lookup"><span data-stu-id="134b0-133">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>



| <span data-ttu-id="134b0-134">Каноническая команда</span><span class="sxs-lookup"><span data-stu-id="134b0-134">Canonical verb</span></span> | <span data-ttu-id="134b0-135">Описание</span><span class="sxs-lookup"><span data-stu-id="134b0-135">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="134b0-136">Открыть</span><span class="sxs-lookup"><span data-stu-id="134b0-136">Open</span></span>           | <span data-ttu-id="134b0-137">Открывает файл или папку.</span><span class="sxs-lookup"><span data-stu-id="134b0-137">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="134b0-138">опеннев</span><span class="sxs-lookup"><span data-stu-id="134b0-138">Opennew</span></span>        | <span data-ttu-id="134b0-139">Открывает файл или папку в новом окне.</span><span class="sxs-lookup"><span data-stu-id="134b0-139">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="134b0-140">Печать</span><span class="sxs-lookup"><span data-stu-id="134b0-140">Print</span></span>          | <span data-ttu-id="134b0-141">Выводит файл.</span><span class="sxs-lookup"><span data-stu-id="134b0-141">Prints the file.</span></span>                                                     |
| <span data-ttu-id="134b0-142">принтто</span><span class="sxs-lookup"><span data-stu-id="134b0-142">Printto</span></span>        | <span data-ttu-id="134b0-143">Разрешает пользователю печатать файл, перетаскивая его на объект принтера.</span><span class="sxs-lookup"><span data-stu-id="134b0-143">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="134b0-144">Обзор</span><span class="sxs-lookup"><span data-stu-id="134b0-144">Explore</span></span>        | <span data-ttu-id="134b0-145">Открывает проводник Windows с выбранной папкой.</span><span class="sxs-lookup"><span data-stu-id="134b0-145">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="134b0-146">Свойства</span><span class="sxs-lookup"><span data-stu-id="134b0-146">Properties</span></span>     | <span data-ttu-id="134b0-147">Открывает страницу свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="134b0-147">Opens the object's property sheet.</span></span>                                   |



 

> [!Note]  
> <span data-ttu-id="134b0-148">Команда **принтто** также является канонической, но никогда не отображается.</span><span class="sxs-lookup"><span data-stu-id="134b0-148">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="134b0-149">Его включение позволяет пользователю распечатать файл, перетащив его в объект принтера.</span><span class="sxs-lookup"><span data-stu-id="134b0-149">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

 

<span data-ttu-id="134b0-150">Обработчики контекстного меню могут предоставлять собственные канонические команды через [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) с **GC \_ вербв** или **GC \_ verb**.</span><span class="sxs-lookup"><span data-stu-id="134b0-150">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="134b0-151">Система будет использовать канонические команды в качестве второго параметра (*лпоператион*), переданного в [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), и является [**кминвокекоммандинфо**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). член **лпверб** , переданный в метод [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="134b0-151">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="134b0-152">Расширенные глаголы</span><span class="sxs-lookup"><span data-stu-id="134b0-152">Extended Verbs</span></span>

<span data-ttu-id="134b0-153">Когда пользователь щелкает правой кнопкой мыши объект, в контекстном меню отображаются команды по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="134b0-153">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="134b0-154">Может потребоваться добавить и поддерживать команды в некоторых контекстных меню, которые не отображаются в каждом из контекстных меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-154">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="134b0-155">Например, можно использовать команды, которые обычно не используются или предназначены для опытных пользователей.</span><span class="sxs-lookup"><span data-stu-id="134b0-155">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="134b0-156">По этой причине можно также определить одну или несколько расширенных команд.</span><span class="sxs-lookup"><span data-stu-id="134b0-156">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="134b0-157">Эти глаголы похожи на обычные глаголы, но отличаются от обычных глаголов способом их регистрации.</span><span class="sxs-lookup"><span data-stu-id="134b0-157">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="134b0-158">Чтобы получить доступ к расширенным командам, пользователь должен щелкнуть объект правой кнопкой мыши и нажать клавишу SHIFT.</span><span class="sxs-lookup"><span data-stu-id="134b0-158">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="134b0-159">Когда пользователь делает это, расширенные команды отображаются в дополнение к командам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="134b0-159">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="134b0-160">С помощью реестра можно определить одну или несколько расширенных команд.</span><span class="sxs-lookup"><span data-stu-id="134b0-160">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="134b0-161">Связанные команды будут отображаться только в том случае, если пользователь щелкнет правой кнопкой мыши объект, а также нажмет клавишу SHIFT.</span><span class="sxs-lookup"><span data-stu-id="134b0-161">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="134b0-162">Чтобы определить команду как расширенную, добавьте расширенное значение **reg \_ SZ** в подраздел команды.</span><span class="sxs-lookup"><span data-stu-id="134b0-162">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="134b0-163">С этим значением не должно быть связано никаких данных.</span><span class="sxs-lookup"><span data-stu-id="134b0-163">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="134b0-164">Настройка контекстного меню с помощью статических команд</span><span class="sxs-lookup"><span data-stu-id="134b0-164">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="134b0-165">После [выбора статической или динамической команды для контекстного меню](shortcut-choose-method.md) можно расширить контекстное меню для типа файла, зарегистрировав статическую команду для типа файла.</span><span class="sxs-lookup"><span data-stu-id="134b0-165">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="134b0-166">Для этого добавьте подраздел **Shell** под подразделом для ProgID приложения, связанного с типом файла.</span><span class="sxs-lookup"><span data-stu-id="134b0-166">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="134b0-167">При необходимости можно определить глагол по умолчанию для типа файла, сделав его значением по умолчанию для подраздела **Shell** .</span><span class="sxs-lookup"><span data-stu-id="134b0-167">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="134b0-168">Команда по умолчанию отображается в контекстном меню первой.</span><span class="sxs-lookup"><span data-stu-id="134b0-168">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="134b0-169">Его назначение — предоставить оболочке команду, которую она может использовать при вызове функции [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) , но команда не указана.</span><span class="sxs-lookup"><span data-stu-id="134b0-169">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="134b0-170">Оболочка не обязательно выбирает команду по умолчанию, когда **ShellExecuteEx** используется таким образом.</span><span class="sxs-lookup"><span data-stu-id="134b0-170">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="134b0-171">Оболочка использует первую доступную команду в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="134b0-171">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="134b0-172">Команда по умолчанию</span><span class="sxs-lookup"><span data-stu-id="134b0-172">The default verb</span></span>
2.  <span data-ttu-id="134b0-173">Первая команда в реестре, если указан порядок команд</span><span class="sxs-lookup"><span data-stu-id="134b0-173">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="134b0-174">Команда **открытия**</span><span class="sxs-lookup"><span data-stu-id="134b0-174">The **Open** verb</span></span>
4.  <span data-ttu-id="134b0-175">Команда **Open With**</span><span class="sxs-lookup"><span data-stu-id="134b0-175">The **Open With** verb</span></span>

<span data-ttu-id="134b0-176">Если ни одна из указанных команд не доступна, операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="134b0-176">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="134b0-177">Создайте один подраздел для каждой команды, которую необходимо добавить в подраздел Shell.</span><span class="sxs-lookup"><span data-stu-id="134b0-177">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="134b0-178">Для каждого из этих подразделов должно быть задано значение **reg \_ SZ** для отображаемой строки команды (локализованная строка).</span><span class="sxs-lookup"><span data-stu-id="134b0-178">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="134b0-179">Для каждого подраздела команды создайте подраздел команды со значением по умолчанию, равным командной строке для активации элементов.</span><span class="sxs-lookup"><span data-stu-id="134b0-179">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="134b0-180">Для канонических команд, таких как **Open** и **Print**, можно опустить отображаемую строку, так как система автоматически отображает правильно локализованную строку.</span><span class="sxs-lookup"><span data-stu-id="134b0-180">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="134b0-181">Для неканонических глаголов, если не указана отображаемая строка, строка команды отображается.</span><span class="sxs-lookup"><span data-stu-id="134b0-181">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="134b0-182">В следующем примере реестра Обратите внимание на следующее:</span><span class="sxs-lookup"><span data-stu-id="134b0-182">In the following registry example, note that:</span></span>

-   <span data-ttu-id="134b0-183">Поскольку **доит** не является канонической командой, ей присваивается отображаемое имя, которое можно выбрать, нажав клавишу D.</span><span class="sxs-lookup"><span data-stu-id="134b0-183">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="134b0-184">Команда **принтто** не отображается в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-184">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="134b0-185">Однако его включение в реестр позволяет пользователю печатать файлы путем их перетаскивания на значок принтера.</span><span class="sxs-lookup"><span data-stu-id="134b0-185">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="134b0-186">Для каждой команды отображается один подраздел.</span><span class="sxs-lookup"><span data-stu-id="134b0-186">One subkey is shown for each verb.</span></span> <span data-ttu-id="134b0-187">**%1** представляет имя файла и **%2** имя принтера.</span><span class="sxs-lookup"><span data-stu-id="134b0-187">**%1** represents the file name and **%2** the printer name.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

<span data-ttu-id="134b0-188">На следующей схеме показано расширение контекстного меню в соответствии с приведенными выше записями реестра.</span><span class="sxs-lookup"><span data-stu-id="134b0-188">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="134b0-189">Это контекстное **меню открыло**, **сделает его** и команды **печати** в своем меню, и **сделает его** в качестве глагола по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="134b0-189">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![снимок экрана контекстного меню выполнения команды по умолчанию](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="134b0-191">Активация обработчика с помощью интерфейса интерфейс IDropTarget</span><span class="sxs-lookup"><span data-stu-id="134b0-191">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="134b0-192">Платформа динамических данных Exchange (DDE) является устаревшим; Вместо этого используйте [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="134b0-192">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="134b0-193">**Интерфейс IDropTarget** является более надежным и обеспечивает лучшую поддержку активации, так как использует com-активацию обработчика.</span><span class="sxs-lookup"><span data-stu-id="134b0-193">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="134b0-194">В случае выбора нескольких элементов **интерфейс IDropTarget** не зависит от ограничений размера буфера, находящихся как в DDE, так и в [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="134b0-194">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="134b0-195">Кроме того, элементы передаются в приложение в виде объекта данных, который можно преобразовать в массив элементов с помощью функции [**шкреатешеллитемаррайфромдатаобжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="134b0-195">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="134b0-196">Это упрощается и не теряет сведения о пространстве имен, как это происходит при преобразовании элемента в путь для протоколов командной строки или DDE.</span><span class="sxs-lookup"><span data-stu-id="134b0-196">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="134b0-197">Дополнительные сведения о [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) и оболочке запросов для атрибутов сопоставления файлов см. в разделе [наблюдаемые типы и регистрация приложений](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="134b0-197">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="134b0-198">Указание расположения и порядка статических глаголов</span><span class="sxs-lookup"><span data-stu-id="134b0-198">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="134b0-199">Обычно команды упорядочиваются в контекстном меню в зависимости от того, как они перечислены. Сначала перечисление основано на порядке массива ассоциаций, а затем в порядке элементов в массиве ассоциаций, как определено в порядке сортировки реестра.</span><span class="sxs-lookup"><span data-stu-id="134b0-199">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="134b0-200">Команды можно упорядочить, указав значение по умолчанию для подраздела Shell для записи ассоциации.</span><span class="sxs-lookup"><span data-stu-id="134b0-200">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="134b0-201">Это значение по умолчанию может включать один элемент, который будет отображаться в верхней части контекстного меню, или список элементов, разделенных пробелами или запятыми.</span><span class="sxs-lookup"><span data-stu-id="134b0-201">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="134b0-202">В последнем случае первый элемент в списке является элементом по умолчанию, а остальные команды отображаются непосредственно под ним в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="134b0-202">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="134b0-203">Например, следующая запись реестра создает команды контекстного меню в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="134b0-203">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="134b0-204">Отображение</span><span class="sxs-lookup"><span data-stu-id="134b0-204">Display</span></span>
2.  <span data-ttu-id="134b0-205">Приложения</span><span class="sxs-lookup"><span data-stu-id="134b0-205">Gadgets</span></span>
3.  <span data-ttu-id="134b0-206">Personalization</span><span class="sxs-lookup"><span data-stu-id="134b0-206">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="134b0-207">Аналогичным образом следующая запись реестра создает команды контекстного меню в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="134b0-207">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="134b0-208">Personalization</span><span class="sxs-lookup"><span data-stu-id="134b0-208">Personalization</span></span>
2.  <span data-ttu-id="134b0-209">Приложения</span><span class="sxs-lookup"><span data-stu-id="134b0-209">Gadgets</span></span>
3.  <span data-ttu-id="134b0-210">Отображение</span><span class="sxs-lookup"><span data-stu-id="134b0-210">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="134b0-211">Размещение команд в верхней или нижней части меню</span><span class="sxs-lookup"><span data-stu-id="134b0-211">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="134b0-212">Следующий атрибут реестра можно использовать для размещения команды в верхней или нижней части меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-212">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="134b0-213">Если существует несколько глаголов, указывающих этот атрибут, последний из них получает приоритет:</span><span class="sxs-lookup"><span data-stu-id="134b0-213">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="134b0-214">Создание статических каскадных меню</span><span class="sxs-lookup"><span data-stu-id="134b0-214">Creating Static Cascading Menus</span></span>

<span data-ttu-id="134b0-215">В Windows 7 и более поздних версиях реализация каскадного меню поддерживается с помощью параметров реестра.</span><span class="sxs-lookup"><span data-stu-id="134b0-215">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="134b0-216">До Windows 7 создание каскадных меню было возможно только через реализацию интерфейса [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="134b0-216">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="134b0-217">В Windows 7 и более поздних версиях следует прибегать к решениям на основе кода COM только в том случае, если статические методы недостаточны.</span><span class="sxs-lookup"><span data-stu-id="134b0-217">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="134b0-218">На следующем снимке экрана приведен пример каскадного меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-218">The following screen shot provides an example of a cascading menu.</span></span>

![снимок экрана, демонстрирующий Пример каскадного меню](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="134b0-220">В Windows 7 и более поздних версиях существует три способа создания каскадных меню:</span><span class="sxs-lookup"><span data-stu-id="134b0-220">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="134b0-221">Создание каскадных меню с записью реестра "подкоманды"</span><span class="sxs-lookup"><span data-stu-id="134b0-221">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="134b0-222">Создание каскадных меню с помощью записи реестра Екстендедсубкоммандскэй</span><span class="sxs-lookup"><span data-stu-id="134b0-222">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="134b0-223">Создание каскадных меню с помощью интерфейса Иексплореркомманд</span><span class="sxs-lookup"><span data-stu-id="134b0-223">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="134b0-224">Создание каскадных меню с записью реестра "подкоманды"</span><span class="sxs-lookup"><span data-stu-id="134b0-224">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="134b0-225">В Windows 7 и более поздних версиях можно использовать запись подкоманд для создания каскадных меню с помощью следующей процедуры.</span><span class="sxs-lookup"><span data-stu-id="134b0-225">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="134b0-226">**Создание каскадного меню с помощью записи подкоманд**</span><span class="sxs-lookup"><span data-stu-id="134b0-226">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="134b0-227">Создайте подраздел в разделе **\_ Classes \_ root** \\ *ProgID* \\ **Shell** , чтобы представить свое каскадное меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-227">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="134b0-228">В этом примере мы присваиваем этому подразделу имя *каскадетест*.</span><span class="sxs-lookup"><span data-stu-id="134b0-228">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="134b0-229">Убедитесь, что значение по умолчанию для подраздела *каскадетест* пусто и отображается как **(значение не задано)**.</span><span class="sxs-lookup"><span data-stu-id="134b0-229">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="134b0-230">В подраздел *каскадетест* добавьте запись Муиверб типа **reg \_ SZ** и назначьте ей текст, который будет отображаться в контекстном меню как имя.</span><span class="sxs-lookup"><span data-stu-id="134b0-230">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="134b0-231">В этом примере мы присваиваем его «тестировать каскадное меню».</span><span class="sxs-lookup"><span data-stu-id="134b0-231">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="134b0-232">В подраздел *каскадетест* добавьте запись подкоманд с типом **reg \_ SZ** , назначенный List, демлимитед с точкой с запятой, для команд, которые должны отображаться в меню в порядке их отображения.</span><span class="sxs-lookup"><span data-stu-id="134b0-232">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="134b0-233">Например, здесь мы присваиваем ряд команд, предоставляемых системой:</span><span class="sxs-lookup"><span data-stu-id="134b0-233">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="134b0-234">В случае с пользовательскими командами реализуйте их с помощью любого из методов реализации статических команд и перечислите их в подразделе **коммандсторе** , как показано в этом примере для вымышленной глагола *вербнаме*:</span><span class="sxs-lookup"><span data-stu-id="134b0-234">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> <span data-ttu-id="134b0-235">Этот метод имеет преимущество, что пользовательские команды могут быть зарегистрированы один раз и повторно использоваться путем перечисления имени команды в записи подкоманд.</span><span class="sxs-lookup"><span data-stu-id="134b0-235">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="134b0-236">Однако для этого требуется, чтобы приложение имело разрешение на изменение реестра на **\_ локальном \_ компьютере** в разделе hKey.</span><span class="sxs-lookup"><span data-stu-id="134b0-236">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="134b0-237">Создание каскадных меню с помощью записи реестра Екстендедсубкоммандскэй</span><span class="sxs-lookup"><span data-stu-id="134b0-237">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="134b0-238">В Windows 7 и более поздних версиях можно использовать запись Екстендедсубкоммандкэй для создания расширенных каскадных меню: каскадные меню в каскадных меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-238">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="134b0-239">На следующем снимке экрана показан пример расширенного каскадного меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-239">The following screen shot is an example of an extended cascading menu.</span></span>

![снимок экрана с расширенным каскадным меню для устройств](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="134b0-241">Поскольку **\_ \_ корневой класс hKey classes** является сочетанием **\_ текущего \_ пользователя hKey** и раздела **hKey \_ \_**, можно зарегистрировать любые пользовательские команды в подразделе "классы" программного обеспечения **\_ текущего \_ пользователя "hKey** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="134b0-241">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="134b0-242">Основное преимущество этого подхода в том, что повышенное разрешение не требуется.</span><span class="sxs-lookup"><span data-stu-id="134b0-242">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="134b0-243">Кроме того, другие сопоставления файлов могут повторно использовать этот полный набор команд, указав тот же подраздел Екстендедсубкоммандскэй.</span><span class="sxs-lookup"><span data-stu-id="134b0-243">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="134b0-244">Если не требуется повторно использовать этот набор команд, можно вывести список команд в родительском объекте, но убедитесь, что значение по умолчанию родительского элемента пустое.</span><span class="sxs-lookup"><span data-stu-id="134b0-244">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="134b0-245">**Создание каскадного меню с помощью записи Екстендедсубкоммандскэй**</span><span class="sxs-lookup"><span data-stu-id="134b0-245">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="134b0-246">Создайте подраздел в разделе **\_ Classes \_ root** \\ *ProgID* \\ **Shell** , чтобы представить свое каскадное меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-246">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="134b0-247">В этом примере мы присваиваем этому подразделу имя *CascadeTest2*.</span><span class="sxs-lookup"><span data-stu-id="134b0-247">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="134b0-248">Убедитесь, что значение по умолчанию для подраздела *каскадетест* пусто и отображается как **(значение не задано)**.</span><span class="sxs-lookup"><span data-stu-id="134b0-248">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="134b0-249">В подраздел *каскадетест* добавьте запись Муиверб типа **reg \_ SZ** и назначьте ей текст, который будет отображаться в контекстном меню как имя.</span><span class="sxs-lookup"><span data-stu-id="134b0-249">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="134b0-250">В этом примере мы присваиваем его «тестировать каскадное меню».</span><span class="sxs-lookup"><span data-stu-id="134b0-250">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="134b0-251">В созданном вами подразделе *каскадетест* добавьте подраздел **екстендедсубкоммандскэй** , а затем добавьте подкоманды документа (типа **reg \_ SZ** ), например:</span><span class="sxs-lookup"><span data-stu-id="134b0-251">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    <span data-ttu-id="134b0-252">Убедитесь, что значение по умолчанию для подраздела *тест Cascade меню 2* пусто и отображается как **(значение не задано)**.</span><span class="sxs-lookup"><span data-stu-id="134b0-252">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="134b0-253">Заполните подкоманды с помощью любой из следующих статических реализаций глаголов.</span><span class="sxs-lookup"><span data-stu-id="134b0-253">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="134b0-254">Обратите внимание, что подраздел Коммандфлагс представляет значения ЕКСПКМДФЛАГС.</span><span class="sxs-lookup"><span data-stu-id="134b0-254">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="134b0-255">Если вы хотите добавить разделитель до или после пункта меню Cascade, используйте ЕКФ \_ сепараторбефоре (0x20) или ЕКФ \_ сепараторафтер (0x40).</span><span class="sxs-lookup"><span data-stu-id="134b0-255">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="134b0-256">Описание этих флагов Windows 7 и более поздних версий см. в разделе [**иексплореркомманд::-flags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="134b0-256">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="134b0-257">ЕКФ \_ сепараторбефоре работает только для пунктов меню верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="134b0-257">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="134b0-258">Муиверб имеет тип **reg \_ SZ**, а Коммандфлагс имеет тип **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="134b0-258">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

<span data-ttu-id="134b0-259">На следующем снимке экрана показан пример записи предыдущего раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="134b0-259">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![снимок экрана, показывающий пример каскадного меню, в котором отображаются параметры блокнота и WordPad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="134b0-261">Создание каскадных меню с помощью интерфейса Иексплореркомманд</span><span class="sxs-lookup"><span data-stu-id="134b0-261">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="134b0-262">Другим вариантом добавления команд в каскадное меню является [**иексплореркомманд:: енумсубкоммандс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="134b0-262">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="134b0-263">Этот метод позволяет источникам данных, которые предоставляют команды командного модуля через [**иексплореркоммандпровидер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) , использовать эти команды в качестве команд в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-263">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="134b0-264">В Windows 7 и более поздних версиях вы можете предоставить ту же реализацию команды с помощью [**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , как и с [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="134b0-264">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="134b0-265">Следующие два снимка экрана иллюстрируют использование каскадных меню в папке **Devices** .</span><span class="sxs-lookup"><span data-stu-id="134b0-265">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Снимок экрана, на котором показан пример каскадного меню в папке Devices.](images/file-assoc/filecascademenu.png)

<span data-ttu-id="134b0-267">На следующем снимке экрана показана другая реализация каскадного меню в папке **Devices** .</span><span class="sxs-lookup"><span data-stu-id="134b0-267">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![снимок экрана, показывающий пример каскадного меню в папке "устройства"](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="134b0-269">Так как [**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) поддерживает только внутрипроцессный активацию, рекомендуется использовать их в качестве источников данных оболочки, которые должны совместно использовать реализацию команд и контекстных меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-269">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="134b0-270">Получение динамического поведения для статических команд с помощью расширенного синтаксиса запросов</span><span class="sxs-lookup"><span data-stu-id="134b0-270">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="134b0-271">Расширенный синтаксис запросов (АКС) может выразить условие, которое будет оцениваться с помощью свойств элемента, для которого создается экземпляр команды.</span><span class="sxs-lookup"><span data-stu-id="134b0-271">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="134b0-272">Эта система работает только с быстрыми свойствами.</span><span class="sxs-lookup"><span data-stu-id="134b0-272">This system works only with fast properties.</span></span> <span data-ttu-id="134b0-273">Это свойства, которые источник данных оболочки сообщает быстро, не возвращая [\* \* \* \* школстате \_ медленный \* \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* \* из [**IShellFolder2:: жетдефаултколумнстате**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span><span class="sxs-lookup"><span data-stu-id="134b0-273">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="134b0-274">Windows 7 и более поздние версии поддерживают канонические значения, что позволяет избежать проблем в локализованных сборках.</span><span class="sxs-lookup"><span data-stu-id="134b0-274">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="134b0-275">Для использования этого расширения Windows 7 в локализованных сборках требуется следующий канонический синтаксис.</span><span class="sxs-lookup"><span data-stu-id="134b0-275">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="134b0-276">В следующем примере запись реестра:</span><span class="sxs-lookup"><span data-stu-id="134b0-276">In the following example registry entry:</span></span>

-   <span data-ttu-id="134b0-277">Значение **appliesTo** определяет, отображается ли глагол или скрыт.</span><span class="sxs-lookup"><span data-stu-id="134b0-277">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="134b0-278">Значение Дефаултапплиесто определяет, какая команда является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="134b0-278">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="134b0-279">Значение Хаслуашиелд определяет, отображается ли экранирование контроля учетных записей (UAC).</span><span class="sxs-lookup"><span data-stu-id="134b0-279">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="134b0-280">В этом примере значение **дефаултапплиесто** делает эту команду по умолчанию для любого файла с словом "exampleText1" в имени файла.</span><span class="sxs-lookup"><span data-stu-id="134b0-280">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="134b0-281">Значение **appliesTo** позволяет команде для любого файла с именем "exampleText1" в имени.</span><span class="sxs-lookup"><span data-stu-id="134b0-281">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="134b0-282">Значение **хаслуашиелд** отображает экранирование для файлов с именем "exampleText2" в имени.</span><span class="sxs-lookup"><span data-stu-id="134b0-282">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="134b0-283">Добавьте подраздел **Command** и значение:</span><span class="sxs-lookup"><span data-stu-id="134b0-283">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="134b0-284">В реестре Windows 7 ознакомьтесь с разделом **\_ \_ корневые диски классов hKey** в \\  качестве примера команд BitLocker, которые используют следующий подход:</span><span class="sxs-lookup"><span data-stu-id="134b0-284">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="134b0-285">AppliesTo = System. Volume. Битлоккерпротектион: = 2</span><span class="sxs-lookup"><span data-stu-id="134b0-285">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="134b0-286">System. Volume. Битлоккеррекуиресадмин: = System. Структуредкуеритипе. Boolean \# true</span><span class="sxs-lookup"><span data-stu-id="134b0-286">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="134b0-287">Дополнительные сведения о АКС см. в разделе [Расширенный синтаксис запросов](../search/-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="134b0-287">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="134b0-288">Не рекомендуется: связывание команд с командами платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="134b0-288">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="134b0-289">DDE устарело; Вместо этого используйте [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="134b0-289">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="134b0-290">Протокол DDE является устаревшим, так как он использует широковещательное сообщение окна для обнаружения сервера DDE.</span><span class="sxs-lookup"><span data-stu-id="134b0-290">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="134b0-291">Зависание сервера DDE приводит к зависанию окна вещания и, следовательно, зависания диалога DDE для других приложений.</span><span class="sxs-lookup"><span data-stu-id="134b0-291">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="134b0-292">Обычно для одного задержанного приложения возникает необходимость в последующем зависании в работе пользователя.</span><span class="sxs-lookup"><span data-stu-id="134b0-292">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="134b0-293">Метод [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) является более надежным и обеспечивает лучшую поддержку активации, поскольку он использует com-активацию обработчика.</span><span class="sxs-lookup"><span data-stu-id="134b0-293">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="134b0-294">В случае выбора нескольких элементов **интерфейс IDropTarget** не зависит от ограничений размера буфера, находящихся как в DDE, так и в [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="134b0-294">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="134b0-295">Кроме того, элементы передаются в приложение в виде объекта данных, который можно преобразовать в массив элементов с помощью функции [**шкреатешеллитемаррайфромдатаобжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="134b0-295">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="134b0-296">Это упрощается и не теряет сведения о пространстве имен, как это происходит при преобразовании элемента в путь для протоколов командной строки или DDE.</span><span class="sxs-lookup"><span data-stu-id="134b0-296">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="134b0-297">Дополнительные сведения о [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) и оболочке запросов для атрибутов сопоставления файлов см. в разделе [наблюдаемые типы и регистрация приложений](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="134b0-297">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="134b0-298">Завершение задач реализации команд</span><span class="sxs-lookup"><span data-stu-id="134b0-298">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="134b0-299">Следующие задачи для реализации команд относятся к реализации статических и динамических команд.</span><span class="sxs-lookup"><span data-stu-id="134b0-299">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="134b0-300">Дополнительные сведения о динамических командах см. в разделе [Настройка контекстного меню с помощью динамических команд](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="134b0-300">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="134b0-301">Настройка контекстного меню для предопределенных объектов оболочки</span><span class="sxs-lookup"><span data-stu-id="134b0-301">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="134b0-302">У многих предопределенных объектов оболочки есть контекстные меню, которые можно настроить.</span><span class="sxs-lookup"><span data-stu-id="134b0-302">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="134b0-303">Зарегистрируйте команду практически так же, как при регистрации типов файлов, но используйте имя предопределенного объекта в качестве имени типа файла.</span><span class="sxs-lookup"><span data-stu-id="134b0-303">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="134b0-304">Список предопределенных объектов находится в разделе *предопределенных объектов оболочки* , посвященном [созданию обработчиков расширений оболочки](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="134b0-304">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="134b0-305">Эти предопределенные объекты оболочки, контекстные меню которых можно настроить путем добавления команд в реестр, помечаются в таблице с помощью команды Word.</span><span class="sxs-lookup"><span data-stu-id="134b0-305">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="134b0-306">Расширение нового подменю</span><span class="sxs-lookup"><span data-stu-id="134b0-306">Extending a New Submenu</span></span>

<span data-ttu-id="134b0-307">Когда пользователь открывает меню **файл** в проводнике Windows, одна из отображаемых команд является **новой**.</span><span class="sxs-lookup"><span data-stu-id="134b0-307">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="134b0-308">При выборе этой команды отображается подменю.</span><span class="sxs-lookup"><span data-stu-id="134b0-308">Selecting this command displays a submenu.</span></span> <span data-ttu-id="134b0-309">По умолчанию подменю содержит две команды, **папку** и **ярлык**, которые позволяют пользователям создавать вложенные папки и ярлыки.</span><span class="sxs-lookup"><span data-stu-id="134b0-309">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="134b0-310">Это подменю можно расширить, включив команды создания файлов для любого типа файлов.</span><span class="sxs-lookup"><span data-stu-id="134b0-310">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="134b0-311">Чтобы добавить команду создания файла в подменю **создать** , файлы приложения должны иметь связанный тип файлов.</span><span class="sxs-lookup"><span data-stu-id="134b0-311">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="134b0-312">Включите подраздел **шеллнев** под именем файла.</span><span class="sxs-lookup"><span data-stu-id="134b0-312">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="134b0-313">Если выбрана команда **создать** меню **файл** , оболочка добавляет тип файла в подменю **создать** .</span><span class="sxs-lookup"><span data-stu-id="134b0-313">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="134b0-314">Отображаемая строка команды представляет собой описательную строку, назначенную ProgID программы.</span><span class="sxs-lookup"><span data-stu-id="134b0-314">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="134b0-315">Чтобы указать метод создания файла, назначьте одно или несколько значений данных подразделу **шеллнев** .</span><span class="sxs-lookup"><span data-stu-id="134b0-315">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="134b0-316">Доступные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="134b0-316">The available values are listed in the following table.</span></span>



| <span data-ttu-id="134b0-317">Значение подраздела Шеллнев</span><span class="sxs-lookup"><span data-stu-id="134b0-317">ShellNew subkey value</span></span> | <span data-ttu-id="134b0-318">Описание</span><span class="sxs-lookup"><span data-stu-id="134b0-318">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="134b0-319">Команда</span><span class="sxs-lookup"><span data-stu-id="134b0-319">Command</span></span>               | <span data-ttu-id="134b0-320">Выполняет приложение.</span><span class="sxs-lookup"><span data-stu-id="134b0-320">Executes an application.</span></span> <span data-ttu-id="134b0-321">Это значение **reg \_ SZ** указывает путь к выполняемому приложению.</span><span class="sxs-lookup"><span data-stu-id="134b0-321">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="134b0-322">Например, можно задать запуск мастера.</span><span class="sxs-lookup"><span data-stu-id="134b0-322">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="134b0-323">Данные</span><span class="sxs-lookup"><span data-stu-id="134b0-323">Data</span></span>                  | <span data-ttu-id="134b0-324">Создает файл, содержащий указанные данные.</span><span class="sxs-lookup"><span data-stu-id="134b0-324">Creates a file containing specified data.</span></span> <span data-ttu-id="134b0-325">Этот **\_ двоичный параметр reg** задает данные файла.</span><span class="sxs-lookup"><span data-stu-id="134b0-325">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="134b0-326">**Данные** пропускаются, если указано либо **Нуллфиле** , либо **filename** .</span><span class="sxs-lookup"><span data-stu-id="134b0-326">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="134b0-327">FileName</span><span class="sxs-lookup"><span data-stu-id="134b0-327">FileName</span></span>              | <span data-ttu-id="134b0-328">Создает файл, который является копией указанного файла.</span><span class="sxs-lookup"><span data-stu-id="134b0-328">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="134b0-329">Это значение **reg \_ SZ** указывает полный путь к копируемому файлу.</span><span class="sxs-lookup"><span data-stu-id="134b0-329">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="134b0-330">нуллфиле</span><span class="sxs-lookup"><span data-stu-id="134b0-330">NullFile</span></span>              | <span data-ttu-id="134b0-331">Создает пустой файл.</span><span class="sxs-lookup"><span data-stu-id="134b0-331">Creates an empty file.</span></span> <span data-ttu-id="134b0-332">**Нуллфиле** не имеет присвоенного значения.</span><span class="sxs-lookup"><span data-stu-id="134b0-332">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="134b0-333">Если указан параметр **нуллфиле** , значения реестра **Data** и **filename** игнорируются.</span><span class="sxs-lookup"><span data-stu-id="134b0-333">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="134b0-334">В следующем примере раздела реестра и снимке экрана показано **новое** подменю для типа файла МИП-MS.</span><span class="sxs-lookup"><span data-stu-id="134b0-334">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="134b0-335">У него есть команда **MyProgram Application**.</span><span class="sxs-lookup"><span data-stu-id="134b0-335">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="134b0-336">На снимке экрана показано **новое** подменю.</span><span class="sxs-lookup"><span data-stu-id="134b0-336">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="134b0-337">Когда пользователь выбирает **приложение MyProgram** из подменю **создать** , оболочка создает файл с именем **New MyProgram Application. МИП-ms** и передает его в **MyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="134b0-337">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![снимок экрана Windows Explorer с новой командой "приложение MyProgram" в подменю "создать"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="134b0-339">Создание обработчиков перетаскивания</span><span class="sxs-lookup"><span data-stu-id="134b0-339">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="134b0-340">Базовая процедура реализации обработчика перетаскивания аналогична процедуре для обычных обработчиков контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-340">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="134b0-341">Однако обработчики контекстного меню обычно используют только указатель [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) , передаваемый методу [**Ишеллекстинит:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) обработчика, для извлечения имени объекта.</span><span class="sxs-lookup"><span data-stu-id="134b0-341">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="134b0-342">Обработчик перетаскивания может реализовать более сложный обработчик данных для изменения поведения перетаскиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="134b0-342">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="134b0-343">Когда пользователь щелкает правой кнопкой мыши объект оболочки для перетаскивания объекта, контекстное меню отображается, когда пользователь пытается удалить объект.</span><span class="sxs-lookup"><span data-stu-id="134b0-343">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="134b0-344">На следующем снимке экрана показан типичный контекстный меню для перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="134b0-344">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![снимок экрана с контекстным меню перетаскивания](images/context-menu/context-dragdrop.png)

<span data-ttu-id="134b0-346">Обработчик перетаскивания — это обработчик контекстного меню, который может добавлять элементы в контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="134b0-346">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="134b0-347">Обработчики перетаскивания обычно регистрируются в следующем подразделе.</span><span class="sxs-lookup"><span data-stu-id="134b0-347">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="134b0-348">Добавьте подраздел в подраздел **драгдрофандлерс** с именем для обработчика перетаскивания и задайте в качестве значения по умолчанию для подраздела строковое значение GUID идентификатора класса обработчика (CLSID).</span><span class="sxs-lookup"><span data-stu-id="134b0-348">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="134b0-349">В следующем примере активируется обработчик перетаскивания **мидд** .</span><span class="sxs-lookup"><span data-stu-id="134b0-349">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="134b0-350">Подавление команд и управление видимостью</span><span class="sxs-lookup"><span data-stu-id="134b0-350">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="134b0-351">Для управления видимостью команды можно использовать параметры политики Windows.</span><span class="sxs-lookup"><span data-stu-id="134b0-351">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="134b0-352">Команды можно подавлять с помощью параметров политики, добавив значение **суппрессионполици** или значение GUID **суппрессионполициекс** в подраздел реестра команды.</span><span class="sxs-lookup"><span data-stu-id="134b0-352">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="134b0-353">Присвойте параметру подраздела **СУППРЕССИОНПОЛИЦИ** идентификатор политики.</span><span class="sxs-lookup"><span data-stu-id="134b0-353">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="134b0-354">Если политика включена, команда и связанная с ней запись контекстного меню подавляются.</span><span class="sxs-lookup"><span data-stu-id="134b0-354">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="134b0-355">Возможные значения идентификатора политики см. в описании перечисления [**ограничений**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="134b0-355">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="134b0-356">Применение модели выбора глагола</span><span class="sxs-lookup"><span data-stu-id="134b0-356">Employing the Verb Selection Model</span></span>

<span data-ttu-id="134b0-357">Значения реестра должны быть заданы для команд, чтобы обрабатывать ситуации, когда пользователь может выбрать один элемент, несколько элементов или выбрать из элемента.</span><span class="sxs-lookup"><span data-stu-id="134b0-357">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="134b0-358">Команда требует наличия отдельных значений реестра для каждой из трех ситуаций, поддерживаемых командой.</span><span class="sxs-lookup"><span data-stu-id="134b0-358">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="134b0-359">Ниже приведены возможные значения для модели выбора команд.</span><span class="sxs-lookup"><span data-stu-id="134b0-359">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="134b0-360">Укажите значение Мултиселектмодел для всех команд.</span><span class="sxs-lookup"><span data-stu-id="134b0-360">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="134b0-361">Если значение Мултиселектмодел не указано, оно выводится из выбранного типа реализации глагола.</span><span class="sxs-lookup"><span data-stu-id="134b0-361">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="134b0-362">Для **методов,** основанных на com (например, Дроптаржет и **ExecuteCommand),** предполагается, а для других методов —.</span><span class="sxs-lookup"><span data-stu-id="134b0-362">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="134b0-363">Укажите **одну** для команд, поддерживающих только один выбор.</span><span class="sxs-lookup"><span data-stu-id="134b0-363">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="134b0-364">Укажите **проигрыватель** для команд, которые поддерживают любое количество элементов.</span><span class="sxs-lookup"><span data-stu-id="134b0-364">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="134b0-365">Укажите **документ** для команд, которые создают окно верхнего уровня для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="134b0-365">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="134b0-366">Это ограничивает количество активированных элементов и помогает избежать переполнения системных ресурсов, если пользователь открывает слишком много окон.</span><span class="sxs-lookup"><span data-stu-id="134b0-366">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="134b0-367">Если выбранное число элементов не соответствует модели выбора глагола или превышает ограничения по умолчанию, описанные в следующей таблице, команда не отображается.</span><span class="sxs-lookup"><span data-stu-id="134b0-367">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="134b0-368">Тип реализации глагола</span><span class="sxs-lookup"><span data-stu-id="134b0-368">Type of verb implementation</span></span> | <span data-ttu-id="134b0-369">Документ</span><span class="sxs-lookup"><span data-stu-id="134b0-369">Document</span></span> | <span data-ttu-id="134b0-370">Проигрыватель</span><span class="sxs-lookup"><span data-stu-id="134b0-370">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="134b0-371">Прежняя версия</span><span class="sxs-lookup"><span data-stu-id="134b0-371">Legacy</span></span>                      | <span data-ttu-id="134b0-372">15 элементов</span><span class="sxs-lookup"><span data-stu-id="134b0-372">15 items</span></span> | <span data-ttu-id="134b0-373">100 элементов</span><span class="sxs-lookup"><span data-stu-id="134b0-373">100 items</span></span> |
| <span data-ttu-id="134b0-374">COM</span><span class="sxs-lookup"><span data-stu-id="134b0-374">COM</span></span>                         | <span data-ttu-id="134b0-375">15 элементов</span><span class="sxs-lookup"><span data-stu-id="134b0-375">15 items</span></span> | <span data-ttu-id="134b0-376">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="134b0-376">No limit</span></span>  |



 

<span data-ttu-id="134b0-377">Ниже приведены примеры записей реестра с использованием значения Мултиселектмодел.</span><span class="sxs-lookup"><span data-stu-id="134b0-377">The following are example registry entries using the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a><span data-ttu-id="134b0-378">Использование атрибутов элементов</span><span class="sxs-lookup"><span data-stu-id="134b0-378">Using Item Attributes</span></span>

<span data-ttu-id="134b0-379">Значения флагов [**сфгао**](sfgao.md) атрибутов оболочки для элемента можно проверить, чтобы определить, должна ли команда быть включена или отключена.</span><span class="sxs-lookup"><span data-stu-id="134b0-379">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="134b0-380">Чтобы использовать эту функцию атрибута, добавьте следующие значения **reg \_ DWORD** в команду:</span><span class="sxs-lookup"><span data-stu-id="134b0-380">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="134b0-381">Значение Аттрибутемаск указывает значение [**сфгао**](sfgao.md) для битовых значений маски для проверки.</span><span class="sxs-lookup"><span data-stu-id="134b0-381">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="134b0-382">Значение AttributeValue указывает значение [**сфгао**](sfgao.md) для проверяемых битов.</span><span class="sxs-lookup"><span data-stu-id="134b0-382">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="134b0-383">Имплиедселектионмодел указывает ноль для глаголов элемента или ненулевое значение для команд в контекстном меню фона.</span><span class="sxs-lookup"><span data-stu-id="134b0-383">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="134b0-384">В следующем примере записи реестра Аттрибутемаск имеет значение [**сфгао \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="134b0-384">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="134b0-385">Реализация пользовательских команд для папок с помощью Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="134b0-385">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="134b0-386">В Windows 7 и более поздних версиях можно добавлять команды в папку с помощью Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="134b0-386">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="134b0-387">Дополнительные сведения о Desktop.ini файлах см. [в статье Настройка папок с помощью Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="134b0-387">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="134b0-388">Desktop.ini файлы всегда должны быть помечены как   +  **скрытые** системой, чтобы они не отображались для пользователей.</span><span class="sxs-lookup"><span data-stu-id="134b0-388">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="134b0-389">**Чтобы добавить пользовательские команды для папок с помощью файла Desktop.ini, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="134b0-389">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="134b0-390">Создайте папку, которая помечена как доступная **только для чтения** или как **система**.</span><span class="sxs-lookup"><span data-stu-id="134b0-390">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="134b0-391">Создайте файл Desktop.ini, содержащий \[ . Шеллклассинфо \] директорикласс = ProgID папки.</span><span class="sxs-lookup"><span data-stu-id="134b0-391">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="134b0-392">В реестре создайте **класс hKey с \_ \_ корневой** \\ **папкой ProgID** со значением канусефордиректори.</span><span class="sxs-lookup"><span data-stu-id="134b0-392">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="134b0-393">Значение Канусефордиректори позволяет избежать неправильного использования ProgID, которые не участвуют в реализации пользовательских команд для папок с помощью Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="134b0-393">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="134b0-394">Добавьте команды в подключе ProgID **папки**, например:</span><span class="sxs-lookup"><span data-stu-id="134b0-394">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="134b0-395">Эти глаголы могут быть глаголами по умолчанию. в этом случае двойной щелчок папки активирует команду.</span><span class="sxs-lookup"><span data-stu-id="134b0-395">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="134b0-396">См. также</span><span class="sxs-lookup"><span data-stu-id="134b0-396">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="134b0-397">Рекомендации по работе с обработчиками контекстного меню и несколькими командами выбора</span><span class="sxs-lookup"><span data-stu-id="134b0-397">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="134b0-398">Выбор статической или динамической команды для контекстного меню</span><span class="sxs-lookup"><span data-stu-id="134b0-398">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="134b0-399">Настройка контекстного меню с помощью динамических команд</span><span class="sxs-lookup"><span data-stu-id="134b0-399">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="134b0-400">Контекстное меню (контекст) и обработчики контекстного меню</span><span class="sxs-lookup"><span data-stu-id="134b0-400">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="134b0-401">Команды и сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="134b0-401">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="134b0-402">Справочник по контекстному меню</span><span class="sxs-lookup"><span data-stu-id="134b0-402">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
