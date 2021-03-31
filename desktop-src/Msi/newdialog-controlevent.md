---
description: Это событие уведомляет установщик о необходимости перехода модального диалогового окна в другое диалоговое окно. Установщик удаляет текущее диалоговое окно и создает новое с именем, указанным в аргументе.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: Невдиалог таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155519"
---
# <a name="newdialog-controlevent"></a><span data-ttu-id="aba86-104">Невдиалог таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="aba86-104">NewDialog ControlEvent</span></span>

<span data-ttu-id="aba86-105">Это событие уведомляет установщик о необходимости перехода модального диалогового окна в другое диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="aba86-105">This event notifies the installer to transition a modal dialog box to another dialog box.</span></span> <span data-ttu-id="aba86-106">Установщик удаляет текущее диалоговое окно и создает новое с именем, указанным в аргументе.</span><span class="sxs-lookup"><span data-stu-id="aba86-106">The installer removes the present dialog box and creates the new one with the name indicated in the argument.</span></span>

<span data-ttu-id="aba86-107">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="aba86-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="aba86-108">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="aba86-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="aba86-109">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="aba86-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="aba86-110">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="aba86-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="aba86-111">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="aba86-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="aba86-112">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="aba86-112">Published By</span></span>

<span data-ttu-id="aba86-113">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="aba86-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="aba86-114">Аргумент</span><span class="sxs-lookup"><span data-stu-id="aba86-114">Argument</span></span>

<span data-ttu-id="aba86-115">Строка, которая является именем нового диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="aba86-115">A string that is the name of the new dialog.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="aba86-116">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="aba86-116">Action on Subscribers</span></span>

<span data-ttu-id="aba86-117">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="aba86-117">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="aba86-118">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="aba86-118">Typical Use</span></span>

<span data-ttu-id="aba86-119">Элемент управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне связан с этим событием в таблице [таблице ControlEvent событие](controlevent-table.md) , чтобы передать переход в следующее или предыдущее диалоговое окно той же последовательности мастера.</span><span class="sxs-lookup"><span data-stu-id="aba86-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to signal a transition to the next or previous dialog box of the same wizard sequence.</span></span>

 

 



