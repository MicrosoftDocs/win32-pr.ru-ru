---
description: Спавнваитдиалог таблице ControlEvent событие активирует диалоговое окно, заданное в столбце Argument таблицы таблице ControlEvent событие, если выражение в столбце Condition имеет значение FALSE.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: Спавнваитдиалог таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991221"
---
# <a name="spawnwaitdialog-controlevent"></a><span data-ttu-id="85f46-103">Спавнваитдиалог таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="85f46-103">SpawnWaitDialog ControlEvent</span></span>

<span data-ttu-id="85f46-104">Спавнваитдиалог таблице ControlEvent событие активирует диалоговое окно, заданное в столбце Argument [таблицы таблице ControlEvent событие](controlevent-table.md), если выражение в столбце Condition имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="85f46-104">The SpawnWaitDialog ControlEvent triggers the dialog box specified by the Argument column of the [ControlEvent table](controlevent-table.md), if the expression in the Condition column evaluates as FALSE.</span></span> <span data-ttu-id="85f46-105">Диалоговое окно остается в состоянии до тех пор, пока условное выражение остается ЛОЖНЫм и удаляется сразу после вычисления условия TRUE.</span><span class="sxs-lookup"><span data-stu-id="85f46-105">The dialog box remains up for as long as the conditional expression remains FALSE and is removed as soon as the condition evaluates TRUE.</span></span>

<span data-ttu-id="85f46-106">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="85f46-106">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="85f46-107">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="85f46-107">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="85f46-108">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="85f46-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="85f46-109">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="85f46-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="85f46-110">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="85f46-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="85f46-111">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="85f46-111">Published By</span></span>

<span data-ttu-id="85f46-112">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="85f46-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="85f46-113">Аргумент</span><span class="sxs-lookup"><span data-stu-id="85f46-113">Argument</span></span>

<span data-ttu-id="85f46-114">Диалоговое окно в [таблице диалоговых окон](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="85f46-114">A dialog box in the [Dialog table](dialog-table.md).</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="85f46-115">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="85f46-115">Action on Subscribers</span></span>

<span data-ttu-id="85f46-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="85f46-116">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="85f46-117">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="85f46-117">Typical Use</span></span>

<span data-ttu-id="85f46-118">Спавнваитдиалог таблице ControlEvent событие можно использовать для ожидания любой фоновой задачи, которая может быть протестирована с помощью условного выражения, такого как состояние свойства.</span><span class="sxs-lookup"><span data-stu-id="85f46-118">The SpawnWaitDialog ControlEvent can be used to wait for any background task the completion of which can be tested using a conditional expression such as the state of a property.</span></span> <span data-ttu-id="85f46-119">Пример использования таблице ControlEvent событие Спавнваитдиалог см. в разделе [создание условного выражения "Подождите...". Окно сообщения](authoring-a-conditional-please-wait-------message-box.md).</span><span class="sxs-lookup"><span data-stu-id="85f46-119">For an example of using the SpawnWaitDialog ControlEvent, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

 

 



