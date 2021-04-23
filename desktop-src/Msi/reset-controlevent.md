---
description: Диалоговое окно сбрасывается. Иными словами, все элементы управления в диалоговом окне вызываются для отмены изменений свойств, которые они выполнили. Это событие сбрасывает все значения свойств на то, что было при создании диалогового окна.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: Сбросить таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663572"
---
# <a name="reset-controlevent"></a><span data-ttu-id="5895b-105">Сбросить таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="5895b-105">Reset ControlEvent</span></span>

<span data-ttu-id="5895b-106">Диалоговое окно сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="5895b-106">The dialog box is reset.</span></span> <span data-ttu-id="5895b-107">Иными словами, все элементы управления в диалоговом окне вызываются для отмены изменений свойств, которые они выполнили.</span><span class="sxs-lookup"><span data-stu-id="5895b-107">In other words, all the controls on the dialog box are called to undo the property changes they have performed.</span></span> <span data-ttu-id="5895b-108">Это событие сбрасывает все значения свойств на то, что было при создании диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5895b-108">This event resets all the property values to what they were when the dialog box was created.</span></span>

<span data-ttu-id="5895b-109">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-109">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="5895b-110">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-110">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="5895b-111">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5895b-111">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="5895b-112">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-112">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="5895b-113">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="5895b-113">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="5895b-114">Существует случай, который на практике может происходить редко, который не обрабатывается должным образом этим таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="5895b-114">There is a case, which should occur rarely in practice, that is not handled properly by this ControlEvent.</span></span> <span data-ttu-id="5895b-115">Если два или более элемента управления в одном диалоговом окне связаны косвенно с одним и тем же свойством и хотя бы один из них начал использовать другое свойство, значение этого свойства иногда сбрасывается до второго значения.</span><span class="sxs-lookup"><span data-stu-id="5895b-115">If there are two or more controls on the same dialog box linked indirectly to the same property and at least one of them started having some other property, then this property value will sometimes be reset to its second value.</span></span>

## <a name="published-by"></a><span data-ttu-id="5895b-116">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="5895b-116">Published By</span></span>

<span data-ttu-id="5895b-117">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="5895b-117">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="5895b-118">Аргумент</span><span class="sxs-lookup"><span data-stu-id="5895b-118">Argument</span></span>

<span data-ttu-id="5895b-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="5895b-119">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="5895b-120">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="5895b-120">Action on Subscribers</span></span>

<span data-ttu-id="5895b-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="5895b-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="5895b-122">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="5895b-122">Typical Use</span></span>

<span data-ttu-id="5895b-123">Элемент управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне используется для сброса всех значений в диалоговом окне и для отмены всех изменений на странице.</span><span class="sxs-lookup"><span data-stu-id="5895b-123">A [PushButton](pushbutton-control.md) control on a modal dialog box is used to reset all the values on the dialog box and to cancel all the changes on the page.</span></span>

 

 



