---
description: Контролевентс аналогичны сообщениям Microsoft Windows в приложениях на основе Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Обзор таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913083"
---
# <a name="controlevent-overview"></a><span data-ttu-id="356f6-103">Обзор таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-103">ControlEvent Overview</span></span>

<span data-ttu-id="356f6-104">Контролевентс аналогичны сообщениям Microsoft Windows в приложениях на основе Win32.</span><span class="sxs-lookup"><span data-stu-id="356f6-104">ControlEvents are analogous to Microsoft Windows messages in Win32-based applications.</span></span> <span data-ttu-id="356f6-105">Однако вместо того, чтобы создавать функцию обратного вызова для получения сообщений Windows и отправки сообщений Windows с помощью функции [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) , установщик пользовательского интерфейса и элементы управления публикуют [контролевентс](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="356f6-105">However, rather than creating a callback function to receive Windows messages and sending Windows messages with the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function, the user interface (UI) installer and controls publish [ControlEvents](control-events.md).</span></span> <span data-ttu-id="356f6-106">Другие элементы управления и установщик можно указать для подписки на определенные Контролевентс, которые затем будут изменять атрибуты элемента управления подписки.</span><span class="sxs-lookup"><span data-stu-id="356f6-106">Other controls and the installer can be specified to subscribe to particular ControlEvents that will then change attributes of the subscribing control.</span></span> <span data-ttu-id="356f6-107">Чтобы добавить рабочие элементы управления в диалоговые окна, автор пользовательского интерфейса определяет публикацию Контролевентс в [таблице таблице ControlEvent событие](controlevent-table.md) и подписывает элементы управления в контролевентс в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="356f6-107">To add working controls to dialog boxes, the author of the UI specifies the publication of ControlEvents in the [ControlEvent table](controlevent-table.md) and subscribes controls to ControlEvents in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="356f6-108">Установщик опубликует следующие события для подписки на элементы управления, перечисленные в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="356f6-108">The installer will publish the following events to subscribing controls listed in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="356f6-109">[Элемент управления ProgressBar](progressbar-control.md) или [элемент управления "объявление](billboard-control.md) " обычно подписывается на сетпрогресс, а остальные подписываются [элементами управления "текст](text-control.md)".</span><span class="sxs-lookup"><span data-stu-id="356f6-109">A [ProgressBar control](progressbar-control.md) or [Billboard control](billboard-control.md) typically subscribes to SetProgress, the rest are subscribed to by [Text controls](text-control.md).</span></span>

[<span data-ttu-id="356f6-110">Актиондата таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-110">ActionData ControlEvent</span></span>](actiondata-controlevent.md)

[<span data-ttu-id="356f6-111">Актионтекст таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-111">ActionText ControlEvent</span></span>](actiontext-controlevent.md)

[<span data-ttu-id="356f6-112">Сетпрогресс таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-112">SetProgress ControlEvent</span></span>](setprogress-controlevent.md)

[<span data-ttu-id="356f6-113">TimeRemaining таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-113">TimeRemaining ControlEvent</span></span>](timeremaining-controlevent.md)

[<span data-ttu-id="356f6-114">Скриптинпрогресс таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-114">ScriptInProgress ControlEvent</span></span>](scriptinprogress-controlevent.md)

<span data-ttu-id="356f6-115">Следующие события публикуются элементом управления при перемещении выбора элементов в элемент управления [селектионтри](selectiontree-control.md) или [директорилист](directorylist-control.md).</span><span class="sxs-lookup"><span data-stu-id="356f6-115">The following events are published by the control when the item selection is moved in a [SelectionTree control](selectiontree-control.md) or [DirectoryList Control](directorylist-control.md).</span></span> <span data-ttu-id="356f6-116">Элементы управления подписки должны находиться в одном и том же диалоговом окне и перечислены в таблице таблица eventmapping.</span><span class="sxs-lookup"><span data-stu-id="356f6-116">Subscribing controls must be located on the same dialog box and listed in the EventMapping table.</span></span>

[<span data-ttu-id="356f6-117">Игноречанже таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-117">IgnoreChange ControlEvent</span></span>](ignorechange-controlevent.md)

[<span data-ttu-id="356f6-118">Селектиондескриптион таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-118">SelectionDescription ControlEvent</span></span>](selectiondescription-controlevent.md)

[<span data-ttu-id="356f6-119">Селектионсизе таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-119">SelectionSize ControlEvent</span></span>](selectionsize-controlevent.md)

[<span data-ttu-id="356f6-120">Селектионпас таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-120">SelectionPath ControlEvent</span></span>](selectionpath-controlevent.md)

[<span data-ttu-id="356f6-121">Селектионактион таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-121">SelectionAction ControlEvent</span></span>](selectionaction-controlevent.md)

[<span data-ttu-id="356f6-122">Селектионноитемс таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-122">SelectionNoItems ControlEvent</span></span>](selectionnoitems-controlevent.md)

<span data-ttu-id="356f6-123">Следующие Контролевентс могут быть опубликованы по собственному усмотрению пользователя путем взаимодействия с [элементом управления "кнопка](pushbutton-control.md) " или ["флажок](checkbox-control.md) " в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="356f6-123">The following ControlEvents can be published at the discretion of a user by interacting with a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) on a dialog box.</span></span> <span data-ttu-id="356f6-124">Элемент управления CheckBox может публиковать только события AddLocal, Аддсаурце, Remove, DoAction и SetProperty.</span><span class="sxs-lookup"><span data-stu-id="356f6-124">The Checkbox control can only publish the AddLocal, AddSource, Remove, DoAction, and SetProperty events.</span></span> <span data-ttu-id="356f6-125">С установщик Windows версиями, поставляемыми в составе Windows Server 2003 и более поздних версий, [элемент управления селектионтри](selectiontree-control.md) может публиковать DoAction, таблице ControlEvent событие и SetProperty контролевентс.</span><span class="sxs-lookup"><span data-stu-id="356f6-125">With Windows Installer versions that shipped with Windows Server 2003 and later, the [SelectionTree control](selectiontree-control.md) can publish the DoAction, ControlEvent and SetProperty ControlEvents.</span></span> <span data-ttu-id="356f6-126">Автор пользовательского интерфейса должен вывести список таблице ControlEvent событие в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="356f6-126">The author of the UI should list the ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="356f6-127">Обработчик пользовательского интерфейса установщика — это подписчик на эти события.</span><span class="sxs-lookup"><span data-stu-id="356f6-127">The UI handler of the installer is the subscriber to these events.</span></span>

[<span data-ttu-id="356f6-128">AddLocal таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-128">AddLocal ControlEvent</span></span>](addlocal-controlevent.md)

[<span data-ttu-id="356f6-129">Аддсаурце таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-129">AddSource ControlEvent</span></span>](addsource-controlevent.md)

[<span data-ttu-id="356f6-130">Чеккексистингтаржетпас таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-130">CheckExistingTargetPath ControlEvent</span></span>](checkexistingtargetpath-controlevent.md)

[<span data-ttu-id="356f6-131">Чекктаржетпас таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-131">CheckTargetPath ControlEvent</span></span>](checktargetpath-controlevent.md)

[<span data-ttu-id="356f6-132">DoAction таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-132">DoAction ControlEvent</span></span>](doaction-controlevent.md)

[<span data-ttu-id="356f6-133">Енаблероллбакк таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-133">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

[<span data-ttu-id="356f6-134">EndDialog таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-134">EndDialog ControlEvent</span></span>](enddialog-controlevent.md)

[<span data-ttu-id="356f6-135">Невдиалог таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-135">NewDialog ControlEvent</span></span>](newdialog-controlevent.md)

[<span data-ttu-id="356f6-136">Повторная установка таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-136">Reinstall ControlEvent</span></span>](reinstall-controlevent.md)

[<span data-ttu-id="356f6-137">ReinstallMode таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-137">ReinstallMode ControlEvent</span></span>](reinstallmode-controlevent.md)

[<span data-ttu-id="356f6-138">Удалить таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-138">Remove ControlEvent</span></span>](remove-controlevent.md)

[<span data-ttu-id="356f6-139">Сбросить таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-139">Reset ControlEvent</span></span>](reset-controlevent.md)

[<span data-ttu-id="356f6-140">Сетинсталллевел таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-140">SetInstallLevel ControlEvent</span></span>](setinstalllevel-controlevent.md)

[<span data-ttu-id="356f6-141">SetProperty таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-141">SetProperty ControlEvent</span></span>](setproperty-controlevent.md)

[<span data-ttu-id="356f6-142">Сеттаржетпас таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-142">SetTargetPath ControlEvent</span></span>](settargetpath-controlevent.md)

[<span data-ttu-id="356f6-143">Спавндиалог таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-143">SpawnDialog ControlEvent</span></span>](spawndialog-controlevent.md)

[<span data-ttu-id="356f6-144">Спавнваитдиалог таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-144">SpawnWaitDialog ControlEvent</span></span>](spawnwaitdialog-controlevent.md)

[<span data-ttu-id="356f6-145">Валидатепродуктид таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-145">ValidateProductID ControlEvent</span></span>](validateproductid-controlevent.md)

<span data-ttu-id="356f6-146">[Элемент управления "кнопка](pushbutton-control.md) " может публиковать следующие события в подписке [элемента управления селектионтри](selectiontree-control.md) или [элементе управления директорилист](directorylist-control.md) , расположенном в том же диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="356f6-146">A [PushButton control](pushbutton-control.md) can publish the following events to a subscribing [SelectionTree control](selectiontree-control.md) or [DirectoryList control](directorylist-control.md) located in the same dialog box.</span></span> <span data-ttu-id="356f6-147">Элемент управления "Кнопка" должен быть указан в таблице таблице ControlEvent событие, а элементы управления подписки должны присутствовать в таблице таблица eventmapping.</span><span class="sxs-lookup"><span data-stu-id="356f6-147">The PushButton Control should be listed in the ControlEvent table and the subscribing controls should be listed in the EventMapping table.</span></span>

[<span data-ttu-id="356f6-148">Селектионбровсе таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-148">SelectionBrowse ControlEvent</span></span>](selectionbrowse-controlevent.md)

[<span data-ttu-id="356f6-149">Директорилиступ таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-149">DirectoryListUp ControlEvent</span></span>](directorylistup-controlevent.md)

[<span data-ttu-id="356f6-150">Директорилистнев таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-150">DirectoryListNew ControlEvent</span></span>](directorylistnew-controlevent.md)

[<span data-ttu-id="356f6-151">Директорилистопен таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="356f6-151">DirectoryListOpen ControlEvent</span></span>](directorylistopen-controlevent.md)

<span data-ttu-id="356f6-152">Для событий элемента управления обычно требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="356f6-152">Control events generally require that the UI be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="356f6-153">Большинство Контролевентс не будут работать с [*меньшим пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md) пользователя, поскольку на этих уровнях отображаются только немодальные диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="356f6-153">Most ControlEvents will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md) because these levels only display modeless dialog boxes.</span></span> <span data-ttu-id="356f6-154">События Актионтекст, Аддсаурце, Сетпрогресс, TimeRemaining и Скриптинпрогресс являются исключениями и будут работать в сокращенном или базовом пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="356f6-154">The ActionText, AddSource, SetProgress, TimeRemaining, and ScriptInProgress events are exceptions and will work in reduced or basic UI.</span></span> <span data-ttu-id="356f6-155">Дополнительные сведения об уровнях ПОЛЬЗОВАТЕЛЬСКОГО интерфейса см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="356f6-155">For more information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="356f6-156">Для выполнения [настраиваемых действий](custom-actions.md) можно опубликовать таблице ControlEvent событие из [элемента управления "кнопка](pushbutton-control.md) [" или "флажок"](checkbox-control.md).</span><span class="sxs-lookup"><span data-stu-id="356f6-156">You can run [custom actions](custom-actions.md) by publishing a ControlEvent from a [PushButton control](pushbutton-control.md) or [Checkbox control](checkbox-control.md).</span></span> <span data-ttu-id="356f6-157">Добавьте запись в [таблицу таблице ControlEvent событие](controlevent-table.md) с именами диалогового окна и элементом управления, публикующий таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="356f6-157">Add a record to the [ControlEvent table](controlevent-table.md) with the names of the dialog and the control publishing the ControlEvent.</span></span> <span data-ttu-id="356f6-158">Этот элемент управления должен публиковать [DoAction таблице ControlEvent событие](doaction-controlevent.md) , уведомляя установщик о необходимости запуска настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="356f6-158">This control should publish a [DoAction ControlEvent](doaction-controlevent.md) notifying the installer to run the custom action.</span></span> <span data-ttu-id="356f6-159">В Windows XP или более ранних системах нельзя выполнить пользовательское действие путем публикации таблице ControlEvent событие из [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="356f6-159">On Windows XP or earlier systems, you cannot run a custom action by publishing a ControlEvent from a [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="356f6-160">Дополнительные сведения о конкретных Контролевентс см. в списке стандартных [контролевентс](control-events.md) в [справочнике по пользовательскому интерфейсу](user-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="356f6-160">For a more information about particular ControlEvents, see the list of standard [ControlEvents](control-events.md) in [User Interface Reference](user-interface-reference.md).</span></span>

 

 
