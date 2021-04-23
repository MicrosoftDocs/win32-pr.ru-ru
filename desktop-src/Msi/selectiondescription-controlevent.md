---
description: Элемент управления Селектионтри использует событие Селектиондескриптион для публикации строки, содержащей описание выделенного элемента. Эта строка представляет собой поле Description таблицы Feature. Это событие должно быть создано в таблице таблица eventmapping.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: Селектиондескриптион таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663525"
---
# <a name="selectiondescription-controlevent"></a><span data-ttu-id="4159f-105">Селектиондескриптион таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="4159f-105">SelectionDescription ControlEvent</span></span>

<span data-ttu-id="4159f-106">[Элемент управления селектионтри](selectiontree-control.md) использует событие селектиондескриптион для публикации строки, содержащей описание выделенного элемента.</span><span class="sxs-lookup"><span data-stu-id="4159f-106">The [SelectionTree control](selectiontree-control.md) uses the SelectionDescription event to publish a string that contains the description for the highlighted item.</span></span> <span data-ttu-id="4159f-107">Эта строка представляет собой поле **Description** [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="4159f-107">This string is the **Description** field of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="4159f-108">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="4159f-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="4159f-109">Это событие может влиять только на элементы управления, находящиеся в том же диалоговом окне, что и [элемент управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="4159f-109">This event can only affect controls that are located on the same dialog box as the [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="4159f-110">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4159f-110">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="4159f-111">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4159f-111">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="4159f-112">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="4159f-112">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="4159f-113">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="4159f-113">Published By</span></span>

[<span data-ttu-id="4159f-114">селектионтри</span><span class="sxs-lookup"><span data-stu-id="4159f-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="4159f-115">Аргумент</span><span class="sxs-lookup"><span data-stu-id="4159f-115">Argument</span></span>

<span data-ttu-id="4159f-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="4159f-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="4159f-117">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="4159f-117">Action on Subscribers</span></span>

<span data-ttu-id="4159f-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="4159f-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="4159f-119">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="4159f-119">Typical Use</span></span>

<span data-ttu-id="4159f-120">Элемент управления " [текст](text-control.md) " в том же модальном диалоговом окне, в котором селектионтри подписывается на этот таблице ControlEvent событие через [таблицу таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="4159f-120">A [Text](text-control.md) control on the same modal dialog as the SelectionTree subscribes to this ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="4159f-121">Элемент управления "текст" использует это событие для вывода описания выделенного элемента.</span><span class="sxs-lookup"><span data-stu-id="4159f-121">The Text Control uses this event to display the description of the highlighted item.</span></span>

 

 



