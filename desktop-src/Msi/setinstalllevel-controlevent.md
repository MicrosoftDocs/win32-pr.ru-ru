---
description: Событие Сетинсталллевел изменяет уровень установки на значение, заданное аргументом.
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: Сетинсталллевел таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347f54cee1494b2ff91f7dc1701f0b7749d47e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263338"
---
# <a name="setinstalllevel-controlevent"></a><span data-ttu-id="c6fb6-103">Сетинсталллевел таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="c6fb6-103">SetInstallLevel ControlEvent</span></span>

<span data-ttu-id="c6fb6-104">Событие Сетинсталллевел изменяет уровень установки на значение, заданное аргументом.</span><span class="sxs-lookup"><span data-stu-id="c6fb6-104">The SetInstallLevel event changes the installation level to the value specified by the argument.</span></span>

<span data-ttu-id="c6fb6-105">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="c6fb6-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="c6fb6-106">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="c6fb6-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="c6fb6-107">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c6fb6-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="c6fb6-108">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c6fb6-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="c6fb6-109">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c6fb6-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="c6fb6-110">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="c6fb6-110">Published By</span></span>

<span data-ttu-id="c6fb6-111">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="c6fb6-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="c6fb6-112">Аргумент</span><span class="sxs-lookup"><span data-stu-id="c6fb6-112">Argument</span></span>

<span data-ttu-id="c6fb6-113">Целое число, которое является новым значением уровня установки.</span><span class="sxs-lookup"><span data-stu-id="c6fb6-113">An integer that is the new value of the installation level.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c6fb6-114">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="c6fb6-114">Action on Subscribers</span></span>

<span data-ttu-id="c6fb6-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="c6fb6-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c6fb6-116">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="c6fb6-116">Typical Use</span></span>

<span data-ttu-id="c6fb6-117">Элемент управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне связан с этим событием в таблице [таблице ControlEvent событие](controlevent-table.md) для изменения уровня установки.</span><span class="sxs-lookup"><span data-stu-id="c6fb6-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to change the installation level.</span></span>

 

 



