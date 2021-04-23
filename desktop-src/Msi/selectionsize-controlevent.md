---
description: Элемент управления Селектионтри использует событие Селектионсизе для публикации размера выделенного элемента.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: Селектионсизе таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264832"
---
# <a name="selectionsize-controlevent"></a><span data-ttu-id="a8f3d-103">Селектионсизе таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="a8f3d-103">SelectionSize ControlEvent</span></span>

<span data-ttu-id="a8f3d-104">[Элемент управления селектионтри](selectiontree-control.md) использует событие селектионсизе для публикации размера выделенного элемента.</span><span class="sxs-lookup"><span data-stu-id="a8f3d-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionSize event to publish the size of the highlighted item.</span></span> <span data-ttu-id="a8f3d-105">Если это родительский элемент, то число выбранных дочерних элементов также публикуется.</span><span class="sxs-lookup"><span data-stu-id="a8f3d-105">If it is a parent item, then the number of children selected is also published.</span></span> <span data-ttu-id="a8f3d-106">Строка является одной из строк **селчилдкостпос**, **селчилдкостнег**, **селпаренткостпоспос**, **Селпаренткостпоснег**, **селпаренткостнегпос** или **SelParentCostNegNeg** из [таблицы UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="a8f3d-106">The string is one of the **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** or **SelParentCostNegNeg** strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="a8f3d-107">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="a8f3d-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="a8f3d-108">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a8f3d-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="a8f3d-109">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a8f3d-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="a8f3d-110">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="a8f3d-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="a8f3d-111">Это событие может влиять только на элементы управления, находящиеся в том же диалоговом окне, что и элемент управления Селектионтри.</span><span class="sxs-lookup"><span data-stu-id="a8f3d-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="a8f3d-112">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="a8f3d-112">Published By</span></span>

[<span data-ttu-id="a8f3d-113">селектионтри</span><span class="sxs-lookup"><span data-stu-id="a8f3d-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="a8f3d-114">Аргумент</span><span class="sxs-lookup"><span data-stu-id="a8f3d-114">Argument</span></span>

<span data-ttu-id="a8f3d-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="a8f3d-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="a8f3d-116">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="a8f3d-116">Action on Subscribers</span></span>

<span data-ttu-id="a8f3d-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="a8f3d-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="a8f3d-118">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="a8f3d-118">Typical Use</span></span>

<span data-ttu-id="a8f3d-119">Элемент управления " [текст](text-control.md) " в том же модальном диалоговом окне, что и элемент управления селектионтри, через [таблицу таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="a8f3d-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree Control via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="a8f3d-120">Элемент управления "текст" использует это событие для вывода размера выделенного элемента.</span><span class="sxs-lookup"><span data-stu-id="a8f3d-120">The Text Control uses this event to display the size of the highlighted item.</span></span>

 

 



