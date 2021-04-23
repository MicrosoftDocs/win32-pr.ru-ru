---
description: Это событие выбирает и выделяет каталог в элементе управления Директорилист, который пользователь выбрал для открытия. Связанные сведения см. в разделе Диалоговое окно обзора.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: Директорилистопен таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273114"
---
# <a name="directorylistopen-controlevent"></a><span data-ttu-id="f3211-104">Директорилистопен таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="f3211-104">DirectoryListOpen ControlEvent</span></span>

<span data-ttu-id="f3211-105">Это событие выбирает и выделяет каталог в [элементе управления директорилист](directorylist-control.md) , который пользователь выбрал для открытия.</span><span class="sxs-lookup"><span data-stu-id="f3211-105">This event selects and highlights a directory in the [DirectoryList control](directorylist-control.md) that the user has chosen to open.</span></span> <span data-ttu-id="f3211-106">Связанные сведения см. в разделе [диалоговое окно обзора](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="f3211-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="f3211-107">Это событие должно быть опубликовано [элементом управления "кнопка](pushbutton-control.md) ", расположенным в том же диалоговом окне, что и элемент управления, подписавшийся на это событие.</span><span class="sxs-lookup"><span data-stu-id="f3211-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="f3211-108">Событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="f3211-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="f3211-109">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f3211-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f3211-110">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f3211-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f3211-111">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f3211-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="f3211-112">Если каталог не выбран в [элементе управления директорилист](directorylist-control.md), событие директорилистопен отключает все другие элементы управления, которые публикуют событие директорилистопен.</span><span class="sxs-lookup"><span data-stu-id="f3211-112">If no directory has been selected in the [DirectoryList control](directorylist-control.md), a DirectoryListOpen event disables any other controls that publish a DirectoryListOpen event.</span></span>

## <a name="published-by"></a><span data-ttu-id="f3211-113">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="f3211-113">Published By</span></span>

[<span data-ttu-id="f3211-114">директорилист</span><span class="sxs-lookup"><span data-stu-id="f3211-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="f3211-115">Аргумент</span><span class="sxs-lookup"><span data-stu-id="f3211-115">Argument</span></span>

<span data-ttu-id="f3211-116">В этом таблице ControlEvent событие не используется аргумент.</span><span class="sxs-lookup"><span data-stu-id="f3211-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f3211-117">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="f3211-117">Action on Subscribers</span></span>

<span data-ttu-id="f3211-118">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="f3211-118">This ControlEvent performs no action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f3211-119">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="f3211-119">Typical Use</span></span>

<span data-ttu-id="f3211-120">Элемент управления " [кнопка](pushbutton-control.md) " в том же модальном диалоговом окне, что и директорилист, используется для активации шага в пути.</span><span class="sxs-lookup"><span data-stu-id="f3211-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping down in the path.</span></span>

 

 



