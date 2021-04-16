---
description: Элемент управления Селектионтри использует событие Селектионноитемс для удаления устаревшего текста описания элемента или для отключения кнопок, которые стали бесполезными. Это событие должно быть создано в таблице таблица eventmapping.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: Селектионноитемс таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651194"
---
# <a name="selectionnoitems-controlevent"></a><span data-ttu-id="ecbac-104">Селектионноитемс таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="ecbac-104">SelectionNoItems ControlEvent</span></span>

<span data-ttu-id="ecbac-105">[Элемент управления селектионтри](selectiontree-control.md) использует событие селектионноитемс для удаления устаревшего текста описания элемента или для отключения кнопок, которые стали бесполезными.</span><span class="sxs-lookup"><span data-stu-id="ecbac-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionNoItems event to delete obsolete item description text or to disable buttons that have become useless.</span></span> <span data-ttu-id="ecbac-106">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="ecbac-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="ecbac-107">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ecbac-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="ecbac-108">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ecbac-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ecbac-109">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ecbac-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="ecbac-110">Это событие может влиять только на элементы управления, находящиеся в том же диалоговом окне, что и элемент управления Селектионтри.</span><span class="sxs-lookup"><span data-stu-id="ecbac-110">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="ecbac-111">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="ecbac-111">Published By</span></span>

<span data-ttu-id="ecbac-112">[Элемент управления селектионтри](selectiontree-control.md) , если в выделенном фрагменте нет узлов.</span><span class="sxs-lookup"><span data-stu-id="ecbac-112">[SelectionTree control](selectiontree-control.md) if the selection has no nodes.</span></span>

## <a name="argument"></a><span data-ttu-id="ecbac-113">Аргумент</span><span class="sxs-lookup"><span data-stu-id="ecbac-113">Argument</span></span>

<span data-ttu-id="ecbac-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="ecbac-114">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ecbac-115">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="ecbac-115">Action on Subscribers</span></span>

<span data-ttu-id="ecbac-116">Удаляет устаревший текст описания элемента или отключает устаревшие кнопки.</span><span class="sxs-lookup"><span data-stu-id="ecbac-116">Deletes obsolete item description text or disables obsolete buttons.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ecbac-117">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="ecbac-117">Typical Use</span></span>

<span data-ttu-id="ecbac-118">Может использоваться для отключения кнопок Далее, сброс и Дисккост в [диалоговом окне выбора](selection-dialog.md) , если в выделенном фрагменте нет узлов и эти кнопки становятся бесполезными.</span><span class="sxs-lookup"><span data-stu-id="ecbac-118">May be used to disable the Next, Reset, and DiskCost buttons on the [Selection Dialog](selection-dialog.md) when a selection has no nodes and these buttons become useless.</span></span>

 

 



