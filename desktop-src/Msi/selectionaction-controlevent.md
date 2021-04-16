---
description: Элемент управления Селектионтри использует это событие для публикации строки, описывающей выделенный элемент. Строка является одним из &\# 0034; SEL \* & \# 0034; строки из таблицы уитекст. Это событие должно быть создано в таблице таблица eventmapping.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: Селектионактион таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664662"
---
# <a name="selectionaction-controlevent"></a><span data-ttu-id="709b4-105">Селектионактион таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="709b4-105">SelectionAction ControlEvent</span></span>

<span data-ttu-id="709b4-106">[Элемент управления селектионтри](selectiontree-control.md) использует это событие для публикации строки, описывающей выделенный элемент.</span><span class="sxs-lookup"><span data-stu-id="709b4-106">The [SelectionTree control](selectiontree-control.md) uses this event to publish a string describing the highlighted item.</span></span> <span data-ttu-id="709b4-107">Строка является одной из строк "SEL \* " из [таблицы уитекст](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="709b4-107">The string is one of the "Sel\*" strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="709b4-108">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="709b4-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="709b4-109">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="709b4-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="709b4-110">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="709b4-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="709b4-111">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="709b4-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="709b4-112">Это событие может влиять только на элементы управления, находящиеся в том же диалоговом окне, что и элемент управления Селектионтри.</span><span class="sxs-lookup"><span data-stu-id="709b4-112">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="709b4-113">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="709b4-113">Published By</span></span>

[<span data-ttu-id="709b4-114">селектионтри</span><span class="sxs-lookup"><span data-stu-id="709b4-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="709b4-115">Аргумент</span><span class="sxs-lookup"><span data-stu-id="709b4-115">Argument</span></span>

<span data-ttu-id="709b4-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="709b4-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="709b4-117">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="709b4-117">Action on Subscribers</span></span>

<span data-ttu-id="709b4-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="709b4-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="709b4-119">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="709b4-119">Typical Use</span></span>

<span data-ttu-id="709b4-120">Элемент управления " [текст](text-control.md) " в том же модальном диалоговом окне, что и селектионтри, должен подписываться на это событие через [таблицу таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="709b4-120">A [Text](text-control.md) control in the same modal dialog box as the SelectionTree should subscribe to this event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="709b4-121">Элемент управления "текст" отображает описание выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="709b4-121">The Text Control displays the explanation of the selected item.</span></span>

 

 



