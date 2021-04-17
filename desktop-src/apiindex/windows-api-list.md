---
description: Список справочных материалов по API Windows.
ms.assetid: 9CA123F9-92F1-4761-9468-266DA422F70E
title: Указатель API Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cace235af1c729e450bdf99b276eca1bfc000
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105704041"
---
# <a name="windows-api-index"></a><span data-ttu-id="77b98-103">Указатель API Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-103">Windows API index</span></span>

<span data-ttu-id="77b98-104">Ниже приведен список справочных материалов по интерфейсу прикладного программирования (API) Windows для настольных и серверных приложений.</span><span class="sxs-lookup"><span data-stu-id="77b98-104">The following is a list of the reference content for the Windows application programming interface (API) for desktop and server applications.</span></span>

<span data-ttu-id="77b98-105">С помощью API Windows можно разрабатывать приложения, которые успешно выполняются во всех версиях Windows, а также использовать возможности и возможности, уникальные для каждой версии.</span><span class="sxs-lookup"><span data-stu-id="77b98-105">Using the Windows API, you can develop applications that run successfully on all versions of Windows while taking advantage of the features and capabilities unique to each version.</span></span> <span data-ttu-id="77b98-106">(Обратите внимание, что раньше это называлось API Win32.</span><span class="sxs-lookup"><span data-stu-id="77b98-106">(Note that this was formerly called the Win32 API.</span></span> <span data-ttu-id="77b98-107">Имя API Windows более точно отражает его корни в 16-разрядной версии Windows и поддерживает 64-разрядную версию Windows.)</span><span class="sxs-lookup"><span data-stu-id="77b98-107">The name Windows API more accurately reflects its roots in 16-bit Windows and its support on 64-bit Windows.)</span></span>

## <a name="user-interface"></a><span data-ttu-id="77b98-108">Пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="77b98-108">User interface</span></span>

<span data-ttu-id="77b98-109">API пользовательского интерфейса Windows создают и используют окна для вывода выходных данных, запроса вводимых пользователем данных и выполнения других задач, поддерживающих взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="77b98-109">The Windows UI API create and use windows to display output, prompt for user input, and carry out the other tasks that support interaction with the user.</span></span> <span data-ttu-id="77b98-110">Большинство приложений создают по крайней мере одно окно.</span><span class="sxs-lookup"><span data-stu-id="77b98-110">Most applications create at least one window.</span></span>

-   [<span data-ttu-id="77b98-111">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="77b98-111">Accessibility</span></span>](../winauto/windows-accessibility-features-reference.md)
-   [<span data-ttu-id="77b98-112">Диспетчер окон рабочего стола (DWM)</span><span class="sxs-lookup"><span data-stu-id="77b98-112">Desktop Window Manager (DWM)</span></span>](../dwm/reference.md)
-   [<span data-ttu-id="77b98-113">Службы глобализации</span><span class="sxs-lookup"><span data-stu-id="77b98-113">Globalization Services</span></span>](../intl/globalization-services.md)
-   [<span data-ttu-id="77b98-114">Приложения с высоким DPI</span><span class="sxs-lookup"><span data-stu-id="77b98-114">High DPI</span></span>](../hidpi/high-dpi-reference.md)
-   [<span data-ttu-id="77b98-115">Многоязыковой интерфейс пользователя (MUI)</span><span class="sxs-lookup"><span data-stu-id="77b98-115">Multilingual User Interface (MUI)</span></span>](../intl/multilingual-user-interface-reference.md)
-   [<span data-ttu-id="77b98-116">Многоязыковая поддержка (NLS)</span><span class="sxs-lookup"><span data-stu-id="77b98-116">National Language Support (NLS)</span></span>](../intl/national-language-support-reference.md)
-   <span data-ttu-id="77b98-117">[Элементы пользовательского интерфейса](../devnotes/user-interface.md):</span><span class="sxs-lookup"><span data-stu-id="77b98-117">[User Interface elements](../devnotes/user-interface.md):</span></span>

    -   [<span data-ttu-id="77b98-118">Кнопки</span><span class="sxs-lookup"><span data-stu-id="77b98-118">Buttons</span></span>](../controls/bumper-button-button-control-reference.md)
    -   [<span data-ttu-id="77b98-119">Крышки</span><span class="sxs-lookup"><span data-stu-id="77b98-119">Carets</span></span>](../menurc/caret-functions.md)
    -   [<span data-ttu-id="77b98-120">Поля со списком</span><span class="sxs-lookup"><span data-stu-id="77b98-120">Combo Boxes</span></span>](../controls/bumper-combobox-combobox-control-reference.md)
    -   [<span data-ttu-id="77b98-121">Общие диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="77b98-121">Common Dialog Boxes</span></span>](../dlgbox/common-dialog-box-reference.md)
    -   [<span data-ttu-id="77b98-122">Стандартные элементы управления</span><span class="sxs-lookup"><span data-stu-id="77b98-122">Common Controls</span></span>](../controls/individual-control-info.md)
    -   [<span data-ttu-id="77b98-123">Курсоры</span><span class="sxs-lookup"><span data-stu-id="77b98-123">Cursors</span></span>](../menurc/cursor-reference.md)
    -   [<span data-ttu-id="77b98-124">Диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="77b98-124">Dialog Boxes</span></span>](../dlgbox/dialog-box-reference.md)
    -   [<span data-ttu-id="77b98-125">Изменить элементы управления</span><span class="sxs-lookup"><span data-stu-id="77b98-125">Edit Controls</span></span>](../controls/bumper-edit-control-edit-control-reference.md)
    -   [<span data-ttu-id="77b98-126">Элементы управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="77b98-126">Header Controls</span></span>](../controls/bumper-header-control-header-control-reference.md)
    -   [<span data-ttu-id="77b98-127">Значки</span><span class="sxs-lookup"><span data-stu-id="77b98-127">Icons</span></span>](../menurc/icon-reference.md)
    -   [<span data-ttu-id="77b98-128">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="77b98-128">Keyboard Accelerators</span></span>](../menurc/keyboard-accelerator-reference.md)
    -   [<span data-ttu-id="77b98-129">Списки</span><span class="sxs-lookup"><span data-stu-id="77b98-129">List Boxes</span></span>](../controls/bumper-list-box-list-box-control-reference.md)
    -   [<span data-ttu-id="77b98-130">Элементы управления "представление списка"</span><span class="sxs-lookup"><span data-stu-id="77b98-130">List-View Controls</span></span>](../controls/bumper-list-view-list-view-control-reference.md)
    -   [<span data-ttu-id="77b98-131">Меню</span><span class="sxs-lookup"><span data-stu-id="77b98-131">Menus</span></span>](../menurc/menu-reference.md)
    -   [<span data-ttu-id="77b98-132">Индикаторы выполнения</span><span class="sxs-lookup"><span data-stu-id="77b98-132">Progress Bars</span></span>](../controls/bumper-progress-bar-progress-bar-control-reference.md)
    -   [<span data-ttu-id="77b98-133">Вкладки свойств</span><span class="sxs-lookup"><span data-stu-id="77b98-133">Property Sheets</span></span>](../controls/bumper-property-sheet-property-sheets-reference.md)
    -   [<span data-ttu-id="77b98-134">Элементы управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="77b98-134">Rich Edit Controls</span></span>](../controls/bumper-rich-edit-rich-edit-control-reference.md)
    -   [<span data-ttu-id="77b98-135">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="77b98-135">Scroll Bars</span></span>](../controls/bumper-scroll-bar-scroll-bars-reference.md)
    -   [<span data-ttu-id="77b98-136">Статические элементы управления</span><span class="sxs-lookup"><span data-stu-id="77b98-136">Static Controls</span></span>](../controls/bumper-static-control-static-control-reference.md)
    -   [<span data-ttu-id="77b98-137">Строки</span><span class="sxs-lookup"><span data-stu-id="77b98-137">Strings</span></span>](../menurc/string-reference.md)
    -   [<span data-ttu-id="77b98-138">Панели инструментов</span><span class="sxs-lookup"><span data-stu-id="77b98-138">Toolbars</span></span>](../controls/bumper-toolbar-toolbar-control-reference.md)
    -   [<span data-ttu-id="77b98-139">Подсказки</span><span class="sxs-lookup"><span data-stu-id="77b98-139">Tooltips</span></span>](../controls/bumper-tooltip-tooltip-control-reference.md)
    -   [<span data-ttu-id="77b98-140">Линейки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="77b98-140">Trackbars</span></span>](../controls/bumper-trackbar-trackbar-control-reference.md)
    -   [<span data-ttu-id="77b98-141">Элементы управления "дерево-представление"</span><span class="sxs-lookup"><span data-stu-id="77b98-141">Tree-View Controls</span></span>](../controls/bumper-tree-view-tree-view-control-reference.md)

-   [<span data-ttu-id="77b98-142">Диспетчер анимации Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-142">Windows Animation Manager</span></span>](../uianimation/windows-animation-reference.md)
-   [<span data-ttu-id="77b98-143">Платформа ленты Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-143">Windows Ribbon Framework</span></span>](../windowsribbon/windowsribbon-reference-entry.md)

## <a name="windows-environment-shell"></a><span data-ttu-id="77b98-144">Среда Windows (оболочка)</span><span class="sxs-lookup"><span data-stu-id="77b98-144">Windows environment (Shell)</span></span>

-   [<span data-ttu-id="77b98-145">Система свойств Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-145">Windows Property System</span></span>](../properties/property-system-reference.md)
-   <span data-ttu-id="77b98-146">[Оболочка Windows](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-146">[Windows Shell](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))</span></span>
-   [<span data-ttu-id="77b98-147">Поиск Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-147">Windows Search</span></span>](../search/-search-reference-entry-page.md)
-   [<span data-ttu-id="77b98-148">Консоли</span><span class="sxs-lookup"><span data-stu-id="77b98-148">Consoles</span></span>](/windows/console/console-reference)

## <a name="user-input-and-messaging"></a><span data-ttu-id="77b98-149">Ввод пользователя и обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="77b98-149">User input and messaging</span></span>

-   [<span data-ttu-id="77b98-150">Взаимодействие с пользователем</span><span class="sxs-lookup"><span data-stu-id="77b98-150">User Interaction</span></span>](../user-interaction.md)
    -   [<span data-ttu-id="77b98-151">Непосредственная манипуляция</span><span class="sxs-lookup"><span data-stu-id="77b98-151">Direct Manipulation</span></span>](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)
    -   [<span data-ttu-id="77b98-152">Рукописный ввод</span><span class="sxs-lookup"><span data-stu-id="77b98-152">Ink input</span></span>](/previous-versions/windows/desktop/input_ink/input-ink-portal)
    -   [<span data-ttu-id="77b98-153">Настройка обратной связи для ввода</span><span class="sxs-lookup"><span data-stu-id="77b98-153">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
    -   [<span data-ttu-id="77b98-154">Контекст взаимодействия</span><span class="sxs-lookup"><span data-stu-id="77b98-154">Interaction Context</span></span>](/previous-versions/windows/desktop/input_intcontext/interaction-context-portal)
    -   [<span data-ttu-id="77b98-155">Входной стек устройства указателя</span><span class="sxs-lookup"><span data-stu-id="77b98-155">Pointer Device Input Stack</span></span>](/previous-versions/windows/desktop/input_pointerdevice/pointer-device-stack-portal)
    -   [<span data-ttu-id="77b98-156">Входные сообщения и уведомления указателя</span><span class="sxs-lookup"><span data-stu-id="77b98-156">Pointer Input Messages and Notifications</span></span>](/previous-versions/windows/desktop/inputmsg/messages-and-notifications)
    -   [<span data-ttu-id="77b98-157">Входные данные радиального контроллера</span><span class="sxs-lookup"><span data-stu-id="77b98-157">Radial controller input</span></span>](/previous-versions/windows/desktop/input_radial/radialcontroller-portal)
    -   [<span data-ttu-id="77b98-158">инфраструктуры текстовых служб (TSF)</span><span class="sxs-lookup"><span data-stu-id="77b98-158">Text Services Framework</span></span>](../tsf/text-services-framework.md)
    -   [<span data-ttu-id="77b98-159">Проверка нажатия касания</span><span class="sxs-lookup"><span data-stu-id="77b98-159">Touch Hit Testing</span></span>](/previous-versions/windows/desktop/input_touchhittest/touch-hit-testing-portal)
    -   [<span data-ttu-id="77b98-160">Внедрение сенсорного ввода</span><span class="sxs-lookup"><span data-stu-id="77b98-160">Touch Injection</span></span>](/previous-versions/windows/desktop/input_touchinjection/touch-injection-portal)
-   [<span data-ttu-id="77b98-161">Взаимодействие с пользователем прежних версий</span><span class="sxs-lookup"><span data-stu-id="77b98-161">Legacy User Interaction</span></span>](../legacy-user-interaction-features.md)
    -   [<span data-ttu-id="77b98-162">Сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="77b98-162">Touch Input</span></span>](../wintouch/windows-touch-portal.md)
    -   [<span data-ttu-id="77b98-163">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="77b98-163">Keyboard Input</span></span>](../inputdev/keyboard-input.md)
    -   [<span data-ttu-id="77b98-164">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="77b98-164">Mouse Input</span></span>](../inputdev/mouse-input.md)
    -   [<span data-ttu-id="77b98-165">Необработанный ввод</span><span class="sxs-lookup"><span data-stu-id="77b98-165">Raw Input</span></span>](../inputdev/raw-input.md)
-   <span data-ttu-id="77b98-166">[Окна и сообщения](../winmsg/windowing.md):</span><span class="sxs-lookup"><span data-stu-id="77b98-166">[Windows and Messages](../winmsg/windowing.md):</span></span>

    -   [<span data-ttu-id="77b98-167">Сообщения и очереди сообщений</span><span class="sxs-lookup"><span data-stu-id="77b98-167">Messages and Message Queues</span></span>](../winmsg/message-and-message-queue-reference.md)
    -   [<span data-ttu-id="77b98-168">Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-168">Windows</span></span>](../winmsg/window-reference.md)
    -   [<span data-ttu-id="77b98-169">Классы окон</span><span class="sxs-lookup"><span data-stu-id="77b98-169">Window Classes</span></span>](../winmsg/window-class-reference.md)
    -   [<span data-ttu-id="77b98-170">Процедуры окна</span><span class="sxs-lookup"><span data-stu-id="77b98-170">Window Procedures</span></span>](../winmsg/window-procedure-reference.md)
    -   [<span data-ttu-id="77b98-171">Таймеры</span><span class="sxs-lookup"><span data-stu-id="77b98-171">Timers</span></span>](../winmsg/timer-reference.md)
    -   [<span data-ttu-id="77b98-172">Свойства окна</span><span class="sxs-lookup"><span data-stu-id="77b98-172">Window Properties</span></span>](../winmsg/window-property-reference.md)
    -   [<span data-ttu-id="77b98-173">Обработчики</span><span class="sxs-lookup"><span data-stu-id="77b98-173">Hooks</span></span>](../winmsg/hook-reference.md)

## <a name="data-access-and-storage"></a><span data-ttu-id="77b98-174">Доступ к данным и хранилища данных</span><span class="sxs-lookup"><span data-stu-id="77b98-174">Data access and storage</span></span>

-   [<span data-ttu-id="77b98-175">Фоновая интеллектуальная служба передачи (BITS)</span><span class="sxs-lookup"><span data-stu-id="77b98-175">Background Intelligent Transfer Service (BITS)</span></span>](../bits/bits-reference.md)
-   [<span data-ttu-id="77b98-176">Резервное копирование данных</span><span class="sxs-lookup"><span data-stu-id="77b98-176">Data Backup</span></span>](../backup/backup.md)
    -   [<span data-ttu-id="77b98-177">Azure Backup</span><span class="sxs-lookup"><span data-stu-id="77b98-177">Backup</span></span>](../backup/backup-reference.md)
    -   [<span data-ttu-id="77b98-178">Дедупликация данных</span><span class="sxs-lookup"><span data-stu-id="77b98-178">Data Deduplication</span></span>](/previous-versions/windows/desktop/dedup/data-deduplication-api-reference)
    -   [<span data-ttu-id="77b98-179">Служба теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="77b98-179">Volume Shadow Copy</span></span>](../vss/volume-shadow-copy-reference.md)
    -   [<span data-ttu-id="77b98-180">Система архивации данных Windows Server</span><span class="sxs-lookup"><span data-stu-id="77b98-180">Windows Server Backup</span></span>](/previous-versions/windows/desktop/wsb/windows-server-backup-api-interfaces)
-   <span data-ttu-id="77b98-181">[Обмен данными](../dataxchg/data-exchange.md):</span><span class="sxs-lookup"><span data-stu-id="77b98-181">[Data Exchange](../dataxchg/data-exchange.md):</span></span>

    -   [<span data-ttu-id="77b98-182">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="77b98-182">Clipboard</span></span>](../dataxchg/clipboard-reference.md)
    -   [<span data-ttu-id="77b98-183">Платформа динамических данных Exchange (DDE)</span><span class="sxs-lookup"><span data-stu-id="77b98-183">Dynamic Data Exchange (DDE)</span></span>](../dataxchg/dynamic-data-exchange-reference.md)
    -   [<span data-ttu-id="77b98-184">Управление платформа динамических данных Exchange (ДДЕМЛ)</span><span class="sxs-lookup"><span data-stu-id="77b98-184">Dynamic Data Exchange Management (DDEML)</span></span>](../dataxchg/dynamic-data-exchange-management-library-reference.md)

-   [<span data-ttu-id="77b98-185">Управление каталогом</span><span class="sxs-lookup"><span data-stu-id="77b98-185">Directory Management</span></span>](../fileio/directory-management-reference.md)
-   [<span data-ttu-id="77b98-186">Управление дисками</span><span class="sxs-lookup"><span data-stu-id="77b98-186">Disk Management</span></span>](../fileio/disk-management-reference.md)
-   [<span data-ttu-id="77b98-187">Распределенная файловая система (DFS)</span><span class="sxs-lookup"><span data-stu-id="77b98-187">Distributed File System (DFS)</span></span>](/previous-versions/windows/desktop/dfs/distributed-file-system-reference)
-   [<span data-ttu-id="77b98-188">Репликация распределенная файловая система</span><span class="sxs-lookup"><span data-stu-id="77b98-188">Distributed File System Replication</span></span>](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)
-   [<span data-ttu-id="77b98-189">Расширяемая подсистема хранилища</span><span class="sxs-lookup"><span data-stu-id="77b98-189">Extensible Storage Engine</span></span>](../extensible-storage-engine/extensible-storage-engine-reference.md)
-   [<span data-ttu-id="77b98-190">Файлы и операции ввода-вывода (локальная файловая система)</span><span class="sxs-lookup"><span data-stu-id="77b98-190">Files and I/O (Local file system)</span></span>](../fileio/file-management-reference.md)
-   [<span data-ttu-id="77b98-191">API библиотеки обнаружения iSCSI</span><span class="sxs-lookup"><span data-stu-id="77b98-191">iSCSI Discovery Library API</span></span>](/previous-versions/windows/desktop/iscsidisc/iscsi-discovery-library-reference)
-   [<span data-ttu-id="77b98-192">Автономные файлы</span><span class="sxs-lookup"><span data-stu-id="77b98-192">Offline Files</span></span>](/previous-versions/windows/desktop/offlinefiles/offline-files-reference)
-   [<span data-ttu-id="77b98-193">Упаковка</span><span class="sxs-lookup"><span data-stu-id="77b98-193">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging-programming-reference)
-   [<span data-ttu-id="77b98-194">Протокол удаленного разностного сжатия</span><span class="sxs-lookup"><span data-stu-id="77b98-194">Remote Differential Compression</span></span>](/previous-versions/windows/desktop/rdc/remote-differential-compression-reference)
-   [<span data-ttu-id="77b98-195">Поддержка транзакций в NTFS</span><span class="sxs-lookup"><span data-stu-id="77b98-195">Transactional NTFS</span></span>](../fileio/transactional-ntfs-reference.md)
-   [<span data-ttu-id="77b98-196">Управление томами</span><span class="sxs-lookup"><span data-stu-id="77b98-196">Volume Management</span></span>](../fileio/volume-management-reference.md)
-   <span data-ttu-id="77b98-197">[Виртуальный жесткий диск (VHD)](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-197">[Virtual Hard Disk (VHD)](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))</span></span>
-   [<span data-ttu-id="77b98-198">Управление хранилищем Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-198">Windows Storage Management</span></span>](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   <span data-ttu-id="77b98-199">[Компоненты доступа к данным Windows DAC](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-199">[Windows Data Access Components](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))</span></span>
    -   [<span data-ttu-id="77b98-200">Microsoft Open Database Connectivity (ODBC)</span><span class="sxs-lookup"><span data-stu-id="77b98-200">Microsoft Open Database Connectivity (ODBC)</span></span>](/sql/odbc/reference/syntax/odbc-reference)
    -   <span data-ttu-id="77b98-201">[OLE DB (Майкрософт)](/previous-versions/windows/desktop/ms718050(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-201">[Microsoft OLE DB](/previous-versions/windows/desktop/ms718050(v=vs.85))</span></span>
    -   [<span data-ttu-id="77b98-202">Объекты данных Microsoft ActiveX (ADO)</span><span class="sxs-lookup"><span data-stu-id="77b98-202">Microsoft ActiveX Data Objects (ADO)</span></span>](/sql/ado/reference/ado-programmer-s-reference)

## <a name="diagnostics"></a><span data-ttu-id="77b98-203">Диагностика</span><span class="sxs-lookup"><span data-stu-id="77b98-203">Diagnostics</span></span>

<span data-ttu-id="77b98-204">API [диагностики](/previous-versions//bb648685(v=vs.85)) позволяет устранять неполадки в приложениях и системах, а также наблюдать за производительностью.</span><span class="sxs-lookup"><span data-stu-id="77b98-204">The [Diagnostics](/previous-versions//bb648685(v=vs.85)) API enable you to troubleshoot application or system problems and monitor performance.</span></span>

-   [<span data-ttu-id="77b98-205">Восстановление приложений и перезагрузка</span><span class="sxs-lookup"><span data-stu-id="77b98-205">Application Recovery and Restart</span></span>](../recovery/application-recovery-and-restart-reference.md)
-   [<span data-ttu-id="77b98-206">Отладка</span><span class="sxs-lookup"><span data-stu-id="77b98-206">Debugging</span></span>](../debug/debugging-reference.md)
-   [<span data-ttu-id="77b98-207">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="77b98-207">Error Handling</span></span>](../debug/error-handling-reference.md)
-   [<span data-ttu-id="77b98-208">Ведение журналов событий</span><span class="sxs-lookup"><span data-stu-id="77b98-208">Event Logging</span></span>](../eventlog/event-logging-reference.md)
-   [<span data-ttu-id="77b98-209">Трассировка событий</span><span class="sxs-lookup"><span data-stu-id="77b98-209">Event Tracing</span></span>](../etw/event-tracing-reference.md)
-   [<span data-ttu-id="77b98-210">Профилирование счетчиков оборудования (HCP)</span><span class="sxs-lookup"><span data-stu-id="77b98-210">Hardware Counter Profiling (HCP)</span></span>](/previous-versions/windows/desktop/hcp/hcp-reference)
-   [<span data-ttu-id="77b98-211">Инфраструктура диагностики сети (NDF)</span><span class="sxs-lookup"><span data-stu-id="77b98-211">Network Diagnostics Framework (NDF)</span></span>](../ndf/ndf-reference.md)
-   [<span data-ttu-id="77b98-212">Сетевой монитор</span><span class="sxs-lookup"><span data-stu-id="77b98-212">Network Monitor</span></span>](../netmon2/reference.md)
-   [<span data-ttu-id="77b98-213">Счетчики производительности</span><span class="sxs-lookup"><span data-stu-id="77b98-213">Performance Counters</span></span>](../perfctrs/performance-counters-reference.md)
-   [<span data-ttu-id="77b98-214">Журналы и оповещения производительности (PLA)</span><span class="sxs-lookup"><span data-stu-id="77b98-214">Performance Logs and Alerts (PLA)</span></span>](/previous-versions/windows/desktop/pla/performance-logs-and-alerts-reference)
-   [<span data-ttu-id="77b98-215">Обработка значит</span><span class="sxs-lookup"><span data-stu-id="77b98-215">Process Snapshotting</span></span>](/previous-versions/windows/desktop/proc_snap/process-snapshotting-reference)
-   [<span data-ttu-id="77b98-216">Состояние процесса (PSAPI)</span><span class="sxs-lookup"><span data-stu-id="77b98-216">Process Status (PSAPI)</span></span>](../psapi/psapi-reference.md)
-   [<span data-ttu-id="77b98-217">Структурированная обработка исключений</span><span class="sxs-lookup"><span data-stu-id="77b98-217">Structured Exception Handling</span></span>](../debug/structured-exception-handling-reference.md)
-   [<span data-ttu-id="77b98-218">Системный монитор</span><span class="sxs-lookup"><span data-stu-id="77b98-218">System Monitor</span></span>](../sysmon/system-monitor-reference.md)
-   [<span data-ttu-id="77b98-219">Ожидание обхода цепочки</span><span class="sxs-lookup"><span data-stu-id="77b98-219">Wait Chain Traversal</span></span>](../debug/wait-chain-traversal.md)
-   [<span data-ttu-id="77b98-220">Отчеты об ошибках Windows (WER)</span><span class="sxs-lookup"><span data-stu-id="77b98-220">Windows Error Reporting (WER)</span></span>](../wer/wer-reference.md)
-   [<span data-ttu-id="77b98-221">Журнал событий Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-221">Windows Event Log</span></span>](../wes/windows-event-log-reference.md)
-   [<span data-ttu-id="77b98-222">Платформа устранения неполадок Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-222">Windows Troubleshooting Platform</span></span>](/previous-versions/windows/desktop/wintt/windows-troubleshooting-reference)

## <a name="graphics-and-multimedia"></a><span data-ttu-id="77b98-223">Графика и мультимедиа</span><span class="sxs-lookup"><span data-stu-id="77b98-223">Graphics and multimedia</span></span>

<span data-ttu-id="77b98-224">API-интерфейсы [Graphics, мультимедиа,](/previous-versions//aa969176(v=vs.85)) [аудио и видео](../audio-and-video.md) позволяют приложениям включать форматированный текст, графику, аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="77b98-224">The [Graphics, multimedia,](/previous-versions//aa969176(v=vs.85)) [audio, and video](../audio-and-video.md) APIs enable applications to incorporate formatted text, graphics, audio, and video.</span></span>

-   [<span data-ttu-id="77b98-225">Основной звук</span><span class="sxs-lookup"><span data-stu-id="77b98-225">Core Audio</span></span>](../coreaudio/programming-reference.md)
-   [<span data-ttu-id="77b98-226">Direct2D</span><span class="sxs-lookup"><span data-stu-id="77b98-226">Direct2D</span></span>](../direct2d/reference.md)
-   [<span data-ttu-id="77b98-227">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="77b98-227">DirectComposition</span></span>](../directcomp/reference.md)
-   [<span data-ttu-id="77b98-228">DirectShow</span><span class="sxs-lookup"><span data-stu-id="77b98-228">DirectShow</span></span>](../directshow/directshow-reference.md)
-   [<span data-ttu-id="77b98-229">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="77b98-229">DirectWrite</span></span>](../directwrite/reference.md)
-   [<span data-ttu-id="77b98-230">DirectX</span><span class="sxs-lookup"><span data-stu-id="77b98-230">DirectX</span></span>](../directx-sdk--august-2009-.md)
-   [<span data-ttu-id="77b98-231">Интерфейс графических устройств (GDI)</span><span class="sxs-lookup"><span data-stu-id="77b98-231">Graphics Device Interface (GDI)</span></span>](../gdi/windows-gdi.md)
-   [<span data-ttu-id="77b98-232">GDI+</span><span class="sxs-lookup"><span data-stu-id="77b98-232">GDI+</span></span>](../gdiplus/-gdiplus-class-gdi-reference.md)
-   [<span data-ttu-id="77b98-233">Потоковая передача мультимедиа</span><span class="sxs-lookup"><span data-stu-id="77b98-233">Media Streaming</span></span>](../mediastreaming/media-streaming-api-portal.md)
-   [<span data-ttu-id="77b98-234">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77b98-234">Microsoft Media Foundation</span></span>](../medfound/media-foundation-programming-reference.md)
-   [<span data-ttu-id="77b98-235">Технологии Microsoft TV</span><span class="sxs-lookup"><span data-stu-id="77b98-235">Microsoft TV Technologies</span></span>](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-application-interface)
-   [<span data-ttu-id="77b98-236">OpenGL</span><span class="sxs-lookup"><span data-stu-id="77b98-236">OpenGL</span></span>](../opengl/opengl-reference.md)
-   [<span data-ttu-id="77b98-237">Конфигурация монитора</span><span class="sxs-lookup"><span data-stu-id="77b98-237">Monitor Configuration</span></span>](../monitor/monitor-configuration-reference.md)
-   [<span data-ttu-id="77b98-238">Несколько мониторов экрана</span><span class="sxs-lookup"><span data-stu-id="77b98-238">Multiple Display Monitors</span></span>](../gdi/multiple-display-monitors-reference.md)
-   [<span data-ttu-id="77b98-239">Получение изображений</span><span class="sxs-lookup"><span data-stu-id="77b98-239">Picture Acquisition</span></span>](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [<span data-ttu-id="77b98-240">Цветовая система Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-240">Windows Color System</span></span>](../wcs/reference.md)
-   [<span data-ttu-id="77b98-241">Компонент обработки изображений Windows (WIC)</span><span class="sxs-lookup"><span data-stu-id="77b98-241">Windows Imaging Component (WIC)</span></span>](../wic/-wic-codec-reference.md)
-   <span data-ttu-id="77b98-242">[Кодек аудио и видео Windows Media и DSP](/previous-versions//dd443208(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-242">[Windows Media Audio and Video Codec and DSP](/previous-versions//dd443208(v=vs.85))</span></span>
-   [<span data-ttu-id="77b98-243">Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="77b98-243">Windows Media Center</span></span>](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [<span data-ttu-id="77b98-244">Формат Windows Media</span><span class="sxs-lookup"><span data-stu-id="77b98-244">Windows Media Format</span></span>](../wmformat/programming-reference.md)
-   [<span data-ttu-id="77b98-245">Службы общего доступа к библиотеке Windows Media</span><span class="sxs-lookup"><span data-stu-id="77b98-245">Windows Media Library Sharing Services</span></span>](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal)
-   [<span data-ttu-id="77b98-246">Проигрыватель Windows Media</span><span class="sxs-lookup"><span data-stu-id="77b98-246">Windows Media Player</span></span>](../wmp/windows-media-player-object-model-reference.md)
-   <span data-ttu-id="77b98-247">[Службы Windows Media](/previous-versions/windows/desktop/dd893580(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-247">[Windows Media Services](/previous-versions/windows/desktop/dd893580(v=vs.85))</span></span>
-   [<span data-ttu-id="77b98-248">Windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="77b98-248">Windows Movie Maker</span></span>](/previous-versions/windows/desktop/wmmdvdm/windows-movie-maker-apis)
-   [<span data-ttu-id="77b98-249">Мультимедиа Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-249">Windows Multimedia</span></span>](../multimedia/multimedia-reference.md)

## <a name="devices"></a><span data-ttu-id="77b98-250">Устройства</span><span class="sxs-lookup"><span data-stu-id="77b98-250">Devices</span></span>

-   [<span data-ttu-id="77b98-251">AllJoyn</span><span class="sxs-lookup"><span data-stu-id="77b98-251">AllJoyn</span></span>](/previous-versions/windows/desktop/alljoyn/alljoyn-api-portal)
-   [<span data-ttu-id="77b98-252">Ресурсы для связи</span><span class="sxs-lookup"><span data-stu-id="77b98-252">Communications Resources</span></span>](../devio/communications-reference.md)
-   [<span data-ttu-id="77b98-253">Доступ устройств</span><span class="sxs-lookup"><span data-stu-id="77b98-253">Device Access</span></span>](/previous-versions/windows/desktop/deviceaccess/device-access-api-c---programming-reference)
-   [<span data-ttu-id="77b98-254">Управление устройствами</span><span class="sxs-lookup"><span data-stu-id="77b98-254">Device Management</span></span>](../devio/device-management-reference.md)
-   [<span data-ttu-id="77b98-255">Enhanced Storage;</span><span class="sxs-lookup"><span data-stu-id="77b98-255">Enhanced Storage</span></span>](/previous-versions/windows/desktop/enstor/enhanced-storage-reference)
-   [<span data-ttu-id="77b98-256">Обнаружение функций</span><span class="sxs-lookup"><span data-stu-id="77b98-256">Function Discovery</span></span>](/previous-versions/windows/desktop/fundisc/function-discovery-reference)
-   [<span data-ttu-id="77b98-257">Основное изображение</span><span class="sxs-lookup"><span data-stu-id="77b98-257">Image Mastering</span></span>](../imapi/imapi-reference.md)
-   [<span data-ttu-id="77b98-258">Расположение</span><span class="sxs-lookup"><span data-stu-id="77b98-258">Location</span></span>](../locationapi/windows-location-programming-reference.md)
-   [<span data-ttu-id="77b98-259">База данных сопоставления PnP-X</span><span class="sxs-lookup"><span data-stu-id="77b98-259">PnP-X Association Database</span></span>](/previous-versions/windows/desktop/fundisc/pnp-x-association-database-reference)
-   [<span data-ttu-id="77b98-260">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="77b98-260">Printing</span></span>](/windows-hardware/drivers/print/introduction-to-printing)
    -   [<span data-ttu-id="77b98-261">Очередь печати принтера</span><span class="sxs-lookup"><span data-stu-id="77b98-261">Print Spooler</span></span>](../printdocs/printing-and-print-spooler-reference.md)
    -   [<span data-ttu-id="77b98-262">Печать пакета документа</span><span class="sxs-lookup"><span data-stu-id="77b98-262">Print Document Package</span></span>](../printdocs/tailored-app-printing-api.md)
    -   [<span data-ttu-id="77b98-263">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="77b98-263">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
    -   [<span data-ttu-id="77b98-264">Билет на печать</span><span class="sxs-lookup"><span data-stu-id="77b98-264">Print Ticket</span></span>](../printdocs/print-ticket-api.md)
    -   [<span data-ttu-id="77b98-265">Печать XPS</span><span class="sxs-lookup"><span data-stu-id="77b98-265">XPS Print</span></span>](../printdocs/xpsprint-api.md)
-   [<span data-ttu-id="77b98-266">Датчики</span><span class="sxs-lookup"><span data-stu-id="77b98-266">Sensors</span></span>](../sensorsapi/sensor-api-programming-reference.md)
-   [<span data-ttu-id="77b98-267">Служба уведомлений о системных событиях (Сенс)</span><span class="sxs-lookup"><span data-stu-id="77b98-267">System Event Notification Service (SENS)</span></span>](../sens/sens-reference.md)
-   [<span data-ttu-id="77b98-268">Справка по инструментам</span><span class="sxs-lookup"><span data-stu-id="77b98-268">Tool Help</span></span>](../toolhelp/tool-help-reference.md)
-   [<span data-ttu-id="77b98-269">UPnP</span><span class="sxs-lookup"><span data-stu-id="77b98-269">UPnP</span></span>](../upnp/universal-plug-and-play-start-page.md)
-   [<span data-ttu-id="77b98-270">Веб-службы на устройствах</span><span class="sxs-lookup"><span data-stu-id="77b98-270">Web Services on Devices</span></span>](../wsdapi/web-services-for-devices-reference.md)
-   [<span data-ttu-id="77b98-271">Служба загрузки изображений (WIA)</span><span class="sxs-lookup"><span data-stu-id="77b98-271">Windows Image Acquisition (WIA)</span></span>](../wia/-wia-reference.md)
-   [<span data-ttu-id="77b98-272">диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="77b98-272">Windows Media Device Manager</span></span>](../wmdm/programming-reference.md)
-   [<span data-ttu-id="77b98-273">Портативные устройства Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-273">Windows Portable Devices</span></span>](../wpd_sdk/programming-reference.md)

## <a name="system-services"></a><span data-ttu-id="77b98-274">Системные службы</span><span class="sxs-lookup"><span data-stu-id="77b98-274">System services</span></span>

<span data-ttu-id="77b98-275">Интерфейсы API [системных служб](/previous-versions//aa969179(v=vs.85)) предоставляют приложениям доступ к ресурсам компьютера и функциям базовой операционной системы, таким как память, файловые системы, устройства, процессы и потоки.</span><span class="sxs-lookup"><span data-stu-id="77b98-275">The [System Services](/previous-versions//aa969179(v=vs.85)) APIs give applications access to the resources of the computer and the features of the underlying operating system, such as memory, file systems, devices, processes, and threads.</span></span>

-   [<span data-ttu-id="77b98-276">COM</span><span class="sxs-lookup"><span data-stu-id="77b98-276">COM</span></span>](../com/reference.md)
-   [<span data-ttu-id="77b98-277">COM</span><span class="sxs-lookup"><span data-stu-id="77b98-277">COM+</span></span>](../cossdk/com--reference.md)
-   [<span data-ttu-id="77b98-278">API сжатия</span><span class="sxs-lookup"><span data-stu-id="77b98-278">Compression API</span></span>](../cmpapi/-compression-portal.md)
-   <span data-ttu-id="77b98-279">[Координатор распределенных транзакций (DTC)](/previous-versions/windows/desktop/ms686108(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-279">[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms686108(v=vs.85))</span></span>
-   [<span data-ttu-id="77b98-280">Библиотеки динамической компоновки (DLL)</span><span class="sxs-lookup"><span data-stu-id="77b98-280">Dynamic-Link Libraries (DLLs)</span></span>](../dlls/dynamic-link-library-functions.md)
-   [<span data-ttu-id="77b98-281">API справки</span><span class="sxs-lookup"><span data-stu-id="77b98-281">Help API</span></span>](/previous-versions/windows/desktop/helpapi/help-api-reference)
-   <span data-ttu-id="77b98-282">[Обмен данными между процессами](../ipc/interprocess-communications.md):</span><span class="sxs-lookup"><span data-stu-id="77b98-282">[Interprocess Communications](../ipc/interprocess-communications.md):</span></span>
    -   [<span data-ttu-id="77b98-283">маилслотс</span><span class="sxs-lookup"><span data-stu-id="77b98-283">Mailslots</span></span>](../ipc/mailslot-functions.md)
    -   [<span data-ttu-id="77b98-284">Каналы</span><span class="sxs-lookup"><span data-stu-id="77b98-284">Pipes</span></span>](../ipc/pipe-functions.md)
-   [<span data-ttu-id="77b98-285">Диспетчер транзакций ядра (KTM)</span><span class="sxs-lookup"><span data-stu-id="77b98-285">Kernel Transaction Manager (KTM)</span></span>](../ktm/ktm-reference.md)
-   [<span data-ttu-id="77b98-286">Управление памятью</span><span class="sxs-lookup"><span data-stu-id="77b98-286">Memory Management</span></span>](../memory/memory-management-reference.md)
-   [<span data-ttu-id="77b98-287">Записывающая операция</span><span class="sxs-lookup"><span data-stu-id="77b98-287">Operation Recorder</span></span>](/previous-versions/windows/desktop/oprec/-operation-portal)
-   [<span data-ttu-id="77b98-288">Управление питанием</span><span class="sxs-lookup"><span data-stu-id="77b98-288">Power Management</span></span>](../power/power-management-reference.md)
-   [<span data-ttu-id="77b98-289">Службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="77b98-289">Remote Desktop Services</span></span>](../termserv/terminal-services-reference.md)
-   [<span data-ttu-id="77b98-290">Процессы</span><span class="sxs-lookup"><span data-stu-id="77b98-290">Processes</span></span>](../procthread/process-and-thread-reference.md)
-   [<span data-ttu-id="77b98-291">Службы</span><span class="sxs-lookup"><span data-stu-id="77b98-291">Services</span></span>](../services/service-reference.md)
-   [<span data-ttu-id="77b98-292">Синхронизация</span><span class="sxs-lookup"><span data-stu-id="77b98-292">Synchronization</span></span>](../sync/synchronization-reference.md)
-   [<span data-ttu-id="77b98-293">Потоки</span><span class="sxs-lookup"><span data-stu-id="77b98-293">Threads</span></span>](../procthread/process-and-thread-reference.md)
-   [<span data-ttu-id="77b98-294">Общий доступ к рабочему столу Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-294">Windows Desktop Sharing</span></span>](/previous-versions/windows/desktop/rdp/windows-desktop-sharing-reference)
-   [<span data-ttu-id="77b98-295">Сведения о системе Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-295">Windows System Information</span></span>](../sysinfo/windows-system-information.md)
    -   [<span data-ttu-id="77b98-296">Handle и Objects</span><span class="sxs-lookup"><span data-stu-id="77b98-296">Handle and Objects</span></span>](../sysinfo/handle-and-object-functions.md)
    -   [<span data-ttu-id="77b98-297">Реестр</span><span class="sxs-lookup"><span data-stu-id="77b98-297">Registry</span></span>](../sysinfo/registry-reference.md)
    -   [<span data-ttu-id="77b98-298">Time</span><span class="sxs-lookup"><span data-stu-id="77b98-298">Time</span></span>](../sysinfo/time-reference.md)
    -   [<span data-ttu-id="77b98-299">Поставщик времени</span><span class="sxs-lookup"><span data-stu-id="77b98-299">Time Provider</span></span>](../sysinfo/time-provider-reference.md)

## <a name="security-and-identity"></a><span data-ttu-id="77b98-300">Безопасность и идентификация</span><span class="sxs-lookup"><span data-stu-id="77b98-300">Security and identity</span></span>

<span data-ttu-id="77b98-301">Интерфейсы API [безопасности и идентификации](../devnotes/security.md) обеспечивают проверку пароля при входе в систему, избирательную защиту для всех совместно используемый системных объектов, управление привилегированным доступом, управление правами и аудит безопасности.</span><span class="sxs-lookup"><span data-stu-id="77b98-301">The [Security and Identity](../devnotes/security.md) APIs enable password authentication at logon, discretionary protection for all sharable system objects, privileged access control, rights management, and security auditing.</span></span>

-   [<span data-ttu-id="77b98-302">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="77b98-302">Authentication</span></span>](../secauthn/authentication-reference.md)
-   [<span data-ttu-id="77b98-303">Авторизация</span><span class="sxs-lookup"><span data-stu-id="77b98-303">Authorization</span></span>](../secauthz/authorization-reference.md)
-   [<span data-ttu-id="77b98-304">Регистрация сертификата</span><span class="sxs-lookup"><span data-stu-id="77b98-304">Certificate Enrollment</span></span>](../seccertenroll/certificate-enrollment-api-reference.md)
-   [<span data-ttu-id="77b98-305">Шифрование</span><span class="sxs-lookup"><span data-stu-id="77b98-305">Cryptography</span></span>](../seccrypto/cryptography-reference.md)
-   [<span data-ttu-id="77b98-306">Криптографическое следующее поколение (CNG)</span><span class="sxs-lookup"><span data-stu-id="77b98-306">Cryptographic Next Generation (CNG)</span></span>](../seccng/cng-reference.md)
-   <span data-ttu-id="77b98-307">[Служба каталогов](/previous-versions//ms682458(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-307">[Directory Services](/previous-versions//ms682458(v=vs.85))</span></span>
    -   [<span data-ttu-id="77b98-308">Доменные службы Active Directory</span><span class="sxs-lookup"><span data-stu-id="77b98-308">Active Directory Domain Services</span></span>](../ad/active-directory-domain-services-reference.md)
    -   [<span data-ttu-id="77b98-309">Интерфейсы служб Active Directory (ADSI)</span><span class="sxs-lookup"><span data-stu-id="77b98-309">Active Directory Service Interfaces (ADSI)</span></span>](../adsi/adsi-reference.md)
-   [<span data-ttu-id="77b98-310">Протокол расширенной проверки подлинности (EAP)</span><span class="sxs-lookup"><span data-stu-id="77b98-310">Extensible Authentication Protocol (EAP)</span></span>](../eap/extensible-authentication-protocol-reference.md)
-   [<span data-ttu-id="77b98-311">Узел протокола расширенной проверки подлинности (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="77b98-311">Extensible Authentication Protocol Host (EAPHost)</span></span>](../eaphost/about-eap-host.md)
-   [<span data-ttu-id="77b98-312">Управление паролями MS-CHAP</span><span class="sxs-lookup"><span data-stu-id="77b98-312">MS-CHAP Password Management</span></span>](/previous-versions/windows/desktop/mschap/ms-chap-password-management-reference)
-   [<span data-ttu-id="77b98-313">Защита доступа к сети (NAP)</span><span class="sxs-lookup"><span data-stu-id="77b98-313">Network Access Protection (NAP)</span></span>](../nap/nap-reference.md)
-   [<span data-ttu-id="77b98-314">Расширения сервера политики сети (NPS)</span><span class="sxs-lookup"><span data-stu-id="77b98-314">Network Policy Server Extensions (NPS)</span></span>](../nps/ias-internet-authentication-service-reference.md)
-   [<span data-ttu-id="77b98-315">Родительский контроль</span><span class="sxs-lookup"><span data-stu-id="77b98-315">Parental Controls</span></span>](../parcon/parental-controls-reference.md)
-   [<span data-ttu-id="77b98-316">Поставщики WMI для системы безопасности</span><span class="sxs-lookup"><span data-stu-id="77b98-316">Security WMI Providers</span></span>](../secprov/security-wmi-providers-reference.md)
-   [<span data-ttu-id="77b98-317">Базовые службы TPM (TBS)</span><span class="sxs-lookup"><span data-stu-id="77b98-317">TPM Base Services (TBS)</span></span>](../tbs/tbs-reference.md)
-   [<span data-ttu-id="77b98-318">Биометрическая платформа Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-318">Windows Biometric Framework</span></span>](../secbiomet/biometric-service-api-reference.md)

## <a name="application-installation-and-servicing"></a><span data-ttu-id="77b98-319">Установка и обслуживание приложения</span><span class="sxs-lookup"><span data-stu-id="77b98-319">Application installation and servicing</span></span>

-   <span data-ttu-id="77b98-320">[Обозреватель игр](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-320">[Games Explorer](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))</span></span>
-   [<span data-ttu-id="77b98-321">Параллельные сборки</span><span class="sxs-lookup"><span data-stu-id="77b98-321">Side-by-side Assemblies</span></span>](../sbscs/side-by-side-assemblies-reference.md)
-   [<span data-ttu-id="77b98-322">Интерфейсы API упаковки, развертывания и запросов</span><span class="sxs-lookup"><span data-stu-id="77b98-322">Packaging, deployment, and query APIs</span></span>](../appxpkg/api-reference.md
)
-   [<span data-ttu-id="77b98-323">Лицензия разработчика</span><span class="sxs-lookup"><span data-stu-id="77b98-323">Developer License</span></span>](../devlic/developer-license-apis.md)
-   [<span data-ttu-id="77b98-324">Диспетчер перезапуска</span><span class="sxs-lookup"><span data-stu-id="77b98-324">Restart Manager</span></span>](../rstmgr/restart-manager-reference.md)
-   [<span data-ttu-id="77b98-325">Установщик Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-325">Windows Installer</span></span>](../msi/windows-installer-portal.md)

## <a name="system-admin-and-management"></a><span data-ttu-id="77b98-326">Системный администратор и управление</span><span class="sxs-lookup"><span data-stu-id="77b98-326">System admin and management</span></span>

<span data-ttu-id="77b98-327">Интерфейсы [системного администрирования](../srvnodes/system-administration.md) позволяют устанавливать, настраивать и обслуживать приложения или системы.</span><span class="sxs-lookup"><span data-stu-id="77b98-327">The [System administration](../srvnodes/system-administration.md) interfaces enable you to install, configure, and service applications or systems.</span></span>

-   [<span data-ttu-id="77b98-328">Поставщик WMI данные конфигурации загрузки</span><span class="sxs-lookup"><span data-stu-id="77b98-328">Boot Configuration Data WMI Provider</span></span>](/previous-versions/windows/desktop/bcd/bcd-reference)
-   [<span data-ttu-id="77b98-329">отказоустойчивые кластеры</span><span class="sxs-lookup"><span data-stu-id="77b98-329">Failover Clusters</span></span>](/previous-versions/windows/desktop/mscs/failover-cluster-apis-portal)
-   [<span data-ttu-id="77b98-330">Диспетчер ресурсов файлового сервера</span><span class="sxs-lookup"><span data-stu-id="77b98-330">File Server Resource Manager (FSRM)</span></span>](/previous-versions/windows/desktop/fsrm/fsrm-reference)
-   [<span data-ttu-id="77b98-331">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="77b98-331">Group Policy</span></span>](/previous-versions/windows/desktop/Policy/group-policy-reference)
-   [<span data-ttu-id="77b98-332">Консоль управления Microsoft (MMC) 2,0</span><span class="sxs-lookup"><span data-stu-id="77b98-332">Microsoft Management Console (MMC) 2.0</span></span>](/previous-versions/windows/desktop/mmc/mmc-reference)
-   [<span data-ttu-id="77b98-333">NetShell</span><span class="sxs-lookup"><span data-stu-id="77b98-333">NetShell</span></span>](/previous-versions/windows/desktop/netshell/netshell-reference)
-   [<span data-ttu-id="77b98-334">Инфраструктура управления параметрами</span><span class="sxs-lookup"><span data-stu-id="77b98-334">Settings Management Infrastructure</span></span>](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [<span data-ttu-id="77b98-335">Ведение журнала инвентаризации программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="77b98-335">Software Inventory Logging</span></span>](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
-   [<span data-ttu-id="77b98-336">Лицензирование ПО</span><span class="sxs-lookup"><span data-stu-id="77b98-336">Software Licensing</span></span>](/previous-versions/windows/desktop/secslapi/software-licensing-api-reference)
-   [<span data-ttu-id="77b98-337">Диспетчер перезапуска</span><span class="sxs-lookup"><span data-stu-id="77b98-337">Restart Manager</span></span>](../rstmgr/restart-manager-portal.md)
-   [<span data-ttu-id="77b98-338">Инфраструктура управления параметрами</span><span class="sxs-lookup"><span data-stu-id="77b98-338">Settings Management Infrastructure</span></span>](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [<span data-ttu-id="77b98-339">"Восстановление системы"</span><span class="sxs-lookup"><span data-stu-id="77b98-339">System Restore</span></span>](../sr/system-restore-portal.md)
-   [<span data-ttu-id="77b98-340">Завершение работы системы</span><span class="sxs-lookup"><span data-stu-id="77b98-340">System Shutdown</span></span>](../shutdown/system-shutdown.md)
-   [<span data-ttu-id="77b98-341">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="77b98-341">Task Scheduler</span></span>](../taskschd/task-scheduler-start-page.md)
-   [<span data-ttu-id="77b98-342">Ведение журнала доступа пользователей</span><span class="sxs-lookup"><span data-stu-id="77b98-342">User Access Logging</span></span>](/previous-versions/windows/desktop/ual/user-access-logging-reference)
-   [<span data-ttu-id="77b98-343">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="77b98-343">Windows Virtual PC</span></span>](../vpc/virtual-pc-reference.md)
-   [<span data-ttu-id="77b98-344">Microsoft Virtual Server</span><span class="sxs-lookup"><span data-stu-id="77b98-344">Microsoft Virtual Server</span></span>](/previous-versions/windows/desktop/msvs/microsoft-virtual-server-reference)
-   [<span data-ttu-id="77b98-345">Поставщик балансировки сетевой нагрузки</span><span class="sxs-lookup"><span data-stu-id="77b98-345">Network Load Balancing Provider</span></span>](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-reference)
-   [<span data-ttu-id="77b98-346">WMI в Защитнике Windows версии 2</span><span class="sxs-lookup"><span data-stu-id="77b98-346">Windows Defender WMI v2</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
-   [<span data-ttu-id="77b98-347">Windows Deployment Services</span><span class="sxs-lookup"><span data-stu-id="77b98-347">Windows Deployment Services</span></span>](../wds/windows-deployment-services-portal.md)
-   [<span data-ttu-id="77b98-348">Подлинное преимущество Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-348">Windows Genuine Advantage</span></span>](/previous-versions/windows/desktop/wingen/windows-genuine-advantage-api-functions)
-   [<span data-ttu-id="77b98-349">Инфраструктура управления Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-349">Windows Management Infrastructure</span></span>](/previous-versions/windows/desktop/wmi_v2/wmi-reference)
-   [<span data-ttu-id="77b98-350">Инструментарий управления Windows (WMI)</span><span class="sxs-lookup"><span data-stu-id="77b98-350">Windows Management Instrumentation (WMI)</span></span>](../wmisdk/wmi-reference.md)
-   [<span data-ttu-id="77b98-351">Удаленное управление Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-351">Windows Remote Management</span></span>](../winrm/portal.md)
-   [<span data-ttu-id="77b98-352">защита ресурсов Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-352">Windows Resource Protection</span></span>](../wfp/windows-resource-protection-portal.md)
-   <span data-ttu-id="77b98-353">[Службы Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-353">[Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))</span></span>
-   [<span data-ttu-id="77b98-354">Средство оценки системы Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-354">Windows System Assessment Tool</span></span>](../winsat/winsat-reference.md)
-   [<span data-ttu-id="77b98-355">Агент обновления Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-355">Windows Update Agent</span></span>](../wua_sdk/portal-client.md)

## <a name="networking-and-internet"></a><span data-ttu-id="77b98-356">Сетевые подключения и Интернет</span><span class="sxs-lookup"><span data-stu-id="77b98-356">Networking and internet</span></span>

<span data-ttu-id="77b98-357">[Сетевые](../devnotes/networking.md) интерфейсы API обеспечивают взаимодействие между приложениями по сети.</span><span class="sxs-lookup"><span data-stu-id="77b98-357">The [Networking](../devnotes/networking.md) APIs enable communication between applications over a network.</span></span> <span data-ttu-id="77b98-358">Вы также можете создавать и администрировать доступ к общим ресурсам, таким как каталоги и сетевые принтеры.</span><span class="sxs-lookup"><span data-stu-id="77b98-358">You can also create and manage access to shared resources, such as directories and network printers.</span></span>

-   <span data-ttu-id="77b98-359">[Domain Name System (DNS)](../dns/dns-reference.md) (Служба доменных имен (DNS))</span><span class="sxs-lookup"><span data-stu-id="77b98-359">[Domain Name System (DNS)](../dns/dns-reference.md)</span></span>
-   <span data-ttu-id="77b98-360">[Dynamic Host Configuration Protocol (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page) (Протокол DHCP)</span><span class="sxs-lookup"><span data-stu-id="77b98-360">[Dynamic Host Configuration Protocol (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)</span></span>
-   [<span data-ttu-id="77b98-361">Служба факсов</span><span class="sxs-lookup"><span data-stu-id="77b98-361">Fax Service</span></span>](/previous-versions/windows/desktop/fax/-mfax-fax-service-reference)
-   [<span data-ttu-id="77b98-362">Мастер новых подключений</span><span class="sxs-lookup"><span data-stu-id="77b98-362">Get Connected Wizard</span></span>](/previous-versions/windows/desktop/get_connected/get-connected-wizard-api-reference)
-   [<span data-ttu-id="77b98-363">HTTP-сервер</span><span class="sxs-lookup"><span data-stu-id="77b98-363">HTTP Server</span></span>](../http/http-server-api-reference.md)
-   [<span data-ttu-id="77b98-364">Общий доступ к подключению к Интернету и брандмауэр</span><span class="sxs-lookup"><span data-stu-id="77b98-364">Internet Connection Sharing and Firewall</span></span>](/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference)
-   [<span data-ttu-id="77b98-365">Вспомогательная служба IP</span><span class="sxs-lookup"><span data-stu-id="77b98-365">IP Helper</span></span>](../iphlp/ip-helper-function-reference.md)
-   [<span data-ttu-id="77b98-366">Брандмауэр подключения к Интернету IPv6</span><span class="sxs-lookup"><span data-stu-id="77b98-366">IPv6 Internet Connection Firewall</span></span>](/previous-versions/windows/desktop/ics/ipv6-firewall-configuration-reference)
-   [<span data-ttu-id="77b98-367">База сведений об управлении</span><span class="sxs-lookup"><span data-stu-id="77b98-367">Management Information Base</span></span>](/previous-versions/windows/desktop/mib/management-information-base-reference)
-   <span data-ttu-id="77b98-368">[Служба очередей сообщений (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-368">[Message Queuing (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))</span></span>
-   [<span data-ttu-id="77b98-369">Динамический протокол выделения клиентов (MADCAP) адреса многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="77b98-369">Multicast Address Dynamic Client Allocation Protocol (MADCAP)</span></span>](/previous-versions/windows/desktop/madcap/madcap-reference)
-   [<span data-ttu-id="77b98-370">Преобразование сетевых адресов (NAT)</span><span class="sxs-lookup"><span data-stu-id="77b98-370">Network Address Translation (NAT)</span></span>](/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference)
-   [<span data-ttu-id="77b98-371">Диспетчер списка сетей (NLM)</span><span class="sxs-lookup"><span data-stu-id="77b98-371">Network List Manager (NLM)</span></span>](../nla/network-list-manager-api-reference.md)
-   [<span data-ttu-id="77b98-372">Управление сетью</span><span class="sxs-lookup"><span data-stu-id="77b98-372">Network Management</span></span>](../netmgmt/network-management-reference.md)
-   [<span data-ttu-id="77b98-373">Управление сетевой общей папкой</span><span class="sxs-lookup"><span data-stu-id="77b98-373">Network Share Management</span></span>](../netshare/network-share-management-reference.md)
-   [<span data-ttu-id="77b98-374">Одноранговая сеть</span><span class="sxs-lookup"><span data-stu-id="77b98-374">Peer-to-Peer</span></span>](../p2psdk/portal.md)
-   [<span data-ttu-id="77b98-375">Качество обслуживания (QOS)</span><span class="sxs-lookup"><span data-stu-id="77b98-375">Quality of Service (QOS)</span></span>](/previous-versions/windows/desktop/qos/qos-reference)
-   [<span data-ttu-id="77b98-376">Удаленный вызов процедур</span><span class="sxs-lookup"><span data-stu-id="77b98-376">Remote Procedure Call</span></span>](../rpc/reference.md)
-   [<span data-ttu-id="77b98-377">Служба маршрутизации и удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="77b98-377">Routing and Remote Access Service (RAS)</span></span>](../rras/portal.md)
-   [<span data-ttu-id="77b98-378">Протокол SNMP</span><span class="sxs-lookup"><span data-stu-id="77b98-378">Simple Network Management Protocol (SNMP)</span></span>](../snmp/snmp-reference.md)
-   [<span data-ttu-id="77b98-379">Управление SMB</span><span class="sxs-lookup"><span data-stu-id="77b98-379">SMB Management</span></span>](/previous-versions/windows/desktop/smb/smb-management-api-portal)
-   [<span data-ttu-id="77b98-380">Интерфейсы программирования приложений телефонии (TAPI)</span><span class="sxs-lookup"><span data-stu-id="77b98-380">Telephony Application Programming Interfaces (TAPI)</span></span>](../tapi/telephony-application-programming-interfaces.md)
-   [<span data-ttu-id="77b98-381">WebDAV</span><span class="sxs-lookup"><span data-stu-id="77b98-381">WebDAV</span></span>](../webdav/webdav-api-reference.md)
-   [<span data-ttu-id="77b98-382">Компонент протокола WebSocket</span><span class="sxs-lookup"><span data-stu-id="77b98-382">WebSocket Protocol Component</span></span>](../websock/web-socket-protocol-component-api-portal.md)
-   <span data-ttu-id="77b98-383">Беспроводные сети:</span><span class="sxs-lookup"><span data-stu-id="77b98-383">Wireless networking:</span></span>
    -   [<span data-ttu-id="77b98-384">Bluetooth</span><span class="sxs-lookup"><span data-stu-id="77b98-384">Bluetooth</span></span>](../bluetooth/bluetooth-reference.md)
    -   [<span data-ttu-id="77b98-385">IrDA</span><span class="sxs-lookup"><span data-stu-id="77b98-385">IrDA</span></span>](/previous-versions/windows/desktop/irda/irda-and-windows-sockets-reference)
    -   [<span data-ttu-id="77b98-386">Мобильное широкополосное подключение</span><span class="sxs-lookup"><span data-stu-id="77b98-386">Mobile Broadband</span></span>](../mbn/mobile-broadband-networks-api-reference.md)
    -   [<span data-ttu-id="77b98-387">Встроенный WiFi</span><span class="sxs-lookup"><span data-stu-id="77b98-387">Native Wifi</span></span>](../nativewifi/native-wifi-reference.md)
    -   [<span data-ttu-id="77b98-388">Windows Connect Now</span><span class="sxs-lookup"><span data-stu-id="77b98-388">Windows Connect Now</span></span>](../wcn/windows-connect-now-reference.md)
    -   [<span data-ttu-id="77b98-389">Диспетчер подключений Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-389">Windows Connection Manager</span></span>](../wcm/windows-connection-manager-reference.md)
-   [<span data-ttu-id="77b98-390">Платформа фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-390">Windows Filtering Platform</span></span>](../fwp/fwp-reference.md)
-   [<span data-ttu-id="77b98-391">Брандмауэр Windows в режиме повышенной безопасности</span><span class="sxs-lookup"><span data-stu-id="77b98-391">Windows Firewall with Advanced Security</span></span>](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference)
-   [<span data-ttu-id="77b98-392">Службы HTTP Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="77b98-392">Windows HTTP Services (WinHTTP)</span></span>](../winhttp/winhttp-reference.md)
-   [<span data-ttu-id="77b98-393">Windows Internet (WinINet)</span><span class="sxs-lookup"><span data-stu-id="77b98-393">Windows Internet (WinINet)</span></span>](../wininet/wininet-reference.md)
-   [<span data-ttu-id="77b98-394">Сеть Windows (Внет)</span><span class="sxs-lookup"><span data-stu-id="77b98-394">Windows Networking (WNet)</span></span>](../wnet/windows-networking-reference.md)
-   [<span data-ttu-id="77b98-395">Виртуализация сети Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-395">Windows Network Virtualization</span></span>](/previous-versions/windows/desktop/wnv/windows-network-virtualization-portal)
-   <span data-ttu-id="77b98-396">[Платформа Windows RSS](/previous-versions/windows/desktop/ms684702(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-396">[Windows RSS Platform](/previous-versions/windows/desktop/ms684702(v=vs.85))</span></span>
-   [<span data-ttu-id="77b98-397">Сокеты Windows (Winsock)</span><span class="sxs-lookup"><span data-stu-id="77b98-397">Windows Sockets (Winsock)</span></span>](../winsock/winsock-reference.md)
-   [<span data-ttu-id="77b98-398">Веб-службы Windows</span><span class="sxs-lookup"><span data-stu-id="77b98-398">Windows Web Services</span></span>](../wsw/windows-web-services-reference.md)
-   [<span data-ttu-id="77b98-399">Расширенный запрос XML HTTP</span><span class="sxs-lookup"><span data-stu-id="77b98-399">XML HTTP Extended Request</span></span>](/previous-versions/windows/desktop/ixhr2/ixmlhttprequest2-portal)

## <a name="deprecated-or-legacy-apis"></a><span data-ttu-id="77b98-400">Устаревшие или устаревшие API</span><span class="sxs-lookup"><span data-stu-id="77b98-400">Deprecated or legacy APIs</span></span>

<span data-ttu-id="77b98-401">Ниже перечислены технологии и интерфейсы API, устаревшие или замененные или устаревшие из клиентских и серверных операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="77b98-401">The following are technologies and APIs that are outdated or have been replaced or deprecated from the Windows client and server operating systems.</span></span>

-   <span data-ttu-id="77b98-402">[DirectMusic](/previous-versions/ms807133(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="77b98-402">[DirectMusic](/previous-versions/ms807133(v=msdn.10))</span></span>
-   <span data-ttu-id="77b98-403">[Звука](/previous-versions/windows/desktop/ee416975(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-403">[DirectSound](/previous-versions/windows/desktop/ee416975(v=vs.85))</span></span>
-   <span data-ttu-id="77b98-404">[Пакет Microsoft UDDI SDK](/previous-versions/windows/desktop/aa966237(v=bts.10)) теперь входит в состав [Microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="77b98-404">[Microsoft UDDI SDK](/previous-versions/windows/desktop/aa966237(v=bts.10)) is now included with [Microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10)).</span></span>
-   [<span data-ttu-id="77b98-405">Сетевой платформа динамических данных Exchange (DDE)</span><span class="sxs-lookup"><span data-stu-id="77b98-405">Network Dynamic Data Exchange (DDE)</span></span>](../ipc/network-dde-reference.md)
-   <span data-ttu-id="77b98-406">[Служба удаленной установки](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10)). вместо этого используйте [службы развертывания Windows](../wds/windows-deployment-services-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="77b98-406">[Remote Installation Service](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10)): Use [Windows Deployment Services](../wds/windows-deployment-services-portal.md) instead.</span></span>
-   <span data-ttu-id="77b98-407">[Служба виртуальных дисков (VDS)](../vds/vds-reference.md). вместо этого используйте [Управление хранилищем Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal) .</span><span class="sxs-lookup"><span data-stu-id="77b98-407">[Virtual Disk Service (VDS)](../vds/vds-reference.md): Use [Windows Storage Management](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal) instead.</span></span>
-   <span data-ttu-id="77b98-408">Службы терминалов. Используйте [службы удаленных рабочих столов](../termserv/terminal-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="77b98-408">Terminal Services: Use [Remote Desktop Services](../termserv/terminal-services-reference.md).</span></span>
-   <span data-ttu-id="77b98-409">[Диспетчер прав Windows Media](/previous-versions//bb614742(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77b98-409">[Windows Media Rights Manager](/previous-versions//bb614742(v=vs.85))</span></span>
-   <span data-ttu-id="77b98-410">[Windows Messaging (MAPI)](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi). вместо этого используйте [Office MAPI](/previous-versions/office/developer/office-2007/cc765775(v=office.12)) .</span><span class="sxs-lookup"><span data-stu-id="77b98-410">[Windows Messaging (MAPI)](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi): Use [Office MAPI](/previous-versions/office/developer/office-2007/cc765775(v=office.12)) instead.</span></span>
-   <span data-ttu-id="77b98-411">[Платформа мини-приложений Windows](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal). вместо этого создайте приложения UWP.</span><span class="sxs-lookup"><span data-stu-id="77b98-411">[Windows Gadget Platform](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal): Create UWP apps instead.</span></span>
-   <span data-ttu-id="77b98-412">[Боковая панель Windows](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry): вместо этого создайте приложения UWP.</span><span class="sxs-lookup"><span data-stu-id="77b98-412">[Windows Sidebar](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry): Create UWP apps instead.</span></span>
-   <span data-ttu-id="77b98-413">[Windows SideShow](/previous-versions//ms744179(v=vs.85)): нет замены.</span><span class="sxs-lookup"><span data-stu-id="77b98-413">[Windows SideShow](/previous-versions//ms744179(v=vs.85)): No replacement.</span></span>
-   [<span data-ttu-id="77b98-414">Растровые эффекты WPF</span><span class="sxs-lookup"><span data-stu-id="77b98-414">WPF Bitmap Effects</span></span>](/previous-versions/windows/desktop/wibe/-wibe-about-bitmapeffects)
