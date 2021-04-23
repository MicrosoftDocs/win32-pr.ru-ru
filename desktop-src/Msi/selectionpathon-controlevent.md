---
description: Элемент управления Селектионтри использует событие Селектионпасон для публикации логического значения, указывающего, связан ли с текущим выбранным компонентом путь выбора. Это событие должно быть создано в таблице таблица eventmapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: Селектионпасон таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664661"
---
# <a name="selectionpathon-controlevent"></a><span data-ttu-id="f4b27-104">Селектионпасон таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="f4b27-104">SelectionPathOn ControlEvent</span></span>

<span data-ttu-id="f4b27-105">[Элемент управления селектионтри](selectiontree-control.md) использует событие селектионпасон для публикации логического значения, указывающего, связан ли с текущим выбранным компонентом путь выбора.</span><span class="sxs-lookup"><span data-stu-id="f4b27-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionPathOn event to publish a Boolean value indicating whether there is a selection path associated with the currently selected feature.</span></span> <span data-ttu-id="f4b27-106">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="f4b27-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="f4b27-107">Это событие может влиять только на элементы управления, находящиеся в том же диалоговом окне, что и элемент управления Селектионтри.</span><span class="sxs-lookup"><span data-stu-id="f4b27-107">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

<span data-ttu-id="f4b27-108">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f4b27-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f4b27-109">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f4b27-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f4b27-110">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f4b27-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="f4b27-111">Селектионпасон таблице ControlEvent событие никогда не публикуется во время [установки обслуживания](maintenance-installation.md).</span><span class="sxs-lookup"><span data-stu-id="f4b27-111">The SelectionPathOn ControlEvent is never published during a [Maintenance Installation](maintenance-installation.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="f4b27-112">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="f4b27-112">Published By</span></span>

[<span data-ttu-id="f4b27-113">селектионтри</span><span class="sxs-lookup"><span data-stu-id="f4b27-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="f4b27-114">Аргумент</span><span class="sxs-lookup"><span data-stu-id="f4b27-114">Argument</span></span>

<span data-ttu-id="f4b27-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="f4b27-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f4b27-116">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="f4b27-116">Action on Subscribers</span></span>

<span data-ttu-id="f4b27-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="f4b27-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f4b27-118">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="f4b27-118">Typical Use</span></span>

<span data-ttu-id="f4b27-119">Элемент управления " [текст](text-control.md) " в том же модальном диалоговом окне, что и селектионтри, должен подписываться на событие через [таблицу таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="f4b27-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="f4b27-120">Элемент управления "текст" отображает заголовок пути выделения.</span><span class="sxs-lookup"><span data-stu-id="f4b27-120">The Text Control displays the caption of the selection path.</span></span> <span data-ttu-id="f4b27-121">Этот текстовый элемент управления является видимым или скрытым в зависимости от события.</span><span class="sxs-lookup"><span data-stu-id="f4b27-121">This text control is visible or hidden depending on the event.</span></span>

 

 



