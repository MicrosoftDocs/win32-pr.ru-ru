---
description: 'Этот раздел организован следующим образом:'
title: Выбор метода статического или динамического контекстного меню
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 70c6cb74e2c9a432bfdae2f26da1fdbebfc5f00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081097"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a><span data-ttu-id="a12b4-103">Выбор метода статического или динамического контекстного меню</span><span class="sxs-lookup"><span data-stu-id="a12b4-103">Choosing a Static or Dynamic Shortcut Menu Method</span></span>

<span data-ttu-id="a12b4-104">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a12b4-104">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a12b4-105">Выбор метода глагола</span><span class="sxs-lookup"><span data-stu-id="a12b4-105">Choose a Verb Method</span></span>](#choose-a-verb-method)
    -   [<span data-ttu-id="a12b4-106">Статические методы глагола</span><span class="sxs-lookup"><span data-stu-id="a12b4-106">Static Verb Methods</span></span>](#static-verb-methods)
    -   [<span data-ttu-id="a12b4-107">Предпочтительные динамические методы команд</span><span class="sxs-lookup"><span data-stu-id="a12b4-107">Preferred Dynamic Verb Methods</span></span>](#preferred-dynamic-verb-methods)
    -   [<span data-ttu-id="a12b4-108">Нерекомендованные динамические методы команд</span><span class="sxs-lookup"><span data-stu-id="a12b4-108">Discouraged Dynamic Verb Methods</span></span>](#discouraged-dynamic-verb-methods)
-   [<span data-ttu-id="a12b4-109">Расширение контекстного меню</span><span class="sxs-lookup"><span data-stu-id="a12b4-109">Extend a Shortcut Menu</span></span>](#extend-a-shortcut-menu)
-   [<span data-ttu-id="a12b4-110">Поддержка методов команд операционной системой</span><span class="sxs-lookup"><span data-stu-id="a12b4-110">Support for Verb Methods by Operating System</span></span>](#support-for-verb-methods-by-operating-system)
-   [<span data-ttu-id="a12b4-111">См. также</span><span class="sxs-lookup"><span data-stu-id="a12b4-111">Related topics</span></span>](#related-topics)

## <a name="choose-a-verb-method"></a><span data-ttu-id="a12b4-112">Выбор метода глагола</span><span class="sxs-lookup"><span data-stu-id="a12b4-112">Choose a Verb Method</span></span>

<span data-ttu-id="a12b4-113">Настоятельно рекомендуется реализовать контекстное меню с помощью одного из статических методов глагола.</span><span class="sxs-lookup"><span data-stu-id="a12b4-113">It is strongly encouraged that you implement a shortcut menu using one of the static verb methods.</span></span>

### <a name="static-verb-methods"></a><span data-ttu-id="a12b4-114">Статические методы глагола</span><span class="sxs-lookup"><span data-stu-id="a12b4-114">Static Verb Methods</span></span>

<span data-ttu-id="a12b4-115">Статические глаголы являются простейшими глаголами для реализации, но они по-прежнему предоставляют широкие функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="a12b4-115">Static verbs are the simplest verbs to implement, but they still provide rich functionality.</span></span> <span data-ttu-id="a12b4-116">Всегда выберете простейший метод контекстного меню, соответствующий вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="a12b4-116">Always chose the simplest shortcut menu method that meets your needs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a12b4-117">Статическая команда</span><span class="sxs-lookup"><span data-stu-id="a12b4-117">Static Verb</span></span></th>
<th><span data-ttu-id="a12b4-118">Описание</span><span class="sxs-lookup"><span data-stu-id="a12b4-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a12b4-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> с параметрами командной строки</span><span class="sxs-lookup"><span data-stu-id="a12b4-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> with command line parameters</span></span></td>
<td><span data-ttu-id="a12b4-120">Это самый простой и привычный способ реализации статической команды.</span><span class="sxs-lookup"><span data-stu-id="a12b4-120">This is the simplest and most familiar means of implementing a static verb.</span></span> <span data-ttu-id="a12b4-121">Процесс вызывается через вызов функции <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> с выбранными файлами и любыми необязательными параметрами, передаваемыми в командной строке.</span><span class="sxs-lookup"><span data-stu-id="a12b4-121">A process is invoked through a call to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> function with the selected files and any optional parameters passed as the command line.</span></span> <span data-ttu-id="a12b4-122">Откроется файл или папка.</span><span class="sxs-lookup"><span data-stu-id="a12b4-122">This opens the file or folder.</span></span><br/> <span data-ttu-id="a12b4-123">Этот метод имеет следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="a12b4-123">This method has the following limitations:</span></span>
<ul>
<li><span data-ttu-id="a12b4-124">Длина командной строки ограничена 2000 символами, что ограничивает число элементов, которое может быть обработано командой.</span><span class="sxs-lookup"><span data-stu-id="a12b4-124">The command-line length is limited to 2000 characters, which limits the number of items that the verb can handle.</span></span></li>
<li><span data-ttu-id="a12b4-125">Может использоваться только с элементами файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a12b4-125">Can only be used with file system items.</span></span></li>
<li><span data-ttu-id="a12b4-126">Не включает повторное использование уже запущенного процесса.</span><span class="sxs-lookup"><span data-stu-id="a12b4-126">Does not enable re-use of an already running process.</span></span></li>
<li><span data-ttu-id="a12b4-127">Требует установки исполняемого файла для выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="a12b4-127">Requires that an executable be installed to handle the verb.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a12b4-128"><strong>Дроптаржет</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>Интерфейс IDropTarget</strong></a></span><span class="sxs-lookup"><span data-stu-id="a12b4-128"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a></span></span></td>
<td><span data-ttu-id="a12b4-129">Активация глагола на основе COM означает, что поддерживает in-proc или внепроцессные активация.</span><span class="sxs-lookup"><span data-stu-id="a12b4-129">A COM-based verb activation means that supports in-proc or out-of-proc activation.</span></span> <span data-ttu-id="a12b4-130"><strong>Дроптаржет</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>Интерфейс IDropTarget</strong></a> также поддерживает повторное использование уже запущенного обработчика, когда интерфейс <strong>интерфейс IDropTarget</strong> реализуется локальным сервером.</span><span class="sxs-lookup"><span data-stu-id="a12b4-130"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> also supports re-use of an already running handler when the <strong>IDropTarget</strong> interface is implemented by a local server.</span></span> <span data-ttu-id="a12b4-131">Он также полностью выражает элементы через упакованный объект данных и предоставляет ссылку на вызывающую цепочку сайтов, чтобы можно было взаимодействовать с вызывающим объектом через <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a12b4-131">It also perfectly expresses the items via the marshaled data object and provides a reference to the invoking site chain so that you can interact with the invoker through the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a12b4-132">Windows 7 и более поздние версии: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>иексекутекомманд</strong></a></span><span class="sxs-lookup"><span data-stu-id="a12b4-132">Windows 7 and later: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a></span></span></td>
<td><span data-ttu-id="a12b4-133">Наиболее прямой метод реализации.</span><span class="sxs-lookup"><span data-stu-id="a12b4-133">The most direct implementation method.</span></span> <span data-ttu-id="a12b4-134">Поскольку это метод вызова на основе COM (например, Дроптаржет), этот интерфейс поддерживает внутрипроцессную и внепроцессных активации.</span><span class="sxs-lookup"><span data-stu-id="a12b4-134">Because this is a COM-based invoke method (like DropTarget) this interface supports in-proc and out-of-proc activation.</span></span> <span data-ttu-id="a12b4-135">Команда реализует <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>иексекутекомманд</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>иобжектвисселектион</strong></a>и, при необходимости, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>иинитиализекомманд</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a12b4-135">The verb implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>, and optionally <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span></span> <span data-ttu-id="a12b4-136">Элементы передаются непосредственно в качестве массива элементов оболочки, а другие параметры из вызывающего объекта доступны для реализации глагола, включая точку вызова, состояние клавиатуры и т. д.</span><span class="sxs-lookup"><span data-stu-id="a12b4-136">The items are passed directly as a Shell item array and more of the parameters from the invoker are available to the verb implementation, including the invoke point, keyboard state, and so forth.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a12b4-137">Windows 7 и более поздние версии:<strong>експлореркомманд</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>иексплореркомманд</strong></a></span><span class="sxs-lookup"><span data-stu-id="a12b4-137">Windows 7 and later:<strong>ExplorerCommand</strong>/ <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span></span></td>
<td><span data-ttu-id="a12b4-138">Включает источники данных, предоставляющие команды командного модуля через <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>иексплореркоммандпровидер</strong></a> для использования этих команд в контекстном меню в качестве команд.</span><span class="sxs-lookup"><span data-stu-id="a12b4-138">Enables data sources that provide their command module commands through <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="a12b4-139">Поскольку этот интерфейс поддерживает только внутрипроцессный процесс, рекомендуется использовать его в качестве источников данных оболочки, которые должны совместно использовать реализацию команд и контекстных меню.</span><span class="sxs-lookup"><span data-stu-id="a12b4-139">Because this interface supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="a12b4-140">[**Иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) — это гибрид между статической и динамической глаголами.</span><span class="sxs-lookup"><span data-stu-id="a12b4-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) is a hybrid between a static and dynamic verb.</span></span> <span data-ttu-id="a12b4-141">**Иексплореркомманд** был объявлен в Windows Vista, но его способность реализовать глагол в контекстном меню — это новая возможность для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a12b4-141">**IExplorerCommand** was declared in Windows Vista, but its ability to implement a verb in a shortcut menu is new to Windows 7.</span></span>

 

<span data-ttu-id="a12b4-142">Дополнительные сведения о [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) и оболочке запросов для атрибутов сопоставления файлов см. в разделе [наблюдаемые типы и регистрация приложений](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="a12b4-142">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="preferred-dynamic-verb-methods"></a><span data-ttu-id="a12b4-143">Предпочтительные динамические методы команд</span><span class="sxs-lookup"><span data-stu-id="a12b4-143">Preferred Dynamic Verb Methods</span></span>

<span data-ttu-id="a12b4-144">Следующие динамические методы являются предпочтительными:</span><span class="sxs-lookup"><span data-stu-id="a12b4-144">The following dynamic verb methods are preferred:</span></span>



| <span data-ttu-id="a12b4-145">Тип команды</span><span class="sxs-lookup"><span data-stu-id="a12b4-145">Verb Type</span></span>                                                                                 | <span data-ttu-id="a12b4-146">Описание</span><span class="sxs-lookup"><span data-stu-id="a12b4-146">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a12b4-147">Статическая команда (указанная в предыдущей таблице) + расширенный синтаксис запросов (АКС)</span><span class="sxs-lookup"><span data-stu-id="a12b4-147">Static verb (listed in the previous table) + Advanced Query Syntax (AQS)</span></span>                  | <span data-ttu-id="a12b4-148">Этот вариант возвращает видимость динамической команды.</span><span class="sxs-lookup"><span data-stu-id="a12b4-148">This choice gets dynamic verb visibility.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a12b4-149">Windows 7 и более поздние версии: [ **иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span><span class="sxs-lookup"><span data-stu-id="a12b4-149">Windows 7 and later: [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span></span>                         | <span data-ttu-id="a12b4-150">Этот вариант позволяет реализовать общую реализацию команд и команд обозревателя, отображаемых в командном модуле в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="a12b4-150">This choice enables a common implementation of verbs and explorer commands that are displayed in the command module in Windows Explorer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a12b4-151">Windows 7 и более поздние версии: статическая команда [**иексплореркоммандстате**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) +</span><span class="sxs-lookup"><span data-stu-id="a12b4-151">Windows 7 and later: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + static verb</span></span> | <span data-ttu-id="a12b4-152">Этот вариант также возвращает видимость динамической команды.</span><span class="sxs-lookup"><span data-stu-id="a12b4-152">This choice also gets dynamic verb visibility.</span></span> <span data-ttu-id="a12b4-153">Это гибридная модель, где простой внутрипроцессный обработчик используется для вычислений, если заданная статическая команда должна быть приведена.</span><span class="sxs-lookup"><span data-stu-id="a12b4-153">It is a hybrid model where a simple in-process handler is used to compute if a given static verb should be displyed.</span></span> <span data-ttu-id="a12b4-154">Это можно применить ко всем методам реализации статических команд, чтобы обеспечить динамическое поведение и снизить вероятность раскрытия логики внутри процесса.</span><span class="sxs-lookup"><span data-stu-id="a12b4-154">This can be applied to all of the static verb implementation methods to achieve dynamic behavior and minimize the exposure of the in-process logic.</span></span> <span data-ttu-id="a12b4-155">[**Иексплореркоммандстате**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) имеет преимущество выполнения в фоновом потоке и тем самым предотвращает ЗАВИСАНИЕ пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a12b4-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) has the advantage of running on a background thread, and thereby avoids UI hangs.</span></span> <span data-ttu-id="a12b4-156">Это значительно проще, чем [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="a12b4-156">It is considerably simpler than [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> |



 

### <a name="discouraged-dynamic-verb-methods"></a><span data-ttu-id="a12b4-157">Нерекомендованные динамические методы команд</span><span class="sxs-lookup"><span data-stu-id="a12b4-157">Discouraged Dynamic Verb Methods</span></span>

<span data-ttu-id="a12b4-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) является самым мощным, но и самым сложным методом для реализации.</span><span class="sxs-lookup"><span data-stu-id="a12b4-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="a12b4-159">Он основан на внутрипроцессного COM-объектах, которые выполняются в потоке вызывающего, который обычно является проводником Windows, но может быть любым приложением, в котором размещены элементы.</span><span class="sxs-lookup"><span data-stu-id="a12b4-159">It is based on in-process COM objects that run on the thread of the caller, which usually Windows Explorer but can be any application hosting the items.</span></span> <span data-ttu-id="a12b4-160">**IContextMenu** поддерживает видимость команд, упорядочение и пользовательское рисование.</span><span class="sxs-lookup"><span data-stu-id="a12b4-160">**IContextMenu** supports verb visibility, ordering, and custom drawing.</span></span> <span data-ttu-id="a12b4-161">Некоторые из этих функций были добавлены в функции статической команды, такие как значок, связываемый с командой, и [**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) для работы с видимостью.</span><span class="sxs-lookup"><span data-stu-id="a12b4-161">Some of these features have been added to the static verb features, such as an icon to be associated with a command, and [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) to deal with visibility.</span></span>

<span data-ttu-id="a12b4-162">Если необходимо расширить контекстное меню для типа файла, зарегистрировав динамическую команду для типа файла, следуйте инструкциям, приведенным в разделе [Настройка контекстного меню с помощью динамических команд](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="a12b4-162">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided in [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

## <a name="extend-a-shortcut-menu"></a><span data-ttu-id="a12b4-163">Расширение контекстного меню</span><span class="sxs-lookup"><span data-stu-id="a12b4-163">Extend a Shortcut Menu</span></span>

<span data-ttu-id="a12b4-164">После выбора метода команда можно расширить контекстное меню для типа файла, зарегистрировав статическую команду для типа файла.</span><span class="sxs-lookup"><span data-stu-id="a12b4-164">After you choose a verb method you can extend a shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="a12b4-165">Дополнительные сведения см. в разделе [Создание обработчиков контекстного меню](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a12b4-165">For more information, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="support-for-verb-methods-by-operating-system"></a><span data-ttu-id="a12b4-166">Поддержка методов команд операционной системой</span><span class="sxs-lookup"><span data-stu-id="a12b4-166">Support for Verb Methods by Operating System</span></span>

<span data-ttu-id="a12b4-167">Поддержка методов вызова команд по операционной системе указана в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a12b4-167">Support for verb invocation methods by operating system are listed in the following table.</span></span>



|                      |            |               |                      |
|----------------------|------------|---------------|----------------------|
|                      | <span data-ttu-id="a12b4-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a12b4-168">Windows XP</span></span> | <span data-ttu-id="a12b4-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a12b4-169">Windows Vista</span></span> | <span data-ttu-id="a12b4-170">Windows 7 и более поздние</span><span class="sxs-lookup"><span data-stu-id="a12b4-170">Windows 7 and beyond</span></span> |
| <span data-ttu-id="a12b4-171">CreateProcess</span><span class="sxs-lookup"><span data-stu-id="a12b4-171">CreateProcess</span></span>        | <span data-ttu-id="a12b4-172">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-172">X</span></span>          | <span data-ttu-id="a12b4-173">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-173">X</span></span>             | <span data-ttu-id="a12b4-174">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-174">X</span></span>                    |
| <span data-ttu-id="a12b4-175">DDE</span><span class="sxs-lookup"><span data-stu-id="a12b4-175">DDE</span></span>                  | <span data-ttu-id="a12b4-176">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-176">X</span></span>          | <span data-ttu-id="a12b4-177">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-177">X</span></span>             | <span data-ttu-id="a12b4-178">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-178">X</span></span>                    |
| <span data-ttu-id="a12b4-179">DropTarget</span><span class="sxs-lookup"><span data-stu-id="a12b4-179">DropTarget</span></span>           | <span data-ttu-id="a12b4-180">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-180">X</span></span>          | <span data-ttu-id="a12b4-181">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-181">X</span></span>             | <span data-ttu-id="a12b4-182">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-182">X</span></span>                    |
| <span data-ttu-id="a12b4-183">ExecuteCommand</span><span class="sxs-lookup"><span data-stu-id="a12b4-183">ExecuteCommand</span></span>       |            | <span data-ttu-id="a12b4-184">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-184">X</span></span>             | <span data-ttu-id="a12b4-185">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-185">X</span></span>                    |
| <span data-ttu-id="a12b4-186">експлореркомманд</span><span class="sxs-lookup"><span data-stu-id="a12b4-186">ExplorerCommand</span></span>      |            |               | <span data-ttu-id="a12b4-187">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-187">X</span></span>                    |
| <span data-ttu-id="a12b4-188">експлореркоммандстате</span><span class="sxs-lookup"><span data-stu-id="a12b4-188">ExplorerCommandState</span></span> |            |               | <span data-ttu-id="a12b4-189">X</span><span class="sxs-lookup"><span data-stu-id="a12b4-189">X</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="a12b4-190">См. также</span><span class="sxs-lookup"><span data-stu-id="a12b4-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a12b4-191">Рекомендации по работе с обработчиками контекстного меню и несколькими командами выбора</span><span class="sxs-lookup"><span data-stu-id="a12b4-191">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="a12b4-192">Создание обработчиков контекстного меню</span><span class="sxs-lookup"><span data-stu-id="a12b4-192">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="a12b4-193">Настройка контекстного меню с помощью динамических команд</span><span class="sxs-lookup"><span data-stu-id="a12b4-193">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="a12b4-194">Контекстное меню (контекст) и обработчики контекстного меню</span><span class="sxs-lookup"><span data-stu-id="a12b4-194">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="a12b4-195">Справочник по контекстному меню</span><span class="sxs-lookup"><span data-stu-id="a12b4-195">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> <dt>

[<span data-ttu-id="a12b4-196">Команды и сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="a12b4-196">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> </dl>

 

 
