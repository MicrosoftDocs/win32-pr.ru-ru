---
description: Представляет объект в оболочке.
title: Объект Ишеллдиспатч (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 20c6cc9f0b3a2e2fde8f56311564d63bc1cc9c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984697"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="b3470-103">Объект Ишеллдиспатч</span><span class="sxs-lookup"><span data-stu-id="b3470-103">IShellDispatch object</span></span>

<span data-ttu-id="b3470-104">Представляет объект в оболочке.</span><span class="sxs-lookup"><span data-stu-id="b3470-104">Represents an object in the Shell.</span></span> <span data-ttu-id="b3470-105">Предоставляются методы для управления оболочкой и выполнения команд в оболочке.</span><span class="sxs-lookup"><span data-stu-id="b3470-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="b3470-106">Существуют также методы для получения других объектов, связанных с оболочкой.</span><span class="sxs-lookup"><span data-stu-id="b3470-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="b3470-107">**Ишеллдиспатч** реализован и доступен через объект [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="b3470-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="b3470-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="b3470-108">Members</span></span>

<span data-ttu-id="b3470-109">Объект **ишеллдиспатч** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b3470-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="b3470-110">Методы</span><span class="sxs-lookup"><span data-stu-id="b3470-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b3470-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b3470-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b3470-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b3470-112">Methods</span></span>

<span data-ttu-id="b3470-113">Объект **ишеллдиспатч** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="b3470-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b3470-114">Метод</span><span class="sxs-lookup"><span data-stu-id="b3470-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b3470-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b3470-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-116"><a href="ishelldispatch-browseforfolder.md"><strong>бровсефорфолдер</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-117">Создает диалоговое окно, которое позволяет пользователю выбрать папку, а затем возвращает объект <a href="folder.md"><strong>папки</strong></a> выбранной папки.</span><span class="sxs-lookup"><span data-stu-id="b3470-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b3470-118"><a href="ishelldispatch-cascadewindows.md"><strong>каскадевиндовс</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-119">Каскадное расположение всех окон на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="b3470-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="b3470-120">Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора <strong>окна каскадом</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3470-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-122">Запускает указанное приложение панели управления.</span><span class="sxs-lookup"><span data-stu-id="b3470-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="b3470-123">Если приложение уже открыто, будет активирован запущенный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="b3470-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="b3470-124">Начиная с Windows Vista, большинство приложений панели управления являются элементами оболочки и не могут быть открыты с помощью этой функции.</span><span class="sxs-lookup"><span data-stu-id="b3470-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="b3470-125">Чтобы открыть эти приложения панели управления, передайте каноническое имя в control.exe.</span><span class="sxs-lookup"><span data-stu-id="b3470-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="b3470-126">Например:</span><span class="sxs-lookup"><span data-stu-id="b3470-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b3470-127"><a href="ishelldispatch-ejectpc.md"><strong>ежектпк</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-128">Извлекает компьютер из стыковочного узла.</span><span class="sxs-lookup"><span data-stu-id="b3470-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="b3470-129">Это то же самое, что и при нажатии кнопки " <strong>Пуск</strong> " и выборе пункта " <strong>извлечь компьютер</strong>", если компьютер поддерживает эту команду.</span><span class="sxs-lookup"><span data-stu-id="b3470-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-130"><a href="ishelldispatch-explore.md"><strong>Обзор</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-131">Открывает указанную папку в окне проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="b3470-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b3470-132"><a href="ishelldispatch-filerun.md"><strong>филерун</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-133">Отображает диалоговое окно <strong>запуска</strong> для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3470-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-134"><a href="ishelldispatch-findcomputer.md"><strong>финдкомпутер</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-135">Отображает диалоговое окно <strong>Результаты поиска: компьютеры</strong> .</span><span class="sxs-lookup"><span data-stu-id="b3470-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="b3470-136">В диалоговом окне отображается результат поиска указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="b3470-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b3470-137"><a href="ishelldispatch-findfiles.md"><strong>финдфилес</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-138">Отображает диалоговое окно <strong>Поиск: все файлы</strong> .</span><span class="sxs-lookup"><span data-stu-id="b3470-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="b3470-139">Это то же самое, что и при щелчке в меню <strong>Пуск</strong> , а затем выбрав <strong>Поиск</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3470-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-140"><a href="ishelldispatch-help.md"><strong>Справка</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-141">Отображает окно справки и поддержки Windows.</span><span class="sxs-lookup"><span data-stu-id="b3470-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="b3470-142">Этот метод действует так же, как и при щелчке меню <strong>Пуск</strong> и выбрав пункт <strong>Справка и поддержка</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3470-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b3470-143"><a href="ishelldispatch-minimizeall.md"><strong>минимизеалл</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-144">Свертывает все окна на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="b3470-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="b3470-145">Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора пункта <strong>Свернуть все окна</strong> в старых системах или нажатия значка " <strong>Свернуть Рабочий стол</strong> " на панели задач.</span><span class="sxs-lookup"><span data-stu-id="b3470-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-146"><a href="ishelldispatch-namespace.md"><strong>Имен</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-147">Создает и возвращает объект <a href="folder.md"><strong>Folder</strong></a> для указанной папки.</span><span class="sxs-lookup"><span data-stu-id="b3470-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b3470-148"><a href="ishelldispatch-open.md"><strong>Открыт</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-149">Открывает указанную папку.</span><span class="sxs-lookup"><span data-stu-id="b3470-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-150"><a href="ishelldispatch-refreshmenu.md"><strong>рефрешмену</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-151">Обновляет содержимое меню " <strong>Пуск</strong> ".</span><span class="sxs-lookup"><span data-stu-id="b3470-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="b3470-152">Используется только с системами, предшествующими Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b3470-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b3470-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-154">Отображает диалоговое окно <strong>Дата и время</strong> .</span><span class="sxs-lookup"><span data-stu-id="b3470-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="b3470-155">Этот метод действует так же, как и щелчок правой кнопкой мыши по часам в области состояние панели задач и выбор параметра <strong>настроить дату и время</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3470-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-156"><a href="ishelldispatch-shutdownwindows.md"><strong>шутдовнвиндовс</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-157">Отображает диалоговое окно <strong>Завершение работы Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="b3470-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="b3470-158">Это то же самое, что и при нажатии кнопки « <strong>Пуск</strong> », и при выборе « <strong>Завершение работы</strong>».</span><span class="sxs-lookup"><span data-stu-id="b3470-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b3470-159"><a href="ishelldispatch-suspend.md"><strong>Анализируем</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-160"><a href="ishelldispatch-tilehorizontally.md"><strong>тилехоризонталли</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-161">Мозаичное отображение всех окон на рабочем столе по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="b3470-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="b3470-162">Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора пункта <strong>Показывать окна с накоплением</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3470-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b3470-163"><a href="ishelldispatch-tilevertically.md"><strong>тилевертикалли</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-164">Располагает все окна на рабочем столе по вертикали.</span><span class="sxs-lookup"><span data-stu-id="b3470-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="b3470-165">Этот метод оказывает тот же результат, что и щелчок правой кнопкой мыши панели задач и выбора параметра <strong>Показывать окна рядом</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3470-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-166"><a href="ishelldispatch-trayproperties.md"><strong>трайпропертиес</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-167">Отображает диалоговое окно <strong>Свойства панели задач и меню "Пуск</strong> ".</span><span class="sxs-lookup"><span data-stu-id="b3470-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="b3470-168">Этот метод действует так же, как и щелчком правой кнопкой мыши панели задач и выбора <strong>свойств</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3470-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b3470-169"><a href="ishelldispatch-undominimizeall.md"><strong>ундоминимизеалл</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-170">Восстанавливает все настольные окна до состояния, в котором они были до последней команды <a href="shell-minimizeall.md"><strong>минимизеалл</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b3470-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="b3470-171">Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора команды <strong>отменить свернуть все окна</strong> (в старых системах) или второй щелчок значка Свернуть <strong>Рабочий стол</strong> на панели задач.</span><span class="sxs-lookup"><span data-stu-id="b3470-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b3470-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3470-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b3470-173">Создает и возвращает объект <a href="shellwindows.md"><strong>шеллвиндовс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b3470-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="b3470-174">Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.</span><span class="sxs-lookup"><span data-stu-id="b3470-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="b3470-175">Свойства</span><span class="sxs-lookup"><span data-stu-id="b3470-175">Properties</span></span>

<span data-ttu-id="b3470-176">Объект **ишеллдиспатч** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b3470-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="b3470-177">Свойство</span><span class="sxs-lookup"><span data-stu-id="b3470-177">Property</span></span>                                                     | <span data-ttu-id="b3470-178">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="b3470-178">Access type</span></span>          | <span data-ttu-id="b3470-179">Описание</span><span class="sxs-lookup"><span data-stu-id="b3470-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="b3470-180">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="b3470-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="b3470-181">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b3470-181">Read-only</span></span><br/> | <span data-ttu-id="b3470-182">Содержит объект, представляющий приложение.</span><span class="sxs-lookup"><span data-stu-id="b3470-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="b3470-183">**Parent**</span><span class="sxs-lookup"><span data-stu-id="b3470-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="b3470-184">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b3470-184">Read-only</span></span><br/> | <span data-ttu-id="b3470-185">Извлекает объект, представляющий родителя текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="b3470-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b3470-186">Требования</span><span class="sxs-lookup"><span data-stu-id="b3470-186">Requirements</span></span>



| <span data-ttu-id="b3470-187">Требование</span><span class="sxs-lookup"><span data-stu-id="b3470-187">Requirement</span></span> | <span data-ttu-id="b3470-188">Значение</span><span class="sxs-lookup"><span data-stu-id="b3470-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3470-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3470-189">Minimum supported client</span></span><br/> | <span data-ttu-id="b3470-190">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b3470-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b3470-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3470-191">Minimum supported server</span></span><br/> | <span data-ttu-id="b3470-192">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b3470-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b3470-193">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b3470-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3470-194"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3470-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b3470-195">IDL</span><span class="sxs-lookup"><span data-stu-id="b3470-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3470-196"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3470-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b3470-197">DLL</span><span class="sxs-lookup"><span data-stu-id="b3470-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3470-198"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b3470-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3470-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3470-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3470-200">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="b3470-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="b3470-201">**Объект оболочки**</span><span class="sxs-lookup"><span data-stu-id="b3470-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
