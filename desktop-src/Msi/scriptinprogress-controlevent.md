---
description: Установщик использует это событие для вывода информационной строки во время компиляции скрипта выполнения установки.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: Скриптинпрогресс таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650800"
---
# <a name="scriptinprogress-controlevent"></a><span data-ttu-id="aa0e7-103">Скриптинпрогресс таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="aa0e7-103">ScriptInProgress ControlEvent</span></span>

<span data-ttu-id="aa0e7-104">Установщик использует это событие для вывода информационной строки во время компиляции скрипта выполнения установки.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-104">The installer uses this event to display an informational string while the installation's execution script is being compiled.</span></span> <span data-ttu-id="aa0e7-105">Информационную строку можно отобразить в диалоговом окне с помощью [элемента управления "текст](text-control.md) ", который подписывается на этот таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-105">The informational string can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="aa0e7-106">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa0e7-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="aa0e7-107">Этот таблице ControlEvent событие может обрабатываться пользовательским интерфейсом, который работает на [*базовом интерфейсе*](b-gly.md), [*сокращенном пользовательском интерфейсе*](r-gly.md)или на [*всех уровнях пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="aa0e7-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="aa0e7-108">Сведения об уровнях ПОЛЬЗОВАТЕЛЬСКОГО интерфейса см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="aa0e7-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="aa0e7-109">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="aa0e7-109">Published By</span></span>

<span data-ttu-id="aa0e7-110">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="aa0e7-111">Аргумент</span><span class="sxs-lookup"><span data-stu-id="aa0e7-111">Argument</span></span>

<span data-ttu-id="aa0e7-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="aa0e7-113">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="aa0e7-113">Action on Subscribers</span></span>

<span data-ttu-id="aa0e7-114">[Элемент управления "текст](text-control.md) ", подписавшийся на скриптинпрогресс, будет отображать текстовую строку, указанную в [таблице уитекст](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa0e7-114">A [Text control](text-control.md) subscribing to ScriptInProgress will display text string specified in [UIText table](uitext-table.md).</span></span>

## <a name="typical-use"></a><span data-ttu-id="aa0e7-115">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="aa0e7-115">Typical Use</span></span>

<span data-ttu-id="aa0e7-116">Во время компиляции скрипта выполнения программа установки отображает ProgressBar, указывающий время, оставшееся до начала выполнения скрипта.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-116">While the execution script is being compiled, the installer displays a ProgressBar indicating the time remaining before the beginning of script execution.</span></span> <span data-ttu-id="aa0e7-117">Автор пакета может отобразить предварительное сообщение в это время, объясняющее элемент ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-117">The package author can display a preliminary message at this time explaining the ProgressBar.</span></span> <span data-ttu-id="aa0e7-118">Чтобы отобразить предварительное сообщение, включите [элемент управления "текст](text-control.md) " в то же немодальное диалоговое окно, что и ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-118">To display a preliminary message, include a [Text control](text-control.md) on the same modeless dialog box as the ProgressBar.</span></span> <span data-ttu-id="aa0e7-119">Укажите, что этот элемент управления "текст" подписывается на Скриптинпрогресс таблице ControlEvent событие через [таблицу таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa0e7-119">Specify that this Text control subscribe to the ScriptInProgress ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="aa0e7-120">Включите в [таблицу уитекст](uitext-table.md) запись с скриптинпрогресс, указанным в поле Key.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-120">Include an entry in the [UIText table](uitext-table.md) with ScriptInProgress specified in the Key field.</span></span> <span data-ttu-id="aa0e7-121">Укажите предварительное сообщение в виде текстовой строки в текстовом поле таблицы Уитекст.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-121">Specify the preliminary message as a text string in the Text field of the UIText table.</span></span> <span data-ttu-id="aa0e7-122">Затем во время компиляции сценария установщик отобразит эту строку в элементе управления Text.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-122">Then during script compilation, the installer will display this string within the text control.</span></span> <span data-ttu-id="aa0e7-123">Отображаемый текст исчезает сразу после завершения компиляции скрипта.</span><span class="sxs-lookup"><span data-stu-id="aa0e7-123">The displayed text disappears as soon as the script compilation is finished.</span></span>

<span data-ttu-id="aa0e7-124">Тот же элемент управления текстом, который подписывается на Скриптинпрогресс таблице ControlEvent событие, может также подписываться на [TimeRemaining таблице ControlEvent событие](timeremaining-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="aa0e7-124">The same text control that subscribes to the ScriptInProgress ControlEvent can also subscribe to the [TimeRemaining ControlEvent](timeremaining-controlevent.md).</span></span> <span data-ttu-id="aa0e7-125">В этом случае, как текст предварительной строки Скриптинпрогресс исчезает, он заменяется строкой "оставшееся время: XX минут".</span><span class="sxs-lookup"><span data-stu-id="aa0e7-125">In this case, as text of the preliminary ScriptInProgress string disappears, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



