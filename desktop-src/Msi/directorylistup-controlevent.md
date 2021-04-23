---
description: Это событие уведомляет элемент управления Директорилист, что пользователь хочет выбрать родителя текущего каталога. Связанные сведения см. в разделе Диалоговое окно обзора.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: Директорилиступ таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999765"
---
# <a name="directorylistup-controlevent"></a><span data-ttu-id="e1546-104">Директорилиступ таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="e1546-104">DirectoryListUp ControlEvent</span></span>

<span data-ttu-id="e1546-105">Это событие уведомляет [элемент управления директорилист](directorylist-control.md) , что пользователь хочет выбрать родителя текущего каталога.</span><span class="sxs-lookup"><span data-stu-id="e1546-105">This event notifies the [DirectoryList control](directorylist-control.md) that the user wants to select the parent of the present directory.</span></span> <span data-ttu-id="e1546-106">Связанные сведения см. в разделе [диалоговое окно обзора](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="e1546-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="e1546-107">Это событие должно быть опубликовано [элементом управления "кнопка](pushbutton-control.md) ", расположенным в том же диалоговом окне, что и элемент управления, подписавшийся на это событие.</span><span class="sxs-lookup"><span data-stu-id="e1546-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="e1546-108">Событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1546-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="e1546-109">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e1546-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="e1546-110">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e1546-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="e1546-111">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e1546-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="e1546-112">Если текущий каталог является корневым каталогом диска, то событие Директорилиступ отключает все другие элементы управления, публикующие событие Директорилиступ.</span><span class="sxs-lookup"><span data-stu-id="e1546-112">If the current directory is the root directory of the drive, a DirectoryListUp event disables any other controls that publish a DirectoryListUp event.</span></span>

## <a name="published-by"></a><span data-ttu-id="e1546-113">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="e1546-113">Published By</span></span>

[<span data-ttu-id="e1546-114">директорилист</span><span class="sxs-lookup"><span data-stu-id="e1546-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="e1546-115">Аргумент</span><span class="sxs-lookup"><span data-stu-id="e1546-115">Argument</span></span>

<span data-ttu-id="e1546-116">В этом таблице ControlEvent событие не используется аргумент.</span><span class="sxs-lookup"><span data-stu-id="e1546-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e1546-117">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="e1546-117">Action on Subscribers</span></span>

<span data-ttu-id="e1546-118">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="e1546-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="e1546-119">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="e1546-119">Typical Use</span></span>

<span data-ttu-id="e1546-120">Элемент управления " [кнопка](pushbutton-control.md) " в том же модальном диалоговом окне, что и директорилист, используется для активации шага в пути.</span><span class="sxs-lookup"><span data-stu-id="e1546-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping up in the path.</span></span>

 

 



