---
description: Это событие уведомляет установщик о необходимости удаления модального диалогового окна. Во всех случаях установщик удаляет текущее диалоговое окно.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264853"
---
# <a name="enddialog-controlevent"></a><span data-ttu-id="982aa-104">EndDialog таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="982aa-104">EndDialog ControlEvent</span></span>

<span data-ttu-id="982aa-105">Это событие уведомляет установщик о необходимости удаления модального диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="982aa-105">This event notifies the installer to remove a modal dialog box.</span></span> <span data-ttu-id="982aa-106">Во всех случаях установщик удаляет текущее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="982aa-106">In all cases the installer removes the present dialog box.</span></span>

<span data-ttu-id="982aa-107">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="982aa-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="982aa-108">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="982aa-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="982aa-109">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="982aa-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="982aa-110">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="982aa-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="982aa-111">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="982aa-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="982aa-112">В следующей таблице перечислены действия события, возникающие в результате различных аргументов, вводимых в [таблицу таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="982aa-112">The following table lists the action of the event resulting from different arguments entered into the [ControlEvent table](controlevent-table.md).</span></span>



| <span data-ttu-id="982aa-113">Аргумент</span><span class="sxs-lookup"><span data-stu-id="982aa-113">Argument</span></span> | <span data-ttu-id="982aa-114">Действие установщика</span><span class="sxs-lookup"><span data-stu-id="982aa-114">Action by the installer</span></span>                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="982aa-115">Выход</span><span class="sxs-lookup"><span data-stu-id="982aa-115">Exit</span></span>     | <span data-ttu-id="982aa-116">Последовательность мастера закрывается, и элемент управления возвращается в установщик со значением Усерексит.</span><span class="sxs-lookup"><span data-stu-id="982aa-116">The wizard sequence is closed and the control returns to the installer with the UserExit value.</span></span> <span data-ttu-id="982aa-117">Этот аргумент нельзя использовать в диалоговом окне, который является дочерним для другого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="982aa-117">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="982aa-118">Повторить попытку</span><span class="sxs-lookup"><span data-stu-id="982aa-118">Retry</span></span>    | <span data-ttu-id="982aa-119">Последовательность мастера закрывается, и элемент управления возвращается в установщик со значением приостановки.</span><span class="sxs-lookup"><span data-stu-id="982aa-119">The wizard sequence is closed and the control returns to the installer with the Suspend value.</span></span> <span data-ttu-id="982aa-120">Этот аргумент нельзя использовать в диалоговом окне, который является дочерним для другого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="982aa-120">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span>  |
| <span data-ttu-id="982aa-121">Игнорировать</span><span class="sxs-lookup"><span data-stu-id="982aa-121">Ignore</span></span>   | <span data-ttu-id="982aa-122">Последовательность мастера закрывается, и элемент управления возвращается в установщик с завершенным значением.</span><span class="sxs-lookup"><span data-stu-id="982aa-122">The wizard sequence is closed and the control returns to the installer with the Finished value.</span></span> <span data-ttu-id="982aa-123">Этот аргумент нельзя использовать в диалоговом окне, который является дочерним для другого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="982aa-123">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="982aa-124">Возвращает</span><span class="sxs-lookup"><span data-stu-id="982aa-124">Return</span></span>   | <span data-ttu-id="982aa-125">Элемент управления возвращается к родителю текущего диалогового окна или, если родительский объект отсутствует, элемент управления возвращается в установщик со значением Success.</span><span class="sxs-lookup"><span data-stu-id="982aa-125">The control returns to the parent of the present dialog box, or if there is no parent, the control returns to the installer with the Success value.</span></span>                                 |



 

## <a name="published-by"></a><span data-ttu-id="982aa-126">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="982aa-126">Published By</span></span>

<span data-ttu-id="982aa-127">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="982aa-127">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="982aa-128">Аргумент</span><span class="sxs-lookup"><span data-stu-id="982aa-128">Argument</span></span>

<span data-ttu-id="982aa-129">В обычных диалоговых окнах столбец Argument [таблицы таблице ControlEvent событие](controlevent-table.md) может быть "return", "Exit", "Retry" или "ignore".</span><span class="sxs-lookup"><span data-stu-id="982aa-129">On regular dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "Return", "Exit", "Retry", or "Ignore".</span></span>

<span data-ttu-id="982aa-130">В диалоговых окнах ошибок столбец Argument [таблицы таблице ControlEvent событие](controlevent-table.md) может иметь значение "ерророк", "еррорканцел", "еррораборт", "еррорретри", "ерроригноре", "еррорес" или "еррорно".</span><span class="sxs-lookup"><span data-stu-id="982aa-130">On error dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes", or "ErrorNo".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="982aa-131">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="982aa-131">Action on Subscribers</span></span>

<span data-ttu-id="982aa-132">Нет.</span><span class="sxs-lookup"><span data-stu-id="982aa-132">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="982aa-133">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="982aa-133">Typical Use</span></span>

<span data-ttu-id="982aa-134">Элемент управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне привязывается к этому событию в таблице [таблице ControlEvent событие](controlevent-table.md) , чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="982aa-134">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to close a dialog box.</span></span>

 

 



