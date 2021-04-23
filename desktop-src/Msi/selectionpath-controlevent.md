---
description: Элемент управления Селектионтри использует событие Селектионпас для публикации пути к выделенному элементу.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: Селектионпас таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998685"
---
# <a name="selectionpath-controlevent"></a><span data-ttu-id="5ca39-103">Селектионпас таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="5ca39-103">SelectionPath ControlEvent</span></span>

<span data-ttu-id="5ca39-104">[Элемент управления селектионтри](selectiontree-control.md) использует событие селектионпас для публикации пути к выделенному элементу.</span><span class="sxs-lookup"><span data-stu-id="5ca39-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionPath event to publish the path for the highlighted item.</span></span> <span data-ttu-id="5ca39-105">Если элемент выбран для выполнения из источника, то это путь к источнику.</span><span class="sxs-lookup"><span data-stu-id="5ca39-105">If the item is selected to run from source, then this is the path of the source.</span></span> <span data-ttu-id="5ca39-106">Если элемент выбран для отсутствия, то строка является строкой **абсентпас** из [таблицы уитекст](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="5ca39-106">If the item is selected to be absent, then the string is the **AbsentPath** string from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="5ca39-107">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="5ca39-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="5ca39-108">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5ca39-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="5ca39-109">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5ca39-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="5ca39-110">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="5ca39-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="5ca39-111">Это событие может влиять только на элементы управления, находящиеся в том же диалоговом окне, что и элемент управления Селектионтри.</span><span class="sxs-lookup"><span data-stu-id="5ca39-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="5ca39-112">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="5ca39-112">Published By</span></span>

[<span data-ttu-id="5ca39-113">селектионтри</span><span class="sxs-lookup"><span data-stu-id="5ca39-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="5ca39-114">Аргумент</span><span class="sxs-lookup"><span data-stu-id="5ca39-114">Argument</span></span>

<span data-ttu-id="5ca39-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="5ca39-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="5ca39-116">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="5ca39-116">Action on Subscribers</span></span>

<span data-ttu-id="5ca39-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="5ca39-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="5ca39-118">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="5ca39-118">Typical Use</span></span>

<span data-ttu-id="5ca39-119">Элемент управления " [текст](text-control.md) " в том же модальном диалоговом окне, что и селектионтри, должен подписываться на событие через [таблицу таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="5ca39-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="5ca39-120">Элемент управления "текст" отображает путь выделенного элемента.</span><span class="sxs-lookup"><span data-stu-id="5ca39-120">The Text Control displays the path of the highlighted item.</span></span>

 

 



