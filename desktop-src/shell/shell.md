---
description: Представляет объекты в оболочке. Предоставляются методы для управления оболочкой и выполнения команд в оболочке. Существуют также методы для получения других объектов, связанных с оболочкой.
title: 'Объект оболочки (Shldisp.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: 55f8062b71e553ec5ceefa413b45f439874744b8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841765"
---
# <a name="shell-object"></a><span data-ttu-id="e5aee-105">Объект оболочки</span><span class="sxs-lookup"><span data-stu-id="e5aee-105">Shell object</span></span>

<span data-ttu-id="e5aee-106">Представляет объекты в оболочке.</span><span class="sxs-lookup"><span data-stu-id="e5aee-106">Represents the objects in the Shell.</span></span> <span data-ttu-id="e5aee-107">Предоставляются методы для управления оболочкой и выполнения команд в оболочке.</span><span class="sxs-lookup"><span data-stu-id="e5aee-107">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="e5aee-108">Существуют также методы для получения других объектов, связанных с оболочкой.</span><span class="sxs-lookup"><span data-stu-id="e5aee-108">There are also methods to obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="e5aee-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="e5aee-109">Members</span></span>

<span data-ttu-id="e5aee-110">Объект **оболочки** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e5aee-110">The **Shell** object has these types of members:</span></span>

-   [<span data-ttu-id="e5aee-111">Методы</span><span class="sxs-lookup"><span data-stu-id="e5aee-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e5aee-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5aee-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e5aee-113">Методы</span><span class="sxs-lookup"><span data-stu-id="e5aee-113">Methods</span></span>

<span data-ttu-id="e5aee-114">Объект **оболочки** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e5aee-114">The **Shell** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e5aee-115">Метод</span><span class="sxs-lookup"><span data-stu-id="e5aee-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e5aee-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e5aee-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>аддторецент</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-118">Добавляет файл в список последних использованных файлов (MRU).</span><span class="sxs-lookup"><span data-stu-id="e5aee-118">Adds a file to the most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-119"><a href="shell-browseforfolder.md"><strong>бровсефорфолдер</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-120">Создает диалоговое окно, которое позволяет пользователю выбрать папку, а затем возвращает объект <a href="folder.md"><strong>папки</strong></a> выбранной папки.</span><span class="sxs-lookup"><span data-stu-id="e5aee-120">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>канстартстопсервице</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-122">Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.</span><span class="sxs-lookup"><span data-stu-id="e5aee-122">Determines if the current user can start and stop the named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-123"><a href="shell-cascadewindows.md"><strong>каскадевиндовс</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-124">Каскадное расположение всех окон на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="e5aee-124">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="e5aee-125">Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора <strong>окна каскадом</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5aee-125">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade Windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-127">Запускает указанное приложение панели управления (\*. cpl).</span><span class="sxs-lookup"><span data-stu-id="e5aee-127">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="e5aee-128">Если приложение уже открыто, будет активирован запущенный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e5aee-128">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="e5aee-129">Начиная с Windows Vista, большинство приложений панели управления являются элементами оболочки и не могут быть открыты с помощью этой функции.</span><span class="sxs-lookup"><span data-stu-id="e5aee-129">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="e5aee-130">Чтобы открыть эти приложения панели управления, передайте каноническое имя в control.exe.</span><span class="sxs-lookup"><span data-stu-id="e5aee-130">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="e5aee-131">Пример:</span><span class="sxs-lookup"><span data-stu-id="e5aee-131">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-132"><a href="shell-ejectpc.md"><strong>ежектпк</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-133">Извлекает компьютер из стыковочного узла.</span><span class="sxs-lookup"><span data-stu-id="e5aee-133">Ejects the computer from its docking station.</span></span> <span data-ttu-id="e5aee-134">Это то же самое, что и при нажатии кнопки " <strong>Пуск</strong> " и выборе пункта " <strong>извлечь компьютер</strong>", если компьютер поддерживает эту команду.</span><span class="sxs-lookup"><span data-stu-id="e5aee-134">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-135"><a href="shell-explore.md"><strong>Просматриваем</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-135"><a href="shell-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-136">Открывает указанную папку в окне проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="e5aee-136">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-137"><a href="shell-explorerpolicy.md"><strong>експлорерполици</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-138">Возвращает значение для указанной политики Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e5aee-138">Gets the value for a specified Internet Explorer policy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-139"><a href="shell-filerun.md"><strong>филерун</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-140">Отображает диалоговое окно <strong>запуска</strong> для пользователя.</span><span class="sxs-lookup"><span data-stu-id="e5aee-140">Displays the <strong>Run</strong> dialog to the user.</span></span> <span data-ttu-id="e5aee-141">Этот метод оказывает тот же результат, что и при щелчке меню <strong>Пуск</strong> и выборе <strong>Run</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5aee-141">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Run</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-142"><a href="shell-findcomputer.md"><strong>финдкомпутер</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-143">Отображает диалоговое окно <strong>Результаты поиска: компьютеры</strong> .</span><span class="sxs-lookup"><span data-stu-id="e5aee-143">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="e5aee-144">В диалоговом окне отображается результат поиска указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="e5aee-144">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-145"><a href="shell-findfiles.md"><strong>финдфилес</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-146">Отображает диалоговое окно <strong>Поиск: все файлы</strong> .</span><span class="sxs-lookup"><span data-stu-id="e5aee-146">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="e5aee-147">Это то же самое, что и при нажатии кнопки « <strong>Пуск</strong> », а затем при выборе <strong>поиска</strong> (или его эквивалента в системах, предшествующих Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e5aee-147">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong> (or its equivalent under systems earlier than Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>финдпринтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-149">Отображает диалоговое окно <strong>Поиск принтера</strong> .</span><span class="sxs-lookup"><span data-stu-id="e5aee-149">Displays the <strong>Find Printer</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-151">Извлекает параметр глобальной оболочки.</span><span class="sxs-lookup"><span data-stu-id="e5aee-151">Retrieves a global Shell setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>жетсистеминформатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-153">Возвращает сведения о системе.</span><span class="sxs-lookup"><span data-stu-id="e5aee-153">Retrieves system information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-154"><a href="shell-help.md"><strong>Справка</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-154"><a href="shell-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-155">Отображает центр справки и поддержки Windows.</span><span class="sxs-lookup"><span data-stu-id="e5aee-155">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="e5aee-156">Этот метод действует так же, как и при щелчке меню <strong>Пуск</strong> и выбрав пункт <strong>Справка и поддержка</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5aee-156">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>Ограниченный доступ</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-158">Извлекает из реестра параметр ограничений группы.</span><span class="sxs-lookup"><span data-stu-id="e5aee-158">Retrieves a group's restriction setting from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>иссервицеруннинг</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-160">Возвращает значение, указывающее, запущена ли определенная служба.</span><span class="sxs-lookup"><span data-stu-id="e5aee-160">Returns a value that indicates whether a particular service is running.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-161"><a href="shell-minimizeall.md"><strong>минимизеалл</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-162">Свертывает все окна на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="e5aee-162">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="e5aee-163">Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора пункта <strong>Свернуть все окна</strong> в старых системах или нажатия значка <strong>Показывать Рабочий стол</strong> в области Быстрый запуск панели задач в Windows 2000 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e5aee-163">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-164"><a href="shell-namespace.md"><strong>Имен</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-165">Создает и возвращает объект <a href="folder.md"><strong>Folder</strong></a> для указанной папки.</span><span class="sxs-lookup"><span data-stu-id="e5aee-165">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-166"><a href="shell-open.md"><strong>Открыт</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-166"><a href="shell-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-167">Открывает указанную папку.</span><span class="sxs-lookup"><span data-stu-id="e5aee-167">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-168"><a href="shell-refreshmenu.md"><strong>рефрешмену</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-169">Обновляет содержимое меню " <strong>Пуск</strong> ".</span><span class="sxs-lookup"><span data-stu-id="e5aee-169">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="e5aee-170">Используется только с системами, предшествующими Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e5aee-170">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-171"><a href="shell-searchcommand.md"><strong>сеарчкомманд</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-172">Отображает панель поиска приложений.</span><span class="sxs-lookup"><span data-stu-id="e5aee-172">Displays the Apps Search pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>сервицестарт</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-174">Запускает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="e5aee-174">Starts a named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>сервицестоп</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-176">Останавливает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="e5aee-176">Stops a named service.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-178">Отображает диалоговое окно <strong>Свойства даты и времени</strong> .</span><span class="sxs-lookup"><span data-stu-id="e5aee-178">Displays the <strong>Date and Time Properties</strong> dialog box.</span></span> <span data-ttu-id="e5aee-179">Этот метод действует так же, как и щелчок правой кнопкой мыши по часам в области состояние панели задач и выбор параметра <strong>настроить дату и время</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5aee-179">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust Date/Time</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-181">Выполняет указанную операцию с указанным файлом.</span><span class="sxs-lookup"><span data-stu-id="e5aee-181">Performs a specified operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>шовбровсербар</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-183">Отображает панель браузера.</span><span class="sxs-lookup"><span data-stu-id="e5aee-183">Displays a browser bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-184"><a href="shell-shutdownwindows.md"><strong>шутдовнвиндовс</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-185">Отображает диалоговое окно <strong>Завершение работы Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="e5aee-185">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="e5aee-186">Это то же самое, что и при нажатии кнопки « <strong>Пуск</strong> », и при выборе « <strong>Завершение работы</strong>».</span><span class="sxs-lookup"><span data-stu-id="e5aee-186">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-187"><a href="shell-suspend.md"><strong>Анализируем</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-188"><a href="shell-tilehorizontally.md"><strong>тилехоризонталли</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-189">Мозаичное отображение всех окон на рабочем столе по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="e5aee-189">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="e5aee-190">Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбор <strong>окон мозаики по горизонтали</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5aee-190">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Horizontally</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-191"><a href="shell-tilevertically.md"><strong>тилевертикалли</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-192">Располагает все окна на рабочем столе по вертикали.</span><span class="sxs-lookup"><span data-stu-id="e5aee-192">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="e5aee-193">Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбор <strong>окон мозаики по вертикали</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5aee-193">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Vertically</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-194"><a href="shell-toggledesktop.md"><strong>тоггледесктоп</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-195">Отображает или скрывает Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="e5aee-195">Displays or hides the desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-196"><a href="shell-trayproperties.md"><strong>трайпропертиес</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-197">Отображает диалоговое окно <strong>Свойства панели задач и меню "Пуск</strong> ".</span><span class="sxs-lookup"><span data-stu-id="e5aee-197">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="e5aee-198">Этот метод действует так же, как и щелчком правой кнопкой мыши панели задач и выбора <strong>свойств</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5aee-198">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-199"><a href="shell-undominimizeall.md"><strong>ундоминимизеалл</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-200">Восстанавливает все настольные компьютеры в том же состоянии, в котором они находились до последней команды <a href="shell-minimizeall.md"><strong>минимизеалл</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5aee-200">Restores all desktop windows to the same state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="e5aee-201">Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора команды <strong>отменить свернуть все окна</strong> в старых системах или второй щелчок значка Свернуть <strong>Рабочий стол</strong> в области Быстрый запуск панели задач в Windows 2000 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e5aee-201">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> on older systems or a second clicking of the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-202"><a href="shell-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-202"><a href="shell-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-203">Создает и возвращает объект <a href="shellwindows.md"><strong>шеллвиндовс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5aee-203">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="e5aee-204">Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.</span><span class="sxs-lookup"><span data-stu-id="e5aee-204">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5aee-205"><a href="shell-windowssecurity.md"><strong>виндовссекурити</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-206">Отображает диалоговое окно <strong>Безопасность Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="e5aee-206">Displays the <strong>Windows Security</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5aee-207"><a href="shell-windowswitcher.md"><strong>виндовсвитчер</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5aee-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5aee-208">Отображает открытые окна в трехмерном стеке, который можно переворачивать.</span><span class="sxs-lookup"><span data-stu-id="e5aee-208">Displays your open windows in a 3D stack that you can flip through.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="e5aee-209">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5aee-209">Properties</span></span>

<span data-ttu-id="e5aee-210">Объект **оболочки** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e5aee-210">The **Shell** object has these properties.</span></span>



| <span data-ttu-id="e5aee-211">Свойство</span><span class="sxs-lookup"><span data-stu-id="e5aee-211">Property</span></span>                                            | <span data-ttu-id="e5aee-212">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="e5aee-212">Access type</span></span>          | <span data-ttu-id="e5aee-213">Описание</span><span class="sxs-lookup"><span data-stu-id="e5aee-213">Description</span></span>                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="e5aee-214">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="e5aee-214">**Application**</span></span>](shell-application.md)<br/> | <span data-ttu-id="e5aee-215">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5aee-215">Read-only</span></span><br/> | <span data-ttu-id="e5aee-216">Содержит объект приложения объекта.</span><span class="sxs-lookup"><span data-stu-id="e5aee-216">Contains the object's Application object.</span></span><br/>                        |
| [<span data-ttu-id="e5aee-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="e5aee-217">**Parent**</span></span>](shell-parent.md)<br/>           | <span data-ttu-id="e5aee-218">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5aee-218">Read-only</span></span><br/> | <span data-ttu-id="e5aee-219">Возвращает объект, представляющий родительский объект текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="e5aee-219">Gets an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e5aee-220">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="e5aee-220">Requirements</span></span>



| <span data-ttu-id="e5aee-221">Требование</span><span class="sxs-lookup"><span data-stu-id="e5aee-221">Requirement</span></span> | <span data-ttu-id="e5aee-222">Значение</span><span class="sxs-lookup"><span data-stu-id="e5aee-222">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5aee-223">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5aee-223">Minimum supported client</span></span><br/> | <span data-ttu-id="e5aee-224">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e5aee-224">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e5aee-225">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5aee-225">Minimum supported server</span></span><br/> | <span data-ttu-id="e5aee-226">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5aee-226">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e5aee-227">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e5aee-227">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5aee-228"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5aee-228"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e5aee-229">IDL</span><span class="sxs-lookup"><span data-stu-id="e5aee-229">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5aee-230"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5aee-230"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e5aee-231">DLL</span><span class="sxs-lookup"><span data-stu-id="e5aee-231">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5aee-232"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="e5aee-232"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
