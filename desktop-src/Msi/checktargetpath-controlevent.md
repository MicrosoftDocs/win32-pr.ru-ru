---
description: Это событие уведомляет установщик о необходимости проверки правильности выбранного пути. Если путь является недопустимым, это событие блокирует дальнейшее Контролевентс, связанное с элементом управления.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: Чекктаржетпас таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49301dbe1fcc6becc1bc757a0fe487061e1dcdbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662902"
---
# <a name="checktargetpath-controlevent"></a><span data-ttu-id="66845-104">Чекктаржетпас таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="66845-104">CheckTargetPath ControlEvent</span></span>

<span data-ttu-id="66845-105">Это событие уведомляет установщик о необходимости проверки правильности выбранного пути.</span><span class="sxs-lookup"><span data-stu-id="66845-105">This event notifies the installer that it has to verify that the selected path is valid.</span></span> <span data-ttu-id="66845-106">Если путь является недопустимым, это событие блокирует дальнейшее Контролевентс, связанное с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="66845-106">If the path is not valid, then this event blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="66845-107">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="66845-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="66845-108">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="66845-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="66845-109">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="66845-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="66845-110">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="66845-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="66845-111">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="66845-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="66845-112">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="66845-112">Published By</span></span>

<span data-ttu-id="66845-113">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="66845-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="66845-114">Аргумент</span><span class="sxs-lookup"><span data-stu-id="66845-114">Argument</span></span>

<span data-ttu-id="66845-115">Имя свойства, содержащего путь.</span><span class="sxs-lookup"><span data-stu-id="66845-115">The name of the property containing the path.</span></span> <span data-ttu-id="66845-116">Если свойство является косвенным, имя свойства заключено в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="66845-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="66845-117">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="66845-117">Action on Subscribers</span></span>

<span data-ttu-id="66845-118">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="66845-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="66845-119">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="66845-119">Typical Use</span></span>

<span data-ttu-id="66845-120">Элемент управления " [кнопка](pushbutton-control.md) " в диалоговом окне "Обзор" связан с этим событием в таблице [таблице ControlEvent событие](controlevent-table.md) , чтобы проверить выбранный путь перед возвратом в диалоговое окно "выбор".</span><span class="sxs-lookup"><span data-stu-id="66845-120">A [PushButton](pushbutton-control.md) control on a browse dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog box.</span></span>

 

 



