---
description: Обработчики контекстного меню, также известные как обработчики контекстного меню или обработчиков команд, являются типом обработчика типов файлов. Как и все такие обработчики, они являются внутрипроцессный COM-объектами, реализованными в виде библиотек DLL.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Создание обработчиков контекстного меню
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e102833453566f42d058ff82061f34ebc65691
ms.sourcegitcommit: 9655f82be96b11258276fdefff14423c30552fbb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "109740575"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="aacd3-104">Создание обработчиков контекстного меню</span><span class="sxs-lookup"><span data-stu-id="aacd3-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="aacd3-105">Обработчики контекстного меню, также известные как обработчики контекстного меню или обработчиков команд, являются типом обработчика типов файлов.</span><span class="sxs-lookup"><span data-stu-id="aacd3-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="aacd3-106">Эти обработчики могут быть импелментед, что приводит к их загрузке в собственном процессе или в обозревателе или других сторонних процессах.</span><span class="sxs-lookup"><span data-stu-id="aacd3-106">These handlers may be impelmented in a way that causes them to load in their own process or in the explorer, or other 3rd party processes.</span></span> <span data-ttu-id="aacd3-107">Следите за тем, чтобы создавать внутрипроцессный обработчики, так как они могут причинить вред процессу, который их загружает.</span><span class="sxs-lookup"><span data-stu-id="aacd3-107">Take care when creating in-process handlers as they can cause harm to the process that loads them.</span></span>

> [!Note]  
> <span data-ttu-id="aacd3-108">Существуют специальные рекомендации по 64-разрядным версиям Windows при регистрации обработчиков, работающих в контексте 32-разрядных приложений: при вызове в контексте приложения с разной разрядностью Подсистема WOW64 перенаправляет доступ файловой системы к некоторым путям.</span><span class="sxs-lookup"><span data-stu-id="aacd3-108">There are special considerations for 64-bit based versions of Windows when registering handlers that work in the context of 32-bit applications: when invoked in the context of an application of different bitness, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="aacd3-109">Если обработчик. exe хранится в одном из этих путей, он недоступен в этом контексте.</span><span class="sxs-lookup"><span data-stu-id="aacd3-109">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="aacd3-110">Поэтому в качестве решения сохраните EXE-файл в пути, который не перенаправлен, или сохраните версию заглушки exe-файла, которая запускает реальную версию.</span><span class="sxs-lookup"><span data-stu-id="aacd3-110">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

<span data-ttu-id="aacd3-111">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="aacd3-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="aacd3-112">Канонические команды</span><span class="sxs-lookup"><span data-stu-id="aacd3-112">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="aacd3-113">Расширенные глаголы</span><span class="sxs-lookup"><span data-stu-id="aacd3-113">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="aacd3-114">Программный доступ только к командам</span><span class="sxs-lookup"><span data-stu-id="aacd3-114">Programmatic Access Only Verbs</span></span>](#programmaticaccessonly-verbs)
-   [<span data-ttu-id="aacd3-115">Настройка контекстного меню с помощью статических команд</span><span class="sxs-lookup"><span data-stu-id="aacd3-115">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="aacd3-116">Активация обработчика с помощью интерфейса интерфейс IDropTarget</span><span class="sxs-lookup"><span data-stu-id="aacd3-116">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="aacd3-117">Указание расположения и порядка статических глаголов</span><span class="sxs-lookup"><span data-stu-id="aacd3-117">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="aacd3-118">Размещение команд в верхней или нижней части меню</span><span class="sxs-lookup"><span data-stu-id="aacd3-118">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="aacd3-119">Создание статических каскадных меню</span><span class="sxs-lookup"><span data-stu-id="aacd3-119">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="aacd3-120">Получение динамического поведения для статических команд с помощью расширенного синтаксиса запросов</span><span class="sxs-lookup"><span data-stu-id="aacd3-120">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="aacd3-121">Не рекомендуется: связывание команд с командами платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="aacd3-121">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="aacd3-122">Завершение задач реализации команд</span><span class="sxs-lookup"><span data-stu-id="aacd3-122">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="aacd3-123">Настройка контекстного меню для предопределенных объектов оболочки</span><span class="sxs-lookup"><span data-stu-id="aacd3-123">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="aacd3-124">Расширение нового подменю</span><span class="sxs-lookup"><span data-stu-id="aacd3-124">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="aacd3-125">Подавление команд и управление видимостью</span><span class="sxs-lookup"><span data-stu-id="aacd3-125">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="aacd3-126">Применение модели выбора глагола</span><span class="sxs-lookup"><span data-stu-id="aacd3-126">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="aacd3-127">Использование атрибутов элементов</span><span class="sxs-lookup"><span data-stu-id="aacd3-127">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="aacd3-128">Реализация пользовательских команд для папок с помощью Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="aacd3-128">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="aacd3-129">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="aacd3-129">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="aacd3-130">Канонические команды</span><span class="sxs-lookup"><span data-stu-id="aacd3-130">Canonical Verbs</span></span>

<span data-ttu-id="aacd3-131">Приложения обычно отвечают за предоставление локализованных отображаемых строк для глаголов, которые они определяют.</span><span class="sxs-lookup"><span data-stu-id="aacd3-131">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="aacd3-132">Однако для обеспечения степени независимости от языка система определяет стандартный набор часто используемых глаголов, называемых каноническими глаголами.</span><span class="sxs-lookup"><span data-stu-id="aacd3-132">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="aacd3-133">Каноническая команда никогда не отображается для пользователя и может использоваться с любым языком пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="aacd3-133">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="aacd3-134">Система использует каноническое имя для автоматического создания правильно локализованной отображаемой строки.</span><span class="sxs-lookup"><span data-stu-id="aacd3-134">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="aacd3-135">Например, отображаемая строка команды открытия задается как **открытая** в системе на английском языке и как эквивалент немецкого в системе на немецком языке.</span><span class="sxs-lookup"><span data-stu-id="aacd3-135">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>


| <span data-ttu-id="aacd3-136">Каноническая команда</span><span class="sxs-lookup"><span data-stu-id="aacd3-136">Canonical verb</span></span> | <span data-ttu-id="aacd3-137">Описание</span><span class="sxs-lookup"><span data-stu-id="aacd3-137">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="aacd3-138">Открыть</span><span class="sxs-lookup"><span data-stu-id="aacd3-138">Open</span></span>           | <span data-ttu-id="aacd3-139">Открывает файл или папку.</span><span class="sxs-lookup"><span data-stu-id="aacd3-139">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="aacd3-140">опеннев</span><span class="sxs-lookup"><span data-stu-id="aacd3-140">Opennew</span></span>        | <span data-ttu-id="aacd3-141">Открывает файл или папку в новом окне.</span><span class="sxs-lookup"><span data-stu-id="aacd3-141">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="aacd3-142">Печать</span><span class="sxs-lookup"><span data-stu-id="aacd3-142">Print</span></span>          | <span data-ttu-id="aacd3-143">Выводит файл.</span><span class="sxs-lookup"><span data-stu-id="aacd3-143">Prints the file.</span></span>                                                     |
| <span data-ttu-id="aacd3-144">принтто</span><span class="sxs-lookup"><span data-stu-id="aacd3-144">Printto</span></span>        | <span data-ttu-id="aacd3-145">Разрешает пользователю печатать файл, перетаскивая его на объект принтера.</span><span class="sxs-lookup"><span data-stu-id="aacd3-145">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="aacd3-146">Анализ</span><span class="sxs-lookup"><span data-stu-id="aacd3-146">Explore</span></span>        | <span data-ttu-id="aacd3-147">Открывает проводник Windows с выбранной папкой.</span><span class="sxs-lookup"><span data-stu-id="aacd3-147">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="aacd3-148">Свойства</span><span class="sxs-lookup"><span data-stu-id="aacd3-148">Properties</span></span>     | <span data-ttu-id="aacd3-149">Открывает страницу свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="aacd3-149">Opens the object's property sheet.</span></span>                                   |

> [!Note]  
> <span data-ttu-id="aacd3-150">Команда **принтто** также является канонической, но никогда не отображается.</span><span class="sxs-lookup"><span data-stu-id="aacd3-150">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="aacd3-151">Его включение позволяет пользователю распечатать файл, перетащив его в объект принтера.</span><span class="sxs-lookup"><span data-stu-id="aacd3-151">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

<span data-ttu-id="aacd3-152">Обработчики контекстного меню могут предоставлять собственные канонические команды через [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) с **GC \_ вербв** или **GC \_ verb**.</span><span class="sxs-lookup"><span data-stu-id="aacd3-152">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="aacd3-153">Система будет использовать канонические команды в качестве второго параметра (*лпоператион*), переданного в [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), и является [**кминвокекоммандинфо**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). член **лпверб** , переданный в метод [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="aacd3-153">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="aacd3-154">Расширенные глаголы</span><span class="sxs-lookup"><span data-stu-id="aacd3-154">Extended Verbs</span></span>

<span data-ttu-id="aacd3-155">Когда пользователь щелкает правой кнопкой мыши объект, в контекстном меню отображаются команды по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aacd3-155">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="aacd3-156">Может потребоваться добавить и поддерживать команды в некоторых контекстных меню, которые не отображаются в каждом из контекстных меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-156">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="aacd3-157">Например, можно использовать команды, которые обычно не используются или предназначены для опытных пользователей.</span><span class="sxs-lookup"><span data-stu-id="aacd3-157">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="aacd3-158">По этой причине можно также определить одну или несколько расширенных команд.</span><span class="sxs-lookup"><span data-stu-id="aacd3-158">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="aacd3-159">Эти глаголы похожи на обычные глаголы, но отличаются от обычных глаголов способом их регистрации.</span><span class="sxs-lookup"><span data-stu-id="aacd3-159">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="aacd3-160">Чтобы получить доступ к расширенным командам, пользователь должен щелкнуть объект правой кнопкой мыши и нажать клавишу SHIFT.</span><span class="sxs-lookup"><span data-stu-id="aacd3-160">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="aacd3-161">Когда пользователь делает это, расширенные команды отображаются в дополнение к командам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aacd3-161">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="aacd3-162">С помощью реестра можно определить одну или несколько расширенных команд.</span><span class="sxs-lookup"><span data-stu-id="aacd3-162">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="aacd3-163">Связанные команды будут отображаться только в том случае, если пользователь щелкнет правой кнопкой мыши объект, а также нажмет клавишу SHIFT.</span><span class="sxs-lookup"><span data-stu-id="aacd3-163">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="aacd3-164">Чтобы определить команду как расширенную, добавьте расширенное значение **reg \_ SZ** в подраздел команды.</span><span class="sxs-lookup"><span data-stu-id="aacd3-164">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="aacd3-165">С этим значением не должно быть связано никаких данных.</span><span class="sxs-lookup"><span data-stu-id="aacd3-165">The value should not have any data associated with it.</span></span>

## <a name="programmatic-access-only"></a><span data-ttu-id="aacd3-166">Только программный доступ</span><span class="sxs-lookup"><span data-stu-id="aacd3-166">Programmatic Access Only</span></span>

<span data-ttu-id="aacd3-167">Эти команды никогда не отображаются в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-167">These verbs are never displayed in a context menu.</span></span> <span data-ttu-id="aacd3-168">Для доступа к ним можно использовать [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) и указать поле **лпверб** параметра *пексеЦинфо* (объект [шеллексекутеинфо](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) ).</span><span class="sxs-lookup"><span data-stu-id="aacd3-168">These can be accessed by using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) and specifying the **lpVerb** field of the *pExecInfo* parameter (a [SHELLEXECUTEINFO](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) object).</span></span> <span data-ttu-id="aacd3-169">Чтобы определить команду как программный доступ, добавьте значение **reg \_ SZ** программатикакцессонли в подраздел команды.</span><span class="sxs-lookup"><span data-stu-id="aacd3-169">To define a verb as programmatic access only, add a "ProgrammaticAccessOnly" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="aacd3-170">С этим значением не должно быть связано никаких данных.</span><span class="sxs-lookup"><span data-stu-id="aacd3-170">The value should not have any data associated with it.</span></span>

<span data-ttu-id="aacd3-171">С помощью реестра можно определить одну или несколько расширенных команд.</span><span class="sxs-lookup"><span data-stu-id="aacd3-171">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="aacd3-172">Связанные команды будут отображаться только в том случае, если пользователь щелкнет правой кнопкой мыши объект, а также нажмет клавишу SHIFT.</span><span class="sxs-lookup"><span data-stu-id="aacd3-172">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="aacd3-173">Чтобы определить команду как расширенную, добавьте расширенное значение **reg \_ SZ** в подраздел команды.</span><span class="sxs-lookup"><span data-stu-id="aacd3-173">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="aacd3-174">С этим значением не должно быть связано никаких данных.</span><span class="sxs-lookup"><span data-stu-id="aacd3-174">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="aacd3-175">Настройка контекстного меню с помощью статических команд</span><span class="sxs-lookup"><span data-stu-id="aacd3-175">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="aacd3-176">После [выбора статической или динамической команды для контекстного меню](shortcut-choose-method.md) можно расширить контекстное меню для типа файла, зарегистрировав статическую команду для типа файла.</span><span class="sxs-lookup"><span data-stu-id="aacd3-176">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="aacd3-177">Для этого добавьте подраздел **Shell** под подразделом для ProgID приложения, связанного с типом файла.</span><span class="sxs-lookup"><span data-stu-id="aacd3-177">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="aacd3-178">При необходимости можно определить глагол по умолчанию для типа файла, сделав его значением по умолчанию для подраздела **Shell** .</span><span class="sxs-lookup"><span data-stu-id="aacd3-178">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="aacd3-179">Команда по умолчанию отображается в контекстном меню первой.</span><span class="sxs-lookup"><span data-stu-id="aacd3-179">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="aacd3-180">Его назначение — предоставить оболочке команду, которую она может использовать при вызове функции [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) , но команда не указана.</span><span class="sxs-lookup"><span data-stu-id="aacd3-180">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="aacd3-181">Оболочка не обязательно выбирает команду по умолчанию, когда **ShellExecuteEx** используется таким образом.</span><span class="sxs-lookup"><span data-stu-id="aacd3-181">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="aacd3-182">Оболочка использует первую доступную команду в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="aacd3-182">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="aacd3-183">Команда по умолчанию</span><span class="sxs-lookup"><span data-stu-id="aacd3-183">The default verb</span></span>
2.  <span data-ttu-id="aacd3-184">Первая команда в реестре, если указан порядок команд</span><span class="sxs-lookup"><span data-stu-id="aacd3-184">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="aacd3-185">Команда **открытия**</span><span class="sxs-lookup"><span data-stu-id="aacd3-185">The **Open** verb</span></span>
4.  <span data-ttu-id="aacd3-186">Команда **Open With**</span><span class="sxs-lookup"><span data-stu-id="aacd3-186">The **Open With** verb</span></span>

<span data-ttu-id="aacd3-187">Если ни одна из указанных команд не доступна, операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="aacd3-187">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="aacd3-188">Создайте один подраздел для каждой команды, которую необходимо добавить в подраздел Shell.</span><span class="sxs-lookup"><span data-stu-id="aacd3-188">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="aacd3-189">Для каждого из этих подразделов должно быть задано значение **reg \_ SZ** для отображаемой строки команды (локализованная строка).</span><span class="sxs-lookup"><span data-stu-id="aacd3-189">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="aacd3-190">Для каждого подраздела команды создайте подраздел команды со значением по умолчанию, равным командной строке для активации элементов.</span><span class="sxs-lookup"><span data-stu-id="aacd3-190">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="aacd3-191">Для канонических команд, таких как **Open** и **Print**, можно опустить отображаемую строку, так как система автоматически отображает правильно локализованную строку.</span><span class="sxs-lookup"><span data-stu-id="aacd3-191">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="aacd3-192">Для неканонических глаголов, если не указана отображаемая строка, строка команды отображается.</span><span class="sxs-lookup"><span data-stu-id="aacd3-192">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="aacd3-193">В следующем примере реестра Обратите внимание на следующее:</span><span class="sxs-lookup"><span data-stu-id="aacd3-193">In the following registry example, note that:</span></span>

-   <span data-ttu-id="aacd3-194">Поскольку **доит** не является канонической командой, ей присваивается отображаемое имя, которое можно выбрать, нажав клавишу D.</span><span class="sxs-lookup"><span data-stu-id="aacd3-194">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="aacd3-195">Команда **принтто** не отображается в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-195">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="aacd3-196">Однако его включение в реестр позволяет пользователю печатать файлы путем их перетаскивания на значок принтера.</span><span class="sxs-lookup"><span data-stu-id="aacd3-196">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="aacd3-197">Для каждой команды отображается один подраздел.</span><span class="sxs-lookup"><span data-stu-id="aacd3-197">One subkey is shown for each verb.</span></span> <span data-ttu-id="aacd3-198">**%1** представляет имя файла и **%2** имя принтера.</span><span class="sxs-lookup"><span data-stu-id="aacd3-198">**%1** represents the file name and **%2** the printer name.</span></span>

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

<span data-ttu-id="aacd3-199">На следующей схеме показано расширение контекстного меню в соответствии с приведенными выше записями реестра.</span><span class="sxs-lookup"><span data-stu-id="aacd3-199">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="aacd3-200">Это контекстное **меню открыло**, **сделает его** и команды **печати** в своем меню, и **сделает его** в качестве глагола по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aacd3-200">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![снимок экрана контекстного меню выполнения команды по умолчанию](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="aacd3-202">Активация обработчика с помощью интерфейса интерфейс IDropTarget</span><span class="sxs-lookup"><span data-stu-id="aacd3-202">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="aacd3-203">Платформа динамических данных Exchange (DDE) является устаревшим; Вместо этого используйте [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="aacd3-203">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="aacd3-204">**Интерфейс IDropTarget** является более надежным и обеспечивает лучшую поддержку активации, так как использует com-активацию обработчика.</span><span class="sxs-lookup"><span data-stu-id="aacd3-204">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="aacd3-205">В случае выбора нескольких элементов **интерфейс IDropTarget** не зависит от ограничений размера буфера, находящихся как в DDE, так и в [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="aacd3-205">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="aacd3-206">Кроме того, элементы передаются в приложение в виде объекта данных, который можно преобразовать в массив элементов с помощью функции [**шкреатешеллитемаррайфромдатаобжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="aacd3-206">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="aacd3-207">Это упрощается и не теряет сведения о пространстве имен, как это происходит при преобразовании элемента в путь для протоколов командной строки или DDE.</span><span class="sxs-lookup"><span data-stu-id="aacd3-207">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="aacd3-208">Дополнительные сведения о [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) и оболочке запросов для атрибутов сопоставления файлов см. в разделе [наблюдаемые типы и регистрация приложений](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="aacd3-208">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="aacd3-209">Указание расположения и порядка статических глаголов</span><span class="sxs-lookup"><span data-stu-id="aacd3-209">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="aacd3-210">Обычно команды упорядочиваются в контекстном меню в зависимости от того, как они перечислены. Сначала перечисление основано на порядке массива ассоциаций, а затем в порядке элементов в массиве ассоциаций, как определено в порядке сортировки реестра.</span><span class="sxs-lookup"><span data-stu-id="aacd3-210">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="aacd3-211">Команды можно упорядочить, указав значение по умолчанию для подраздела Shell для записи ассоциации.</span><span class="sxs-lookup"><span data-stu-id="aacd3-211">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="aacd3-212">Это значение по умолчанию может включать один элемент, который будет отображаться в верхней части контекстного меню, или список элементов, разделенных пробелами или запятыми.</span><span class="sxs-lookup"><span data-stu-id="aacd3-212">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="aacd3-213">В последнем случае первый элемент в списке является элементом по умолчанию, а остальные команды отображаются непосредственно под ним в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="aacd3-213">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="aacd3-214">Например, следующая запись реестра создает команды контекстного меню в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="aacd3-214">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="aacd3-215">Отображение</span><span class="sxs-lookup"><span data-stu-id="aacd3-215">Display</span></span>
2.  <span data-ttu-id="aacd3-216">Приложения</span><span class="sxs-lookup"><span data-stu-id="aacd3-216">Gadgets</span></span>
3.  <span data-ttu-id="aacd3-217">Personalization</span><span class="sxs-lookup"><span data-stu-id="aacd3-217">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="aacd3-218">Аналогичным образом следующая запись реестра создает команды контекстного меню в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="aacd3-218">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="aacd3-219">Personalization</span><span class="sxs-lookup"><span data-stu-id="aacd3-219">Personalization</span></span>
2.  <span data-ttu-id="aacd3-220">Приложения</span><span class="sxs-lookup"><span data-stu-id="aacd3-220">Gadgets</span></span>
3.  <span data-ttu-id="aacd3-221">Отображение</span><span class="sxs-lookup"><span data-stu-id="aacd3-221">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="aacd3-222">Размещение команд в верхней или нижней части меню</span><span class="sxs-lookup"><span data-stu-id="aacd3-222">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="aacd3-223">Следующий атрибут реестра можно использовать для размещения команды в верхней или нижней части меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-223">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="aacd3-224">Если существует несколько глаголов, указывающих этот атрибут, последний из них получает приоритет:</span><span class="sxs-lookup"><span data-stu-id="aacd3-224">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="aacd3-225">Создание статических каскадных меню</span><span class="sxs-lookup"><span data-stu-id="aacd3-225">Creating Static Cascading Menus</span></span>

<span data-ttu-id="aacd3-226">В Windows 7 и более поздних версиях реализация каскадного меню поддерживается с помощью параметров реестра.</span><span class="sxs-lookup"><span data-stu-id="aacd3-226">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="aacd3-227">До Windows 7 создание каскадных меню было возможно только через реализацию интерфейса [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="aacd3-227">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="aacd3-228">В Windows 7 и более поздних версиях следует прибегать к решениям на основе кода COM только в том случае, если статические методы недостаточны.</span><span class="sxs-lookup"><span data-stu-id="aacd3-228">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="aacd3-229">На следующем снимке экрана приведен пример каскадного меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-229">The following screen shot provides an example of a cascading menu.</span></span>

![снимок экрана, демонстрирующий Пример каскадного меню](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="aacd3-231">В Windows 7 и более поздних версиях существует три способа создания каскадных меню:</span><span class="sxs-lookup"><span data-stu-id="aacd3-231">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="aacd3-232">Создание каскадных меню с записью реестра "подкоманды"</span><span class="sxs-lookup"><span data-stu-id="aacd3-232">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="aacd3-233">Создание каскадных меню с помощью записи реестра Екстендедсубкоммандскэй</span><span class="sxs-lookup"><span data-stu-id="aacd3-233">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="aacd3-234">Создание каскадных меню с помощью интерфейса Иексплореркомманд</span><span class="sxs-lookup"><span data-stu-id="aacd3-234">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="aacd3-235">Создание каскадных меню с записью реестра "подкоманды"</span><span class="sxs-lookup"><span data-stu-id="aacd3-235">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="aacd3-236">В Windows 7 и более поздних версиях можно использовать запись подкоманд для создания каскадных меню с помощью следующей процедуры.</span><span class="sxs-lookup"><span data-stu-id="aacd3-236">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="aacd3-237">**Создание каскадного меню с помощью записи подкоманд**</span><span class="sxs-lookup"><span data-stu-id="aacd3-237">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="aacd3-238">Создайте подраздел в разделе **\_ Classes \_ root** \\ *ProgID* \\ **Shell** , чтобы представить свое каскадное меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-238">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="aacd3-239">В этом примере мы присваиваем этому подразделу имя *каскадетест*.</span><span class="sxs-lookup"><span data-stu-id="aacd3-239">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="aacd3-240">Убедитесь, что значение по умолчанию для подраздела *каскадетест* пусто и отображается как **(значение не задано)**.</span><span class="sxs-lookup"><span data-stu-id="aacd3-240">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="aacd3-241">В подраздел *каскадетест* добавьте запись Муиверб типа **reg \_ SZ** и назначьте ей текст, который будет отображаться в контекстном меню как имя.</span><span class="sxs-lookup"><span data-stu-id="aacd3-241">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="aacd3-242">В этом примере мы присваиваем его «тестировать каскадное меню».</span><span class="sxs-lookup"><span data-stu-id="aacd3-242">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="aacd3-243">В подраздел *каскадетест* добавьте запись подкоманд с типом **reg \_ SZ** , назначенный List, демлимитед с точкой с запятой, для команд, которые должны отображаться в меню в порядке их отображения.</span><span class="sxs-lookup"><span data-stu-id="aacd3-243">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="aacd3-244">Например, здесь мы присваиваем ряд команд, предоставляемых системой:</span><span class="sxs-lookup"><span data-stu-id="aacd3-244">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="aacd3-245">В случае с пользовательскими командами реализуйте их с помощью любого из методов реализации статических команд и перечислите их в подразделе **коммандсторе** , как показано в этом примере для вымышленной глагола *вербнаме*:</span><span class="sxs-lookup"><span data-stu-id="aacd3-245">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

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
> <span data-ttu-id="aacd3-246">Этот метод имеет преимущество, что пользовательские команды могут быть зарегистрированы один раз и повторно использоваться путем перечисления имени команды в записи подкоманд.</span><span class="sxs-lookup"><span data-stu-id="aacd3-246">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="aacd3-247">Однако для этого требуется, чтобы приложение имело разрешение на изменение реестра на **\_ локальном \_ компьютере** в разделе hKey.</span><span class="sxs-lookup"><span data-stu-id="aacd3-247">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="aacd3-248">Создание каскадных меню с помощью записи реестра Екстендедсубкоммандскэй</span><span class="sxs-lookup"><span data-stu-id="aacd3-248">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="aacd3-249">В Windows 7 и более поздних версиях можно использовать запись Екстендедсубкоммандкэй для создания расширенных каскадных меню: каскадные меню в каскадных меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-249">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="aacd3-250">На следующем снимке экрана показан пример расширенного каскадного меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-250">The following screen shot is an example of an extended cascading menu.</span></span>

![снимок экрана с расширенным каскадным меню для устройств](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="aacd3-252">Поскольку **\_ \_ корневой класс hKey classes** является сочетанием **\_ текущего \_ пользователя hKey** и раздела **hKey \_ \_**, можно зарегистрировать любые пользовательские команды в подразделе "классы" программного обеспечения **\_ текущего \_ пользователя "hKey** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="aacd3-252">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="aacd3-253">Основное преимущество этого подхода в том, что повышенное разрешение не требуется.</span><span class="sxs-lookup"><span data-stu-id="aacd3-253">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="aacd3-254">Кроме того, другие сопоставления файлов могут повторно использовать этот полный набор команд, указав тот же подраздел Екстендедсубкоммандскэй.</span><span class="sxs-lookup"><span data-stu-id="aacd3-254">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="aacd3-255">Если не требуется повторно использовать этот набор команд, можно вывести список команд в родительском объекте, но убедитесь, что значение по умолчанию родительского элемента пустое.</span><span class="sxs-lookup"><span data-stu-id="aacd3-255">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="aacd3-256">**Создание каскадного меню с помощью записи Екстендедсубкоммандскэй**</span><span class="sxs-lookup"><span data-stu-id="aacd3-256">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="aacd3-257">Создайте подраздел в разделе **\_ Classes \_ root** \\ *ProgID* \\ **Shell** , чтобы представить свое каскадное меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-257">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="aacd3-258">В этом примере мы присваиваем этому подразделу имя *CascadeTest2*.</span><span class="sxs-lookup"><span data-stu-id="aacd3-258">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="aacd3-259">Убедитесь, что значение по умолчанию для подраздела *каскадетест* пусто и отображается как **(значение не задано)**.</span><span class="sxs-lookup"><span data-stu-id="aacd3-259">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="aacd3-260">В подраздел *каскадетест* добавьте запись Муиверб типа **reg \_ SZ** и назначьте ей текст, который будет отображаться в контекстном меню как имя.</span><span class="sxs-lookup"><span data-stu-id="aacd3-260">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="aacd3-261">В этом примере мы присваиваем его «тестировать каскадное меню».</span><span class="sxs-lookup"><span data-stu-id="aacd3-261">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="aacd3-262">В созданном вами подразделе *каскадетест* добавьте подраздел **екстендедсубкоммандскэй** , а затем добавьте подкоманды документа (типа **reg \_ SZ** ), например:</span><span class="sxs-lookup"><span data-stu-id="aacd3-262">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

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

    <span data-ttu-id="aacd3-263">Убедитесь, что значение по умолчанию для подраздела *тест Cascade меню 2* пусто и отображается как **(значение не задано)**.</span><span class="sxs-lookup"><span data-stu-id="aacd3-263">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="aacd3-264">Заполните подкоманды с помощью любой из следующих статических реализаций глаголов.</span><span class="sxs-lookup"><span data-stu-id="aacd3-264">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="aacd3-265">Обратите внимание, что подраздел Коммандфлагс представляет значения ЕКСПКМДФЛАГС.</span><span class="sxs-lookup"><span data-stu-id="aacd3-265">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="aacd3-266">Если вы хотите добавить разделитель до или после пункта меню Cascade, используйте ЕКФ \_ сепараторбефоре (0x20) или ЕКФ \_ сепараторафтер (0x40).</span><span class="sxs-lookup"><span data-stu-id="aacd3-266">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="aacd3-267">Описание этих флагов Windows 7 и более поздних версий см. в разделе [**иексплореркомманд::-flags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="aacd3-267">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="aacd3-268">ЕКФ \_ сепараторбефоре работает только для пунктов меню верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="aacd3-268">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="aacd3-269">Муиверб имеет тип **reg \_ SZ**, а Коммандфлагс имеет тип **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="aacd3-269">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

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

<span data-ttu-id="aacd3-270">На следующем снимке экрана показан пример записи предыдущего раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="aacd3-270">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![снимок экрана, показывающий пример каскадного меню, в котором отображаются параметры блокнота и WordPad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="aacd3-272">Создание каскадных меню с помощью интерфейса Иексплореркомманд</span><span class="sxs-lookup"><span data-stu-id="aacd3-272">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="aacd3-273">Другим вариантом добавления команд в каскадное меню является [**иексплореркомманд:: енумсубкоммандс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="aacd3-273">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="aacd3-274">Этот метод позволяет источникам данных, которые предоставляют команды командного модуля через [**иексплореркоммандпровидер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) , использовать эти команды в качестве команд в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-274">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="aacd3-275">В Windows 7 и более поздних версиях вы можете предоставить ту же реализацию команды с помощью [**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , как и с [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="aacd3-275">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="aacd3-276">Следующие два снимка экрана иллюстрируют использование каскадных меню в папке **Devices** .</span><span class="sxs-lookup"><span data-stu-id="aacd3-276">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Снимок экрана, на котором показан пример каскадного меню в папке Devices.](images/file-assoc/filecascademenu.png)

<span data-ttu-id="aacd3-278">На следующем снимке экрана показана другая реализация каскадного меню в папке **Devices** .</span><span class="sxs-lookup"><span data-stu-id="aacd3-278">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![снимок экрана, показывающий пример каскадного меню в папке "устройства"](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="aacd3-280">Так как [**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) поддерживает только внутрипроцессный активацию, рекомендуется использовать их в качестве источников данных оболочки, которые должны совместно использовать реализацию команд и контекстных меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-280">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="aacd3-281">Получение динамического поведения для статических команд с помощью расширенного синтаксиса запросов</span><span class="sxs-lookup"><span data-stu-id="aacd3-281">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="aacd3-282">Расширенный синтаксис запросов (АКС) может выразить условие, которое будет оцениваться с помощью свойств элемента, для которого создается экземпляр команды.</span><span class="sxs-lookup"><span data-stu-id="aacd3-282">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="aacd3-283">Эта система работает только с быстрыми свойствами.</span><span class="sxs-lookup"><span data-stu-id="aacd3-283">This system works only with fast properties.</span></span> <span data-ttu-id="aacd3-284">Это свойства, которые источник данных оболочки сообщает быстро, не возвращая [\* \* \* \* школстате \_ медленный \* \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* \* из [**IShellFolder2:: жетдефаултколумнстате**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span><span class="sxs-lookup"><span data-stu-id="aacd3-284">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="aacd3-285">Windows 7 и более поздние версии поддерживают канонические значения, что позволяет избежать проблем в локализованных сборках.</span><span class="sxs-lookup"><span data-stu-id="aacd3-285">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="aacd3-286">Для использования этого расширения Windows 7 в локализованных сборках требуется следующий канонический синтаксис.</span><span class="sxs-lookup"><span data-stu-id="aacd3-286">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="aacd3-287">В следующем примере запись реестра:</span><span class="sxs-lookup"><span data-stu-id="aacd3-287">In the following example registry entry:</span></span>

-   <span data-ttu-id="aacd3-288">Значение **appliesTo** определяет, отображается ли глагол или скрыт.</span><span class="sxs-lookup"><span data-stu-id="aacd3-288">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="aacd3-289">Значение Дефаултапплиесто определяет, какая команда является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aacd3-289">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="aacd3-290">Значение Хаслуашиелд определяет, отображается ли экранирование контроля учетных записей (UAC).</span><span class="sxs-lookup"><span data-stu-id="aacd3-290">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="aacd3-291">В этом примере значение **дефаултапплиесто** делает эту команду по умолчанию для любого файла с словом "exampleText1" в имени файла.</span><span class="sxs-lookup"><span data-stu-id="aacd3-291">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="aacd3-292">Значение **appliesTo** позволяет команде для любого файла с именем "exampleText1" в имени.</span><span class="sxs-lookup"><span data-stu-id="aacd3-292">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="aacd3-293">Значение **хаслуашиелд** отображает экранирование для файлов с именем "exampleText2" в имени.</span><span class="sxs-lookup"><span data-stu-id="aacd3-293">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="aacd3-294">Добавьте подраздел **Command** и значение:</span><span class="sxs-lookup"><span data-stu-id="aacd3-294">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="aacd3-295">В реестре Windows 7 ознакомьтесь с разделом **\_ \_ корневые диски классов hKey** в \\  качестве примера команд BitLocker, которые используют следующий подход:</span><span class="sxs-lookup"><span data-stu-id="aacd3-295">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="aacd3-296">AppliesTo = System. Volume. Битлоккерпротектион: = 2</span><span class="sxs-lookup"><span data-stu-id="aacd3-296">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="aacd3-297">System. Volume. Битлоккеррекуиресадмин: = System. Структуредкуеритипе. Boolean \# true</span><span class="sxs-lookup"><span data-stu-id="aacd3-297">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="aacd3-298">Дополнительные сведения о АКС см. в разделе [Расширенный синтаксис запросов](../search/-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="aacd3-298">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="aacd3-299">Не рекомендуется: связывание команд с командами платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="aacd3-299">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="aacd3-300">DDE устарело; Вместо этого используйте [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="aacd3-300">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="aacd3-301">Протокол DDE является устаревшим, так как он использует широковещательное сообщение окна для обнаружения сервера DDE.</span><span class="sxs-lookup"><span data-stu-id="aacd3-301">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="aacd3-302">Зависание сервера DDE приводит к зависанию окна вещания и, следовательно, зависания диалога DDE для других приложений.</span><span class="sxs-lookup"><span data-stu-id="aacd3-302">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="aacd3-303">Обычно для одного задержанного приложения возникает необходимость в последующем зависании в работе пользователя.</span><span class="sxs-lookup"><span data-stu-id="aacd3-303">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="aacd3-304">Метод [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) является более надежным и обеспечивает лучшую поддержку активации, поскольку он использует com-активацию обработчика.</span><span class="sxs-lookup"><span data-stu-id="aacd3-304">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="aacd3-305">В случае выбора нескольких элементов **интерфейс IDropTarget** не зависит от ограничений размера буфера, находящихся как в DDE, так и в [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="aacd3-305">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="aacd3-306">Кроме того, элементы передаются в приложение в виде объекта данных, который можно преобразовать в массив элементов с помощью функции [**шкреатешеллитемаррайфромдатаобжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="aacd3-306">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="aacd3-307">Это упрощается и не теряет сведения о пространстве имен, как это происходит при преобразовании элемента в путь для протоколов командной строки или DDE.</span><span class="sxs-lookup"><span data-stu-id="aacd3-307">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="aacd3-308">Дополнительные сведения о [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) и оболочке запросов для атрибутов сопоставления файлов см. в разделе [наблюдаемые типы и регистрация приложений](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="aacd3-308">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="aacd3-309">Завершение задач реализации команд</span><span class="sxs-lookup"><span data-stu-id="aacd3-309">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="aacd3-310">Следующие задачи для реализации команд относятся к реализации статических и динамических команд.</span><span class="sxs-lookup"><span data-stu-id="aacd3-310">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="aacd3-311">Дополнительные сведения о динамических командах см. в разделе [Настройка контекстного меню с помощью динамических команд](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="aacd3-311">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="aacd3-312">Настройка контекстного меню для предопределенных объектов оболочки</span><span class="sxs-lookup"><span data-stu-id="aacd3-312">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="aacd3-313">У многих предопределенных объектов оболочки есть контекстные меню, которые можно настроить.</span><span class="sxs-lookup"><span data-stu-id="aacd3-313">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="aacd3-314">Зарегистрируйте команду практически так же, как при регистрации типов файлов, но используйте имя предопределенного объекта в качестве имени типа файла.</span><span class="sxs-lookup"><span data-stu-id="aacd3-314">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="aacd3-315">Список предопределенных объектов находится в разделе *предопределенных объектов оболочки* , посвященном [созданию обработчиков расширений оболочки](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="aacd3-315">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="aacd3-316">Эти предопределенные объекты оболочки, контекстные меню которых можно настроить путем добавления команд в реестр, помечаются в таблице с помощью команды Word.</span><span class="sxs-lookup"><span data-stu-id="aacd3-316">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="aacd3-317">Расширение нового подменю</span><span class="sxs-lookup"><span data-stu-id="aacd3-317">Extending a New Submenu</span></span>

<span data-ttu-id="aacd3-318">Когда пользователь открывает меню **файл** в проводнике Windows, одна из отображаемых команд является **новой**.</span><span class="sxs-lookup"><span data-stu-id="aacd3-318">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="aacd3-319">При выборе этой команды отображается подменю.</span><span class="sxs-lookup"><span data-stu-id="aacd3-319">Selecting this command displays a submenu.</span></span> <span data-ttu-id="aacd3-320">По умолчанию подменю содержит две команды, **папку** и **ярлык**, которые позволяют пользователям создавать вложенные папки и ярлыки.</span><span class="sxs-lookup"><span data-stu-id="aacd3-320">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="aacd3-321">Это подменю можно расширить, включив команды создания файлов для любого типа файлов.</span><span class="sxs-lookup"><span data-stu-id="aacd3-321">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="aacd3-322">Чтобы добавить команду создания файла в подменю **создать** , файлы приложения должны иметь связанный тип файлов.</span><span class="sxs-lookup"><span data-stu-id="aacd3-322">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="aacd3-323">Включите подраздел **шеллнев** под именем файла.</span><span class="sxs-lookup"><span data-stu-id="aacd3-323">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="aacd3-324">Если выбрана команда **создать** меню **файл** , оболочка добавляет тип файла в подменю **создать** .</span><span class="sxs-lookup"><span data-stu-id="aacd3-324">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="aacd3-325">Отображаемая строка команды представляет собой описательную строку, назначенную ProgID программы.</span><span class="sxs-lookup"><span data-stu-id="aacd3-325">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="aacd3-326">Чтобы указать метод создания файла, назначьте одно или несколько значений данных подразделу **шеллнев** .</span><span class="sxs-lookup"><span data-stu-id="aacd3-326">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="aacd3-327">Доступные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="aacd3-327">The available values are listed in the following table.</span></span>



| <span data-ttu-id="aacd3-328">Значение подраздела Шеллнев</span><span class="sxs-lookup"><span data-stu-id="aacd3-328">ShellNew subkey value</span></span> | <span data-ttu-id="aacd3-329">Описание</span><span class="sxs-lookup"><span data-stu-id="aacd3-329">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aacd3-330">Get-Help</span><span class="sxs-lookup"><span data-stu-id="aacd3-330">Command</span></span>               | <span data-ttu-id="aacd3-331">Выполняет приложение.</span><span class="sxs-lookup"><span data-stu-id="aacd3-331">Executes an application.</span></span> <span data-ttu-id="aacd3-332">Это значение **reg \_ SZ** указывает путь к выполняемому приложению.</span><span class="sxs-lookup"><span data-stu-id="aacd3-332">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="aacd3-333">Например, можно задать запуск мастера.</span><span class="sxs-lookup"><span data-stu-id="aacd3-333">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="aacd3-334">Данные</span><span class="sxs-lookup"><span data-stu-id="aacd3-334">Data</span></span>                  | <span data-ttu-id="aacd3-335">Создает файл, содержащий указанные данные.</span><span class="sxs-lookup"><span data-stu-id="aacd3-335">Creates a file containing specified data.</span></span> <span data-ttu-id="aacd3-336">Этот **\_ двоичный параметр reg** задает данные файла.</span><span class="sxs-lookup"><span data-stu-id="aacd3-336">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="aacd3-337">**Данные** пропускаются, если указано либо **Нуллфиле** , либо **filename** .</span><span class="sxs-lookup"><span data-stu-id="aacd3-337">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="aacd3-338">FileName</span><span class="sxs-lookup"><span data-stu-id="aacd3-338">FileName</span></span>              | <span data-ttu-id="aacd3-339">Создает файл, который является копией указанного файла.</span><span class="sxs-lookup"><span data-stu-id="aacd3-339">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="aacd3-340">Это значение **reg \_ SZ** указывает полный путь к копируемому файлу.</span><span class="sxs-lookup"><span data-stu-id="aacd3-340">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="aacd3-341">нуллфиле</span><span class="sxs-lookup"><span data-stu-id="aacd3-341">NullFile</span></span>              | <span data-ttu-id="aacd3-342">Создает пустой файл.</span><span class="sxs-lookup"><span data-stu-id="aacd3-342">Creates an empty file.</span></span> <span data-ttu-id="aacd3-343">**Нуллфиле** не имеет присвоенного значения.</span><span class="sxs-lookup"><span data-stu-id="aacd3-343">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="aacd3-344">Если указан параметр **нуллфиле** , значения реестра **Data** и **filename** игнорируются.</span><span class="sxs-lookup"><span data-stu-id="aacd3-344">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="aacd3-345">В следующем примере раздела реестра и снимке экрана показано **новое** подменю для типа файла МИП-MS.</span><span class="sxs-lookup"><span data-stu-id="aacd3-345">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="aacd3-346">У него есть команда **MyProgram Application**.</span><span class="sxs-lookup"><span data-stu-id="aacd3-346">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="aacd3-347">На снимке экрана показано **новое** подменю.</span><span class="sxs-lookup"><span data-stu-id="aacd3-347">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="aacd3-348">Когда пользователь выбирает **приложение MyProgram** из подменю **создать** , оболочка создает файл с именем **New MyProgram Application. МИП-ms** и передает его в **MyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="aacd3-348">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![снимок экрана Windows Explorer с новой командой "приложение MyProgram" в подменю "создать"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="aacd3-350">Создание обработчиков перетаскивания</span><span class="sxs-lookup"><span data-stu-id="aacd3-350">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="aacd3-351">Базовая процедура реализации обработчика перетаскивания аналогична процедуре для обычных обработчиков контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-351">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="aacd3-352">Однако обработчики контекстного меню обычно используют только указатель [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) , передаваемый методу [**Ишеллекстинит:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) обработчика, для извлечения имени объекта.</span><span class="sxs-lookup"><span data-stu-id="aacd3-352">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="aacd3-353">Обработчик перетаскивания может реализовать более сложный обработчик данных для изменения поведения перетаскиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="aacd3-353">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="aacd3-354">Когда пользователь щелкает правой кнопкой мыши объект оболочки для перетаскивания объекта, контекстное меню отображается, когда пользователь пытается удалить объект.</span><span class="sxs-lookup"><span data-stu-id="aacd3-354">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="aacd3-355">На следующем снимке экрана показан типичный контекстный меню для перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="aacd3-355">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![снимок экрана с контекстным меню перетаскивания](images/context-menu/context-dragdrop.png)

<span data-ttu-id="aacd3-357">Обработчик перетаскивания — это обработчик контекстного меню, который может добавлять элементы в контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="aacd3-357">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="aacd3-358">Обработчики перетаскивания обычно регистрируются в следующем подразделе.</span><span class="sxs-lookup"><span data-stu-id="aacd3-358">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="aacd3-359">Добавьте подраздел в подраздел **драгдрофандлерс** с именем для обработчика перетаскивания и задайте в качестве значения по умолчанию для подраздела строковое значение GUID идентификатора класса обработчика (CLSID).</span><span class="sxs-lookup"><span data-stu-id="aacd3-359">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="aacd3-360">В следующем примере активируется обработчик перетаскивания **мидд** .</span><span class="sxs-lookup"><span data-stu-id="aacd3-360">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="aacd3-361">Подавление команд и управление видимостью</span><span class="sxs-lookup"><span data-stu-id="aacd3-361">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="aacd3-362">Для управления видимостью команды можно использовать параметры политики Windows.</span><span class="sxs-lookup"><span data-stu-id="aacd3-362">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="aacd3-363">Команды можно подавлять с помощью параметров политики, добавив значение **суппрессионполици** или значение GUID **суппрессионполициекс** в подраздел реестра команды.</span><span class="sxs-lookup"><span data-stu-id="aacd3-363">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="aacd3-364">Присвойте параметру подраздела **СУППРЕССИОНПОЛИЦИ** идентификатор политики.</span><span class="sxs-lookup"><span data-stu-id="aacd3-364">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="aacd3-365">Если политика включена, команда и связанная с ней запись контекстного меню подавляются.</span><span class="sxs-lookup"><span data-stu-id="aacd3-365">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="aacd3-366">Возможные значения идентификатора политики см. в описании перечисления [**ограничений**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="aacd3-366">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="aacd3-367">Применение модели выбора глагола</span><span class="sxs-lookup"><span data-stu-id="aacd3-367">Employing the Verb Selection Model</span></span>

<span data-ttu-id="aacd3-368">Значения реестра должны быть заданы для команд, чтобы обрабатывать ситуации, когда пользователь может выбрать один элемент, несколько элементов или выбрать из элемента.</span><span class="sxs-lookup"><span data-stu-id="aacd3-368">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="aacd3-369">Команда требует наличия отдельных значений реестра для каждой из трех ситуаций, поддерживаемых командой.</span><span class="sxs-lookup"><span data-stu-id="aacd3-369">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="aacd3-370">Ниже приведены возможные значения для модели выбора команд.</span><span class="sxs-lookup"><span data-stu-id="aacd3-370">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="aacd3-371">Укажите значение Мултиселектмодел для всех команд.</span><span class="sxs-lookup"><span data-stu-id="aacd3-371">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="aacd3-372">Если значение Мултиселектмодел не указано, оно выводится из выбранного типа реализации глагола.</span><span class="sxs-lookup"><span data-stu-id="aacd3-372">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="aacd3-373">Для **методов,** основанных на com (например, Дроптаржет и **ExecuteCommand),** предполагается, а для других методов —.</span><span class="sxs-lookup"><span data-stu-id="aacd3-373">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="aacd3-374">Укажите **одну** для команд, поддерживающих только один выбор.</span><span class="sxs-lookup"><span data-stu-id="aacd3-374">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="aacd3-375">Укажите **проигрыватель** для команд, которые поддерживают любое количество элементов.</span><span class="sxs-lookup"><span data-stu-id="aacd3-375">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="aacd3-376">Укажите **документ** для команд, которые создают окно верхнего уровня для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="aacd3-376">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="aacd3-377">Это ограничивает количество активированных элементов и помогает избежать переполнения системных ресурсов, если пользователь открывает слишком много окон.</span><span class="sxs-lookup"><span data-stu-id="aacd3-377">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="aacd3-378">Если выбранное число элементов не соответствует модели выбора глагола или превышает ограничения по умолчанию, описанные в следующей таблице, команда не отображается.</span><span class="sxs-lookup"><span data-stu-id="aacd3-378">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="aacd3-379">Тип реализации глагола</span><span class="sxs-lookup"><span data-stu-id="aacd3-379">Type of verb implementation</span></span> | <span data-ttu-id="aacd3-380">Документ</span><span class="sxs-lookup"><span data-stu-id="aacd3-380">Document</span></span> | <span data-ttu-id="aacd3-381">Проигрыватель</span><span class="sxs-lookup"><span data-stu-id="aacd3-381">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="aacd3-382">Прежняя версия</span><span class="sxs-lookup"><span data-stu-id="aacd3-382">Legacy</span></span>                      | <span data-ttu-id="aacd3-383">15 элементов</span><span class="sxs-lookup"><span data-stu-id="aacd3-383">15 items</span></span> | <span data-ttu-id="aacd3-384">100 элементов</span><span class="sxs-lookup"><span data-stu-id="aacd3-384">100 items</span></span> |
| <span data-ttu-id="aacd3-385">COM</span><span class="sxs-lookup"><span data-stu-id="aacd3-385">COM</span></span>                         | <span data-ttu-id="aacd3-386">15 элементов</span><span class="sxs-lookup"><span data-stu-id="aacd3-386">15 items</span></span> | <span data-ttu-id="aacd3-387">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="aacd3-387">No limit</span></span>  |



 

<span data-ttu-id="aacd3-388">Ниже приведены примеры записей реестра с использованием значения Мултиселектмодел.</span><span class="sxs-lookup"><span data-stu-id="aacd3-388">The following are example registry entries using the MultiSelectModel value.</span></span>

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

### <a name="using-item-attributes"></a><span data-ttu-id="aacd3-389">Использование атрибутов элементов</span><span class="sxs-lookup"><span data-stu-id="aacd3-389">Using Item Attributes</span></span>

<span data-ttu-id="aacd3-390">Значения флагов [**сфгао**](sfgao.md) атрибутов оболочки для элемента можно проверить, чтобы определить, должна ли команда быть включена или отключена.</span><span class="sxs-lookup"><span data-stu-id="aacd3-390">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="aacd3-391">Чтобы использовать эту функцию атрибута, добавьте следующие значения **reg \_ DWORD** в команду:</span><span class="sxs-lookup"><span data-stu-id="aacd3-391">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="aacd3-392">Значение Аттрибутемаск указывает значение [**сфгао**](sfgao.md) для битовых значений маски для проверки.</span><span class="sxs-lookup"><span data-stu-id="aacd3-392">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="aacd3-393">Значение AttributeValue указывает значение [**сфгао**](sfgao.md) для проверяемых битов.</span><span class="sxs-lookup"><span data-stu-id="aacd3-393">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="aacd3-394">Имплиедселектионмодел указывает ноль для глаголов элемента или ненулевое значение для команд в контекстном меню фона.</span><span class="sxs-lookup"><span data-stu-id="aacd3-394">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="aacd3-395">В следующем примере записи реестра Аттрибутемаск имеет значение [**сфгао \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="aacd3-395">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

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

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="aacd3-396">Реализация пользовательских команд для папок с помощью Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="aacd3-396">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="aacd3-397">В Windows 7 и более поздних версиях можно добавлять команды в папку с помощью Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="aacd3-397">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="aacd3-398">Дополнительные сведения о Desktop.ini файлах см. [в статье Настройка папок с помощью Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="aacd3-398">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="aacd3-399">Desktop.ini файлы всегда должны быть помечены как   +  **скрытые** системой, чтобы они не отображались для пользователей.</span><span class="sxs-lookup"><span data-stu-id="aacd3-399">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="aacd3-400">**Чтобы добавить пользовательские команды для папок с помощью файла Desktop.ini, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="aacd3-400">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="aacd3-401">Создайте папку, которая помечена как доступная **только для чтения** или как **система**.</span><span class="sxs-lookup"><span data-stu-id="aacd3-401">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="aacd3-402">Создайте файл Desktop.ini, содержащий \[ . Шеллклассинфо \] директорикласс = ProgID папки.</span><span class="sxs-lookup"><span data-stu-id="aacd3-402">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="aacd3-403">В реестре создайте **класс hKey с \_ \_ корневой** \\ **папкой ProgID** со значением канусефордиректори.</span><span class="sxs-lookup"><span data-stu-id="aacd3-403">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="aacd3-404">Значение Канусефордиректори позволяет избежать неправильного использования ProgID, которые не участвуют в реализации пользовательских команд для папок с помощью Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="aacd3-404">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="aacd3-405">Добавьте команды в подключе ProgID **папки**, например:</span><span class="sxs-lookup"><span data-stu-id="aacd3-405">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="aacd3-406">Эти глаголы могут быть глаголами по умолчанию. в этом случае двойной щелчок папки активирует команду.</span><span class="sxs-lookup"><span data-stu-id="aacd3-406">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="aacd3-407">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="aacd3-407">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aacd3-408">Рекомендации по работе с обработчиками контекстного меню и несколькими командами выбора</span><span class="sxs-lookup"><span data-stu-id="aacd3-408">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="aacd3-409">Выбор статической или динамической команды для контекстного меню</span><span class="sxs-lookup"><span data-stu-id="aacd3-409">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="aacd3-410">Настройка контекстного меню с помощью динамических команд</span><span class="sxs-lookup"><span data-stu-id="aacd3-410">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="aacd3-411">Контекстное меню (контекст) и обработчики контекстного меню</span><span class="sxs-lookup"><span data-stu-id="aacd3-411">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="aacd3-412">Команды и сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="aacd3-412">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="aacd3-413">Справочник по контекстному меню</span><span class="sxs-lookup"><span data-stu-id="aacd3-413">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
